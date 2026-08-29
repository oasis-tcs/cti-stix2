# Proposal: Add imports to the Windows PE Binary File extension

- **Issue:** [oasis-tcs/cti-stix2#83](https://github.com/oasis-tcs/cti-stix2/issues/83) - "Add Imports to PE File Extension of File Object" (ikiril01, 2018; `Status: Awaiting proposal`, `Target: STIX-2.2`)
- **Status:** Proposal
- **Drafted:** 2026-07-17

## Motivation

The issue asks for explicit imports on the PE binary extension: a specific set
of imported libraries and functions is often indicative of particular malicious
capabilities (process injection, persistence, …), especially for patterning.
Today the extension only carries the **imphash** property, which summarizes the
import table as a single hash - good for exact-match correlation, useless for
expressing *which* imports matter. The extension already models sections
explicitly (**sections**, `windows-pe-section-type`); imports are the missing
counterpart.

## Proposed change

### 1. New `imports` property on `windows-pebinary-ext` (section 6.7.6.1)

Appended to the extension's property table, after **sections** (draft-ready
HTML follows the exact format of the **sections** row):

| Property Name | Type | Description |
|---|---|---|
| **imports** (optional) | `list` of type `windows-pe-import-type` | Specifies metadata about the libraries and functions imported by the PE binary. |

### 2. New sub-object type (new section 6.7.6.2 per alphabetical ordering, plus TOC entry)

> #### Windows™ PE Import Type
>
> **Type Name:** `windows-pe-import-type`
>
> The Windows PE Import type specifies metadata about a library imported by a
> PE file.
>
> ##### Properties
>
> | Property Name | Type | Description |
> |---|---|---|
> | **dll_name** (required) | `string` | Specifies the name of the library (DLL) imported by the PE binary. |
> | **function_names** (optional) | `list` of type `string` | Specifies the names of the functions imported from the library. |

### 3. New example (added under the existing "Typical EXE File" example)

*EXE file with imports*

```json
{
  "type": "file",
  "spec_version": "2.2",
  "id": "file--701857a3-f54b-55e9-b51c-5809c92b8061",
  "name": "example.exe",
  "extensions": {
    "windows-pebinary-ext": {
      "pe_type": "exe",
      "imports": [
        {
          "dll_name": "KERNEL32.dll",
          "function_names": [
            "OpenProcess",
            "VirtualAllocEx",
            "WriteProcessMemory",
            "CreateRemoteThread"
          ]
        },
        {
          "dll_name": "ADVAPI32.dll",
          "function_names": [
            "RegCreateKeyExA",
            "RegSetValueExA"
          ]
        }
      ]
    }
  }
}
```

The file id is a UUIDv5 computed per section 2.9 from the present ID
Contributing Properties (`name`, `extensions`), RFC 8785 serialization,
namespace `00abedb4-aa42-466c-9c01-fed23315a9b7`.

The issue's patterning use case then reads:

```
[file:extensions.'windows-pebinary-ext'.imports[*].function_names[*] = 'CreateRemoteThread']
```

No patterning-section changes are needed - section 9.7.2 already defines the
`[*]` list semantics this relies on.

## Design rationale

- **Mirrors the sections precedent.** One required identifying name plus
  optional detail, exactly like `windows-pe-section-type` (`name` required;
  `size`, `entropy`, `hashes` optional). List-of-objects rather than a
  dictionary keyed by DLL name because patterning over dictionary keys cannot
  express "any library imports function X".
- **Deliberately simpler than CybOX 2.x.** CybOX's `WinExecutableFileObj`
  (same author as the issue) modeled per-function objects with `hint`,
  `ordinal`, `bound` and `virtual_address`. STIX 2.x consistently flattened
  that level of detail (compare `windows-pe-section-type` against CybOX's
  `PESectionType`); function names are what the patterning motivation needs.
- **`dll_name`** follows the PE/COFF specification's own terminology for the
  import directory entry ("the name of the DLL"), and values appear as
  observed in the binary (e.g. `KERNEL32.dll`).
- **Deterministic-ID impact:** none to the spec text - `extensions` is already
  an ID Contributing Property of File, so imports data folds into the UUIDv5
  automatically for producers that include it. No existing example id changes.

