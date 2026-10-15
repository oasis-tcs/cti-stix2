# STIX 2.2 Proposal: Enhance Grouping for Persistent CTI Context

This proposal supersedes the contextual Event SDO proposal in
[oasis-tcs/cti-stix2#349](https://github.com/oasis-tcs/cti-stix2/pull/349).
It follows the [October 2, 2026 TC follow-up](https://github.com/oasis-tcs/cti-stix2/pull/349#issuecomment-5953429514),
which suggests improving Grouping with information about its kind and origin
instead of introducing another contextual container object.

The property names and definitions below are proposed for TC review; the
follow-up did not settle their names, types, or vocabulary values.

This revision also incorporates the subsequent TC meeting feedback on analysis
status, context cardinality, origin cardinality, and publication/reference time,
and [Alexandre's compatibility comment on #354](https://github.com/oasis-tcs/cti-stix2/pull/354#issuecomment-6187791205).
The additions are proposals for discussion, not recorded TC decisions.

## Goals and scope

1. Use the existing Grouping SDO as a persistent, identifiable unit of shared
   analytical context.
2. Describe the analytical kinds of a Grouping and identify its source context.
3. Preserve the identity of an imported CTI container, such as a MISP Event,
   without classifying it as an Incident, Report, or operational Case.
4. Reuse common STIX properties, object references, relationships, markings, and
   versioning.

The new object-specific properties proposed are optional `grouping_types`,
`analysis_status`, and `origin`. The required, single-valued `context` property
is retained, with one proposed addition to `grouping-context-ov` directing
consumers to `grouping_types`. This proposal adds no SDO or identifier namespace.
It does not change the real-world activity Event proposal discussed in
[#340](https://github.com/oasis-tcs/cti-stix2/pull/340).

Publication lifecycle and reference-time metadata are discussed below as open
design questions. Threat level and operational case management from #349 remain
deferred to separate proposals or extensions. This amendment does not claim a
lossless MISP mapping for those fields.

## Why Grouping

Grouping already asserts that its referenced STIX Objects share a context.
It already has an identity, a creator, creation and modification timestamps,
markings, and versions. Its `object_refs` can reference SDOs, SCOs, SROs, and SMOs.

The missing clarification is that this context can be maintained as a persistent
unit of CTI across exchanges and revisions. An investigation, malware analysis,
threat actor analysis, or collection of related indicators can retain that unit's
identity without implying that a security incident has occurred or that an
intelligence report has been produced.

A Bundle transports objects and asserts no shared context. An Incident describes
an incident. A Report conveys an intelligence product. Grouping supplies the
shared analytical context and can reference those objects when appropriate.
An operational Case, if standardized separately, can investigate or manage that
context without determining the Grouping's identity.

## Proposed amendment to the Grouping description

Retain the existing Grouping definition and add the following paragraphs to the
STIX 2.2 Grouping description:

> A Grouping MAY represent a persistent unit of cyber threat intelligence whose
> referenced STIX Objects share an analytical context. The Grouping retains its
> identifier as that context evolves, using the common STIX object versioning
> rules when its content changes.
>
> A Grouping MAY represent an ongoing investigation, malware analysis, threat
> actor analysis, vulnerability analysis, or another coherent collection of
> intelligence. A Grouping does not by itself assert that the context is an
> Incident, a published Report, or an operational case-management process.
>
> The optional grouping_types property describes the analytical kinds of the
> Grouping. The optional origin property identifies the external context from
> which the Grouping was derived. The optional analysis_status property describes
> the state of the analytical work. These properties supplement the required,
> single-valued context property. The context value grouping-types indicates
> that the analytical classifications are supplied in grouping_types.
>
> A Grouping MAY reference an Incident or Report when those objects' semantics
> apply. Producing such an object does not require changing the Grouping's type
> or identifier.

## Proposed properties

Keep all existing Grouping common and object-specific properties and add
`grouping_types`, `analysis_status`, and `origin` to the Grouping-specific
property summary.

| Property | Type | Required | Proposed definition |
| --- | --- | --- | --- |
| `type` | `string` | Required, existing | MUST remain `grouping`. |
| `name` | `string` | Required, existing | A name used to identify the Grouping. |
| `description` | `string` | Optional, existing | Details about the Grouping, its purpose, and its characteristics. |
| `context` | `open-vocab` | Required, existing | The particular context shared by the referenced content; values SHOULD come from `grouping-context-ov`. Remains single-valued. The proposed `grouping-types` value directs consumers to `grouping_types`. |
| `object_refs` | `list` of `identifier` | Required, existing | The STIX Objects referred to by the Grouping. Existing non-empty-list requirements and permitted target types apply. |
| `grouping_types` | `list` of `open-vocab` | Optional, new | The analytical kinds of the Grouping. Values SHOULD come from the proposed `grouping-type-ov` vocabulary. |
| `analysis_status` | `open-vocab` | Optional, new | The state of the analytical work represented by the Grouping. Values SHOULD come from the proposed `grouping-analysis-status-ov` vocabulary. |
| `origin` | `external-reference` | Optional, new | The primary external context from which the Grouping was derived, using the existing STIX External Reference data type. |

### context and backward compatibility

Retain `context` as a required, single-valued `open-vocab`; do not convert it to
a list or require existing producers to supply `grouping_types`. Retain all
existing `grouping-context-ov` values and meanings, including
`suspicious-activity`, `malware-analysis`, and `unspecified`.

Add the following entry to `grouping-context-ov`:

| Value | Meaning |
| --- | --- |
| `grouping-types` | The shared analytical context is described by the classifications in `grouping_types`; consumers should consult that property for details. |

When `context` is `grouping-types`, producers MUST include a non-empty
`grouping_types` list. For other context values, `grouping_types` remains
optional. Producers MAY retain a more specific existing context value alongside
`grouping_types`; they are not required to replace it with `grouping-types`.

Consumers that understand the new value SHOULD use `grouping_types` to interpret
the analytical classifications. Consumers that do not understand it encounter an
unrecognized open-vocabulary string and MUST NOT infer classifications from the
marker itself. Existing open-vocabulary handling applies; the marker does not
guarantee that older applications can display or act on the new classifications.

### grouping_types

The common `type` property is the STIX object discriminator and MUST remain
`grouping`. The proposed `grouping_types` name avoids overloading it.

`context` remains a single descriptor or the `grouping-types` marker defined above.
`grouping_types` allows multiple analytical classifications of the persistent
context. For example, `context: "malware-analysis"` can describe the shared
subject while `grouping_types: ["malware-analysis", "investigation"]` describes
both the kind of analysis and its investigative use.

If present, the list MUST contain at least one value. Producers SHOULD NOT repeat
values. Vocabulary values are not exclusive and do not prescribe workflow state.
Consumers MUST NOT infer that an Incident, Report, or Case exists solely from a
`grouping_types` value.

#### Proposed Grouping Type vocabulary

**Vocabulary name:** `grouping-type-ov`

**Used by:** Grouping `grouping_types`

This is an open vocabulary; custom values remain permitted under the common
STIX open-vocabulary rules.

| Value | Meaning |
| --- | --- |
| `investigation` | Intelligence assembled around an analytical investigation; does not assert an operational Case or workflow state. |
| `incident-analysis` | Intelligence assembled to analyze an actual or suspected incident; any explicit incident assertion belongs in an Incident object. |
| `malware-analysis` | Intelligence assembled to analyze a malware instance or family. |
| `threat-actor-analysis` | Intelligence assembled to analyze a threat actor or intrusion set. |
| `vulnerability-analysis` | Intelligence assembled to analyze a vulnerability or related exploitation activity. |
| `indicator-collection` | Related indicators and supporting objects assembled for a shared analytical purpose. |

An imported container's format is not its analytical kind. A producer SHOULD NOT
use `misp-event` as a substitute for an analytical classification. If its kind
is unknown, the producer MAY omit `grouping_types`; `context` remains required
and can use the existing `unspecified` value.

### analysis_status

`analysis_status` describes the state of the analytical work represented by the
Grouping, independently of its analytical kinds. It does not describe incident
severity, confidence, publication state, or the state of an operational Case.
The property is optional; its absence means no analysis status is asserted and
MUST NOT be interpreted as `initial` or `completed`.

#### Proposed Grouping Analysis Status vocabulary

**Vocabulary name:** `grouping-analysis-status-ov`

**Used by:** Grouping `analysis_status`

This is an open vocabulary. The initial values below follow the MISP Event
analysis states; names and definitions remain subject to TC review.

| Value | Meaning | MISP `Event.analysis` |
| --- | --- | --- |
| `initial` | The analytical work is in its initial state. | `0` (Initial) |
| `ongoing` | The analytical work is in progress. | `1` (Ongoing) |
| `completed` | The analytical work is considered complete at this revision. | `2` (Completed) |

These values do not impose a mandatory sequence. Further work MAY reopen an
analysis previously marked `completed`. Changes use the common STIX versioning
rules, retaining the Grouping identifier and advancing `modified`. Consumers
MUST NOT infer that a completed analysis has been published or that an incident
has been resolved. Unknown source statuses MUST NOT be silently mapped to one
of these values; retain their semantics using a documented custom vocabulary
value or a source-specific extension.

### origin

`origin` designates the primary source container, document, or other external
analytical context represented by the Grouping. It reuses the `external-reference`
data type and all its requirements, including required `source_name` and at
least one of `description`, `url`, or `external_id`.

The producer SHOULD include a stable `external_id` when one is available.
A `url` MAY identify the source context's location. Its inclusion does not
grant access or change the Grouping's markings. The source identifier MUST NOT
be confused with a local database row number when a stable identifier exists.

For a MISP Event, `source_name` can be `misp` and `external_id` its Event UUID.
Where identifiers are only unique within a particular source instance,
`source_name` and the source location SHOULD distinguish that instance.

`origin` identifies the primary derivation source; it is not an Identity
reference and does not replace `created_by_ref`. Other external sources and
citations continue to use `external_references`. Derivation from another STIX
Grouping SHOULD use a `derived-from` Relationship instead of encoding a STIX
identifier as an external origin.

Consumers MUST NOT treat `origin` alone as proof of authenticity, trust, or
authorization. Relaying the same Grouping SHOULD preserve its origin; a relay
does not become its origin merely by distributing it.

#### Origin cardinality for TC review

The current draft keeps a single primary `origin`. A Grouping assembled from
several sources MAY omit `origin` when no primary source can be identified;
other source citations use `external_references`. That list does not by itself
distinguish derivation sources from supporting citations.

If multiple explicit derivation sources are required, the TC should consider a
list of `external-reference` values, for example an `origins` property, and
decide whether a primary source must be designated. This revision does not change
`origin` between an object and a list. Whether the same provenance mechanism
should apply to Report or other SDOs also remains an open design question.

### Publication and reference time for TC review

The meeting raised publication timestamps and an optional reference-time
property on `external-reference` as alternatives to additional Grouping
properties. These describe different subjects:

- A Grouping publication timestamp would describe publication of the Grouping
  itself; it would not describe when its analysis started or completed.
- A timestamp on an external reference would describe the referenced source
  context. A generic reference time would need a defined meaning, such as source
  publication time, and must not be confused with retrieval or observation time.

The TC should decide the subject, cardinality, timestamp precision, and meaning
before selecting a property name or adding it to the shared data type. Any
addition to `external-reference` would affect all objects using that data type,
including Report, and needs separate review. No publication or reference-time
property is added to `external-reference` by this revision.

`created` and `modified` continue to describe the STIX object and its revisions;
converters MUST NOT substitute a source publication time for either merely to
preserve that timestamp. MISP `Event.published`, `Event.publish_timestamp`, and
`Event.date` remain in source-specific extensions pending that decision. Use a
Report's existing `published` property only when Report semantics apply.

## Identity, versioning, and compatibility

- Keep the `grouping--` identifier namespace. No `event--` or `case--`
  identifier is introduced by this proposal.
- Use the common STIX versioning and object-creator rules. A creator revising a
  Grouping retains its `id` and `created`, advances `modified`, and updates
  `object_refs` and other properties as appropriate.
- Referencing an Incident or Report supplements the Grouping; it does not
  convert the Grouping into a different SDO.
- Keep `name`, `context`, and `object_refs` required. An empty source container
  cannot be represented as a conforming Grouping with an empty `object_refs`
  list under this amendment.
- All three new properties are optional for existing representations. A producer
  choosing the new `context: "grouping-types"` value MUST also supply a non-empty
  `grouping_types` list. Existing context values do not acquire this requirement.
- The type and required status of `context` are unchanged. Adding an open-vocabulary
  value preserves its representation; it does not guarantee STIX 2.1 schema or
  application support for the new properties or proposed STIX 2.2 version.
- The examples below target the proposed STIX 2.2 amendment. They do not make
  unprefixed new properties conforming STIX 2.1 properties. STIX 2.1 exchanges
  require an appropriate extension or the applicable customization rules.

## MISP mapping guidance

A converter SHOULD create one Grouping for the MISP Event's shared CTI context.
It SHOULD NOT create an Incident or Report solely to carry container metadata.

| MISP element | Proposed STIX representation | Guidance |
| --- | --- | --- |
| `Event.uuid` | `origin.external_id`; optionally the UUID component of `grouping.id` | Preserve the source UUID in `origin`. Reuse it in the STIX identifier only when it satisfies STIX identifier requirements. |
| `Event.info` | `name` | Human-readable summary. |
| Additional narrative | `description` | When available. |
| Analytical purpose | `context` and optional `grouping_types` | Choose from actual content or explicit classifications. Use `context: "grouping-types"` only with a non-empty `grouping_types` list; otherwise retain an appropriate existing context value. Do not guess an incident or report from the source container name. |
| `Event.analysis` | `analysis_status` | Map `0` to `initial`, `1` to `ongoing`, and `2` to `completed`; omit when no status is asserted. Preserve unknown states without guessing. |
| `Event.timestamp` | `modified` | Convert the Unix timestamp to a STIX timestamp when it represents the corresponding revision. Respect STIX creation/modification ordering and versioning rules. |
| `Event.Orgc` | `created_by_ref`, when its meaning matches | An Identity for the organization responsible for creating the represented STIX content; retain differing source provenance in an extension when necessary. |
| Attributes, Objects, Galaxies, Sightings, and analyst data | Appropriate SDOs, SCOs, SROs, and SMOs in `object_refs` | Convert each item according to its semantics. |
| `EventReport` | Report or Note in `object_refs` | Use Report only when intelligence-product semantics apply. |
| `Event.Tag` | Appropriate labels, markings, or referenced objects | Tags can inform `grouping_types` only when their semantics match. |
| `Event.RelatedEvent` | Another Grouping and a `related-to` Relationship | Preserve each context's own identity. |
| `Event.extends_uuid` | A `derived-from` Relationship when semantically appropriate | Exact MISP extension semantics can be retained in a source-specific extension. |
| `Event.distribution` and sharing restrictions | Appropriate STIX Data Markings | Use markings only where they express the actual policy; retain unsupported policy in an extension and enforce it separately. |
| `Event.date`, `threat_level_id`, publication fields, `Event.Org`, and local synchronization metadata | Source-specific extension or separate future proposal | These have no new core Grouping property in this amendment. Publication/reference-time placement remains under review. Do not silently claim a lossless conversion. |

MISP taxonomy tags and galaxy clusters can inform classifications when their
semantics match; their names, UIDs, and versions are not automatically
`grouping_types` values. Preserve stable source identifiers through appropriate
external references or extensions. The storage and version-selection behavior
of those identifiers needs confirmation in the relevant MISP mappings; this
proposal introduces no new UID format or automatic latest-version rule.

A converter MAY reuse a conforming MISP UUID as the UUID component of the
Grouping identifier, for example `grouping--8f70f1d1-2c88-4b3f-91f9-678098ab3f8f`.
Otherwise it MUST generate a conforming STIX identifier and preserve the original
UUID in `origin.external_id`. Reusing an identifier does not authorize different
creators to publish conflicting versions of the same STIX object.

The reverse conversion can use `origin` to recognize the source MISP Event and
`object_refs` as its analytical boundary. Lossless round-tripping additionally
requires source-specific mappings or extensions for the deferred fields.

## Example: Existing-style Grouping without new properties

This remains usable under the amended Grouping definition.

```json
{
  "type": "grouping",
  "spec_version": "2.2",
  "id": "grouping--84e4d88f-44ea-4bcd-bbf3-b2c1c320bcb3",
  "created": "2026-09-30T08:00:00.000Z",
  "modified": "2026-09-30T08:00:00.000Z",
  "name": "Related infrastructure indicators",
  "context": "unspecified",
  "object_refs": [
    "indicator--52bfa2cb-3f6b-4ee8-9845-230e14729210"
  ]
}
```

The referenced Indicator can be supplied separately.

## Example: MISP-origin analytical context

This Bundle contains the Grouping and every object referenced by the example.
The source context is a MISP Event, while the STIX object remains a Grouping.
The `grouping-types` context marker directs consumers to its two analytical
classifications; `analysis_status` independently records ongoing work.

```json
{
  "type": "bundle",
  "id": "bundle--6d77cc83-9313-4f4c-bd98-54f5977b1a57",
  "objects": [
    {
      "type": "identity",
      "spec_version": "2.2",
      "id": "identity--55f6ea5e-2c60-40e5-964f-47a8950d210f",
      "created": "2026-09-30T08:00:00.000Z",
      "modified": "2026-09-30T08:00:00.000Z",
      "name": "Example CSIRT",
      "identity_class": "organization"
    },
    {
      "type": "grouping",
      "spec_version": "2.2",
      "id": "grouping--8f70f1d1-2c88-4b3f-91f9-678098ab3f8f",
      "created_by_ref": "identity--55f6ea5e-2c60-40e5-964f-47a8950d210f",
      "created": "2026-09-30T08:00:00.000Z",
      "modified": "2026-10-02T12:00:31.000Z",
      "name": "Investigation of Foo ransomware infrastructure",
      "description": "Collaborative analysis of infrastructure associated with Foo ransomware.",
      "context": "grouping-types",
      "grouping_types": ["malware-analysis", "investigation"],
      "analysis_status": "ongoing",
      "origin": {
        "source_name": "misp",
        "external_id": "8f70f1d1-2c88-4b3f-91f9-678098ab3f8f",
        "url": "https://misp.example.invalid/events/view/8f70f1d1-2c88-4b3f-91f9-678098ab3f8f"
      },
      "object_refs": [
        "indicator--52bfa2cb-3f6b-4ee8-9845-230e14729210",
        "malware--0c7b5b88-8ff7-4a4d-aa9d-feb398cd0061",
        "sighting--98fa81c2-a23d-4828-a8ed-d11e3c9ccf95",
        "note--49b73241-7dc4-49c5-96db-a61ad33d70d8"
      ]
    },
    {
      "type": "indicator",
      "spec_version": "2.2",
      "id": "indicator--52bfa2cb-3f6b-4ee8-9845-230e14729210",
      "created": "2026-09-30T08:10:00.000Z",
      "modified": "2026-09-30T08:10:00.000Z",
      "name": "Infrastructure associated with Foo ransomware",
      "pattern_type": "stix",
      "pattern": "[domain-name:value = 'example.invalid']",
      "valid_from": "2026-09-30T00:00:00.000Z"
    },
    {
      "type": "malware",
      "spec_version": "2.2",
      "id": "malware--0c7b5b88-8ff7-4a4d-aa9d-feb398cd0061",
      "created": "2026-09-30T08:15:00.000Z",
      "modified": "2026-09-30T08:15:00.000Z",
      "name": "Foo ransomware",
      "is_family": true,
      "malware_types": ["ransomware"]
    },
    {
      "type": "sighting",
      "spec_version": "2.2",
      "id": "sighting--98fa81c2-a23d-4828-a8ed-d11e3c9ccf95",
      "created": "2026-10-01T09:00:00.000Z",
      "modified": "2026-10-01T09:00:00.000Z",
      "sighting_of_ref": "indicator--52bfa2cb-3f6b-4ee8-9845-230e14729210",
      "where_sighted_refs": ["identity--55f6ea5e-2c60-40e5-964f-47a8950d210f"],
      "first_seen": "2026-10-01T08:00:00.000Z",
      "last_seen": "2026-10-01T08:30:00.000Z",
      "count": 1
    },
    {
      "type": "note",
      "spec_version": "2.2",
      "id": "note--49b73241-7dc4-49c5-96db-a61ad33d70d8",
      "created": "2026-10-02T10:00:00.000Z",
      "modified": "2026-10-02T10:00:00.000Z",
      "content": "Infrastructure is still active; additional indicators are being collected.",
      "object_refs": [
        "indicator--52bfa2cb-3f6b-4ee8-9845-230e14729210",
        "malware--0c7b5b88-8ff7-4a4d-aa9d-feb398cd0061"
      ]
    }
  ]
}
```

As the analysis evolves, the creator can publish a new version of
`grouping--8f70f1d1-2c88-4b3f-91f9-678098ab3f8f` with a later `modified`
timestamp and additional references. If an Incident is identified or a Report
produced, its identifier can be added to `object_refs`; the Grouping's identity
and origin remain stable.

## Questions for TC review

1. Is `grouping-types` an appropriate new `grouping-context-ov` value directing
   consumers to `grouping_types`, while retaining required, single-valued
   `context` and all existing values?
2. Should `origin` designate a single primary external context as proposed, or
   should multiple origins be supported explicitly?
3. Is reusing `external-reference` sufficient for origin, or is a dedicated
   provenance data type needed?
4. Are the proposed analytical kinds appropriate, and which values should be
   standardized initially?
5. Are `analysis_status` and the proposed MISP-aligned values suitable for
   general Grouping use, and should they reuse a broader analysis vocabulary?
6. Should publication metadata describe the Grouping itself or the source
   context through an optional `external-reference` timestamp? What precise
   time semantics and precision would that timestamp have?
7. Should provenance and publication/reference-time support be shared with
   Report and other SDOs, and how should MISP taxonomy/galaxy UIDs and versions
   be preserved in the corresponding mappings?

## Proposed next steps

1. Review the description amendment and the three optional properties.
2. Resolve the context marker, analysis-status vocabulary, origin cardinality,
   and publication/reference-time placement without changing `context` to a list.
3. Incorporate the agreed text into the STIX 2.2 Grouping section, extend
   `grouping-context-ov`, and add `grouping-type-ov` and
   `grouping-analysis-status-ov` to the vocabulary section.
4. Update the corresponding STIX 2.2 schemas and conformance fixtures in the
   repositories that maintain them.
5. Test existing Grouping compatibility, the context marker's non-empty-list
   requirement, all new properties, object reference resolution, and
   source-to-STIX identity/version/status mappings.

