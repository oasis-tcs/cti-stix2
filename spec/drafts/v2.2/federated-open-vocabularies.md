# STIX 2.2 Proposal: Federated Open Vocabularies and Vocabulary Registries

This proposal addresses the current STIX concept of **open vocabularies** and proposes a mechanism to make them genuinely open, extensible, machine-readable, versioned, and independently maintainable.

The proposal is inspired by:

* the existing STIX `open-vocab` datatype and STIX vocabularies;
* the [MISP taxonomy format](https://www.misp-standard.org/rfc/misp-standard-taxonomy-format.html);
* the [MISP galaxy format](https://www.misp-standard.org/rfc/misp-standard-galaxy-format.html);
* the existing public MISP taxonomy and galaxy repositories;
* operational requirements to extend vocabularies without requiring a new version of the STIX specification.

## Goals

1. Preserve the existing STIX `open-vocab` datatype as a string.
2. Preserve all existing STIX 2.0 and STIX 2.1 open-vocabulary values without modification.
3. Move the definition and maintenance of open vocabularies from static lists embedded in the STIX specification toward machine-readable vocabulary registries.
4. Assign stable UUIDs to vocabularies and individual vocabulary entries.
5. Allow vocabularies to evolve independently of the STIX specification lifecycle.
6. Allow organizations and communities to define their own vocabulary extensions.
7. Provide namespaces to avoid collisions between independently maintained extensions.
8. Allow existing MISP taxonomy repositories to be used as STIX vocabulary sources.
9. Allow MISP galaxy repositories to provide richer UUID-based knowledge vocabularies where appropriate.
10. Allow private, community, sector-specific, national, and vendor-specific vocabulary repositories.
11. Ensure that a STIX consumer does not need network access to process a STIX object.
12. Ensure that unknown vocabulary entries remain valid open-vocabulary strings.
13. Keep STIX Enumerations separate from Open Vocabularies; enumerations remain closed and normative.

## Non-goals

* Replacing STIX Enumerations with externally maintained lists.
* Requiring producers or consumers to contact an online vocabulary service.
* Requiring every STIX implementation to support MISP.
* Converting all MISP galaxies into STIX open-vocabulary values.
* Making vocabulary repositories authoritative over STIX objects already exchanged.
* Replacing SDOs such as Malware, Threat Actor, Attack Pattern, Tool, or Vulnerability with vocabulary values.
* Requiring UUIDs to replace the human-readable strings currently used in STIX properties.

## Current STIX open-vocabulary model

STIX 2.1 defines `open-vocab` as a string.

Properties using this datatype identify a suggested vocabulary. Producers SHOULD select a value from that vocabulary but MAY use another string.

For example:

```json
{
  "type": "threat-actor",
  "roles": [
    "director",
    "infrastructure-operator"
  ]
}
```

The current Threat Actor Role Vocabulary defines values such as:

```text
agent
director
independent
infrastructure-architect
infrastructure-operator
malware-author
sponsor
```

A producer may already introduce another value:

```json
{
  "roles": [
    "initial-access-broker"
  ]
}
```

This is syntactically valid STIX because `roles` uses an open vocabulary.

However, there is currently no machine-readable mechanism to determine:

* who defined `initial-access-broker`;
* which vocabulary contains it;
* its semantic definition;
* whether two independently defined strings have the same meaning;
* whether the value has been renamed or deprecated;
* whether aliases exist;
* which version of the vocabulary introduced it;
* where additional metadata can be retrieved;
* whether another vocabulary extends the STIX vocabulary.

The proposed registry mechanism addresses these limitations without changing the serialized property.

## Summary of the proposal

STIX 2.2 SHOULD retain:

```text
open-vocab = string
```

STIX 2.2 SHOULD additionally define a machine-readable **Open Vocabulary Registry model**.

The model separates:

```text
STIX object
       |
       | contains a string
       v
"ransomware"
       |
       | optionally resolved
       v
Vocabulary entry
       |
       +-- UUID
       +-- description
       +-- namespace
       +-- vocabulary
       +-- version
       +-- aliases
       +-- deprecation state
       +-- references
       +-- relationships
```

Vocabulary resolution is OPTIONAL.

The STIX object remains understandable and valid without resolving the vocabulary entry.

## Core design principle

The value serialized in existing STIX objects MUST NOT change solely because the registry mechanism is introduced.

For example:

```json
{
  "malware_types": [
    "ransomware"
  ]
}
```

MUST remain valid.

It MUST NOT become:

```json
{
  "malware_types": [
    {
      "value": "ransomware",
      "uuid": "..."
    }
  ]
}
```

and SHOULD NOT become:

```json
{
  "malware_types": [
    "urn:uuid:..."
  ]
}
```

The UUID belongs to the **vocabulary definition**, not to the base STIX wire representation.

This allows existing implementations to continue treating an open-vocabulary property as a string.

## Vocabulary identity

Every registered vocabulary MUST have a stable UUID.

Every registered vocabulary value MUST also have a stable UUID.

For example, conceptually:

```text
STIX Malware Type Vocabulary
UUID: <vocabulary-uuid>

    ransomware
        UUID: <ransomware-value-uuid>

    rootkit
        UUID: <rootkit-value-uuid>

    spyware
        UUID: <spyware-value-uuid>
```

The UUID provides semantic identity independently from:

* the human-readable value;
* the repository hosting the vocabulary;
* the repository URL;
* the vocabulary version;
* translations;
* aliases;
* display names.

Newly allocated vocabulary and entry identifiers MUST use UUID version 5.

Existing UUIDs from compatible vocabulary repositories MUST be preserved, including UUIDs of other versions. Importing an existing MISP taxonomy or Galaxy entry MUST NOT cause its UUID to be regenerated.

### Deterministic initial allocation

A registry authority MUST publish a stable allocation namespace UUID. At initial allocation, a vocabulary UUID is UUIDv5 of that allocation namespace and the UTF-8 string `namespace:vocabulary-name`; neither component may contain a colon. An entry UUID is UUIDv5 of its vocabulary UUID and the UTF-8 string containing its initial canonical `value`. These strings MUST be used exactly as registered, without case folding, trimming, or other normalization.

For the initial STIX Core Vocabulary Registry, the TC MUST publish the allocation namespace and use the existing vocabulary names and canonical values unchanged. Independent implementations using those inputs will then derive identical initial identifiers.

UUIDv5 is an allocation rule, not a rule for recalculating identifiers on every update. Once allocated, the identifier MUST be retained when a vocabulary or entry is renamed without changing its meaning. A distinct concept MUST receive a distinct initial value within its vocabulary, or a distinct vocabulary identity, so that a previously allocated UUID is never reused for a different concept.

## UUID stability

A vocabulary UUID MUST remain unchanged across updates to the same vocabulary.

A vocabulary entry UUID MUST remain unchanged when:

* its canonical value is renamed without changing its meaning;
* its description is improved;
* references are added;
* aliases are added;
* translations are added;
* non-semantic metadata is modified.

A new UUID MUST be assigned when the semantic meaning of a vocabulary entry changes substantially.

A UUID MUST NOT be reused for a different concept.

When an entry is renamed, its previous canonical value SHOULD be retained as an alias. Consumers MUST continue to accept previously exchanged open-vocabulary strings and MUST NOT silently rewrite them to the new value.

## Core STIX vocabulary registry

The existing STIX open vocabularies SHOULD form the initial **STIX Core Vocabulary Registry**.

For example:

```text
stix
 |
 +-- account-type-ov
 +-- attack-motivation-ov
 +-- attack-resource-level-ov
 +-- grouping-context-ov
 +-- hashing-algorithm-ov
 +-- identity-class-ov
 +-- indicator-type-ov
 +-- industry-sector-ov
 +-- infrastructure-type-ov
 +-- malware-type-ov
 +-- report-type-ov
 +-- threat-actor-type-ov
 +-- threat-actor-role-ov
 +-- threat-actor-sophistication-ov
 +-- tool-type-ov
 +-- ...
```

Each existing vocabulary becomes a persistent vocabulary identified by UUID.

Each existing value receives a persistent UUID.

The canonical string representations defined by earlier STIX versions MUST remain unchanged.

For example:

```text
threat-actor-role-ov
    agent
    director
    independent
    infrastructure-architect
    infrastructure-operator
    malware-author
    sponsor
```

remain serialized exactly as they are today.

## Compatibility with the MISP taxonomy model

The STIX Vocabulary Registry model SHOULD intentionally align with the MISP taxonomy model.

A MISP taxonomy consists conceptually of:

```text
namespace
    |
    +-- predicate
            |
            +-- value
            +-- value
            +-- value
```

A STIX vocabulary can be represented in the same structure:

```text
namespace = stix

predicate = threat-actor-role-ov

values =
    agent
    director
    independent
    infrastructure-architect
    infrastructure-operator
    malware-author
    sponsor
```

This means that a machine-readable representation of the current STIX vocabulary can closely follow the MISP taxonomy format.

### One vocabulary per document

A native `stix-open-vocab` document MUST define exactly one vocabulary. Its `namespace`, `name`, `uuid`, and `version` identify that vocabulary. Every entry in the document belongs only to that vocabulary; an entry MUST NOT feed multiple vocabularies through a list of predicates or bindings. Relationships and explicit mappings can associate concepts across vocabularies without combining their membership.

A registry manifest MAY list multiple vocabulary documents. Existing MISP taxonomy files containing several predicates can remain unchanged as source files; an adapter MUST expose each predicate as a separate logical vocabulary and preserve existing vocabulary and entry UUIDs. A manifest source MAY therefore supply multiple logical vocabularies, but each logical vocabulary has its own identity and entries.

### UUID-keyed entries

The native document's `entries` property MUST be a dictionary keyed by entry UUID in canonical lowercase, hyphenated form. The dictionary key is the entry identifier, so an entry MUST NOT repeat a `uuid` property. Producers and consumers MUST reject duplicate JSON member names before constructing the dictionary, rather than silently discarding an entry. Distinct entries MUST NOT have the same canonical `value` within a vocabulary, and a value or alias MUST NOT ambiguously identify different entries in that vocabulary.

Each entry MUST contain a machine-readable `value` and a nonempty human-readable `description` defining its meaning. An `expanded` label MAY additionally provide display text; a label does not replace the description. Relationships use the dictionary key when referring to an entry by UUID.

For example, the following is illustrative, not a TC allocation. The example allocation namespace is UUIDv5 of the standard URL namespace and `https://docs.oasis-open.org/cti/stix/vocabularies/`, yielding `ec9c0370-639f-5029-b7e1-1e0b931c0345`. The vocabulary UUID is derived from that namespace and `stix:threat-actor-role-ov`; each entry UUID is derived from the vocabulary UUID and its initial value:

```json
{
  "namespace": "stix",
  "name": "threat-actor-role-ov",
  "expanded": "Threat Actor Role Vocabulary",
  "description": "Roles performed by a threat actor.",
  "version": 1,
  "uuid": "0bd60ffa-849e-54c0-963d-ea09bf98bd66",
  "entries": {
    "7eda839f-4b60-57c3-81a3-ed436682536f": {
      "value": "agent",
      "expanded": "Agent",
      "description": "An entity that carries out attacks on behalf of a threat actor."
    },
    "57ada799-4c87-5bd8-bff9-cd04a58d6558": {
      "value": "director",
      "expanded": "Director",
      "description": "An entity that directs and coordinates a threat actor's activities."
    },
    "b48c5d16-f836-5c76-91a4-838bdb5f6155": {
      "value": "infrastructure-operator",
      "expanded": "Infrastructure Operator",
      "description": "An entity that operates infrastructure used to conduct attacks."
    },
    "9981edcd-fa59-5c91-8101-2f2c08ee1aef": {
      "value": "malware-author",
      "expanded": "Malware Author",
      "description": "An entity that develops malware used in attacks."
    }
  }
}
```

The native schema differs from the MISP taxonomy array representation. Adapters SHOULD support lossless conversion, retaining descriptions, identifiers, metadata, and membership for each logical vocabulary. The model SHOULD preserve the following important design characteristics:

* namespace;
* vocabulary/predicate;
* value;
* UUID;
* version;
* description;
* expanded/display value;
* optional numerical value;
* optional metadata.

## Vocabulary bindings

A vocabulary registry SHOULD describe where a vocabulary is normally used.

For example:

```json
{
  "vocabulary": "threat-actor-role-ov",
  "vocabulary_uuid": "0bd60ffa-849e-54c0-963d-ea09bf98bd66",
  "bindings": [
    {
      "object_type": "threat-actor",
      "property": "roles"
    }
  ]
}
```

Another vocabulary may apply to several properties or object types.

Bindings are informative.

They MUST NOT prevent an open-vocabulary value from being used elsewhere when permitted by the STIX specification.

## External vocabulary extensions

Organizations MUST be able to publish additional vocabulary entries without modifying the STIX specification.

For example, an organization may require additional malware types:

```text
loader-as-a-service
browser-injector
credential-relay-malware
```

A custom vocabulary can declare that it extends the STIX Malware Type Vocabulary.

Conceptually:

```text
STIX malware-type-ov
       ^
       |
       | extends
       |
example-org malware taxonomy
```

The external vocabulary has:

* its own namespace;
* its own UUID;
* its own version;
* UUIDs for all entries;
* an explicit reference to the vocabulary it extends.

## Namespaces

Core STIX vocabulary values SHOULD continue to use their existing unqualified representation.

For example:

```json
{
  "malware_types": [
    "ransomware"
  ]
}
```

External vocabulary values SHOULD use a qualified representation when there is a risk of ambiguity or collision.

A MISP-compatible machine-tag representation MAY be used.

For example:

```json
{
  "malware_types": [
    "ransomware",
    "example-org:malware-type=\"loader-as-a-service\""
  ]
}
```

A STIX 2.0 or 2.1 consumer sees both entries as strings.

It understands:

```text
ransomware
```

and may treat:

```text
example-org:malware-type="loader-as-a-service"
```

as an unknown custom open-vocabulary value.

A STIX 2.2 consumer aware of vocabulary registries can additionally resolve the namespace and retrieve its semantic definition.

This provides graceful degradation.

## Why qualified custom values are useful

Consider two organizations that independently define:

```text
broker
```

One may mean:

> a threat actor selling initial network access

while another may mean:

> an intermediary selling stolen data.

Without namespaces, both are represented as:

```json
"broker"
```

With qualified values:

```text
example-a:threat-actor-role="broker"
example-b:threat-actor-role="broker"
```

the concepts remain distinguishable.

The vocabulary entry UUID provides an additional persistent identity.

## Backwards compatibility

The proposed model is designed so that existing STIX objects remain unchanged.

### Existing STIX value

STIX 2.1:

```json
{
  "roles": [
    "infrastructure-operator"
  ]
}
```

STIX 2.2:

```json
{
  "roles": [
    "infrastructure-operator"
  ]
}
```

No change.

### New STIX core value

Suppose the STIX vocabulary registry later adds:

```text
initial-access-broker
```

A STIX 2.2 producer can use:

```json
{
  "roles": [
    "initial-access-broker"
  ]
}
```

A STIX 2.1 consumer already treats this as a syntactically valid unknown open-vocabulary value.

A STIX 2.2 consumer can additionally resolve its UUID and definition.

### External value

```json
{
  "roles": [
    "example-org:threat-actor-role=\"access-broker\""
  ]
}
```

An older implementation still sees a valid string.

A registry-aware implementation understands the namespace and semantic identifier.

## Compatibility matrix

| Producer         | Value                      | STIX 2.0/2.1 Consumer    | Registry-aware STIX 2.2 Consumer  |
| ---------------- | -------------------------- | ------------------------ | --------------------------------- |
| STIX 2.0/2.1     | Existing core value        | Native                   | Native + registry metadata        |
| STIX 2.2         | Existing core value        | Native                   | Native + registry metadata        |
| STIX 2.2         | New core registry value    | Valid unknown open-vocab | Native                            |
| STIX 2.2         | External unqualified value | Valid unknown open-vocab | Resolvable if uniquely registered |
| STIX 2.2         | Qualified external value   | Valid unknown open-vocab | Namespace and UUID resolvable     |
| MISP/STIX bridge | MISP machine tag           | Valid unknown open-vocab | Taxonomy directly resolvable      |

## Vocabulary versioning

Vocabulary definitions SHOULD contain a monotonically increasing version.

For example:

```text
malware-type-ov
UUID: A
Version: 1

  ransomware
  rootkit
  spyware
```

may evolve into:

```text
malware-type-ov
UUID: A
Version: 2

  ransomware
  rootkit
  spyware
  bootkit
```

The vocabulary UUID remains:

```text
A
```

Existing value UUIDs remain unchanged.

Only the registry version changes.

This allows vocabulary updates without requiring:

```text
STIX 2.2
STIX 2.3
STIX 2.4
...
```

for every vocabulary addition.

## Deprecation

Removing vocabulary values creates interoperability problems and SHOULD generally be avoided.

Instead, entries SHOULD support deprecation metadata.

For example:

```json
{
  "entries": {
    "745772a3-5700-5252-9374-7592620c7126": {
      "value": "old-term",
      "description": "A deprecated classification superseded by a distinct replacement concept.",
      "deprecated": true,
      "replaced_by_uuid": "b64be300-1209-5530-bc5c-1f8a7139cc74"
    }
  }
}
```

These snippets illustrate selected entries or metadata, rather than complete vocabulary documents. Their UUIDs use the illustrative allocation namespace above and do not represent TC assignments.

The old entry remains resolvable.

A non-semantic rename instead retains the entry UUID and records the previous value as an alias; it does not allocate a replacement UUID.

Consumers can recommend the newer value without making previously exchanged STIX objects invalid.

## Aliases and synonyms

Vocabulary entries MAY define aliases.

For example:

```json
{
  "entries": {
    "18a30266-cfea-536e-9929-d5df2f95bc92": {
      "value": "initial-access-broker",
      "description": "An entity that sells initial access to compromised networks.",
      "aliases": [
        "access-broker",
        "iab"
      ]
    }
  }
}
```

Aliases are useful for:

* search;
* translation;
* import;
* normalization;
* correlation.

The canonical serialized value remains:

```text
initial-access-broker
```

Aliases SHOULD NOT silently modify STIX content during ingestion.

## Registry directory

Vocabulary repositories SHOULD provide a machine-readable manifest.

This follows the deployment model successfully used by the MISP taxonomy repository.

Conceptually:

```json
{
  "version": 1,
  "description": "STIX Open Vocabulary Registry",
  "uuid": "ec9c0370-639f-5029-b7e1-1e0b931c0345",
  "vocabularies": [
    {
      "name": "threat-actor-role-ov",
      "expanded": "Threat Actor Role Vocabulary",
      "namespace": "stix",
      "vocabulary_uuid": "0bd60ffa-849e-54c0-963d-ea09bf98bd66",
      "version": 1,
      "format": "stix-open-vocab",
      "path": "stix/threat-actor-role-ov.json"
    },
    {
      "name": "Example Organization Vocabulary",
      "namespace": "example-org",
      "version": 4,
      "format": "misp-taxonomy",
      "path": "example-org/machinetag.json"
    }
  ]
}
```

A native manifest entry points to a single vocabulary document. A MISP source file may expose several logical vocabularies through its adapter, as described above.

A registry MAY reference another registry.

This permits federation.

## Federated vocabulary model

There SHOULD NOT be a requirement for a single global repository containing every possible vocabulary.

Instead:

```text
                  STIX Core Registry
                         |
          +--------------+--------------+
          |                             |
     FIRST registry                MISP registry
          |                             |
     sector vocab                +------+------+
                                 |             |
                             taxonomy       galaxy
                                 |
                      organization registry
```

Organizations can select which registries they trust or enable.

This supports:

* OASIS-managed vocabularies;
* FIRST vocabularies;
* MISP community vocabularies;
* national CSIRT vocabularies;
* ISAC/ISAO vocabularies;
* sector-specific vocabularies;
* vendor vocabularies;
* private organizational vocabularies.

## Registry discovery is optional

A critical requirement is that consuming STIX MUST NOT depend on a live external service.

For example:

```json
{
  "malware_types": [
    "example-org:malware-type=\"special-loader\""
  ]
}
```

remains valid even when:

```text
example-org vocabulary registry
```

cannot be reached.

Registry resolution provides additional semantics but MUST NOT be required to parse the STIX object.

Implementations MAY:

* ship vocabulary snapshots;
* periodically synchronize repositories;
* cache vocabulary definitions;
* operate entirely offline;
* disable external registry resolution;
* trust only explicitly configured registries.

## Registry security

Implementations MUST NOT automatically trust arbitrary vocabulary locations received from untrusted STIX content.

Vocabulary repositories SHOULD be configured or discovered through trusted manifests.

Registries SHOULD support integrity mechanisms such as:

* hashes;
* signed manifests;
* pinned repository revisions;
* trusted distribution channels.

A remote vocabulary update MUST NOT retrospectively alter the interpretation of an existing UUID.

The UUID identifies the semantic concept, while a URL merely identifies one possible location from which metadata can be retrieved.

## Source ordering and conflict handling

Implementations that combine vocabulary sources MUST use an explicit, ordered list of trusted sources. The default resolution rule MUST be **first source wins**: for a given vocabulary and entry UUID, the first configured source supplying that entry is authoritative. A later source MAY add previously unseen entries, but MUST NOT silently overwrite an entry already selected from an earlier source. Registry discovery order or network response timing MUST NOT determine precedence.

Within the selected source, a newer version MAY update metadata or rename a value while retaining its UUID under the UUID stability rules. Version counters from independently maintained sources MUST NOT be compared to select a winner. A local operator MAY explicitly reorder trusted sources, but doing so MUST NOT permit an existing UUID to acquire a different semantic meaning.

Consumers MUST detect and report conflicting definitions for the same UUID, canonical values assigned to different UUIDs within one vocabulary, and ambiguous aliases. Conflicting lower-priority entries MUST NOT be merged or silently substituted. Identical cached copies of an entry do not create a new identity. Values in different namespaces remain distinct and MAY be connected through explicit equivalence mappings.

Trust policy MUST identify which sources are authorized to define each namespace, including the `stix` namespace. Merely appearing earlier in a list MUST NOT allow an unauthorized source to redefine core STIX vocabulary entries.

An unavailable source MUST NOT automatically promote a lower-priority source to authoritative status. Implementations MAY use a trusted cached snapshot or an explicitly configured fallback policy, and otherwise leave the value unresolved. This affects optional vocabulary resolution only; the original STIX object and unknown open-vocabulary string remain valid.

## Proposed TAXII vocabulary discovery

TAXII servers SHOULD be able to advertise which vocabulary sources they use and the order in which they read them. This proposal recommends an optional `vocab_sources` endpoint relative to a TAXII API Root, for example `/taxii2/vocab_sources`. It is a proposed TAXII extension for TC discussion, not an endpoint defined by TAXII 2.1 or a change to the STIX wire datatype.

The endpoint SHOULD return an ordered list of source descriptors with:

* `vocabulary`: the qualified vocabulary name (`namespace:name`);
* `vocabulary_uuid`: its stable identity;
* `type`: `url` for a directly retrievable vocabulary document, or `taxii` for a TAXII Collection endpoint;
* `link`: the absolute HTTPS URL of that document or Collection.

For example:

```json
[
  {
    "vocabulary": "stix:threat-actor-role-ov",
    "vocabulary_uuid": "0bd60ffa-849e-54c0-963d-ea09bf98bd66",
    "type": "url",
    "link": "https://registry.example.org/stix/threat-actor-role-ov.json"
  },
  {
    "vocabulary": "stix:threat-actor-role-ov",
    "vocabulary_uuid": "0bd60ffa-849e-54c0-963d-ea09bf98bd66",
    "type": "taxii",
    "link": "https://taxii.example.org/taxii2/collections/role-vocabulary/"
  }
]
```

The array order MUST describe the server's configured precedence using the first-source-wins rule. In this example, the direct document is read first; the TAXII source may supplement it but cannot overwrite its selected entries. Multiple descriptors for the same vocabulary identify sources, not multiple vocabulary memberships for an entry.

For `url`, the consumer retrieves a vocabulary document and verifies its identity and format. For `taxii`, the consumer uses the advertised Collection's object retrieval mechanism. A TAXII extension MUST define the media type and representation used to transport vocabulary documents; this proposal does not treat a vocabulary document as an existing STIX SDO or imply that an unmodified TAXII 2.1 server can serve it.

An advertised source is discovery metadata, not automatic authorization to trust or contact it. Consumers MAY adopt the advertised order only after applying local trust policy, and MUST NOT be required to retrieve any source in order to process STIX objects. Cached and offline vocabulary use remains supported. Endpoint response format, pagination, authentication, and vocabulary transport media types remain TAXII TC design work.

## MISP taxonomy compatibility

MISP taxonomies are especially suitable for representing STIX open vocabularies.

A MISP taxonomy provides:

```text
namespace
predicate
value
UUID
version
description
```

A STIX implementation SHOULD therefore be able to register a MISP taxonomy as a vocabulary source without requiring the taxonomy to be converted into a new conceptual model.

For example:

```text
admiralty-scale:information-credibility="2"
```

can remain exactly the same machine tag in MISP and, when appropriate, be used as an external open-vocabulary value in STIX.

The UUID associated with the MISP taxonomy entry remains its semantic identifier.

## MISP galaxy compatibility

MISP galaxies provide a related but richer model.

A Galaxy defines a collection, and Galaxy Clusters provide:

* persistent UUIDs;
* values;
* descriptions;
* metadata;
* synonyms;
* references;
* relationships to other UUID-backed clusters.

For example:

```text
Galaxy
   |
   +-- Cluster A
   |      UUID A
   |      aliases
   |      references
   |
   +-- Cluster B
          UUID B
          |
          +---- related-to ---> UUID A
```

This model is useful when a vocabulary entry represents more than a simple classification value.

## Classification vocabularies versus knowledge vocabularies

The registry model SHOULD distinguish between two broad categories.

### Classification vocabulary

A classification vocabulary provides values used directly in an open-vocabulary property.

Examples include:

```text
threat-actor-role
malware-type
industry-sector
report-type
infrastructure-type
```

These map naturally to the MISP taxonomy model.

### Knowledge vocabulary

A knowledge vocabulary represents named concepts with richer metadata and relationships.

Examples include:

```text
known threat actors
malware families
tools
attack techniques
ransomware groups
country-specific threat classifications
```

These map naturally to the MISP galaxy model.

Where STIX already has an appropriate SDO, the SDO SHOULD normally be used to represent the actual concept.

For example:

```text
MISP Galaxy Cluster
        |
        | maps to
        v
Threat Actor SDO
```

rather than placing:

```text
APT28
```

in a generic open-vocabulary property.

The Galaxy registry remains useful for:

* UUID identity;
* synonyms;
* mappings;
* import/export;
* enrichment;
* external references;
* relationships;
* cross-ecosystem interoperability.

## Registry source formats

A vocabulary registry SHOULD be capable of describing multiple source formats.

For example:

```text
stix-open-vocab
misp-taxonomy
misp-galaxy
```

A manifest entry might declare:

```json
{
  "name": "Example Threat Vocabulary",
  "namespace": "example",
  "format": "misp-taxonomy",
  "version": 8,
  "path": "machinetag.json"
}
```

or:

```json
{
  "name": "Example Threat Actor Knowledge Base",
  "namespace": "example-actors",
  "format": "misp-galaxy",
  "version": 12,
  "path": "threat-actors.json"
}
```

This allows the existing MISP repositories to participate directly instead of requiring duplicated STIX-specific copies.

## Private vocabularies

Nothing in the registry model SHOULD require a vocabulary to be public.

For example:

```text
banking-isac:fraud-type="account-takeover"
```

could resolve only inside a banking information-sharing community.

Similarly:

```text
internal-soc:incident-origin="honeypot-cluster-3"
```

could be meaningful only within one organization.

The same namespace and UUID mechanisms apply.

## Extending another vocabulary

A vocabulary MAY explicitly extend another vocabulary.

For example:

```json
{
  "namespace": "example-org",
  "name": "extended-malware-types",
  "expanded": "Example Extended Malware Types",
  "uuid": "c572a64b-f1ef-50ff-886b-7033c49225ec",
  "version": 3,
  "extends": [
    {
      "vocabulary": "malware-type-ov",
      "namespace": "stix",
      "uuid": "57112fbe-9939-555e-847f-47a418119ff1"
    }
  ]
}
```

The extension MAY:

* add values;
* add aliases;
* provide mappings;
* add descriptions;
* add translations.

An extension MUST NOT redefine the meaning of an existing value UUID.

## Multiple extensions

Several communities may independently extend the same STIX vocabulary.

For example:

```text
                    STIX malware-type-ov
                           |
          +----------------+----------------+
          |                |                |
       Vendor A          CSIRT A          ISAC B
          |                |                |
      extension        extension        extension
```

No central approval is necessary for private extensions.

Public registries MAY establish their own governance requirements before accepting an extension.

## Vocabulary relationships and mappings

Vocabulary entries MAY contain relationships to other entries.

For example:

```json
{
  "entries": {
    "18a30266-cfea-536e-9929-d5df2f95bc92": {
      "value": "initial-access-broker",
      "description": "An entity that sells initial access to compromised networks.",
      "related": [
        {
          "type": "narrower-than",
          "dest_uuid": "8baf1b75-4ea2-53f7-8c89-b01b48f8fe1e"
        }
      ]
    }
  }
}
```

Useful relationship types MAY include:

```text
equivalent-to
similar-to
broader-than
narrower-than
derived-from
replaced-by
related-to
```

The relationship mechanism SHOULD follow the same UUID-based principle used by MISP Galaxy clusters.

## Cross-vocabulary equivalence

One important benefit of UUID-backed registries is explicit mappings between independently maintained vocabularies.

For example:

```text
STIX:
    malware-type-ov:ransomware
             |
             | equivalent-to
             v
Community taxonomy:
    incident-classification:ransomware
```

This mapping SHOULD be represented as metadata rather than silently replacing one vocabulary value with another.

## Numerical values

Vocabulary entries MAY expose a numerical value when this is semantically useful.

This is compatible with MISP taxonomies.

For example:

```json
{
  "entries": {
    "74bd5a67-0d28-577f-9ff8-d5faf52d928c": {
      "value": "very-high",
      "description": "The highest confidence category in the example organization scale.",
      "numerical_value": 90
    }
  }
}
```

The textual value remains the canonical STIX representation.

The numeric value is supplemental metadata.

## Human-readable labels and translations

Vocabulary entries SHOULD distinguish the machine-readable value from display text.

For example:

```json
{
  "entries": {
    "b48c5d16-f836-5c76-91a4-838bdb5f6155": {
      "value": "infrastructure-operator",
      "expanded": "Infrastructure Operator",
      "description": "An entity that operates infrastructure used to conduct attacks."
    }
  }
}
```

A registry MAY additionally provide localized display strings:

```json
{
  "translations": {
    "fr": "Opérateur d'infrastructure",
    "de": "Infrastrukturbetreiber"
  }
}
```

The STIX wire value remains:

```text
infrastructure-operator
```

This avoids localization affecting interoperability.

## Updating STIX Section 2.14

The definition of `open-vocab` SHOULD be updated conceptually from:

> a string which SHOULD come from a suggested vocabulary defined by the STIX specification

to:

> a string whose value MAY be defined by a STIX core vocabulary or another vocabulary source. STIX core vocabularies provide recommended values. Additional values MAY be defined by registered or private vocabularies. Producers SHOULD use registered values where an appropriate value exists. Consumers MUST NOT reject an object solely because an open-vocabulary value is unknown.

The existing lowercase and hyphen recommendation SHOULD remain for unqualified custom values.

Qualified vocabulary values MAY additionally use a registered namespace syntax.

## Updating STIX Section 10

The existing Section 10 vocabulary definitions SHOULD remain in STIX 2.2 as the **baseline STIX vocabulary snapshot**.

This preserves:

* human-readable documentation;
* backwards compatibility;
* reproducible specification versions.

Each open vocabulary SHOULD additionally identify:

```text
Vocabulary Name
Vocabulary UUID
Registry Namespace
Registry Location
Registry Version
```

For example:

```text
Vocabulary Name: threat-actor-role-ov
Registry Namespace: stix
Vocabulary UUID: <TC-assigned UUID>
```

The values documented in STIX 2.2 become the initial registry values.

Subsequent compatible values MAY be added to the registry without requiring modification of the STIX core object model.

## Enumerations are unchanged

This proposal applies only to:

```text
open-vocab
```

It does not apply to:

```text
enum
```

For example, where STIX defines an Enumeration:

```text
value MUST be one of:
    x
    y
    z
```

the permitted values remain controlled by the STIX specification.

A registry MUST NOT be used to extend an Enumeration.

This distinction remains explicit:

```text
Enumeration
    CLOSED
    specification-controlled

Open Vocabulary
    OPEN
    registry-assisted
```

## Example: current STIX vocabulary

A STIX object:

```json
{
  "type": "threat-actor",
  "spec_version": "2.2",
  "id": "threat-actor--8e2e2d2b-17d4-4cbf-938f-98ee46b3cd3f",
  "created": "2026-08-14T08:00:00.000Z",
  "modified": "2026-08-14T08:00:00.000Z",
  "name": "Example Actor",
  "roles": [
    "infrastructure-operator"
  ]
}
```

A registry-aware consumer resolves:

```text
property:
    threat-actor.roles

vocabulary:
    threat-actor-role-ov

namespace:
    stix

value:
    infrastructure-operator

value UUID:
    <stable UUID>

description:
    <description maintained by the vocabulary>

version:
    <registry version>
```

Nothing additional is required in the STIX object.

## Example: external extension

An organization publishes:

```text
namespace:
    example-org

vocabulary:
    threat-actor-role

extends:
    STIX threat-actor-role-ov

entry:
    initial-access-broker

UUID:
    <stable UUID>
```

It can serialize:

```json
{
  "roles": [
    "infrastructure-operator",
    "example-org:threat-actor-role=\"initial-access-broker\""
  ]
}
```

A legacy implementation can still process the object.

A registry-aware implementation can resolve both terms.

## Example: MISP taxonomy reused directly

Suppose an existing taxonomy contains:

```text
admiralty-scale:information-credibility="2"
```

and its taxonomy entry already has a stable UUID.

A STIX implementation that uses this vocabulary SHOULD preserve:

* the namespace;
* predicate;
* value;
* UUID.

It SHOULD NOT allocate a second STIX-specific UUID for the same imported vocabulary entry.

This enables:

```text
MISP
   |
   | same namespace/value/UUID
   v
STIX
   |
   | same namespace/value/UUID
   v
MISP
```

without creating duplicate vocabulary identities.

## Example: Galaxy-backed knowledge entry

Suppose a MISP Galaxy contains:

```text
Threat Actor: Example Panda
UUID: A
Aliases:
    Example Group
    Panda Team
References:
    ...
```

A STIX converter can create:

```text
threat-actor--...
```

while retaining:

```text
Galaxy Cluster UUID A
```

as an external semantic identifier or mapping.

The vocabulary registry can retain the mapping:

```text
Galaxy Cluster UUID A
           |
           | maps-to
           v
STIX Threat Actor
```

This is preferable to replacing the Threat Actor SDO with a string vocabulary value.

## Why not put UUIDs directly in open-vocab properties?

Changing:

```json
"roles": [
  "director"
]
```

to:

```json
"roles": [
  {
    "value": "director",
    "uuid": "..."
  }
]
```

would change the STIX datatype and break existing implementations.

Changing it to:

```json
"roles": [
  "urn:uuid:..."
]
```

would preserve the JSON datatype but lose human readability and break existing value-based processing.

The registry approach provides both:

```text
human-readable stable wire value
+
persistent semantic UUID
```

without changing existing STIX objects.

## Why not keep vocabularies only in the specification?

Static specification vocabularies create unnecessary coupling between:

```text
vocabulary evolution
```

and:

```text
STIX specification evolution
```

A new malware category, infrastructure role, industry sector, threat actor role, or report type should not necessarily require a new STIX specification revision.

The object model should remain stable while the terminology can evolve.

## Benefits

### Backwards compatibility

No existing STIX vocabulary value changes.

### Forward compatibility

Older consumers already have a defined behavior for unknown open-vocabulary strings.

### Independent evolution

Vocabulary updates do not require changes to the STIX object model.

### Stable semantic identity

UUIDs make vocabulary entries persistent across renames, repository moves, and metadata updates.

### Decentralization

Organizations can maintain their own vocabularies without requesting additions to the core STIX specification.

### Federation

Multiple repositories can coexist and cross-reference one another.

### Offline use

Registry access is optional and vocabularies can be cached or distributed as files.

### Existing ecosystem reuse

MISP taxonomy and galaxy repositories can be directly reused instead of recreating equivalent vocabulary infrastructure.

### Improved mapping

UUID-based equivalence relationships make mappings between MISP, STIX, sector vocabularies, vendor vocabularies, and other CTI standards explicit.

## Open questions for TC discussion

1. Should STIX 2.2 formally separate **open vocabulary definitions** from the STIX specification lifecycle?
2. Should every existing STIX open vocabulary receive a stable UUID?
3. Should every existing STIX open-vocabulary value receive a stable UUID?
4. Which allocation namespace UUID should the TC publish for the proposed deterministic UUIDv5 allocation rules, while preserving imported UUIDs?
5. Should the STIX Core Vocabulary Registry use the proposed single-vocabulary documents with UUID-keyed entries and mandatory descriptions?
6. Should STIX define its own vocabulary format while requiring lossless conversion to and from the MISP taxonomy format?
7. Should MISP machine-tag syntax be RECOMMENDED for qualified external vocabulary values?
8. Should qualified external values use:

```text
namespace:predicate="value"
```

or a simpler STIX-specific representation such as:

```text
namespace:value
```

9. Should unqualified values be implicitly interpreted as belonging to the STIX core vocabulary associated with the property?
10. Should external vocabularies explicitly declare which STIX vocabulary UUID they extend?
11. Should registry manifests be standardized as part of STIX 2.2?
12. Should registry manifests support multiple formats such as:

```text
stix-open-vocab
misp-taxonomy
misp-galaxy
```

13. Should registry entries support aliases and translations?
14. Should registry entries support numerical values?
15. Should vocabulary entries support UUID-based relationships such as `equivalent-to`, `broader-than`, and `replaced-by`?
16. Should deprecated vocabulary entries remain permanently resolvable?
17. Should the STIX TC maintain an official vocabulary registry repository independently from the STIX specification repository?
18. Should third-party registry discovery remain outside STIX validation, with ordered source lists and the proposed first-source-wins conflict handling?
19. Should vocabulary registry integrity or signing mechanisms be standardized or left to repository implementations?
20. Should a common crosswalk format be defined for mappings between STIX vocabularies, MISP taxonomies, MISP galaxies, and other CTI vocabularies?
21. Should TAXII define the proposed optional `vocab_sources` endpoint supporting both direct vocabulary URLs and TAXII Collections, and which media types should carry vocabulary documents?

## Proposed next steps

1. Confirm that the `open-vocab` wire datatype remains a string.
2. Identify all existing STIX open vocabularies and distinguish them from Enumerations.
3. Publish the TC allocation namespace and deterministically allocate UUIDv5 identifiers to each existing STIX open vocabulary.
4. Deterministically allocate UUIDv5 identifiers to all initial core vocabulary entries; preserve existing imported UUIDs and retain allocated UUIDs across non-semantic renames.
5. Define the STIX Core Vocabulary Registry.
6. Create one native document per Section 10 open vocabulary, with UUID-keyed entries and a description for each entry.
7. Define registry versioning and UUID stability rules.
8. Define namespace rules for third-party vocabulary extensions.
9. Define the behavior of qualified and unqualified values.
10. Define a vocabulary registry manifest and ordered, trusted source resolution using first-source-wins conflict handling.
11. Define compatibility rules for MISP taxonomy repositories.
12. Define compatibility and mapping rules for MISP galaxy repositories.
13. Define extension, deprecation, alias, and equivalence mechanisms.
14. Update Section 2.14 to describe registry-backed open vocabularies.
15. Update Section 10 so that its existing vocabulary values remain the STIX 2.2 baseline snapshot.
16. Add conformance tests demonstrating that:

    * all STIX 2.0/2.1 values remain valid;
    * unknown strings remain valid open-vocabulary values;
    * new core registry values are accepted;
    * qualified external values are accepted;
    * registry resolution is optional;
    * UUIDv5 allocation is reproducible and non-semantic renames preserve identifiers;
    * duplicate entry keys and ambiguous values or aliases are detected;
    * later sources cannot silently overwrite earlier authoritative entries;
    * enumerations cannot be extended through the registry.
17. Publish a reference STIX vocabulary repository.
18. Demonstrate interoperability by consuming existing `misp-taxonomies` and `misp-galaxy` repositories without changing their UUID identities.
19. Coordinate the optional TAXII `vocab_sources` discovery endpoint and the media types needed for direct URL and TAXII Collection vocabulary distribution.