## Open questions

1. **Ordinal-only imports** (common in packed malware) cannot be expressed
   with `function_names` alone. Options if wanted: an additional optional
   property (e.g. `function_ordinals`), or the imphash convention of encoding
   them as `ordN` strings. Either can be added later without breaking this
   shape.
2. **Granularity.** If CybOX-style per-function objects are preferred
   (`{name, ordinal, hint}`), the property shape changes to
   `imports[*].functions[*].name` - heavier, but still patternable. The
   simple form is proposed as the default.
3. **Exports symmetry.** No upstream issue requests an `exports` counterpart;
   scoped out here, but one may want the symmetric addition while the type
   design is on the table.

## Fallback shape: per-function objects with ordinal support

If ordinal-only imports (question 1) or per-function granularity (question 2)
are wanted, the following shape answers both at once and is proposed as the
fallback to the simple form:

- `windows-pe-import-type` keeps **dll_name** (required); **function_names**
  is replaced by **functions** (optional, `list` of a new
  `windows-pe-import-function-type`).
- Both properties are optional, with the constraint stated once in the type's
  intro, mirroring the `email-addr` / File precedent ("an Email Address
  object **MUST** contain at least one of the **value** or **display_name**
  properties"): an object using the Windows PE Import Function Type **MUST**
  contain at least one of the **name** or **ordinal** properties.

| Property Name | Type | Description |
|---|---|---|
| **name** (optional) | `string` | Specifies the name of the imported function. |
| **ordinal** (optional) | `integer` | Specifies the ordinal of the imported function, for functions imported by ordinal rather than by name. |

Because the **ordinal** description scopes it to by-ordinal imports, the
three valid combinations are unambiguous:

- **name** only: the function is imported by name (the common case; the
  import table entry carries hint + name, and the hint is dropped as noted
  below).
- **ordinal** only: the function is imported by ordinal and the name was not
  resolved — the packed-malware case the shape exists for.
- both: the function is imported by ordinal and the producer resolved the
  name against the DLL's export table (e.g. `WS2_32.dll` ordinal 23 =
  `socket`). Note for producers: resolved names are analysis-derived rather
  than read from the binary bytes, so two producers observing the same
  binary may serialize different `extensions` values and derive different
  deterministic ids; producers prioritizing id stability **SHOULD** record
  only what the import table carries.

Fragment of the example under this shape (a packed sample importing Winsock
by ordinal):

```json
"imports": [
  {
    "dll_name": "WS2_32.dll",
    "functions": [
      { "ordinal": 23 },
      { "ordinal": 4, "name": "connect" }
    ]
  }
]
```

The patterning form becomes heavier but stays expressive:

```
[file:extensions.'windows-pebinary-ext'.imports[*].functions[*].name = 'CreateRemoteThread']
[file:extensions.'windows-pebinary-ext'.imports[*].functions[*].ordinal = 123]
```

One further case worth a decision while the type design is open:
**delay-loaded imports** (the PE delay-load import directory, used both
legitimately and for evasion). CybOX's `PEImportType` carried a
`delay_load` boolean, and the fact is intrinsic to the binary bytes, so an
optional **delay_loaded** (`boolean`) on `windows-pe-import-type` would be a
safe addition under either shape - proposed as take-or-leave.

Fields considered and rejected for either shape:

- **hint** (the PE import hint): a lookup optimization with no analysis
  value - imphash ignores it, most tools do not record it, and it is exactly
  the level of detail STIX 2.x flattened when adapting CybOX types.
- **address** (IAT / resolved address): ambiguous between static file layout
  and runtime resolution; a resolved address is per-process and
  ASLR-randomized, so it characterizes a Process observation, not the static
  File. Worse, `extensions` is an ID Contributing Property of File, so any
  per-observation-volatile value inside `imports` would give the same binary
  different deterministic ids and defeat the deduplication goal of section
  2.9. Every property carried by `imports` must be intrinsic to the binary
  bytes.

Note: adopting the fallback shape changes the serialization of the example's
`extensions` value, so the example id would need to be recomputed.
