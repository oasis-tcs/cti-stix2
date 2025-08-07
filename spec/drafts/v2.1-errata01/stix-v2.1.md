![OASIS Logo](https://docs.oasis-open.org/templates/OASISLogo-v3.0.png)

---

# STIX Version 2.1 Errata 01

## Committee Specification 01

### 2 April 2025

#### This stage:

https://docs.oasis-open.org/cti/stix/v2.1/stix-v2.1.docx (Authoritative) \
https://docs.oasis-open.org/cti/stix/v2.1/stix-v2.1.html \
https://docs.oasis-open.org/cti/stix/v2.1/stix-v2.1.pdf

#### Previous stage:

https://docs.oasis-open.org/cti/stix/v2.1/os/stix-v2.1-os.docx (Authoritative) \
https://docs.oasis-open.org/cti/stix/v2.1/os/stix-v2.1-os.html \
https://docs.oasis-open.org/cti/stix/v2.1/os/stix-v2.1-os.pdf

#### Latest stage:

https://docs.oasis-open.org/cti/stix/v2.1/stix-v2.1.docx (Authoritative) \
https://docs.oasis-open.org/cti/stix/v2.1/stix-v2.1.html \
https://docs.oasis-open.org/cti/stix/v2.1/stix-v2.1.pdf

#### Technical Committee:

[OASIS Cyber Threat Intelligence (CTI) TC](https://www.oasis-open.org/committees/cti/)

#### Chairs:

Marlon Taylor (<marlon.taylor@cisa.dhs.gov>), [DHS Office of Cybersecurity and Communications](http://www.cisa.gov/)  
Alexandre Dulaunoy (<alexandre.dulaunoy@x.circl.lu>), [CIRCL](https://www.circl.lu/)

#### Editors:

Rich Piazza (<rpiazza@mitre.org>), [MITRE Corporation](http://www.mitre.org/)  
Emily Ratliff (<emily.ratliff@ibm.com>), [IBM](http://www.ibm.com/)  
Stephan Relitz (<stephan.relitz@peraton.com>), [Peraton](https://www.peraton.com/)  
Christian Studer (<christian.studer@circl.lu>), [CIRCL](https://www.circl.lu/)

#### Related work:

This specification replaces or supersedes:

- _STIX Version 2.1._ Edited by Bret Jordan, Rich Piazza, and Trey Darley. Latest stage: <https://docs.oasis-open.org/cti/stix/v2.1/stix-v2.1.html>.

This specification is related to:

- _TAXII Version 2.1._ Edited by Bret Jordan and Drew Varner. Latest stage: <https://docs.oasis-open.org/cti/taxii/v2.1/taxii-v2.1.html>.
- _STIX/TAXII 2.0 Interoperability Test Document: Part 1 Version 1.1._ Edited by Allan Thomson and Jason Keirstead. Latest stage: <https://docs.oasis-open.org/cti/stix-taxii-2-interop-p1/v1.1/stix-taxii-2-interop-p1-v1.1.html>.
- _STIX/TAXII 2.0 Interoperability Test Document: Part 2 Version 1.0._ Edited by Allan Thomson and Jason Keirstead. Latest stage: <https://docs.oasis-open.org/cti/stix-taxii-2-interop-p2/v1.0/stix-taxii-2-interop-p2-v1.0.html>.

#### Abstract:

Structured Threat Information Expression (STIX) is a language for expressing cyber threat and observable information. This document defines concepts that apply across all of STIX and defines the overall structure of the STIX language.

#### Status:

This document was last revised or approved by the membership of OASIS on the above date. The level of approval is also listed above. Check the "Latest stage" location noted above for possible later revisions of this document. Any other numbered Versions and other technical work produced by the Technical Committee (TC) are listed at <https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=cti#technical>.

TC members should send comments on this document to the TC's email list. Others should send comments to the TC's public comment list, after subscribing to it by following the instructions at the "[Send A Comment](https://www.oasis-open.org/committees/comments/index.php?wg_abbrev=cti)" button on the TC's web page at <https://www.oasis-open.org/committees/cti/>.

This specification is provided under the [Non-Assertion](https://www.oasis-open.org/policies-guidelines/ipr#Non-Assertion-Mode) Mode of the [OASIS IPR Policy](https://www.oasis-open.org/policies-guidelines/ipr/), the mode chosen when the Technical Committee was established. For information on whether any patents have been disclosed that may be essential to implementing this specification, and any offers of patent licensing terms, please refer to the Intellectual Property Rights section of the TC's web page (<https://www.oasis-open.org/committees/cti/ipr.php>).

Note that any machine-readable content ([Computer Language Definitions](https://www.oasis-open.org/policies-guidelines/tc-process-2017-05-26#wpComponentsCompLang)) declared Normative for this Work Product is provided in separate plain text files. In the event of a discrepancy between any such plain text file and display content in the Work Product's prose narrative document(s), the content in the separate plain text file prevails.

#### Key words:

The key words "**MUST**", "**MUST NOT**", "**REQUIRED**", "**SHALL**", "**SHALL NOT**", "**SHOULD**", "**SHOULD NOT**", "**RECOMMENDED**", "**NOT RECOMMENDED**", "**MAY**", and "**OPTIONAL**" in this document are to be interpreted as described in BCP 14 \[[RFC2119](#RFC2119)\] \[[RFC8174](#RFC8174)\] when, and only when, they appear in all capitals, as shown here.

#### Citation format:

When referencing this specification the following citation format should be used:

**\[STI-v2.1-errata01\]**

_STIX Version 2.1 Errata 01_. Edited by Rich Piazza, Emily Ratliff, Stephan Relitz and Christian Studer. 02 April 2025. OASIS Committee Specification Draft 01. <https://docs.oasis-open.org/cti/stix/v2.1/stix-v2.1.html>. Latest stage: <https://docs.oasis-open.org/cti/stix/v2.1/stix-v2.1.html>.

---

## Notices

Copyright © OASIS Open 2025. All Rights Reserved.

All capitalized terms in the following text have the meanings assigned to them in the OASIS Intellectual Property Rights Policy (the "OASIS IPR Policy"). The full [Policy](https://www.oasis-open.org/policies-guidelines/ipr/) may be found at the OASIS website.

This document and translations of it may be copied and furnished to others, and derivative works that comment on or otherwise explain it or assist in its implementation may be prepared, copied, published, and distributed, in whole or in part, without restriction of any kind, provided that the above copyright notice and this section are included on all such copies and derivative works. However, this document itself may not be modified in any way, including by removing the copyright notice or references to OASIS, except as needed for the purpose of developing any document or deliverable produced by an OASIS Technical Committee (in which case the rules applicable to copyrights, as set forth in the OASIS IPR Policy, must be followed) or as required to translate it into languages other than English.

The limited permissions granted above are perpetual and will not be revoked by OASIS or its successors or assigns.

This document and the information contained herein is provided on an "AS IS" basis and OASIS DISCLAIMS ALL WARRANTIES, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO ANY WARRANTY THAT THE USE OF THE INFORMATION HEREIN WILL NOT INFRINGE ANY OWNERSHIP RIGHTS OR ANY IMPLIED WARRANTIES OF MERCHANTABILITY OR FITNESS FOR A PARTICULAR PURPOSE.

As stated in the OASIS IPR Policy, the following three paragraphs in brackets apply to OASIS Standards Final Deliverable documents (Committee Specification, Candidate OASIS Standard, OASIS Standard, or Approved Errata).

\[OASIS requests that any OASIS Party or any other party that believes it has patent claims that would necessarily be infringed by implementations of this OASIS Standards Final Deliverable, to notify OASIS TC Administrator and provide an indication of its willingness to grant patent licenses to such patent claims in a manner consistent with the IPR Mode of the OASIS Technical Committee that produced this deliverable.\]

\[OASIS invites any party to contact the OASIS TC Administrator if it is aware of a claim of ownership of any patent claims that would necessarily be infringed by implementations of this OASIS Standards Final Deliverable by a patent holder that is not willing to provide a license to such patent claims in a manner consistent with the IPR Mode of the OASIS Technical Committee that produced this OASIS Standards Final Deliverable. OASIS may include such claims on its website, but disclaims any obligation to do so.\]

\[OASIS takes no position regarding the validity or scope of any intellectual property or other rights that might be claimed to pertain to the implementation or use of the technology described in this OASIS Standards Final Deliverable or the extent to which any license under such rights might or might not be available; neither does it represent that it has made any effort to identify any such rights. Information on OASIS' procedures with respect to rights in any document or deliverable produced by an OASIS Technical Committee can be found on the OASIS website. Copies of claims of rights made available for publication and any assurances of licenses to be made available, or the result of an attempt made to obtain a general license or permission for the use of such proprietary rights by implementers or users of this OASIS Standards Final Deliverable, can be obtained from the OASIS TC Administrator. OASIS makes no representation that any information or list of intellectual property rights will at any time be complete, or that any claims in such list are, in fact, Essential Claims.\]

The name "OASIS" is a trademark of [OASIS](https://www.oasis-open.org/), the owner and developer of this specification, and should be used only to refer to the organization and its official outputs. OASIS welcomes reference to, and implementation and use of, specifications, while reserving the right to enforce its marks against misleading uses. Please see https://www.oasis-open.org/policies-guidelines/trademark/ for above guidance.

---

# Table of Contents

- 1. [Introduction](#introduction)
  - 1.1 [Document Conventions](#document-conventions)
  - 1.2 [Overview](#overview)
    - 1.2.1 [Graph-Based Model](#graph-based-model)
    - 1.2.2 [STIX Domain Objects](#overview-stix-domain-objects)
    - 1.2.3 [STIX Cyber-observable Objects](#overview-stix-cyber-observable-objects)
    - 1.2.4 [STIX Relationships](#stix-relationships)
    - 1.2.5 [STIX Cyber Observable Observed Data Relationships (Deprecated)](#stix-cyber-observable-observed-data-relationships)
    - 1.2.6 [STIX Patterning](#overview-stix-patterning)
    - 1.2.7 [STIX Common Properties](#stix-common-properties)
    - 1.2.8 [STIX Open Vocabularies and Enumerations](#stix-open-vocabularies-and-enumerations)
    - 1.2.9 [Reserved Names](#overview-reserved-names)
    - 1.2.10 [Serialization](#serialization)
    - 1.2.11 [Transporting STIX](#transporting-stix)
    - 1.2.12 [JSON Schemas](#json-schemas)
  - 1.3 [Changes From Earlier Version](#changes-from-earlier-version)
    - 1.3.1 [STIX 2.1 Errata 01 Changes from earlier version](#stix-21-errata-01-changes-from-earlier-version)
  - 1.4 [Glossary](#glossary)
- 2. [Common Data Types](#common-data-types)
  - 2.1 [Binary](#binary)
  - 2.2 [Boolean](#boolean)
  - 2.3 [Dictionary](#dictionary)
  - 2.4 [Enum](#enum)
  - 2.5 [External Reference](#external-reference)
    - 2.5.1 [Properties](#external-reference-properties)
    - 2.5.2 [Requirements](#external-reference-requirements)
  - 2.6 [Float](#float)
  - 2.7 [Hashes](#hashes)
  - 2.8 [Hexadecimal](#hexadecimal)
  - 2.9 [Identifier](#identifier)
  - 2.10 [Integer](#integer)
  - 2.11 [Kill Chain Phase](#kill-chain-phase)
  - 2.12 [List](#list)
  - 2.13 [Observable Container (deprecated)](#observable-container)
  - 2.14 [Open Vocabulary](#open-vocabulary)
  - 2.15 [String](#string)
  - 2.16 [Timestamp](#timestamp)
    - 2.16.1 [Requirements](#timestamp-requirements)
- 3. [STIX General Concepts](#stix-general-concepts)
  - 3.1 [Property Names and String Literals](#property-names-and-string-literals)
  - 3.2 [Common Properties](#stix-common-properties)
  - 3.3 [Object IDs and References](#object-ids-and-references)
  - 3.4 [SCO Deterministic ID Creation](#sco-deterministic-id-creation)
  - 3.5 [Object Creator](#object-creator)
  - 3.6 [Versioning](#versioning)
    - 3.6.1 [Versioning Timestamps](#versioning-timestamps)
    - 3.6.2 [New Version or New Object?](#new-version-or-new-object)
  - 3.7 [Common Relationships](#common-relationships)
  - 3.8 [Reserved Names](#reserved-names)
  - 3.9 [Object Property Metadata](#object-property-metadata)
    - 3.9.1 [SCO String Encoding](#sco-string-encoding)
  - 3.10 [Predefined Object Extensions](#predefined-object-extensions)
- 4. [STIX Domain Objects](#stix-domain-objects)
  - 4.1 [Attack Pattern](#attack-pattern)
    - 4.1.1 [Properties](#attack-pattern-properties)
    - 4.1.2 [Relationships](#attack-pattern-relationships)
  - 4.2 [Campaign](#campaign)
    - 4.2.1 [Properties](#campaign-properties)
    - 4.2.2 [Relationships](#campaign-relationships)
  - 4.3 [Course of Action](#course-of-action)
    - 4.3.1 [Properties](#course-of-action-properties)
    - 4.3.2 [Relationships](#course-of-action-relationships)
  - 4.4 [Grouping](#grouping)
    - 4.4.1 [Properties](#grouping-properties)
    - 4.4.2 [Relationships](#grouping-relationships)
  - 4.5 [Identity](#identity)
    - 4.5.1 [Properties](#identity-properties)
    - 4.5.2 [Relationships](#identity-relationships)
  - 4.6 [Incident](#incident)
    - 4.6.1 [Properties](#incident-properties)
    - 4.6.2 [Relationships](#incident-relationships)
  - 4.7 [Indicator](#indicator)
    - 4.7.1 [Properties](#indicator-properties)
    - 4.7.2 [Relationships](#indicator-relationships)
  - 4.8 [Infrastructure](#infrastructure)
    - 4.8.1 [Properties](#infrastructure-properties)
    - 4.8.2 [Relationships](#infrastructure-relationships)
  - 4.9 [Intrusion Set](#intrusion-set)
    - 4.9.1 [Properties](#intrusion-set-properties)
    - 4.9.2 [Relationships](#intrusion-set-relationships)
  - 4.10 [Location](#location)
    - 4.10.1 [Properties](#location-properties)
    - 4.10.2 [Relationships](#location-relationships)
  - 4.11 [Malware](#malware)
    - 4.11.1 [Properties](#malware-properties)
    - 4.11.2 [Relationships](#malware-relationships)
  - 4.12 [Malware Analysis](#malware-analysis)
    - 4.12.1 [Properties](#malware-analysis-properties)
    - 4.12.2 [Relationships](#malware-analysis-relationships)
  - 4.13 [Note](#note)
    - 4.13.1 [Properties](#note-properties)
    - 4.13.2 [Relationships](#note-relationships)
  - 4.14 [Observed Data](#observed-data)
    - 4.14.1 [Properties](#observed-data-properties)
    - 4.14.2 [Relationships](#observed-data-relationships)
  - 4.15 [Opinion](#opinion)
    - 4.15.1 [Properties](#opinion-properties)
    - 4.15.2 [Relationships](#opinion-relationships)
  - 4.16 [Report](#report)
    - 4.16.1 [Properties](#report-properties)
    - 4.16.2 [Relationships](#report-relationships)
  - 4.17 [Threat Actor](#threat-actor)
    - 4.17.1 [Properties](#threat-actor-properties)
    - 4.17.2 [Relationships](#threat-actor-relationships)
  - 4.18 [Tool](#tool)
    - 4.18.1 [Properties](#tool-properties)
    - 4.18.2 [Relationships](#tool-relationships)
  - 4.19 [Vulnerability](#vulnerability)
    - 4.19.1 [Properties](#vulnerability-properties)
    - 4.19.2 [Relationships](#vulnerability-relationships)
- 5. [STIX Relationship Objects](#stix-relationship-objects)
  - 5.1 [Relationship](#relationship)
    - 5.1.1 [Specification-Defined Relationships Summary](#specification-defined-relationships-summary)
    - 5.1.2 [Properties](#relationship-properties)
    - 5.1.3 [Relationships](#relationship-relationships)
  - 5.2 [Sighting](#sighting)
    - 5.2.1 [Properties](#sighting-properties)
    - 5.2.2 [Relationships](#sighting-relationships)
- 6. [STIX Cyber-observable Objects](#stix-cyber-observable-objects)
  - 6.1 [Artifact Object](#artifact-object)
    - 6.1.1 [Properties](#artifact-object-properties)
  - 6.2 [Autonomous System (AS) Object](#autonomous-system-as-object)
    - 6.2.1 [Properties](#autonomous-system-as-object-properties)
  - 6.3 [Directory Object](#directory-object)
    - 6.3.1 [Properties](#directory-object-properties)
  - 6.4 [Domain Name Object](#domain-name-object)
    - 6.4.1 [Properties](#domain-name-object-properties)
    - 6.4.2 [Relationships](#domain-name-object-relationships)
  - 6.5 [Email Address Object](#email-address-object)
    - 6.5.1 [Properties](#email-address-object-properties)
  - 6.6 [Email Message Object](#email-message-object)
    - 6.6.1 [Properties](#email-message-object-properties)
    - 6.6.2 [Email MIME Component Type](#email-mime-component-type)
      - 6.6.2.1 [Properties](#email-mime-component-type-properties)
  - 6.7 [File Object](#file-object)
    - 6.7.1 [Properties](#file-object-properties)
    - 6.7.2 [Archive File Extension](#archive-file-extension)
      - 6.7.2.1 [Properties](#archive-file-extension-properties)
    - 6.7.3 [NTFS File Extension](#ntfs-file-extension)
      - 6.7.3.1 [Properties](#ntfs-file-extension-properties)
      - 6.7.3.2 [Alternate Data Stream Type](#alternate-data-stream-type)
    - 6.7.4 [PDF File Extension](#pdf-file-extension)
      - 6.7.4.1 [Properties](#pdf-file-extension-properties)
    - 6.7.5 [Raster Image File Extension](#raster-image-file-extension)
      - 6.7.5.1 [Properties](#raster-image-file-extension-properties)
    - 6.7.6 [Windows PE Binary File Extension](#windows-pe-binary-file-extension)
      - 6.7.6.1 [Properties](#windows-pe-binary-file-extension-properties)
      - 6.7.6.2 [Windows PE Optional Header Type](#windows-pe-optional-header-type)
      - 6.7.6.3 [Windows PE Section Type](#windows-pe-section-type)
  - 6.8 [IPv4 Address Object](#ipv4-address-object)
    - 6.8.1 [Properties](#ipv4-address-object-properties)
    - 6.8.2 [Relationships](#ipv4-address-object-relationships)
  - 6.9 [IPv6 Address Object](#ipv6-address-object)
    - 6.9.1 [Properties](#ipv6-address-object-properties)
    - 6.9.2 [Relationships](#ipv6-address-object-relationships)
  - 6.10 [MAC Address Object](#mac-address-object)
    - 6.10.1 [Properties](#mac-address-object-properties)
  - 6.11 [Mutex Object](#mutex-object)
    - 6.11.1 [Properties](#mutex-object-properties)
  - 6.12 [Network Traffic Object](#network-traffic-object)
    - 6.12.1 [Properties](#network-traffic-object-properties)
    - 6.12.2 [HTTP Request Extension](#http-request-extension)
      - 6.12.2.1 [Properties](#http-request-extension-properties)
    - 6.12.3 [ICMP Extension](#icmp-extension)
      - 6.12.3.1 [Properties](#icmp-extension-properties)
    - 6.12.4 [Network Socket Extension](#network-socket-extension)
      - 6.12.4.1 [Properties](#network-socket-extension-properties)
    - 6.12.5 [TCP Extension](#tcp-extension)
      - 6.12.5.1 [Properties](#tcp-extension-properties)
  - 6.13 [Process Object](#process-object)
    - 6.13.1 [Properties](#process-object-properties)
    - 6.13.2 [Windows Process Extension](#windows-process-extension)
      - 6.13.2.1 [Properties](#windows-process-extension-properties)
    - 6.13.3 [Windows Service Extension](#windows-service-extension)
      - 6.13.3.1 [Properties](#windows-service-extension-properties)
  - 6.14 [Software Object](#software-object)
    - 6.14.1 [Properties](#software-object-properties)
  - 6.15 [URL Object](#url-object)
    - 6.15.1 [Properties](#url-object-properties)
  - 6.16 [User Account Object](#user-account-object)
    - 6.16.1 [Properties](#user-account-object-properties)
    - 6.16.2 [UNIX Account Extension](#unix-account-extension)
      - 6.16.2.1 [Properties](#unix-account-extension-properties)
  - 6.17 [Windows Registry Key Object](#windows-registry-key-object)
    - 6.17.1 [Properties](#windows-registry-key-object-properties)
    - 6.17.2 [Windows Registry Value Type](#windows-registry-value-type)
      - 6.17.2.1 [Properties](#windows-registry-value-type-properties)
  - 6.18 [X.509 Certificate Object](#x509-certificate-object)
    - 6.18.1 [Properties](#x509-certificate-object-properties)
    - 6.18.2 [X.509 v3 Extensions Type](#x509-v3-extensions-type)
      - 6.18.2.1 [Properties](#x509-v3-extensions-type-properties)
- 7. [STIX Meta Objects](#stix-meta-objects)
  - 7.1 [Language Content](#language-content)
    - 7.1.1 [Properties](#language-content-properties)
    - 7.1.2 [Relationships](#language-content-relationships)
  - 7.2 [Data Markings](#data-markings)
    - 7.2.1 [Marking Definition](#marking-definition)
      - 7.2.1.1 [Properties](#marking-definition-properties)
      - 7.2.1.2 [Relationships](#marking-definition-relationships)
      - 7.2.1.3 [Statement Marking Object Type](#statement-marking-object-type)
      - 7.2.1.4 [TLP Marking Object Type](#tlp-marking-object-type)
    - 7.2.2 [Object Markings](#object-markings)
    - 7.2.3 [Granular Markings](#granular-markings)
      - 7.2.3.1 [Granular Marking Type](#granular-marking-type)
  - 7.3 [Extension Definition](#extension-definition)
    - 7.3.1 [Extension Definition Properties](#extension-definition-properties)
    - 7.3.2 [Requirements for STIX Extension Schemas](#requirements-for-stix-extension-schemas)
      - 7.3.2.1 [Requirements for Extension Properties](#requirements-for-extension-properties)
      - 7.3.2.2 [Requirements for Extension STIX Objects](#requirements-for-extension-stix-objects)
- 8. [STIX Bundle Object](#stix-bundle-object)
  - 8.1 [Properties](#stix-bundle-object-properties)
  - 8.2 [Relationships](#stix-bundle-object-relationships)
- 9. [STIX Patterning](#stix-patterning)
  - 9.1 [Definitions](#definitions)
  - 9.2 [Constants](#constants)
  - 9.3 [STIX Patterns](#stix-patterns)
  - 9.4 [Pattern Expressions](#pattern-expressions)
  - 9.5 [Observation Expressions](#observation-expressions)
    - 9.5.1 [Observation Expression Qualifiers](#observation-expression-qualifiers)
    - 9.5.2 [Observation Operators](#observation-operators)
    - 9.5.3 [Operator Precedence](#operator-precedence)
  - 9.6 [Comparison Expressions](#comparison-expressions)
    - 9.6.1 [Comparison Operators](#comparison-operators)
    - 9.6.2 [String Comparison](#string-comparison)
    - 9.6.3 [Binary Type Comparison](#binary-type-comparison)
    - 9.6.4 [Native Format Comparison](#native-format-comparison)
    - 9.6.5 [Set Comparison](#set-comparison)
  - 9.7 [Object Path Syntax](#object-path-syntax)
    - 9.7.1 [Basic Object Properties](#basic-object-properties)
    - 9.7.2 [List Object Properties](#list-object-properties)
    - 9.7.3 [Dictionary Object Properties](#dictionary-object-properties)
    - 9.7.4 [Object Reference Properties](#object-reference-properties)
  - 9.8 [Examples](#examples)
- 10. [STIX Vocabularies](#stix-vocabularies)
  - 10.1 [Account Type Vocabulary](#account-type-vocabulary)
  - 10.2 [Attack Motivation Vocabulary](#attack-motivation-vocabulary)
  - 10.3 [Attack Resource Level Vocabulary](#attack-resource-level-vocabulary)
  - 10.4 [Encryption Algorithm Enumeration](#encryption-algorithm-enumeration)
  - 10.5 [Extension Type Enumeration](#extension-type-enumeration)
  - 10.6 [Grouping Context Vocabulary](#grouping-context-vocabulary)
  - 10.7 [Hashing Algorithm Vocabulary](#hashing-algorithm-vocabulary)
  - 10.8 [Identity Class Vocabulary](#identity-class-vocabulary)
  - 10.9 [Implementation Language Vocabulary](#implementation-language-vocabulary)
  - 10.10 [Indicator Type Vocabulary](#indicator-type-vocabulary)
  - 10.11 [Industry Sector Vocabulary](#industry-sector-vocabulary)
  - 10.12 [Infrastructure Type Vocabulary](#infrastructure-type-vocabulary)
  - 10.13 [Malware Result Vocabulary](#malware-result-vocabulary)
  - 10.14 [Malware Capabilities Vocabulary](#malware-capabilities-vocabulary)
  - 10.15 [Malware Type Vocabulary](#malware-type-vocabulary)
  - 10.16 [Network Socket Address Family Enumeration](#network-socket-address-family-enumeration)
  - 10.17 [Network Socket Type Enumeration](#network-socket-type-enumeration)
  - 10.18 [Opinion Enumeration](#opinion-enumeration)
  - 10.19 [Pattern Type Vocabulary](#pattern-type-vocabulary)
  - 10.20 [Processor Architecture Vocabulary](#processor-architecture-vocabulary)
  - 10.21 [Region Vocabulary](#region-vocabulary)
  - 10.22 [Report Type Vocabulary](#report-type-vocabulary)
  - 10.23 [Threat Actor Type Vocabulary](#threat-actor-type-vocabulary)
  - 10.24 [Threat Actor Role Vocabulary](#threat-actor-role-vocabulary)
  - 10.25 [Threat Actor Sophistication Vocabulary](#threat-actor-sophistication-vocabulary)
  - 10.26 [Tool Type Vocabulary](#tool-type-vocabulary)
  - 10.27 [Windows™ Integrity Level Enumeration](#windows-integrity-level-enumeration)
  - 10.28 [Windows™ PE Binary Vocabulary](#windows-pe-binary-vocabulary)
  - 10.29 [Windows™ Registry Datatype Enumeration](#windows-registry-datatype-enumeration)
  - 10.30 [Windows™ Service Start Type Enumeration](#windows-service-start-type-enumeration)
  - 10.31 [Windows™ Service Type Enumeration](#windows-service-type-enumeration)
  - 10.32 [Windows™ Service Status Enumeration](#windows-service-status-enumeration)
- 11. [Customizing STIX (Deprecated)](#customizing-stix)
  - 11.1 [Custom Properties (Deprecated)](#custom-properties)
    - 11.1.1 [Requirements (Deprecated)](#custom-properties-requirements)
  - 11.2 [Custom Objects (Deprecated)](#custom-objects)
    - 11.2.1 [Requirements (Deprecated)](#custom-objects-requirements)
  - 11.3 [Custom Object Extensions (Deprecated)](#custom-object-extensions)
    - 11.3.1 [Requirements (Deprecated)](#custom-object-extensions-requirements)
- 12. [Conformance](#conformance)
  - 12.1 [STIX Object Producers and Consumers](#stix-object-producers-and-consumers)
  - 12.2 [STIX Object Mandatory Features](#stix-object-mandatory-features)
    - 12.2.1 [Versioning](#conformance-versioning)
  - 12.3 [STIX Object Optional Features](#stix-object-optional-features)
    - 12.3.1 [Object-Level Data Markings](#object-level-data-markings)
    - 12.3.2 [Granular Data Markings](#granular-data-markings)
    - 12.3.3 [STIX Extensions](#conformance-stix-extensions)
  - 12.4 [STIX Patterning Conformance](#stix-patterning-conformance)
  - 12.5 [STIX Pattern Producer](#stix-pattern-producer)
  - 12.6 [STIX Pattern Consumer](#stix-pattern-consumer)
  - 12.7 [STIX Patterning Conformance Levels](#stix-patterning-conformance-levels)
    - 12.7.1 [Level 1: Basic Conformance](#level-1-basic-conformance)
    - 12.7.2 [Level 2: Basic Conformance plus Observation Operators](#level-2-basic-conformance-plus-observation-operators)
    - 12.7.3 [Level 3: Full Conformance](#level-3-full-conformance)
- Appendix A: [Confidence Scales](#confidence-scales)
- Appendix B: [Relationship Summary Table](#relationship-summary-table)
- Appendix C: [Additional Examples](#additional-examples)
  - C.1 [Infrastructure Additional Examples](#infrastructure-additional-examples)
    - C.1.1 [Malware & Target List Hosting Domain](#malware-target-list-hosting-domain)
    - C.1.2 [Malware Botnet Infrastructure](#malware-botnet-infrastructure)
    - C.1.3 [Related/Component Botnet Infrastructure](#relatedcomponent-botnet-infrastructure)
    - C.1.4 [Malware Instance Hosted on Compromised Domain](#malware-instance-hosted-on-compromised-domain)
  - C.2 [Extension Definition Additional Examples](#extension-definition-additional-examples)
    - C.2.1 [Create a new object type with a copyright marking definition](#create-a-new-object-type-with-a-copyright-marking-definition)
    - C.2.2 [Adding properties to an existing STIX object instance](#adding-properties-to-an-existing-stix-object-instance)
    - C.2.3 [Adding properties to an existing STIX relationship object instance](#adding-properties-to-an-existing-stix-relationship-object-instance)
    - C.2.4 [Adding properties to an existing STIX marking definition object instance](#adding-properties-to-an-existing-stix-marking-definition-object-instance)
    - C.2.5 [Adding properties to an existing STIX language content object instance](#adding-properties-to-an-existing-stix-language-content-object-instance)
- Appendix D: [IANA Considerations](#iana-considerations)
- Appendix E: [References](#references)
  - E.1 [Normative References](#normative-references)
  - E.2 [Informative References](#informative-references)
- Appendix F: [Acknowledgments](#acknowledgments)
- Appendix G: [Revision History](#revision-history)
- Appendix H: [Notices](#notices)

---

# 1. Introduction <a id='introduction'></a>

Structured Threat Information Expression (STIX) is a language and serialization format used to exchange cyber threat intelligence (CTI).
STIX enables organizations to share CTI with one another in a consistent and machine-readable manner, allowing security communities to better understand what computer-based attacks they are most likely to see and to anticipate and/or respond to those attacks faster and more effectively.
STIX is designed to improve many different capabilities, such as collaborative threat analysis, automated threat exchange, automated detection and response, and more.

The objects and features added for inclusion in STIX 2.1 represent an iterative approach to fulfilling basic consumer and producer requirements for CTI sharing.
Objects and properties not included in this version of STIX, but deemed necessary by the community, will be included in future releases.

## 1.1 Document Conventions <a id='document-conventions'></a>

The following color, font and font style conventions are used in this
document:

- The <span class="stixfont">Consolas</span> font is used for all type
  names, property names and literals.

  - type names are in red with a light red background –
    <span class="stixtype">threat-actor</span>

  - property names are in bold style – **created_at**

  - literals (values) are in blue with a blue background –
    <span class="stixliteral">malicious-activity</span>

  - All relationship types are string literals; therefore, they will
    also appear in blue with a blue background –
    <span class="stixrelationship">related-to</span>

- In an object’s property table, if a common property is being redefined
  in some way, then the background is dark grey.

- All examples in this document are expressed in JSON. They are in
  `mono` font, with straight quotes, black text and a light grey
  background, and using 2-space indentation. JSON examples in this
  document are representations of JSON objects \[[RFC8259](#RFC8259)\].
  They should not be interpreted as string literals. The ordering of
  object keys is insignificant. Whitespace before or after JSON
  structural characters in the examples are insignificant
  \[[RFC8259](#RFC8259)\].

- Parts of the example may be omitted for conciseness and clarity. These
  omitted parts are denoted with the ellipses (…​).

- The term "hyphen" is used throughout this document to refer to the
  ASCII hyphen or minus character, which in Unicode is "hyphen-minus",
  U+002D.

## 1.2 Overview <a id='overview'></a>

STIX is a schema that defines a taxonomy of cyber threat intelligence
that is represented by the following objects:

<table border="1" cellspacing="0" cellpadding="6">
  <tr>
    <th colspan="6" style="text-align:center; background-color:#004A7F; color:white;">STIX Objects</th>
    <th rowspan="3" style="background-color:#d3d3d3; text-align:center;">STIX Bundle Object</th>
  </tr>
  <tr>
    <th colspan="3" style="text-align:center; background-color:#dbe9f4;">STIX Core Objects</th>
    <th colspan="3" style="text-align:center; background-color:#dbe9f4;">STIX Meta Objects (SMO)</th>
  </tr>
  <tr>
    <td>STIX Domain Objects (SDO)</td>
    <td>STIX Cyber-observable Objects (SCO)</td>
    <td>STIX Relationship Objects (SRO)</td>
    <td>Extension Definition Objects</td>
    <td>Language Content Objects</td>
    <td>Marking Definition Objects</td>
  </tr>
</table>

**STIX Core Objects**

Any SDO, SCO, or SRO.

**STIX Domain Objects**

Higher Level Intelligence Objects that represent behaviors and
constructs that threat analysts would typically create or work with
while understanding the threat landscape.

**STIX Cyber-observable Objects**

Objects that represent observed facts about a network or host that may
be used and related to higher level intelligence to form a more complete
understanding of the threat landscape.

**STIX Relationship Objects**

Objects that connect STIX Domain Objects together, STIX Cyber-observable
Objects together, and connect STIX Domain Objects and STIX
Cyber-observable Objects together to form a more complete understanding
of the threat landscape.

**STIX Meta Objects (SMO)**

A STIX Object that provides the necessary glue and associated metadata
to enrich or extend STIX Core Objects to support user and system
workflows.

**STIX Bundle Object**

An object that provides a wrapper mechanism for packaging arbitrary STIX
content together.

### 1.2.1 Graph-Based Model <a id='graph-based-model'></a>

STIX is a connected graph of nodes and edges.
STIX Domain Objects and STIX Cyber-observable Objects define the graph nodes and STIX relationships (including both external STIX Relationship Objects and embedded relationships) define the edges.
This graph-based language conforms to common analysis approaches and allows for flexible, modular, structured, and consistent representations of CTI.

### 1.2.2 STIX Domain Objects <a id='overview-stix-domain-objects'></a>

STIX defines a set of STIX Domain Objects (SDOs): Attack Pattern, Campaign, Course of Action, Grouping, Identity, Indicator, Infrastructure, Intrusion Set, Location, Malware, Malware Analysis, Note, Observed Data, Opinion, Report, Threat Actor, Tool, and Vulnerability.
Each of these objects corresponds to a concept commonly used in CTI.

STIX Domain Objects are defined in [section 4](#stix-domain-objects).

### 1.2.3 STIX Cyber-observable Objects <a id='overview-stix-cyber-observable-objects'></a>

STIX defines a set of STIX Cyber-observable Objects (SCOs) for characterizing host-based and network-based information.
SCOs are used by various STIX Domain Objects (SDOs) to provide supporting context.
The Observed Data SDO, for example, indicates that the raw data was observed at a particular time.

STIX Cyber-observable Objects (SCOs) document the facts concerning what happened on a network or host, and do not capture the who, when, or why.
By associating SCOs with STIX Domain Objects (SDOs), it is possible to convey a higher-level understanding of the threat landscape, and to potentially provide insight as to the who and the why particular intelligence may be relevant to an organization.
For example, information about a file that existed, a process that was observed running, or that network traffic occurred between two IPs can all be captured as SCOs.

STIX Cyber-observable Objects (SCOs) are defined in [section 6](#stix-cyber-observable-objects).

Previously, in STIX 2.0, Cyber-observable Objects could only exist as objects within an Observed Data object. It is still possible to represent Cyber-observable Objects in this way, but this method has been deprecated. See [section 2.13](#observable-container).

### 1.2.4 STIX Relationships <a id='stix-relationships'></a>

A relationship is a link between STIX Domain Objects (SDOs), STIX Cyber-observable Objects (SCOs), or between an SDO and a SCO that describes the way in which the objects are related.
Relationships can be represented using an external STIX Relationship Object (SRO) or, in some cases, through certain properties which store an identifier reference that comprises an embedded relationship, (for example the **created_by_ref** property).

The generic STIX Relationship Object (SRO) is one of two SROs and is used for most relationships in STIX.
This generic SRO contains a property called **relationship_type** to describe more specifically what the relationship represents.
This specification defines a set of known terms to use for the **relationship_type** property between SDOs of specific types.
For example, the Indicator SDO defines a relationship from itself to Malware via a **relationship_type** of <span class="stixliteral">indicates</span> to describe how the Indicator can be used to detect the presence of the corresponding Malware. In addition to the terms defined in the specification, STIX also allows for user-defined terms to be used as the relationship type.

Currently the only other SRO (besides a generic Relationship) is the Sighting SRO.
The Sighting object is used to capture cases where an entity has "seen" an SDO, such as sighting an indicator.
Sighting is a separate SRO because it contains additional properties such as **count** that are only applicable to Sighting relationships.
Other SROs may be defined in future versions of STIX if new relationships are identified that also require additional properties not present on the generic Relationship object.

In addition to relationships created using the SROs (Relationship and Sighting), STIX also uses ID references to represent embedded relationships.
Embedded relationships are simply ID reference properties on STIX Objects that contain the ID of a different STIX Object.
Embedded relationships are used when the property is an inherent part of the object and not something that a third party might add or something that might require the inclusion of a confidence score.
Because they represent an inherent linkage and have no other properties, an SRO is not needed to represent them.
An embedded relationship can only be asserted by the creator of the object ("object creator") it is contained in.

For example, the entity that created a STIX Object is an inherent, factual part of that object and therefore that information is captured in an embedded relationship contained in the **created_by_ref** property rather than through the use of an SRO.

Embedded relationships (ID references) are described in [section 3.3](#object-ids-and-references) and STIX Relationship Objects (SROs) are defined in [section 5](#stix-relationship-objects).

### 1.2.5 STIX Cyber Observable Observed Data Relationships (Deprecated) <a id='stix-cyber-observable-observed-data-relationships'></a>

While refining STIX for the 2.1 specification, the CTI TC reached consensus that the STIX 2.0 Cyber Observable Container (see [section 2.13](#observable-container)) and the Observed Data object's graph within a graph model was insufficient to support critical CTI use cases.
Consequently, in STIX 2.1, the Cyber Observable Container is deprecated, and implementers are encouraged to use STIX Relationship Objects (SROs) instead.
Within the context of the (deprecated) Cyber Observable Container's graph within a graph model, an object relationship is a reference linking two (or more) related SCOs and these relationships are constrained to SCOs contained within the same Cyber Observable Container.

A Cyber Observable Container relationship should not be confused with STIX Relationship Objects (SROs) that are defined in [section 5](#stix-relationship-objects).

### 1.2.6 STIX Patterning <a id='overview-stix-patterning'></a>

The STIX Patterning language enables the detection of activity on networks and endpoints.
This language allows matching against time stamped cyber observable data collected by a threat intelligence platform or other similar system.
STIX Patterning is currently only used by the STIX Indicator object, but it can be employed in other use cases.

Before undertaking work on STIX Patterning, a thorough effort to evaluate existing patterning languages (e.g., Snort or Yara) was performed.
This effort identified that no existing patterning language solves or supports the STIX use cases. Extending other languages was ruled out as unfeasible, both from a technical perspective as well as taking into consideration that from a licensing/IPR perspective, extending an existing language under the auspices of OASIS would have been problematic.

STIX Patterning was primarily designed to support STIX Indicators.
As such it is a mechanism for communicating how to find malicious code and/or threat actors active within a given network or endpoint.

This language release is focused on supporting a common set of use cases and therefore allows for the expression of an initial set of patterns that producers and consumers of STIX can utilize.
As more complex patterns are deemed necessary, the STIX patterning language will be extended in future releases to improve its effectiveness as an automated detection/remediation method.

STIX Patterning is defined in [section 9](#stix-patterning).

### 1.2.7 STIX Common Properties <a id='stix-common-properties'></a>

STIX Domain Objects (SDOs) and Relationship Objects (SROs) all share a common set of properties which provide core capabilities such as versioning and data markings (representing how data can be shared and used).
All STIX Cyber-observable Objects (SCOs) likewise share a common set of properties that are applicable for all SCOs. Similarly, STIX Meta Objects (SMOs) use some but not all of the common properties.

### 1.2.8 STIX Open Vocabularies and Enumerations <a id='stix-open-vocabularies-and-enumerations'></a>

Some STIX properties are defined using open vocabularies or enumerations.
Enumerations and open vocabularies are defined in STIX in order to enhance interoperability by increasing the likelihood that different entities use the same exact string to represent the same concept.
If used consistently, open vocabularies make it less likely that one entity refers to the energy sector as "Energy" and another as "Energy Sector", thereby making comparison and correlation easier.

While using predefined values from STIX vocabularies is strongly encouraged, in some cases this may not be feasible.
To address this, producers are permitted to use values outside of the open vocabulary.
In the case of enumerations, producers are required to use only the values defined within the STIX specification.

STIX open vocabularies and enumerations are defined in [section 10](#stix-vocabularies). Properties that are defined as open vocabularies identify a suggested vocabulary from that section.
For example, the Threat Actor **sophistication** property, as defined in [section 4.17](#threat-actor), uses the Threat Actor Sophistication vocabulary as defined in [section 10.25](#threat-actor-sophistication-vocabulary).

### 1.2.9 Reserved Names <a id='overview-reserved-names'></a>

Reserved property names are marked with a type called <span class="stixtype">RESERVED</span> and a description text of "RESERVED FOR FUTURE USE". For more information please see [section 3.8](#reserved-names)

### 1.2.10 Serialization <a id='serialization'></a>

STIX is defined independent of any specific storage or serialization.
However, the mandatory-to-implement (MTI) serialization for STIX 2.1 is UTF-8 encoded JSON as defined in [RFC7493](#RFC7493) and [RFC8259](#RFC8259), which uses the JSON Object type described within when representing all STIX Objects.
In other words, all STIX-conformant tools have to implement support for JSON but can implement support for other serializations.

### 1.2.11 Transporting STIX <a id='transporting-stix'></a>

STIX 2.1 is transport-agnostic, i.e., the structures and serializations do not rely on any specific transport mechanism.
A companion CTI specification, [TAXII](#related-work), is designed specifically to transport STIX Objects.
STIX provides a Bundle (see [section 8](#stix-bundle-object)) as a container for STIX Objects to allow for transportation of bulk STIX data, especially over non-TAXII communication mechanisms.

### 1.2.12 JSON Schemas <a id='json-schemas'></a>

JSON schemas have been developed by members of the Cyber Threat Intelligence Technical Committee.
The JSON schemas are informative and serve as a best effort attempt to validate that STIX 2.1 content meets the structural requirements identified in this specification.
This specification is the normative description of STIX 2.1.

## 1.3 Changes From Earlier Version <a id='changes-from-earlier-version'></a>

This section lists all of the changes from the previous 2.1 version of STIX.

### 1.3.1 STIX 2.1 Errata 01 Changes From Earlier Version <a id='stix-21-errata-01-changes-from-earlier-version'></a>

STIX 2.1 Errata 01 differs from STIX 2.1 in the following ways:

- Updated Malware Embedded Relationships table with missing property in [section 4.11.2](#malware-relationships).
  - **operating_system_refs** is no longer missing in the table.
- Malware Analysis Relationships table fixed with the right relationship type between Malware Analysis and Malware in [section 4.12.2](#malware-analysis-relationships).
  - wrong <span class="stixliteral">analysis-of</span> is replaced with the right <span class="stixliteral">av-analysis-of</span> relationship type.
- Email Message property descriptions fixed in [section 6.6.1](#email-message-object-properties).
  - **from_ref**, **sender_ref**, **to_refs**, **cc_refs** and **bcc_refs** properties descriptions now mention the right <span class="stixtype">email-addr</span> type they are referencing.
- HTTP Request Extension examples fixed in [section 6.12.2.1](#http-request-extension-properties).
  - the **request_header** property is now a <span class="stixtype">list</span> of type <span class="stixtype">string</span> in the examples, as expected from the description.
- Observation Expression Qualifiers example fixed in [section 9.5.1](#observation-expression-qualifiers).
  - the example used to illustrate the use of *Observation Expression* <span class="stixliteral">WITHIN</span> *x* <span class="stixliteral">SECONDS</span> now has the right <span class="stixtype">windows-registry-key</span> Observable type.
- Updated Implementation Language Vocabulary in [section 10.9](#implementation-language-vocabulary).
  - <span class="stixliteral">rust</span> value was added.
- Updated Industry Sector Vocabulary in [section 10.11](#industry-sector-vocabulary).
  - <span class="stixliteral">egal</span> value was added.
- Fixed Infrastructure Type Vocabulary Summary in [section 10.12](#infrastructure-type-vocabulary).
  - missing <span class="stixliteral">control-system</span>, <span class="stixliteral">firewall</span>, <span class="stixliteral">routers-switches</span> and <span class="stixliteral">workstation</span> values were added to the Summary as they were already described in the Vocabulary table.
- Enhanced Malware Result Vocabulary in [section 10.13](#malware-result-vocabulary).
  - descriptions for every vocabulary values were improved with more descriptive definitions.
- Fixed Report Type Vocabulary in [section 10.22](#report-type-vocabulary).
  - missing <span class="stixliteral">incident</span> value was added.
- Updated Threat Actor Type Vocabulary in [section 10.23](#threat-actor-type-vocabulary).
  - <span class="stixliteral">private-sector</span> value was added.
- Fixed multiple Enumeration headers
  - Enumerations now have the right headers, to differenciate enumerations from vocabularies, including:
    - **Enumeration Name** is now used instead of **Vocabulary Name**
    - **Enumeration Summary** is now used instead of **Vocabulary Summary**
    - **Enumeration Value** is now used instead of **Vocabulary Value**
  - These changes apply on:
    - Encryption Algorithm Enumeration in [section 10.4](#encryption-algorithm-enumeration)
    - Extension Type Enumeration in [section 10.5](#extension-type-enumeration)
    - Network Socket Address Family Enumeration in [section 10.16](#network-socket-address-family-enumeration)
    - Network Socket Type Enumeration in [section 10.17](#network-socket-type-enumeration)
    - Opinion Enumeration [section 10.18](#opinion-enumeration)
    - Windows™ Integrity Level Enumeration in [section 10.27](#windows-integrity-level-enumeration)
    - Windows™ Registry Datatype Enumeration in [section 10.29](#windows-registry-datatype-enumeration)
    - Windows™ Service Start Type Enumeration in [section 10.30](#windows-service-start-type-enumeration)
    - Windows™ Service Type Enumeration in [section 10.31](#windows-service-type-enumeration)
    - Windows™ Service Status Enumeration in [section 10.32](#windows-service-status-enumeration)
- Relationship Summary Table has been update in [Appendix B](#relationship-summary-table).
  - Duplicated relationship <span class="stixliteral">located-at</span> between <span class="stixtype">threat-actor</span> and <span class="stixtype">location</span> has been removed.
  - Misspelled relationship <span class="stixliteral">exfiltrates-to</span> between <span class="stixtype">malware</span> and <span class="stixtype">infrastructure</span> has been fixed.
  - Missing relationships have been added, including:
    - <span class="stixliteral">remediates</span> between <span class="stixtype">course-of-action</span> and <span class="stixtype">malware</span>
    - <span class="stixliteral">remediates</span> between <span class="stixtype">course-of-action</span> and <span class="stixtype">vulnerability</span>
    - <span class="stixliteral">uses</span> between <span class="stixtype">tool</span> and <span class="stixtype">infrastructure</span>
    - <span class="stixliteral">resolves-to</span> between <span class="stixtype">domain-name</span> and <span class="stixtype">domain-name</span>
    - <span class="stixliteral">resolves-to</span> between <span class="stixtype">domain-name</span> and <span class="stixtype">ipv4-addr</span>
    - <span class="stixliteral">resolves-to</span> between <span class="stixtype">domain-name</span> and <span class="stixtype">ipv6-addr</span>
    - <span class="stixliteral">resolves-to</span> between <span class="stixtype">ipv4-addr</span> and <span class="stixtype">mac-addr</span>
    - <span class="stixliteral">belongs-to</span> between <span class="stixtype">ipv6-addr</span> and <span class="stixtype">autonomous-system</span>
    - <span class="stixliteral">resolves-to</span> between <span class="stixtype">ipv4-addr</span> and <span class="stixtype">mac-addr</span>
    - <span class="stixliteral">belongs-to</span> between <span class="stixtype">ipv6-addr</span> and <span class="stixtype">autonomous-system</span>
- Fixed typos in Extension Definition Additional Examples
  - typos were fixed in titles for [section C.2.2](#adding-properties-to-an-existing-stix-object-instance) and [section C.2.3](#adding-properties-to-an-existing-stix-relationship-object-instance).
- Special characters were fixed in some participants names in [Appendix F](#acknowledgments).
- All SCO ids were updated in examples to agree with the `generate_id` method in *python-stix2* library.
- Included all changes based on ITU recommandations.
- Improved references through the document.
  - missing references to sections were added at different places.
  - some references were fixed to point to the right section.
  - in the description of STIX object properties whose value is either a vocabulary or an enumeration, a reference poiting to the given vocabulary or enumeration was added.

## 1.4 Glossary <a id='glossary'></a>

**AV** - Anti-Virus / Anti-Malware solution

**CAPEC** - Common Attack Pattern Enumeration and Classification

**Consumer** - Any entity that receives STIX content

**CTI** - Cyber Threat Intelligence

**Deprecated** - STIX features or properties that are in the process of
being replaced by newer ones.

**Embedded Relationship** - A link (an "edge" in a graph) between one
STIX Object and another represented as a property on one object
containing the ID of another object

**Entity** - Anything that has a separately identifiable existence
(e.g., organization, person, group, etc.)

**IEP** - FIRST (Forum of Incident Response and Security Teams)
Information Exchange Policy

**Instance** - A single occurrence of a STIX Object version#

**MTI** - Mandatory To Implement

**Object Creator** - The entity that created or updated a STIX Object
(see [section 3.5](#object-creator))

**Object Representation** - An instance of an object version that is
serialized as STIX

**Producer** - Any entity that distributes STIX content, including
object creators as well as those passing along existing content

**SCO** - STIX Cyber-observable Object

**SDO -** STIX Domain Object (a "node" in a graph)

**SMO** - STIX Meta Object

**SRO** - STIX Relationship Object (one mechanism to represent an "edge"
in a graph)

**STIX** - Structured Threat Information Expression

**STIX Content** - STIX documents, including STIX Objects, STIX Objects
grouped as bundles, etc.

**STIX Object** - A STIX Domain Object (SDO), STIX Cyber Observable
Object (SCO), STIX Relationship Object (SRO), or STIX Meta Object (SMO).

**STIX Relationship** - A link (an "edge" in a graph) between two STIX
Objects represented by either an SRO or an embedded relationship

**STIX Extension** - A set of mechanisms supporting adding new objects
and updating existing objects in a standard way.

**TAXII** - An application layer protocol for the communication of cyber
threat information

**TLP** - Traffic Light Protocol

**TTP** - Tactic, technique, or procedure; behaviors and resources that
attackers use to carry out their attacks

# 2. Common Data Types <a id='common-data-types'></a>

This section defines the common types used throughout STIX for all STIX Objects.
These types will be referenced by the "Type" column in other sections.
This section defines the names and permitted values of common types that are used in the STIX information model; it does not, however, define the meaning of any properties using these types.
These types may be further restricted elsewhere in the document.

The table below is a summary of the data types defined in this section.

| **<span class="stixtr">Type</span>** | **<span class="stixtr">Description</span>** |
|----|----|
| <span class="stixtype">binary</span> | A sequence of bytes. |
| <span class="stixtype">boolean</span> | A value of **<span class="stixliteral">true</span>** or **<span class="stixliteral">false</span>**. |
| <span class="stixtype">dictionary</span> | A set of key/value pairs. |
| <span class="stixtype">enum</span> | A value from a STIX Enumeration. |
| <span class="stixtype">external-reference</span> | A non-STIX identifier or reference to other related external content. |
| <span class="stixtype">float</span> | An IEEE 754 \[[IEEE 754-2008](#IEEE7542008)\] double-precision number. |
| <span class="stixtype">hashes</span> | One or more cryptographic hashes. |
| <span class="stixtype">hex</span> | An array of octets as hexadecimal. |
| <span class="stixtype">identifier</span> | An identifier (ID) is for STIX Objects. |
| <span class="stixtype">integer</span> | A whole number. |
| <span class="stixtype">kill-chain-phase</span> | A name and a phase of a kill chain. |
| <span class="stixtype">list</span> | A sequence of values ordered based on how they appear in the list. The phrasing "<span class="stixtype">list</span> of type <span class="stixtype">\<type\></span>" is used to indicate that all values within the list **MUST** conform to the specified type. |
| <span class="stixtype">observable-container</span> | One or more STIX Cyber-observable Objects in the deprecated Cyber Observable Container. |
| <span class="stixtype">open-vocab</span> | A value from a STIX open (<span class="stixtype">open-vocab</span>) or suggested vocabulary. |
| <span class="stixtype">string</span> | A series of Unicode characters. |
| <span class="stixtype">timestamp</span> | A time value (date and time). |

## 2.1 Binary <a id='binary'></a>

**Type Name:** <span class="stixtype">binary</span>

The <span class="stixtype">binary</span> data type represents a sequence of bytes. In order to allow pattern matching on custom objects, for all properties that use the binary type, the property name **MUST** end with `_bin`.

The JSON MTI serialization represents this as a base64-­encoded string as specified in \[[RFC4648](#RFC4648)\]​. Other serializations **SHOULD** use a native binary type, if available.

## 2.2 Boolean <a id='boolean'></a>

**Type Name:** <span class="stixtype">boolean</span>

A <span class="stixtype">boolean</span> is a value of either true or false. Properties with this type **MUST** have a value of <span class="stixliteral">true</span> or <span class="stixliteral">false</span>.

The JSON MTI serialization uses the true and false (boolean) values from the JSON values \[[RFC8259](#RFC8259)\], which are a literal (unquoted) <span class="stixliteral">true</span> or <span class="stixliteral">false</span>.

**Example**

```JSON
{
  ...
  "summary": true,
  ...
}
```

## 2.3 Dictionary <a id='dictionary'></a>

**Type Name:** <span class="stixtype">dictionary</span>

A <span class="stixtype">dictionary</span> captures an arbitrary set of key/value pairs. Dictionary keys **MUST** be unique in each dictionary, **MUST** be in ASCII, and are limited to the characters a-z (lowercase ASCII), A-Z (uppercase ASCII), numerals 0-9, hyphen (-), and underscore (\_). Dictionary keys **MUST** be no longer than 250 ASCII characters in length and **SHOULD** be lowercase.

Empty dictionaries are prohibited in STIX and **MUST NOT** be used as a substitute for omitting the property if it is optional. If the property is required, the dictionary **MUST** be present and **MUST** have at least one key-value pair.

<span class="stixtype">dictionary</span> values **MUST** be valid property base types 

## 2.4 Enum <a id='enum'></a>

**Type Name:** <span class="stixtype">enum</span>

The <span class="stixtype">enum</span> type is a hardcoded list of terms that is represented as a <span class="stixtype">string</span>. For properties that use this type there is a defined list of values that is identified in the definition for said properties. The STIX Enumerations are defined in [section 10](#stix-vocabularies). Terms defined in an <span class="stixtype">enum</span> by the specification **MUST NOT** be expanded by implementations.

The JSON MTI serialization uses the JSON String type \[[RFC8259](#RFC8259)\] when representing <span class="stixtype">enum</span> enumeration.

## 2.5 External Reference <a id='external-reference'></a>

**Type Name:** <span class="stixtype">external-reference</span>

External references are used to describe pointers to information represented outside of STIX. For example, a Malware object could use an external reference to indicate an ID for that malware in an external database or a report could use references to represent source material.

The JSON MTI serialization uses the JSON Object type \[[RFC8259](#RFC8259)\] when representing <span class="stixtype">external-reference</span>.

### 2.5.1 Properties <a id='external-reference-properties'></a>

| **<span class="stixtr">Property Name</span>** | **<span class="stixtr">Type</span>** | **<span class="stixtr">Description</span>** |
|----|----|----|
| **source_name** (required) | <span class="stixtype">string</span> | The name of the source that the <span class="stixtype">external-reference</span> is defined within (system, registry, organization, etc.). |
| **description** (optional) | <span class="stixtype">string</span> | A human readable description. |
| **url** (optional) | <span class="stixtype">string</span> | A URL reference to an external resource \[[RFC3986](#RFC3986)\] |
| **hashes** (optional) | <span class="stixtype">hashes</span> | Specifies a dictionary of hashes for the contents of the **url**. This **SHOULD** be provided when the **url** property is present.<br><br>Dictionary keys **MUST** come from one of the entries listed in the [<span class="stixtype">hash-algorithm-ov</span>](#hashing-algorithm-vocabulary) open vocabulary.<br><br>As stated in [section 2.7](#hashes), to ensure interoperability, a SHA-256 hash **SHOULD** be included when possible. |
| **external_id** (optional) | <span class="stixtype">string</span> | An identifier for the external reference content. |

### 2.5.2 Requirements <a id='external-reference-requirements'></a>

- In addition to the **source_name** property, at least one of the **description**, **url** or **external_id** properties **MUST** be present.

**Examples**

An <span class="stixtype">external-reference</span> to a VERIS Community Database (VCDB) \[[VERIS](#VERIS)\] entry

```JSON
{
  ...
  "external_references": [
    {
      "source_name": "veris",
      "external_id": "0001AA7F-C601-424A-B2B8-BE6C9F5164E7",
      "url": "https://github.com/vz-risk/VCDB/blob/125307638178efddd3ecfe2c267ea434667a4eea/data/json/validated/0001AA7F-C601-424A-B2B8-BE6C9F5164E7.json",
      "hashes": {
        "SHA-256": "6db12788c37247f2316052e142f42f4b259d6561751e5f401a1ae2a6df9c674b"
      }
    }
  ],
  ...
}
```

An <span class="stixtype">external-reference</span> from the CAPEC™ \[[CAPEC](#CAPEC)\] repository

```JSON
{
  ...
  "external_references": [
    {
      "source_name": "capec",
      "external_id": "CAPEC-550"
    }
  ],
  ...
}
```

An <span class="stixtype">external-reference</span> from the CAPEC repository with URL

```JSON
{
  ...
  "external_references": [
    {
      "source_name": "capec",
      "external_id": "CAPEC-550",
      "url": "http://capec.mitre.org/data/definitions/550.html"
    }
  ],
  ...
}
```

An <span class="stixtype">external-reference</span> to ACME Threat Intel’s report document

```JSON
{
  ...
  "external_references": [
    {
      "source_name": "ACME Threat Intel",
      "description": "Threat report",
      "url": "http://intelreport.mandiant.com/Mandiant_APT1_Report.pdf"
    }
  ],
  ...
}
```

An <span class="stixtype">external-reference</span> to a Bugzilla item

```JSON
{
  ...
  "external_references": [
    {
      "source_name": "ACME Bugzilla",
      "external_id": "1370",
      "url": "https://issues.oasis-open.org/browse/TAB-1370"
    }
  ],
  ...
}
```

An <span class="stixtype">external-reference</span> to an offline threat report (i.e., e-mailed, offline, etc.)

```JSON
{
  ...
  "external_references": [
    {
      "source_name": "ACME Threat Intel",
      "description": "Threat report"
    }
  ],
  ...
}
```

## 2.6 Float <a id='float'></a>

**Type Name:** <span class="stixtype">float</span>

The float data type represents an IEEE 754 \[[IEEE 754-2008](#IEEE7542008)\] double-precision number (e.g., a number with a fractional part). However, because the values ±Infinity and NaN are not representable in JSON, they are not valid values in STIX.

In the JSON MTI serialization, floating point values are represented by the JSON Number type \[[RFC7493](#RFC7493)\].

**Example**

```JSON
{
  ...
  "distance": 8.321,
  ...
}
```

## 2.7 Hashes <a id='hashes'></a>

**Type Name:** <span class="stixtype">hashes</span>

The Hashes type represents one or more cryptographic hashes, as a special set of key/value pairs. Accordingly, the name of each hashing
algorithm **MUST** be specified as a key in the dictionary and **MUST** identify the name of the hashing algorithm used to generate the corresponding value. This name **SHOULD** come from one of the values defined in the <span class="stixvocab">[hash-algorithm-ov](#hashing-algorithm-vocabulary)</span> open vocabulary.

Dictionary keys **MUST** be unique in each <span class="stixtype">hashes</span> property, **MUST** be in ASCII, and are limited to the characters a-z (lowercase ASCII), A-Z (uppercase ASCII), numerals 0-9, hyphen (-), and underscore (\_). Dictionary keys **MUST** have a minimum length of 3 ASCII characters and **MUST** be no longer than 250 ASCII characters in length. The value **MUST** be a <span class="stixtype">string</span> in the appropriate format defined by the hash type indicated in the dictionary key.

To enhance compatibility, the SHA-256 hash **SHOULD** be used whenever possible.

**Example**

*SHA-256 and User-Defined Hash*

```JSON
{
  "SHA-256": "6db12788c37247f2316052e142f42f4b259d6561751e5f401a1ae2a6df9c674b",
  "x_foo_hash": "aaaabbbbccccddddeeeeffff0123457890"
}
```

## 2.8 Hexadecimal <a id='hexadecimal'></a>

**Type Name:** <span class="stixtype">hex</span>

The <span class="stixtype">hex</span> data type encodes an array of octets (8-bit bytes) as hexadecimal. The string **MUST** consist of an even number of hexadecimal characters, which are the digits '0' through '9' and the lower-case letters 'a' through 'f'. In order to allow pattern matching on custom objects, for all properties that use the **<span class="stixtype">hex</span>** type, the property name **MUST** end with '\_hex'.

**Example**

```JSON
{
  ...
    "src_flags_hex": "00000002"
  ...
}
```

## 2.9 Identifier <a id='identifier'></a>

**Type Name:** <span class="stixtype">identifier</span>

An <span class="stixtype">identifier</span> uniquely identifies a STIX Object and **MAY** do so in a deterministic way. A deterministic <span class="stixtype">identifier</span> means that the <span class="stixtype">identifier</span> generated by more than one producer for the exact same STIX Object using the same namespace, "ID Contributing Properties", and UUID method will have the exact same <span class="stixtype">identifier</span> value.

All <span class="stixtype">identifiers</span>, excluding those used in the deprecated Cyber Observable Container, **MUST** follow the form <span class="stixalt">*object-type*--*UUID*</span>, where *<span class="stixalt">object-type</span>* is the exact value (all type names are lowercase strings, by definition) from the <span class="stixtype">type</span> property of the object being identified or referenced and where the *<span class="stixalt">UUID</span>* **MUST** be an RFC 4122-compliant UUID \[[RFC4122](#RFC4122)\].

The *<span class="stixalt">UUID</span>* part of the <span class="stixtype">identifier</span> **MUST** be unique across all objects produced by a given producer regardless of the type identified by the *<span class="stixalt">object-type</span>* prefix. Meaning, a producer **MUST NOT** reuse the *<span class="stixalt">UUID</span>* portion of the <span class="stixtype">identifier</span> for objects of different types.

STIX Domain Objects, STIX Relationship Objects, STIX Meta Objects, and STIX Bundle Object **SHOULD** use UUIDv4 for the *<span class="stixalt">UUID</span>* portion of the <span class="stixtype">identifier</span>. Producers using something other than UUIDv4 need to be mindful of potential collisions and should use a namespace that guarantees uniqueness, however, they **MUST NOT** use a namespace of <span class="stixliteral">00abedb4-aa42-466c-9c01-fed23315a9b7</span> if generating a UUIDv5.

STIX Cyber-observable Objects **SHOULD** use UUIDv5 for the *<span class="stixalt">UUID</span>* portion of the <span class="stixtype">identifier</span> and the *<span class="stixalt">UUID</span>* portion of the UUIDv5-based <span class="stixtype">identifier</span> **SHOULD** be generated according to the following rules:
- The namespace **SHOULD** be <span class="stixliteral">00abedb4-aa42-466c-9c01-fed23315a9b7</span>. This defined namespace is necessary to support the goal of deduplication and semantic equivalence of some STIX objects in the community of producers.
- The value of the name portion **SHOULD** be the list of "ID Contributing Properties" (property-name and property value pairs) as defined on each SCO object and **SHOULD** be represented as a JSON object that is then serialized / stringified according to \[[RFC8785](#RFC8785)\] to ensure a canonical representation of the JSON data.
- If the contributing properties are all optional, and none are present on the SCO, then a UUIDv4 **MUST** be used.
- Producers not following these rules **MUST NOT** use a namespace of <span class="stixliteral">00abedb4-aa42-466c-9c01-fed23315a9b7</span> and **SHOULD** use UUIDv4 in cases where the id would not be unique.

STIX Cyber-observable Objects that are used in the deprecated Cyber Observable Container **MAY** use any <span class="stixtype">string</span> value for the <span class="stixtype">identifier</span>. For the deprecated Cyber Observable Container, it is common for implementers to use simple numerical strings for these <span class="stixtype">identifiers</span> (e.g., "0", "1", "2", etc.). See [section 2.13](#observable-container) for more information.

- These identifiers, when used inside the deprecated Cyber-observable Objects Container specify a local reference to a Cyber-observable Object. These references **MUST** be valid within the local scope of the Cyber Observable Container (<span class="stixtype">observable-container</span>) that holds both the source Cyber-observable Object and the Cyber-observable Object that it references.
- These identifiers **SHOULD** be a non-negative monotonically increasing integer, incrementing by 1 from a starting value of 0, and represented as a string within the JSON MTI serialization. However, implementers **MAY** elect to use an alternate key format if necessary.

Using Identifiers:  
Consumers of STIX Cyber Threat Intelligence that are processing the **objects** property of an <span class="stixtype">Observed-Data</span> object can assume that the <span class="stixtype">identifier</span> is an old deprecated Cyber Observable Container <span class="stixtype">identifier</span>. Consumers can also inspect the <span class="stixtype">identifier</span> to see if it contains an *<span class="stixalt">object-type</span>*, if not, they can assume that it is a deprecated Cyber Observable Container <span class="stixtype">identifier</span>. If it does have an *<span class="stixalt">object-type</span>* and it matches a SCO, then chances are it is a UUIDv5 deterministic <span class="stixtype">identifier</span>, but this can be verified by inspecting the *<span class="stixalt">UUID</span>* portion of the identifier. \[[RFC4122](#RFC4122)\] defines how one can distinguish between a UUIDv4 and UUIDv5 value.

> NOTE: Please see the security considerations section in [Appendix D](#iana-considerations) for information about using UUIDv5.

The JSON MTI serialization uses the JSON String type \[[RFC8259](#RFC8259)\] when representing <span class="stixtype">identifier</span>.

**​Examples**

```JSON
{
  ...
  "type": "indicator",
  "id": "indicator--e2e1a340-4415-4ba8-9671-f7343fbf0836",
  ...
}

{
  "type": "ipv4-addr",
  "id": "ipv4-addr--28bb3599-77cd-5a82-a950-b5bc3caf07c4",
  "value": "198.51.100.3"
}
```

Deprecated Cyber Observable Container Identifiers

```JSON
{
  "0": {
    "type": "ipv4-addr",
    "value": "198.51.100.2"
  },

  "1": {
    "type": "network-traffic",
    "dst_ref": "0"
  }
}
```

## 2.10 Integer <a id='integer'></a>

**Type Name:** <span class="stixtype">integer</span>

The integer data type represents a whole number. Unless otherwise specified, all integers **MUST** be capable of being represented as a signed 54-bit value (\[-(2\*\*53)+1, (2\*\*53)-1\]) as defined in \[[RFC7493](#RFC7493)\]. Additional restrictions **MAY** be placed on the type as described where it is used. The integer size is limited to a 54-bit value not a 64-bit value as per the RFC.

In the JSON MTI serialization, integers are represented by the JSON Number type \[[RFC7493](#RFC7493)\].

**Example**

```JSON
{
  ...
  "count": 8,
  ...
}
```

## 2.11 Kill Chain Phase <a id='kill-chain-phase'></a>

**Type Name:** <span class="stixtype">kill-chain-phase</span>

The <span class="stixtype">kill-chain-phase</span> represents a phase in a kill chain, which describes the various phases an attacker may undertake in order to achieve their objectives.

The JSON MTI serialization uses the JSON Object type \[[RFC8259](#RFC8259)\] when representing <span class="stixtype">kill-chain-phase</span>.

| **<span class="stixtr">Property Name</span>** | **<span class="stixtr">Type</span>** | **<span class="stixtr">Description</span>** |
|----|----|----|
| **kill_chain_name** (required) | <span class="stixtype">string</span> | The name of the kill chain. The value of this property **SHOULD** be all lowercase and **SHOULD** use hyphens instead of spaces or underscores as word separators. |
| **phase_name** (required)# | <span class="stixtype">string</span> | The name of the phase in the kill chain. The value of this property **SHOULD** be all lowercase and **SHOULD** use hyphens instead of spaces or underscores as word separators. |

When referencing a kill chain, the **kill_chain_name** property **MUST** be the name of that kill chain.

**Examples**

Example specifying the "reconnaissance" phase from the Lockheed Martin Cyber Kill Chain

```JSON
{
  ...
  "kill_chain_phases": [
    {
      "kill_chain_name": "lockheed-martin-cyber-kill-chain",
      "phase_name": "reconnaissance"
    }
  ],
  ...
}
```

Example specifying the "pre-attack" phase from the "foo" kill-chain

```JSON
{
  ...
  "kill_chain_phases": [
    {
      "kill_chain_name": "foo",
      "phase_name": "pre-attack"
    }
  ],
  ...
}
```

## 2.12 List <a id='list'></a>

**Type Name:** <span class="stixtype">list</span>

The <span class="stixtype">list</span> type defines a sequence of values ordered based on how they appear in the list. The phrasing "<span class="stixtype">list</span> of type <span class="stixtype">\<type\></span>" is used to indicate that all values within the list **MUST** conform to the specified type. For instance, <span class="stixtype">list</span> of type <span class="stixtype">integer</span> means that all values of the list must be of the <span class="stixtype">integer</span> type. This specification does not specify the maximum number of allowed values in a <span class="stixtype">list</span>; however, every instance of a <span class="stixtype">list</span> **MUST** have at least one value. Specific STIX Object properties may define more restrictive upper and/or lower bounds for the length of the list.

Empty lists are prohibited in STIX and **MUST NOT** be used as a substitute for omitting the property if it is optional. If the property is required, the list **MUST** be present and **MUST** have at least one value.

The JSON MTI serialization uses the JSON Array type \[[RFC8259](#RFC8259)\], which is an ordered list of zero or more values.

**Example**

```JSON
{
  ...
  "observed_data_refs": [
    "observed-data--b67d30ff-02ac-498a-92f9-32f845f448cf",
    "observed-data--c96f4120-2b4b-47c3-b61f-eceaa54bd9c6",
    "observed-data--787710c9-1988-4a1b-9761-a2de5e19c62f"
  ],
  ...
}
```

## 2.13 Observable Container (deprecated) <a id='observable-container'></a>

**Type Name:** <span class="stixtype">observable-container</span>

Representing Cyber-observable Objects in an Observable Container has been deprecated and **SHOULD NOT** be used when creating new content. Existing Observable Data objects using Observable Containers may contain SCOs as defined in this specification, but also may contain Cyber-observable Objects as described in version 2.0 of STIX ([*STIX Version 2.0. Part 3: STIX Objects*](#related-Work)).

The Observable Container type can contain one or more STIX Cyber-observable Objects as a special set of key/value pairs. The keys in the dictionary are the references used to refer to an object which is located in the observable container as a value to some key. The value of this "key" is a reference that can be used in the embedded relationship properties in other objects, which **MUST** be in the same container (such as the src_ref property on the Network Traffic object).

Resolving a reference is the process of identifying all of the objects in an observable container by their "key" reference value. References resolve to an object when the value of the property (e.g., src_ref) is an exact match with the key of another object that resides in the same container as the object that specifies the reference. All such references are local to the container and the referenced object **MUST** be provided within the same container. This specification does not address the implementation of reference resolution. Each key in the observable container dictionary is an identifier.

**STIX 2.0 Example**

*Network Traffic with Source/Destination IPv4 Addresses and AS*

```JSON
{
  "0": {
    "type": "ipv4-addr",
    "value": "1.2.3.4",
    "belongs_to_refs": ["3"]
  },
  "1": {
    "type": "ipv4-addr",
    "value": "2.3.4.5"
  },
  "2": {
    "type": "network-traffic",
    "src_ref": "0",
    "dst_ref": "1",
  }
  "3": {
    "type": "as"
    "number": 42
  }
}
```

*Email Message with Source/Destination Email Addresses*

```JSON
{
  "0": {
    "type": "email-addr",
    "value": "jdoe@example.com",
    "display_name": "John Doe"
  },
  "1": {
    "type": "email-addr",
    "value": "mary@example.com",
    "display_name": "Mary Smith"
  },
  "2": {
    "type": "email-message",
    "from_ref": "0",
    "to_refs": ["1"],
    "date": "1997-11-21T15:55:06Z",
    "subject": "Saying Hello"
  }
}
```

## 2.14 Open Vocabulary <a id='open-vocabulary'></a>

**Type Name:** <span class="stixtype">open-vocab</span>

The <span class="stixtype">open-vocab</span> type is represented as a <span class="stixtype">string</span>. For properties that use this type there will be a list of suggested values, known as the suggested vocabulary, that is identified in the definition for that property. The suggested vocabularies are defined in [section 10](#stix-vocabularies). The value of the property **SHOULD** be chosen from the suggested vocabulary, but **MAY** be any other <span class="stixtype">string</span> value. Values that are not from the suggested vocabulary **SHOULD** be all lowercase and **SHOULD** use hyphens instead of spaces or underscores as word separators.

A consumer that receives STIX content with one or more <span class="stixtype">open-vocab</span> terms not defined in the suggested vocabulary **MAY** ignore those values.

The JSON MTI serialization uses the JSON String type \[[RFC8259](#RFC8259)\] when representing <span class="stixtype">open-vocab</span>.

**Examples**

Example using value from the suggested vocabulary. In this example the Threat Actor **sophistication** property is an open vocabulary and we are using one of the suggested vocabulary values.

```JSON
{
  ...
  "sophistication": "intermediate",
  ...
}
```

Example using a user-defined value. In this example, for the same Threat Actor **sophistication** property, we are not using a value in the suggested vocabulary.

```JSON
{
  ...
  "sophistication": "pbx-advanced-activity",
  ...
}
```

## 2.15 String <a id='string'></a>

**Type Name:** <span class="stixtype">string</span>

The <span class="stixtype">string</span> data type represents a finite-length string of valid characters from the Unicode coded character set \[[ISO10646](#ISO10646)\]. Unicode incorporates ASCII and the characters of many other international character sets.

The JSON MTI serialization uses the JSON String type \[[RFC8259](#RFC8259)\], which mandates the UTF-8 encoding for supporting Unicode.

**Example**

```JSON
{
  ...
  "name": "The Black Vine Cyberespionage Group",
  ...
}
```

## 2.16 Timestamp <a id='timestamp'></a>

**Type Name:** <span class="stixtype">timestamp</span>

The <span class="stixtype">timestamp</span> type defines how dates and times are represented in STIX.

The JSON MTI serialization uses the JSON String type \[[RFC8259](#RFC8259)\] when representing <span class="stixtype">timestamp</span>.

### 2.16.1 Requirements <a id='timestamp-requirements'></a>

- The <span class="stixtype">timestamp</span> property **MUST** be a valid RFC 3339-formatted timestamp \[[RFC3339](#RFC3339)\] using the format <span class="stixalt">YYYY-MM-DDTHH:mm:ss\[.s+\]Z</span> where the "s+" represents 1 or more sub-second values. The brackets denote that sub-second precision is optional, and that if no digits are provided, the decimal place **MUST NOT** be present.
- The timestamp **MUST** be represented in the UTC timezone and **MUST** use the "Z" designation to indicate this.

> NOTE: when using precisions greater than nanoseconds there may be implications for interoperability as they may be truncated when stored as a UNIX timestamp or floating point number due to the fundamental precision of those formats.

**Example**

```JSON
{
  ...
  "created": "2016-01-20T12:31:12.123Z",
  ...
}
```

# 3. STIX General Concepts <a id="stix-general-concepts"></a>

## 3.1 Property Names and String Literals <a id="property-names-and-string-literals"></a>

All type names, property names, and literals **MUST** be in lowercase, except when referencing canonical names defined in another standard (e.g., literal values from an IANA registry). Lowercase is defined by the locality conventions. Type names and property names **MUST** begin with a letter character (for example in ASCII that would be a through z). Words in property names **MUST** be separated with an underscore (`\_`), while words in type names and string enumerations **MUST** be separated with a hyphen (`-`). Dictionary key and hash algorithm names **MAY** have underscores (`_`) or hyphens (`-`). All type names, property names, object names, and vocabulary terms **MUST** be between three and 250 characters long.

Certain names of properties **MUST** have specific suffixes:

- If the value of the property contains an ID reference for embedded relationships it **MUST** end in `_ref`
- If the value of the property contains a list of embedded relationships it **MUST** end in `_refs`
- If the value of the property contains a binary value, it **MUST** end in `_bin`
- If the value of the property contains a hexadecimal value, it **MUST** end in `_hex`
- A property might contain a string with an alternative encoding. Some object types will define an additional optional property to specify this encoding. The name of the additional property **MUST** end in `_enc`. For example, the **name** property might contain text in an alternative encoding, and the **name_enc** property would be used to specify which encoding is used. The encoding property **MUST NOT** be present when the original property is not present.

In the JSON serialization all property names and string literals **MUST** be exactly the same, including case, as the names listed in the property tables in this specification. For example, the SDO common property **created_by_ref** must result in the JSON key name `"created_by_ref"`. Properties marked required in the property tables **MUST** be present in the JSON serialization.

Some properties may be designated as “deprecated.” These properties are in the process of being removed or replaced and implementers should consider using the newer designs.

## 3.2 Common Properties <a id="common-properties"></a>

This section defines the common properties that **MAY** exist on a STIX Object. While some STIX Objects use all of these common properties, not all object types do. Each type of STIX Object defines which common properties are required, which are optional, and which are not in use. A comparison summary table is provided below in this section. This information can also be found at the start of the properties table for each object.

| **<span class="stixtr">Property Name</span>** | **<span class="stixtr">Type</span>** | **<span class="stixtr">Description</span>** |
| --- | --- | --- |
| **type** | <span class="stixtype">string</span> | The **type** property identifies the type of STIX Object. The value of the **type** property **MUST** be the name of one of the types of STIX Objects defined in [section 4](#stix-domain-objects), [section 5](#stix-relationship-objects), [section 6](#stix-cyber-observable-objects), and [section 7](#stix-meta-objects) (e.g., <span class="stixliteral">indicator</span>) or the name of a Custom Object as defined by section [section 11.2](#custom-objects). |
| **spec_version** | <span class="stixtype">string</span> | The version of the STIX specification used to represent this object. The value of this property **MUST** be <span class="stixliteral">2.1</span> for STIX Objects defined according to this specification. Since SCOs are now top-level objects in STIX 2.1, the default value for SCOs is <span class="stixliteral">2.1</span>. |
| **id** | <span class="stixtype">identifier</span> | The **id** property uniquely identifies this object. For objects that support versioning, all objects with the same **id** are considered different versions of the same object and the version of the object is identified by its **modified** property. |
| **created_by_ref** | <span class="stixtype">identifier</span> | The **created_by_ref** property specifies the **id** property of the <span class="stixtype">identity</span> object that describes the entity that created this object. If this attribute is omitted, the source of this information is undefined. This may be used by object creators who wish to remain anonymous. |
| **created** | <span class="stixtype">timestamp</span> | The **created** property represents the time at which the object was originally created. The object creator can use the time it deems most appropriate as the time the object was created. The minimum precision **MUST** be milliseconds (three digits after the decimal place in seconds), but **MAY** be more precise. The **created** property **MUST NOT** be changed when creating a new version of the object. See [section 3.6](#versioning) for further definition of versioning. |
| **modified** | <span class="stixtype">timestamp</span> | The **modified** property is only used by STIX Objects that support versioning and represents the time that this particular version of the object was last modified. The object creator can use the time it deems most appropriate as the time this version of the object was modified. The minimum precision **MUST** be milliseconds (three digits after the decimal place in seconds), but **MAY** be more precise. If the **created** property is defined, then the value of the **modified** property for a given object version **MUST** be later than or equal to the value of the **created** property. Object creators **MUST** set the **modified** property when creating a new version of an object if the **created** property was set. See [section 3.6](#versioning) for further definition of versioning. |
| **revoked** | <span class="stixtype">boolean</span> | The **revoked** property is only used by STIX Objects that support versioning and indicates whether the object has been revoked. Revoked objects are no longer considered valid by the object creator. Revoking an object is permanent; future versions of the object with this **id** **MUST NOT** be created. The default value of this property is <span class="stixliteral">false</span>. See [section 3.6](#versioning) for further definition of versioning. |
| **labels** | <span class="stixtype">list</span> of type <span class="stixtype">string</span> | The **labels** property specifies a set of terms used to describe this object. The terms are user-defined or trust-group defined and their meaning is outside the scope of this specification and **MAY** be ignored. Where an object has a specific property defined in the specification for characterizing subtypes of that object, the labels property **MUST NOT** be used for that purpose. For example, the Malware SDO has a property **malware_types** that contains a list of Malware subtypes (dropper, RAT, etc.). In this example, the labels property cannot be used to describe these Malware subtypes. |
| **confidence** | <span class="stixtype">integer</span> | The **confidence** property identifies the confidence that the creator has in the correctness of their data. The confidence value **MUST** be a number in the range of 0–100. [Appendix A](#confidence-scales) contains a table of normative mappings to other confidence scales that **MUST** be used when presenting the confidence value in one of those scales. If the confidence property is not present, then the confidence of the content is unspecified. |
| **lang** | <span class="stixtype">string</span> | The **lang** property identifies the language of the text content in this object. When present, it **MUST** be a language code conformant to \[[RFC5646](#RFC5646)\]. If the property is not present, then the language of the content is <span class="stixliteral">en</span> (English). This property **SHOULD** be present if the object type contains translatable text properties (e.g., name, description). The language of individual fields in this object **MAY** be overridden by the **lang** property in granular markings (see [section 7.2.3](#granular-markings)). |
| **external_references** | <span class="stixtype">list</span> of type <span class="stixtype">external-reference</span> | The **external_references** property specifies a list of external references which refers to non-STIX information. This property is used to provide one or more URLs, descriptions, or IDs to records in other systems. |
| **object_marking_refs** | <span class="stixtype">list</span> of type <span class="stixtype">identifier</span> | The **object_marking_refs** property specifies a list of **id** properties of <span class="stixtype">marking-definition</span> objects that apply to this object. In some cases, though uncommon, marking definitions themselves may be marked with sharing or handling guidance. In this case, this property **MUST NOT** contain any references to the same Marking Definition object (i.e., it cannot contain any circular references). See [section 7.2](#data-markings) for further definition of data markings. |
| **granular_markings** | <span class="stixtype">list</span> of type <span class="stixtype">granular-marking</span> | The **granular_markings** property specifies a list of granular markings applied to this object. In some cases, though uncommon, marking definitions themselves may be marked with sharing or handling guidance. In this case, this property **MUST NOT** contain any references to the same Marking Definition object (i.e., it cannot contain any circular references). See [section 7.2](#data-markings) for further definition of data markings. |
| **defanged** | <span class="stixtype">boolean</span> | This property defines whether or not the data contained within the object has been defanged. The default value for this property is <span class="stixliteral">false</span>. This property **MUST NOT** be used on any STIX Objects other than SCOs. |
| **extensions** | <span class="stixtype">dictionary</span> | Specifies any extensions of the object, as a dictionary. Dictionary keys **SHOULD** be the id of a STIX Extension object or the name of a predefined object extension found in this specification, depending on the type of extension being used. The corresponding dictionary values **MUST** contain the contents of the extension instance. Each extension dictionary **MAY** contain the property **extension_type**. The value of this property **MUST** come from the <span class="stixtype">extension-type-enum</span> enumeration. If the **extension_type** property is not present, then this is a predefined extension which does not use the extension facility described in [section 7.3](#extension-definition). When this extension facility is used the **extension_type** property **MUST** be present. |

---

This table lists all common properties and how they are used for each type of STIX Object. The following table is informational, and the body of the spec is normative and the definitive reference.

<table border="1" cellspacing="0" cellpadding="6">
  <tr>
    <th colspan="1" style="background-color:#004A7F;"/>
    <th colspan="3" style="text-align:center; background-color:#004A7F; color:white;">STIX Core Objects</th>
    <th colspan="3" style="text-align:center; background-color:#004A7F; color:white;">STIX Meta Object</th>
    <th colspan="1" style="background-color:#004A7F;"/>
  </tr>
  <tr>
    <th style="text-align:center; background-color:#004A7F; color:white;">Property Name</th>
    <th style="text-align:center; background-color:#004A7F; color:white;">SDOs</th>
    <th style="text-align:center; background-color:#004A7F; color:white;">SROs</th>
    <th style="text-align:center; background-color:#004A7F; color:white;">SCOs</th>
    <th style="text-align:center; background-color:#004A7F; color:white;">Extension</th>
    <th style="text-align:center; background-color:#004A7F; color:white;">Language</th>
    <th style="text-align:center; background-color:#004A7F; color:white;">Markings</th>
    <th style="text-align:center; background-color:#004A7F; color:white;">Bundle</th>
  </tr>
  <tr>
    <td><strong>type</strong></td>
    <td><span class="stixreq">Required</span></td>
    <td><span class="stixreq">Required</span></td>
    <td><span class="stixreq">Required</span></td>
    <td><span class="stixreq">Required</span></td>
    <td><span class="stixreq">Required</span></td>
    <td><span class="stixreq">Required</span></td>
    <td><span class="stixreq">Required</span></td>
  </tr>
  <tr>
    <td><strong>spec_version</strong></td>
    <td><span class="stixreq">Required</span></td>
    <td><span class="stixreq">Required</span></td>
    <td><span class="stixopt">Optional</span></td>
    <td><span class="stixreq">Required</span></td>
    <td><span class="stixreq">Required</span></td>
    <td><span class="stixreq">Required</span></td>
    <td><span class="stixna">N/A</span></td>
  </tr>
  <tr>
    <td><strong>id</strong></td>
    <td><span class="stixreq">Required</span></td>
    <td><span class="stixreq">Required</span></td>
    <td><span class="stixreq">Required</span></td>
    <td><span class="stixreq">Required</span></td>
    <td><span class="stixreq">Required</span></td>
    <td><span class="stixreq">Required</span></td>
    <td><span class="stixreq">Required</span></td>
  </tr>
  <tr>
    <td><strong>created_by_ref</strong></td>
    <td><span class="stixopt">Optional</span></td>
    <td><span class="stixopt">Optional</span></td>
    <td><span class="stixna">N/A</span></td>
    <td><span class="stixreq">Required</span></td>
    <td><span class="stixopt">Optional</span></td>
    <td><span class="stixopt">Optional</span></td>
    <td><span class="stixna">N/A</span></td>
  </tr>
  <tr>
    <td><strong>created</strong></td>
    <td><span class="stixreq">Required</span></td>
    <td><span class="stixreq">Required</span></td>
    <td><span class="stixna">N/A</span></td>
    <td><span class="stixreq">Required</span></td>
    <td><span class="stixreq">Required</span></td>
    <td><span class="stixreq">Required</span></td>
    <td><span class="stixna">N/A</span></td>
  </tr>
  <tr>
    <td><strong>modified</strong></td>
    <td><span class="stixreq">Required</span></td>
    <td><span class="stixreq">Required</span></td>
    <td><span class="stixna">N/A</span></td>
    <td><span class="stixreq">Required</span></td>
    <td><span class="stixreq">Required</span></td>
    <td><span class="stixna">N/A</span></td>
    <td><span class="stixna">N/A</span></td>
  </tr>
  <tr>
    <td><strong>revoked</strong></td>
    <td><span class="stixopt">Optional</span></td>
    <td><span class="stixopt">Optional</span></td>
    <td><span class="stixna">N/A</span></td>
    <td><span class="stixopt">Optional</span></td>
    <td><span class="stixopt">Optional</span></td>
    <td><span class="stixna">N/A</span></td>
    <td><span class="stixna">N/A</span></td>
  </tr>
  <tr>
    <td><strong>labels</strong></td>
    <td><span class="stixopt">Optional</span></td>
    <td><span class="stixopt">Optional</span></td>
    <td><span class="stixna">N/A</span></td>
    <td><span class="stixopt">Optional</span></td>
    <td><span class="stixopt">Optional</span></td>
    <td><span class="stixna">N/A</span></td>
    <td><span class="stixna">N/A</span></td>
  </tr>
  <tr>
    <td><strong>confidence</strong></td>
    <td><span class="stixopt">Optional</span></td>
    <td><span class="stixopt">Optional</span></td>
    <td><span class="stixna">N/A</span></td>
    <td><span class="stixna">N/A</span></td>
    <td><span class="stixopt">Optional</span></td>
    <td><span class="stixna">N/A</span></td>
    <td><span class="stixna">N/A</span></td>
  </tr>
  <tr>
    <td><strong>lang</strong></td>
    <td><span class="stixopt">Optional</span></td>
    <td><span class="stixopt">Optional</span></td>
    <td><span class="stixna">N/A</span></td>
    <td><span class="stixna">N/A</span></td>
    <td><span class="stixna">N/A</span></td>
    <td><span class="stixna">N/A</span></td>
    <td><span class="stixna">N/A</span></td>
  </tr>
  <tr>
    <td><strong>external_references</strong></td>
    <td><span class="stixopt">Optional</span></td>
    <td><span class="stixopt">Optional</span></td>
    <td><span class="stixna">N/A</span></td>
    <td><span class="stixopt">Optional</span></td>
    <td><span class="stixopt">Optional</span></td>
    <td><span class="stixopt">Optional</span></td>
    <td><span class="stixna">N/A</span></td>
  </tr>
  <tr>
    <td><strong>object_marking_refs</strong></td>
    <td><span class="stixopt">Optional</span></td>
    <td><span class="stixopt">Optional</span></td>
    <td><span class="stixopt">Optional</span></td>
    <td><span class="stixopt">Optional</span></td>
    <td><span class="stixopt">Optional</span></td>
    <td><span class="stixopt">Optional</span></td>
    <td><span class="stixna">N/A</span></td>
  </tr>
  <tr>
    <td><strong>granular_markings</strong></td>
    <td><span class="stixopt">Optional</span></td>
    <td><span class="stixopt">Optional</span></td>
    <td><span class="stixopt">Optional</span></td>
    <td><span class="stixopt">Optional</span></td>
    <td><span class="stixopt">Optional</span></td>
    <td><span class="stixopt">Optional</span></td>
    <td><span class="stixna">N/A</span></td>
  </tr>
  <tr>
    <td><strong>defanged</strong></td>
    <td><span class="stixna">N/A</span></td>
    <td><span class="stixna">N/A</span></td>
    <td><span class="stixopt">Optional</span></td>
    <td><span class="stixna">N/A</span></td>
    <td><span class="stixna">N/A</span></td>
    <td><span class="stixna">N/A</span></td>
    <td><span class="stixna">N/A</span></td>
  </tr>
  <tr>
    <td><strong>extensions</strong></td>
    <td><span class="stixopt">Optional</span></td>
    <td><span class="stixopt">Optional</span></td>
    <td><span class="stixopt">Optional</span></td>
    <td><span class="stixna">N/A</span></td>
    <td><span class="stixopt">Optional</span></td>
    <td><span class="stixopt">Optional</span></td>
    <td><span class="stixna">N/A</span></td>
  </tr>
</table>

## 3.3 Object IDs and References <a id="object-ids-and-references"></a>

All STIX Objects and the STIX Bundle Object have an **id** property that uniquely identifies each instance of the object. This **id** **MUST** meet the requirements of the <span class="stixtype">identifier</span> type (see [section 2.9](#identifier)]).

The <span class="stixtype">identifier</span> type is also used as an ID reference to define a relationship to other STIX Objects. Resolving an ID reference is the process of identifying and obtaining the actual object referred to by the ID reference property. ID references resolve to an object when the value of the ID reference property (e.g., **created_by_ref**) is an exact match with the **id** property of another object. If a consumer has access to multiple versions of an object, the consumer **SHOULD** interpret any references to that object as referring to the latest version as defined in [section 3.6](#versioning). ID references can refer to objects to which the consumer/producer may not currently have access; this specification does not address the implementation of ID reference resolution.

Some ID references (embedded relationships) may be restricted to a subset of object types, as specified in the description of the property that defines the relationship. For example, the **object_marking_refs** common property specifies that the only valid target of the relationship is one or more <span class="stixtype">marking-definition</span> objects.

## 3.4 SCO Deterministic ID Creation <a id="sco-deterministic-id-creation"></a>

To enable deterministic IDs for STIX Cyber-observable Objects (SCOs), each SCO defines a set of one or more properties named “ID Contributing Properties.” These properties **MAY** be used in the default calculation of the **id** when creating a SCO. In some cases, additional selection of extension properties that contribute to the ID may be described in the ID Contributing Properties section listed on each SCO. The default algorithm that creates the SCO ID based on those named properties is a UUIDv5 as defined in [section 2.9](#identifier), however, other algorithms for creating the SCO ID **MAY** be used.

Deterministic IDs (UUIDv5) in the example SCOs contained in this specification were computed using the algorithm defined in [section 2.9](#identifier). Every attempt was made for these IDs to be accurate. Certain IDs which were used in reference properties of the examples did not include the actual object, and therefore it was impossible to accurately compute the appropriate UUIDv5. In these cases, a UUIDv4 was generated.

## 3.5 Object Creator <a id="object-creator"></a>

The object creator is the entity (e.g., system, organization, instance of a tool) that generates the **id** property for a given object. Object creators are represented as Identity objects. Some STIX Objects allow this designation (see [section 3.2](#common-properties)). An embedded relationship to the Identity object representing the object creator **SHOULD** be captured in the **created_by_ref** property (or that property can be omitted, meaning the object creator is anonymous).

Entities that re-publish an object from another entity without making any changes to the object, and thus maintaining the original **id**, are not considered the object creator and **MUST NOT** change the **created_by_ref** property. An entity that accepts objects and republishes them with modifications, additions, or omissions **MUST** create a new **id** for the object. They are considered the object creator of the new object for purposes of versioning.

## 3.6 Versioning <a id="versioning"></a>

Versioning is the mechanism that object creators use to update and revoke the STIX Objects that they create. This section describes the versioning process and normative rules for performing versioning and revocation. STIX Objects that are versioned **MUST** use the property names **created_by_ref**, **created**, **modified**, and **revoked**. SCOs are not versioned and thus do not have the four versioning properties. See the properties table in [section 3.2](#common-properties) for full definitions and normative usage of those properties.

STIX Objects **MAY** be versioned in order to update, add, or remove information. A version of a STIX Object is identified uniquely by the combination of its **id** and **modified** properties. The first version of the object **MUST** have the same timestamp for the **created** and **modified** properties. More recent values of the **modified** property indicate later versions of the object. Implementations **MUST** consider the version of the STIX Object with the most recent **modified** value to be the most recent state of the object. For every new version of an object, the **modified** property **MUST** be updated to represent the time that the new version was created. If a consumer receives two objects that are different, but have the same **id** and **modified** timestamp, it is not defined how the consumer handles the objects. This specification does not address how implementations should handle versions of the object that are not current.

STIX Objects have a single *object creator*, the entity that generates the **id** for the object and creates the first version. The object creator **MAY** (but not necessarily will) be identified in the **created_by_ref** property of the object. Only the object creator is permitted to create new versions of a STIX Object. Producers other than the object creator **MUST NOT** create new versions of that object. If a producer other than the object creator wishes to create a new version, they **MUST** instead create a new object with a new **id**. They **SHOULD** additionally create a <span class="stixliteral">derived-from</span> Relationship object to relate their new object to the original object that it was derived from.

Every representation (each time the object version is serialized and shared) of a version of an object (identified by the object's **id** and **modified** properties) **MUST** always have the same set of properties and the same values for each property. If a property has the same value as the default, it **MAY** be omitted from a representation, and this does not represent a change to the object. In order to change the value of any property, or to add or remove properties, the **modified** property **MUST** be updated with the time of the change to indicate a new version.

Objects can also be revoked, which means that they are no longer considered valid by the object creator. As with issuing a new version, only the object creator is permitted to revoke a STIX Object. A value of <span class="stixliteral">true</span> in the **revoked** property indicates that an object (including the current version and all past versions) has been revoked. Revocation is permanent: once an object is marked as revoked, later versions of that object **MUST NOT** be created. Changing the **revoked** property to indicate that an object is revoked is an update to the object, and therefore its **modified** property **MUST** be updated at the same time. This specification does not address how implementations should handle revoked data.

It should be noted that if a producer versions a SCO (assigns value to these four properties) that no other producer would be allowed to create or modify the same SCO with an equivalent deterministic **id**, as that would conflict with the strict versioning rules defined in STIX2. Therefore, for interoperability and sharing, producers versioning SCOs **MUST NOT** use the default namespace for deterministic ID creation. Otherwise multiple different producers will conflict with each other if producing the same SCO intelligence.

### 3.6.1 Versioning Timestamps <a id="versioning-timestamps"></a>

There are two timestamp properties used to indicate when STIX Objects were created and modified: **created** and **modified**. The **created** property indicates the time the first version of the object was created. The **modified** property indicates the time the specific version of the object was created. The **modified** time **MUST NOT** be earlier than the **created** time. This specification does not address the specifics of how implementations should determine the value of the creation and modification times for use in the **created** and **modified** properties (e.g., one system might use when the object is first added to the local database as the creation time, while another might use the time when the object is first distributed as STIX).
