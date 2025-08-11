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

### 3.6.2 New Version or New Object? <a id="new-version-or-new-object"></a>

Eventually an implementation will encounter a case where a decision must be made regarding whether a change is a new version of an existing object or is different enough that it is a new object. This is generally considered a data quality problem and therefore this specification does not provide any normative text.

However, to assist implementers and promote consistency across implementations, some rules of thumb are provided. Any time a change indicates a *material change* to the meaning of the object, a new object with a different **id** should be used. A material change is any change that the object creator believes substantively changes the meaning of the object. As an example, an object creator might consider changing a Threat Actor from one country to another is a material change. These decisions are always made by the object creator. The object creator should also think about relationships to the object when deciding if a change is material. If the change would invalidate the usefulness of relationships to the object, then the change is considered material and a new object **id** should be used.

**Examples**

*Example of a new version*

One object creator has decided that the previous name they used for an SDO is incorrect. They consider that change as an update to the object.

> NOTE: the IDs in the example below use a simplified format to help illustrate the changing IDs more clearly.

<table border="1" cellspacing="0" cellpadding="6">
  <tr>
    <th><span class="stixtr">Step&nbsp;#</span</th>
    <th><span class="stixtr">STIX Object</span></th>
    <th><span class="stixtr">Object Creator Action</span></th>
  </tr>
  <tr>
    <td>1</td>
    <td><pre class="nowrap"><code class="language-JSON">{
  "type": "example",
  "id": "example--1",
  "created": "2016-05-01T06:13:14.000Z",
  "modified": "2016-05-01T06:13:14.000Z",
  "name": "attention",
  "description": "this is the description"
}</code></pre></td>
    <td>Original object created.</td>
  </tr>
  <tr>
    <td>2</td>
    <td>N/A, STIX is not involved in this step</td>
    <td>Object creator changes the name in their internal database.</td>
  </tr>
  <tr>
    <td>3</td>
    <td><pre class="nowrap"><code class="language-JSON">{
  "type": "example",
  "id": "example--1",
  "created": "2016-05-01T06:13:14.000Z",
  "modified": "2016-05-08T03:43:44.000Z",
  "name": "Attention!",
  "description": "this is the description"
}</code></pre></td>
    <td>Object creator updates the <strong>modified</strong> property.</td>
  </tr>
</table>

*Example of a derived object*

One object creator has decided that the previous name they used for an SDO is incorrect. They consider that change fundamental to the meaning of the object and therefore revoke the object and issue a new one.

<table border="1" cellspacing="0" cellpadding="6">
  <tr>
    <th><span class="stixtr">Step&nbsp;#</span></th>
    <th><span class="stixtr">STIX Object</span></th>
    <th><span class="stixtr">Object Creator Action</span></th>
  </tr>
  <tr>
    <td>1</td>
    <td><pre class="nowrap"><code class="language-JSON">{
  "type": "example",
  "id": "example--2",
  "created": "2016-05-01T06:13:14.000Z",
  "modified": "2016-05-01T06:13:14.000Z",
  "name": "attention",
  "description": "this is the description"
}</code></pre></td>
    <td>Original object created (via new id and setting <strong>created</strong> and <strong>modified</strong> to the same value).</td>
  </tr>
  <tr>
    <td>2</td>
    <td>N/A, STIX is not involved in this step</td>
    <td>Object creator changes the name in their internal database.</td>
  </tr>
  <tr>
    <td>3</td>
    <td><pre class="nowrap"><code class="language-JSON">{
  "type": "example",
  "id": "example--2",
  "created": "2016-05-01T06:13:14.000Z",
  "modified": "2016-05-08T03:43:44.000Z",
  "name": "Attention!",
  "description": "this is the description",
  "revoked": true
}</code></pre></td>
    <td>Object creator revokes the existing object by setting <strong>revoked</strong> to <span class="stixliteral">true</span>. The <strong>modified</strong> property is updated.</td>
  </tr>
  <tr>
    <td>4</td>
    <td><pre class="nowrap"><code class="language-JSON">{
  "type": "example",
  "id": "example--3",
  "created": "2016-05-08T03:43:44.000Z",
  "modified": "2016-05-08T03:43:44.000Z",
  "name": "Something completely different",
  "description": "this is the description"
}</code></pre></td>
    <td>Object creator creates a new object (with a new <strong>id</strong> and setting <strong>created</strong> and <strong>modified</strong> to the same value).</td>
  </tr>
  <tr>
    <td>5</td>
    <td><pre class="nowrap"><code class="language-JSON">{
  "type": "relationship",
  "id": "relationship--4",
  "created": "2016-05-08T03:43:44.000Z",
  "modified": "2016-05-08T03:43:44.000Z",
  "relationship_type": "derived-from",
  "source_ref": "example--2",
  "target_ref": "example--3"
}</code></pre></td>
    <td>(Optional) Object creator creates a new Relationship object indicating that the new object is derived from the old object.</td>
  </tr>
</table>

*Examples of consumer workflow*

This section describes an example workflow where a consumer receives multiple updates to a particular object. (In this example, the STIX Objects have been truncated for brevity.)

<table border="1" cellspacing="0" cellpadding="6">
  <tr>
    <th><span class="stixtr">Step&nbsp;#</span></th>
    <th><span class="stixtr">STIX Object</span></th>
    <th><span class="stixtr">Object Creator Action</span></th>
  </tr>
  <tr>
    <td>1</td>
    <td><pre class="nowrap"><code class="language-JSON">{
  "type": "example",
  "id": "example--5",
  "created": "2016-05-01T06:13:14.000Z",
  "modified": "2016-05-01T06:13:14.000Z"
}</code></pre></td>
    <td>Consumer stores example object because this is the first time they have seen the object.</td>
  </tr>
  <tr>
    <td>2</td>
    <td><pre class="nowrap"><code class="language-JSON">{
  "type": "example",
  "id": "example--5",
  "created": "2016-05-01T06:13:14.000Z",
  "modified": "2016-05-08T03:43:44.000Z"
}</code></pre></td>
    <td>Consumer updates example object because the received <strong>modified</strong> property is later than the object that is currently stored.</td>
  </tr>
  <tr>
    <td>3</td>
    <td><pre class="nowrap"><code class="language-JSON">{
  "type": "example",
  "id": "example--5",
  "created": "2016-05-01T06:13:14.000Z",
  "modified": "2016-05-06T06:23:45.000Z"
}</code></pre></td>
    <td>Consumer ignores this object because they already have a newer version of the object.<br><br>Note: consumer might choose to store meta-information about received objects, including versions that were received out-of-order. The consumer also may choose to store a copy for reference.</td>
  </tr>
  <tr>
    <td>4</td>
    <td><pre class="nowrap"><code class="language-JSON">{
  "type": "example",
  "id": "example--5",
  "created": "2016-05-01T06:13:14.000Z",
  "modified": "2016-05-11T06:41:21.000Z",
  "revoked": true
}</code></pre></td>
    <td>Consumer receives revoked version and decides to delete example object but keeps some metadata regarding the object.</td>
  </tr>
  <tr>
    <td>5</td>
    <td><pre class="nowrap"><code class="language-JSON">{
  "type": "example",
  "id": "example--5",
  "created": "2016-05-01T06:13:14.000Z",
  "modified": "2016-05-10T17:28:54.000Z"
}</code></pre></td>
    <td>Consumer ignores this object because they already have a newer version of the object (the revoked version).</td>
  </tr>
</table>

*Example of object creator workflow*

This section describes an example workflow where an object creator publishes multiple updates to a particular object. This scenario assumes a human using a STIX implementation. (In this example, the STIX Objects have been truncated for brevity.)

<table border="1" cellspacing="0" cellpadding="6">
<tr>
    <th><span class="stixtr">Step&nbsp;#</span></th>
    <th><span class="stixtr">STIX Object</span></th>
    <th><span class="stixtr">Object Creator Action</span></th>
  </tr>
  <tr>
    <td>1</td>
    <td>N/A - STIX is not involved in this scenario.<br><br>(Tools <em>could</em> choose to create and track STIX versions for internal changes, but it is not required by the specification.)</td>
    <td>User clicks a create button in the user interface, creates an SDO, then clicks save. This action causes information to be stored in the product’s database.</td>
  </tr>
  <tr>
    <td>2</td>
    <td><pre class="nowrap"><code class="language-JSON">{
  "type": "example",
  "id": "example--6",
  "created": "2016-05-01T06:13:14.000Z",
  "modified": "2016-05-01T06:13:14.000Z"
}</code></pre></td>
    <td>The user clicks the "share" button, delivering the intelligence to sharing partners.</td>
  </tr>
  <tr>
    <td>3</td>
    <td>N/A - STIX is not involved in this scenario.<br><br>(Tools <em>could</em> choose to create and track STIX versions for internal changes, but it is not required by the specification.)</td>
    <td>The user performs additional analysis within the STIX implementation, performing multiple modifications and saving their work multiple times.</td>
  </tr>
  <tr>
    <td>4</td>
    <td><pre class="nowrap"><code class="language-JSON">{
  "type": "example",
  "id": "example--6",
  "created": "2016-05-01T06:13:14.000Z",
  "modified": "2016-05-03T16:33:51.000Z"
}</code></pre></td>
    <td>The user, happy with the status of their work, decides to provide an update to some properties of the previously published object (not shown).</td>
  </tr>
  <tr>
    <td>5</td>
    <td><pre class="nowrap"><code class="language-JSON">{
  "type": "example",
  "id": "example--6",
  "created": "2016-05-01T06:13:14.000Z",
  "modified": "2016-05-08T13:35:12.000Z",
  "revoked": true
}</code></pre></td>
    <td>The user receives lots of negative feedback regarding the quality of their work and decides to retract the object by pressing the "revoke" button.</td>
  </tr>
</table>

## 3.7 Common Relationships <a id='common-relationships'></a>

Each SDO and SCO has its own set of relationship types that are specified in the definition of that SDO or SCO.
The following common relationship types are defined for all SDOs and SCOs.
See <a href="#stix-relationships">STIX Relationships</a> for more information about relationships.

<table border="1" cellspacing="0" cellpadding="6">
  <tr>
    <th><span class="stixtr">Relationship&nbsp;Type</span></th>
    <th><span class="stixtr">Source</span></th>
    <th><span class="stixtr">Target</span></th>
    <th><span class="stixtr">Description</span></th>
  </tr>
  <tr>
    <td><span class="stixliteral">derived-from</span></td>
    <td><span class="stixtype">&lt;SDO or SCO of same type as target&gt;</span></td>
    <td><span class="stixtype">&lt;SDO or SCO of same type as source&gt;</span></td>
    <td>The information in the target object is based on information from the source object.<br><br><span class="stixliteral">derived-from</span> is an explicit relationship between two separate objects. It is not a substitute for the versioning process defined in <a href="#versioning">Section 3.6</a>.</td>
  </tr>
  <tr>
    <td><span class="stixliteral">duplicate-of</span></td>
    <td><span class="stixtype">&lt;SDO or SCO of same type as target&gt;</span></td>
    <td><span class="stixtype">&lt;SDO or SCO of same type as source&gt;</span></td>
    <td>The referenced source and target objects are semantically duplicates of each other.<br><br>This specification does not address whether the source or the target object is the duplicate object or what action, if any, a consumer should take when receiving an instance of this relationship.<br><br>As an example, a Campaign object from one organization could be marked as a <span class="stixliteral">duplicate-of</span> a Campaign object from another organization if they both described the same campaign.</td>
  </tr>
  <tr>
    <td><span class="stixliteral">related-to</span></td>
    <td><span class="stixtype">&lt;SDO or SCO of any type&gt;</span></td>
    <td><span class="stixtype">&lt;SDO or SCO of any type&gt;</span></td>
    <td>Asserts a non-specific relationship between two SDOs. This relationship can be used when none of the other predefined relationships are appropriate, and a user-defined one is not needed.<br><br>As an example, a Malware object describing a piece of malware could be marked as <span class="stixliteral">related-to</span> a Tool if they are commonly used together. That relationship is not common enough to standardize but may be useful to some analysts.</td>
  </tr>
</table>

## 3.8 Reserved Names <a id='reserved-names'></a>

This section defines property names that are reserved for future revisions of this document. The property names defined in this section and any property name that is marked as <span class="strixtype">RESERVED</span> **MUST NOT** be used for the name of any Custom Property or be present in any STIX content conforming to this version of the specification.

Properties that are currently reserved across all STIX Objects are:

- <span class="stixtype">severity</span>
- <span class="stixtype">username</span>
- <span class="stixtype">phone_number</span>
- <span class="stixtype">action</span>

## 3.9 Object Property Metadata <a id='object-property-metadata'></a>

### 3.9.1 SCO String Encoding <a id='sco-string-encoding'></a>

Capturing the observed encoding of a particular STIX Cyber-observable Object (SCO) string is useful for attribution, the creation of indicators, and related use cases.

Certain string properties in STIX Cyber-observable Objects may contain an additional sibling property with the same base name and a suffix of `_enc` that captures the name of the original observed encoding of the property value. All `_enc` properties **MUST** specify their encoding using the ccorresponding name from the IANA character set registry \[[CharacterSets](#character-sets)\]. If the preferred MIME name for a character set is defined, this value **MUST** be used; if it is not defined, then the Name value from the registry **MUST** be used instead.

**Example**

*File with Unicode representation of the filename and a corresponding encoding specification*

```JSON
{
  "type": "file",
  "id": "file-1389b98d-a3d3-5190-a996-716fd444059a",
  "hashes": {
    "SHA-256": "effb46bba03f6c8aea5c653f9cf984f170dcdd3bbbe2ff6843c3e5da0e698766"
  },
  "name": "quêry.dll",
  "name_enc": "windows-1252"
}
```

## 3.10 Predefined Object Extensions <a id='predefined-object-extensions'></a>

Predefined Object Extensions have a specific purpose in STIX Objects: defining coherent sets of properties beyond the base, e.g., HTTP request information for a Network Traffic object. Accordingly, each object may include one or more Predefined Object Extensions.

Each Predefined Object Extension can be defined at most once on a given STIX Object. Each extension is specified under the **extensions** property, which is of type <span class="stixtype">dictionary</span>. Note that this means that each extension is specified through a corresponding key in the <span class="stixtype">extensions</span> property. For example, when specified in a File object instance, the NTFS File Extension would be specified using the key value of <span class="stixtype">ntfs-ext</span>.

**Example**

*Basic File with NTFS Extension*

```JSON
{
  "type": "file",
  "spec_version": "2.1",
  "id": "file--1b40e321-ae73-5637-bd97-33c35a86b80d",
  "hashes": {
    "MD5": "3773a88f65a5e780c8dff9cdc3a056f3"
  },
  "size": 25537,
  "extensions": {
    "ntfs-ext": {
      "sid": "1234567"
    }
  }
}
```


# 4. STIX Domain Objects <a id="stix-domain-objects"></a>

This specification defines the set of STIX Domain Objects (SDOs), each of which corresponds to a unique concept commonly represented in CTI. Using SDOs, STIX Cyber-observable Objects (SCOs), and STIX Relationship Objects (SROs) as building blocks, individuals can create and share broad and comprehensive cyber threat intelligence.

Property information, relationship information, and examples are provided for each SDO defined below.
Property information includes common properties as well as properties that are specific to each SDO.
Relationship information includes embedded relationships (e.g., **created_by_ref**), common relationships (e.g., <span class="stixliteral">related-to</span>), and SDO-specific relationships.
Forward relationships (i.e., relationships *from* the SDO to other SDOs or SCOs) are fully defined, while reverse relationships (i.e., relationships *to* the SDO from other SDOs or SCOs) are duplicated for convenience.

Some SDOs are similar and can be grouped together into categories. Attack Pattern, Malware, and Tool can all be considered types of tactics, techniques, and procedures (TTPs): they describe behaviors and resources that attackers use to carry out their attacks. Similarly, Campaign, Intrusion Set, and Threat Actor all describe information about why adversaries carry out attacks and how they organize themselves.

## 4.1 Attack Pattern <a id="attack-pattern"></a>


**Type Name:** <span class="stixtype">attack-pattern</span>

Attack Patterns are a type of TTP that describe ways that adversaries attempt to compromise targets. Attack Patterns are used to help categorize attacks, generalize specific attacks to the patterns that they follow, and provide detailed information about how attacks are performed. An example of an attack pattern is "spear phishing": a common type of attack where an attacker sends a carefully crafted e-mail message to a party with the intent of getting them to click a link or open an attachment to deliver malware. Attack Patterns can also be more specific; spear phishing as practiced by a particular threat actor (e.g., they might generally say that the target won a contest) can also be an Attack Pattern.

The Attack Pattern SDO contains textual descriptions of the pattern along with references to externally-defined taxonomies of attacks such as [CAPEC](#capec).

### 4.1.1 Properties <a id="attack-pattern-properties"></a>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th><span class='stixtr'>Required Common Properties</span></th>
  </tr>
  <tr>
    <td><strong>type</strong>, <strong>spec_version</strong>, <strong>id</strong>, <strong>created</strong>, <strong>modified</strong></td>
  </tr>
  <tr>
    <th><span class='stixtr'>Optional Common Properties</span></th>
  </tr>
  <tr>
    <td><strong>created_by_ref</strong>, <strong>revoked</strong>, <strong>labels</strong>, <strong>confidence</strong>, <strong>lang</strong>, <strong>external_references</strong>, <strong>object_marking_refs</strong>, <strong>granular_markings</strong>, <strong>extensions</strong></td>
  </tr>
  <tr>
    <th><span class='stixtr'>Not Applicable Common Properties</span></th>
  </tr>
  <tr>
    <td><strong>defanged</strong></td>
  </tr>
  <tr>
    <th><span class='stixtr'>Attack Pattern Specific Properties</span></th>
  </tr>
  <tr>
    <td><strong>name</strong>, <strong>description</strong>, <strong>aliases</strong>, <strong>kill_chain_phases</strong></td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6">
  <tr>
    <th><span class='stixtr'>Property Name</span</th>
    <th><span class='stixtr'>Type</span</th>
    <th><span class='stixtr'>Description</span</th>
  </tr>
  <tr>
    <td><strong>type</strong> (required)</td>
    <td><span class="stixtype">string</span></td>
    <td>The value of this property <strong>MUST</strong> be <span class="stixliteral">attack-pattern</span>.</td>
  </tr>
  <tr>
    <td><strong>external_refererences</strong> (optional)</td>
    <td><span style="white-space:nowrap"><span class="stixtype">list</span> of type <span class="stixtype">external-reference</span></span></td>
    <td>A list of external references which refer to non-STIX information. This property <strong>MAY</strong> be used to provide one or more Attack Pattern identifiers, such as a CAPEC ID. When specifying a CAPEC ID, the <strong>source_name</strong> property of the external reference <strong>MUST</strong> be set to <span class="stixliteral">capec</span> and the <strong>external_id</strong> property <strong>MUST</strong> be formatted as <span class="stixliteral">CAPEC-[id]</span>.</td>
  </tr>
  <tr>
    <td><strong>name</strong> (required)</td>
    <td><span class="stixtype">string</span></td>
    <td>A name used to identify the Attack Pattern.</td>
  </tr>
  <tr>
    <td><strong>description</strong> (optional)</td>
    <td><span class="stixtype">string</span></td>
    <td>A description that provides more details and context about the Attack Pattern, potentially including its purpose and its key characteristics.</td>
  </tr>
  <tr>
    <td><strong>aliases</strong> (optional)</td>
    <td><span style="white-space:nowrap"><span class="stixtype">list</span> of type <span class="stixtype">string</span></span></td>
    <td>Alternative names used to identify this Attack Pattern.</td>
  </tr>
  <tr>
    <td><strong>kill_chain_phases</strong> (optional)</td>
    <td><span style="white-space:nowrap"><span class="stixtype">list</span> of type <span class="stixtype">kill-chain-phase</span></span></td>
    <td>The list of Kill Chain Phases for which this Attack Pattern is used.</td>
  </tr>
</table>

### 4.1.2 Relationships <a id="attack-pattern-relationships"></a>

These are the relationships explicitly defined between the Attack Pattern object and other STIX Objects. The first section lists the embedded relationships by property name along with their corresponding target. The rest of the table identifies the relationships that can be made from this object type to another object type by way of the Relationship object. The reverse relationships section illustrates the relationships targeting this object type from another object type. They are included here for convenience. For their definitions, please see the "Source" object.

Relationships are not restricted to those listed below. Relationships can be created between any objects using the related-to relationship type or, as with open vocabularies, user-defined names.

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th colspan='2'><span class='stixtr'>Embedded Relationships</span></th>
  </tr>
  <tr>
    <td width="50%"><strong>created_by_ref</strong></td>
    <td width="50%"><span class="stixtype">identifier</span> (of type <span class="stixtype">identity</span>)</td>
  </tr>
  <tr>
    <td><strong>object_marking_refs</strong></td>
    <td><span class="stixtype">list</span> of type <span class="stixtype">identifier</span> (of type <span class="stixtype">marking-definition</span>)</td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th><span class='stixtr'>Common Relationships</span></th>
  </tr>
  <tr>
    <td><span class="stixliteral">duplicate-of</span>, <span class="stixliteral">derived-from</span>, <span class="stixliteral">related-to</span></td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6">
  <tr>
    <th width="20%"><span class='stixtr'>Source</span></th>
    <th width="20%""><span class='stixtr'>Relationship Type</span></th>
    <th width="20%"><span class='stixtr'>Target</span></th>
    <th><span class='stixtr'>Description</span></th>
  </tr>
  <tr>
    <td><span class='stixtype'>attack-pattern</span></td>
    <td><span class='stixliteral'>delivers</span></td>
    <td><span class='stixtype'>malware</span></td>
    <td>This Relationship describes that this Attack Pattern is used to deliver this malware instance (or family).</td>
  </tr>
  <tr>
    <td><span class='stixtype'>attack-pattern</span></td>
    <td><span class='stixliteral'>targets</span></td>
    <td><span class='stixtype'>identity</span>, <span class='stixtype'>location</span>, <span class='stixtype'>vulnerability</span></td>
    <td>This Relationship describes that this Attack Pattern typically targets the type of victim, location, or vulnerability represented by the related Identity, Location, or Vulnerability object.<br><br> For example, a <span class='stixliteral'>targets</span> Relationship linking an Attack Pattern for SQL injection to an Identity object representing domain administrators means that the form of SQL injection characterized by the Attack Pattern targets domain administrators in order to achieve its objectives.<br><br>Another example is a Relationship linking an Attack Pattern for SQL injection to a Vulnerability in blogging software means that the particular SQL injection attack exploits that vulnerability.</td>
  </tr>
  <tr>
    <td><span class='stixtype'>attack-pattern</span></td>
    <td><span class='stixliteral'>uses</span></td>
    <td><span class='stixtype'>malware</span>, <span class='stixtype'>tool</span></td>
    <td>This Relationship describes that the related Malware or Tool is used to perform the behavior identified in the Attack Pattern.<br><br>For example, a <span class='stixliteral'>uses</span> Relationship linking an Attack Pattern for a distributed denial of service (DDoS) to a Tool for Low Orbit Ion Cannon (LOIC) indicates that the tool can be used to perform those DDoS attacks.</td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th colspan='4'><span class='stixtr'>Reverse Relationships</span></th>
  </tr>
  <tr>
    <td width="20%"><span class='stixtype'>indicator</span></td>
    <td width="20%""><span class='stixliteral'>indicates</span></td>
    <td width="20%"><span class='stixtype'>attack-pattern</span></td>
    <td>See forward relationship for definition.</td>
  </tr>
  <tr>
    <td><span class='stixtype'>course-of-action</span></td>
    <td><span class='stixliteral'>mitigates</span></td>
    <td><span class='stixtype'>attack-pattern</span></td>
    <td>See forward relationship for definition.</td>
  </tr>
  <tr>
    <td><span class='stixtype'>campaign</span>, <span class='stixtype'>intrusion-set</span>, <span class='stixtype'>malware</span>, <span class='stixtype'>threat-actor</span></td>
    <td><span class='stixliteral'>uses</span></td>
    <td><span class='stixtype'>attack-pattern</span></td>
    <td>See forward relationship for definition.</td>
  </tr>
</table>

**Examples**

*A generic attack pattern for spear phishing, referencing CAPEC*

```JSON
{
  "type": "attack-pattern",
  "spec_version": "2.1",
  "id": "attack-pattern--0c7b5b88-8ff7-4a4d-aa9d-feb398cd0061",
  "created": "2016-05-12T08:17:27.000Z",
  "modified": "2016-05-12T08:17:27.000Z",
  "name": "Spear Phishing",
  "description": "...",
  "external_references": [
    {
      "source_name": "capec",
      "external_id": "CAPEC-163"
    }
  ]
}
```

*A specific attack pattern for a particular form of spear phishing, referencing CAPEC*

```JSON
[
  {
    "type": "attack-pattern",
    "spec_version": "2.1",
    "id": "attack-pattern--7e33a43e-e34b-40ec-89da-36c9bb2cacd5",
    "created": "2016-05-12T08:17:27.000Z",
    "modified": "2016-05-12T08:17:27.000Z",
    "name": "Spear Phishing as Practiced by Adversary X",
    "description": "A particular form of spear phishing where the attacker claims that the target had won a contest, including personal details, to get them to click on a link.",
    "external_references": [
      {
        "source_name": "capec",
        "external_id": "CAPEC-163"
      }
    ]
  },
  {
    "type": "relationship",
    "spec_version": "2.1",
    "id": "relationship--57b56a43-b8b0-4cba-9deb-34e3e1faed9e",
    "created": "2016-05-12T08:17:27.000Z",
    "modified": "2016-05-12T08:17:27.000Z",
    "relationship_type": "uses",
    "source_ref": "intrusion-set--0c7e22ad-b099-4dc3-b0df-2ea3f49ae2e6",
    "target_ref": "attack-pattern--7e33a43e-e34b-40ec-89da-36c9bb2cacd5"
  },
  {
    "type": "intrusion-set",
    "spec_version": "2.1",
    "id": "intrusion-set--0c7e22ad-b099-4dc3-b0df-2ea3f49ae2e6",
    "created": "2016-05-12T08:17:27.000Z",
    "modified": "2016-05-12T08:17:27.000Z",
    "name": "Adversary X"
  }
]
```

## 4.2 Campaign <a id="campaign"></a>

**Type Name:** <span class="stixtype">campaign</span>

A Campaign is a grouping of adversarial behaviors that describes a set of malicious activities or attacks (sometimes called waves) that occur over a period of time against a specific set of targets. Campaigns usually have well defined objectives and may be part of an Intrusion Set.

Campaigns are often attributed to an intrusion set and threat actors. The threat actors may reuse known infrastructure from the intrusion set or may set up new infrastructure specific for conducting that campaign.

Campaigns can be characterized by their objectives and the incidents they cause, people or resources they target, and the resources (infrastructure, intelligence, Malware, Tools, etc.) they use.

For example, a Campaign could be used to describe a crime syndicate’s attack using a specific variant of malware and new C2 servers against the executives of ACME Bank during the summer of 2016 in order to gain secret information about an upcoming merger with another bank.

### 4.2.1 Properties <a id="campaign-properties"></a>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th><span class='stixtr'>Required Common Properties</span></th>
  </tr>
  <tr>
    <td><strong>type</strong>, <strong>spec_version</strong>, <strong>id</strong>, <strong>created</strong>, <strong>modified</strong></td>
  </tr>
  <tr>
    <th><span class='stixtr'>Optional Common Properties</span></th>
  </tr>
  <tr>
    <td><strong>created_by_ref</strong>, <strong>revoked</strong>, <strong>labels</strong>, <strong>confidence</strong>, <strong>lang</strong>, <strong>external_references</strong>, <strong>object_marking_refs</strong>, <strong>granular_markings</strong>, <strong>extensions</strong></td>
  </tr>
  <tr>
    <th><span class='stixtr'>Not Applicable Common Properties</span></th>
  </tr>
  <tr>
    <td><strong>defanged</strong></td>
  </tr>
  <tr>
    <th><span class='stixtr'>Attack Pattern Specific Properties</span></th>
  </tr>
  <tr>
    <td><strong>name</strong>, <strong>description</strong>, <strong>aliases</strong>, <strong>first_seen</strong>, <strong>last_seen</strong>, <strong>objective</strong></td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6">
  <tr>
    <th><span class='stixtr'>Property Name</span</th>
    <th><span class='stixtr'>Type</span</th>
    <th><span class='stixtr'>Description</span</th>
  </tr>
  <tr>
    <td><strong>type</strong> (required)</td>
    <td><span class="stixtype">string</span></td>
    <td>The value of this property <strong>MUST</strong> be <span class="stixliteral">campaign</span>.</td>
  </tr>
  <tr>
    <td><strong>name</strong> (required)</td>
    <td><span class="stixtype">string</span></td>
    <td>A name used to identify the Campaign.</td>
  </tr>
  <tr>
    <td><strong>description</strong> (optional)</td>
    <td><span class="stixtype">string</span></td>
    <td>A description that provides more details and context about the Campaign, potentially including its purpose and its key characteristics.</td>
  </tr>
  <tr>
    <td><strong>aliases</strong> (optional)</td>
    <td><span style="white-space:nowrap"><span class="stixtype">list</span> of type <span class="stixtype">string</span></span></td>
    <td>Alternative names used to identify this Campaign.</td>
  </tr>
  <tr>
    <td><strong>first_seen</strong> (optional)</td>
    <td><span class="stixtype">timestamp</span></td>
    <td>The time that this Campaign was first seen.<br><br>A summary property of data from sightings and other data that may or may not be available in STIX. If new sightings are received that are earlier than the first seen timestamp, the object may be updated to account for the new data.</td>
  </tr>
  <tr>
    <td><strong>last_seen</strong> (optional)</td>
    <td><span class="stixtype">timestamp</span></td>
    <td>The time that this Campaign was last seen.<br><br>A summary property of data from sightings and other data that may or may not be available in STIX. If new sightings are received that are later than the last seen timestamp, the object may be updated to account for the new data.<br><br>If this property and the <strong>first_seen</strong> property are both defined, then this property <strong>MUST</strong> be greater than or equal to the timestamp in the <strong>first_seen</strong> property.</td>
  </tr>
  <tr>
    <td><strong>objective</strong> (optional)</td>
    <td><span class="stixtype">string</span></td>
    <td>The Campaign’s primary goal, objective, desired outcome, or intended effect — what the Threat Actor or Intrusion Set hopes to accomplish with this Campaign.</td>
  </tr>
</table>

### 4.2.2 Relationships <a id="campaign-relationships"></a>

These are the relationships explicitly defined between the Campaign object and other STIX Objects. The first section lists the embedded relationships by property name along with their corresponding target. The rest of the table identifies the relationships that can be made from this object type to another object type by way of the Relationship object. The reverse relationships section illustrates the relationships targeting this object type from another object type. They are included here for convenience. For their definitions, please see the "Source" object.

Relationships are not restricted to those listed below. Relationships can be created between any objects using the related-to relationship type or, as with open vocabularies, user-defined names.

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th colspan='2'><span class='stixtr'>Embedded Relationships</span></th>
  </tr>
  <tr>
    <td width="50%"><strong>created_by_ref</strong></td>
    <td width="50%"><span class="stixtype">identifier</span> (of type <span class="stixtype">identity</span>)</td>
  </tr>
  <tr>
    <td><strong>object_marking_refs</strong></td>
    <td><span class="stixtype">list</span> of type <span class="stixtype">identifier</span> (of type <span class="stixtype">marking-definition</span>)</td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th><span class='stixtr'>Common Relationships</span></th>
  </tr>
  <tr>
    <td><span class="stixliteral">duplicate-of</span>, <span class="stixliteral">derived-from</span>, <span class="stixliteral">related-to</span></td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6">
  <tr>
    <th width="20%"><span class='stixtr'>Source</span></th>
    <th width="20%""><span class='stixtr'>Relationship Type</span></th>
    <th width="20%"><span class='stixtr'>Target</span></th>
    <th><span class='stixtr'>Description</span></th>
  </tr>
  <tr>
    <td><span class='stixtype'>campaign</span></td>
    <td><span class='stixliteral'>attributed-to</span></td>
    <td><span class='stixtype'>intrusion-set</span>, <span class='stixtype'>threat-actor</span></td>
    <td>This Relationship describes that the Intrusion Set or Threat Actor that is involved in carrying out the Campaign.<br><br>For example, an <span class='stixliteral'>attributed-to</span> Relationship from the Glass Gazelle Campaign to the Urban Fowl Threat Actor means that the actor carried out or was involved in some of the activity described by the Campaign.</td>
  </tr>
  <tr>
    <td><span class='stixtype'>campaign</span></td>
    <td><span class='stixliteral'>compromises</span></td>
    <td><span class='stixtype'>infrastructure</span></td>
    <td>This Relationship describes that the Campaign compromises the related Infrastructure.</td>
  </tr>
  <tr>
    <td><span class='stixtype'>campaign</span></td>
    <td><span class='stixliteral'>originates-from</span></td>
    <td><span class='stixtype'>location</span></td>
    <td>This Relationship describes that the Campaign originates from the related Location.<br><br>For example, an <span class='stixliteral'>originates-from</span> Relationship from the Glass Gazelle Campaign to a Location representing North America means that Glass Gazelle appears to originate from or is located in North America.</td>
  </tr>
  <tr>
    <td><span class='stixtype'>campaign</span></td>
    <td><span class='stixliteral'>targets</span></td>
    <td><span class='stixtype'>identity</span>, <span class='stixtype'>location</span>, <span class='stixtype'>vulnerability</span></td>
    <td>This Relationship describes that the Campaign uses exploits of the related Vulnerability or targets the type of victims described by the related Identity or Location.<br><br>For example, a <span class='stixliteral'>targets</span> Relationship from the Glass Gazelle Campaign to a Vulnerability in a blogging platform indicates that attacks performed as part of Glass Gazelle often exploit that Vulnerability.<br><br>Similarly, a <span class='stixliteral'>targets</span> Relationship from the Glass Gazelle Campaign to an Identity describing the energy sector in the United States means that the Campaign typically carries out attacks against targets in that sector.</td>
  </tr>
  <tr>
    <td><span class='stixtype'>campaign</span></td>
    <td><span class='stixliteral'>uses</span></td>
    <td><span class='stixtype'>attack-pattern</span>, <span class='stixtype'>infrastructure</span>, <span class='stixtype'>malware</span>, <span class='stixtype'>tool</span></td>
    <td>This Relationship describes that attacks carried out as part of the Campaign typically use the related Attack Pattern, Infrastructure, Malware, or Tool.<br><br>For example, a <span class='stixliteral'>uses</span> Relationship from the Glass Gazelle Campaign to the xInject Malware indicates that xInject is often used during attacks attributed to that Campaign.<br><br>A campaign, threat actor, intrusion set, malware, or tool takes infrastructure and compromises and/or uses it for their own.</td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th colspan='4'><span class='stixtr'>Reverse Relationships</span></th>
  </tr>
  <tr>
    <td width="20%"><span class='stixtype'>indicator</span></td>
    <td width="20%""><span class='stixliteral'>indicates</span></td>
    <td width="20%"><span class='stixtype'>campaign</span></td>
    <td>See forward relationship for definition.</td>
  </tr>
</table>

**Example**

```JSON
{
  "type": "campaign",
  "spec_version": "2.1",
  "id": "campaign--8e2e2d2b-17d4-4cbf-938f-98ee46b3cd3f",
  "created_by_ref": "identity--f431f809-377b-45e0-aa1c-6a4751cae5ff",
  "created": "2016-04-06T20:03:00.000Z",
  "modified": "2016-04-06T20:03:00.000Z",
  "name": "Green Group Attacks Against Finance",
  "description": "Campaign by Green Group against a series of targets in the financial services sector."
}
```

## 4.3 Course of Action <a id="course-of-action"></a>

**Type Name:** <span class='stixtype'>course-of-action</span>

> NOTE: The Course of Action object in STIX 2.1 is a stub. It is included to support basic use cases (such as sharing prose courses of action) but does not support the ability to represent automated courses of action or contain properties to represent metadata about courses of action. Future STIX 2 releases will expand it to include these capabilities.

A Course of Action is an action taken either to prevent an attack or to respond to an attack that is in progress. It may describe technical, automatable responses (applying patches, reconfiguring firewalls) but can also describe higher level actions like employee training or policy changes. For example, a course of action to mitigate a vulnerability could describe applying the patch that fixes it.

The Course of Action SDO contains a textual description of the action; a reserved **action** property also serves as a placeholder for future inclusion of machine automatable courses of action.

### 4.3.1 Properties <a id="course-of-action-properties"></a>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th><span class='stixtr'>Required Common Properties</span></th>
  </tr>
  <tr>
    <td><strong>type</strong>, <strong>spec_version</strong>, <strong>id</strong>, <strong>created</strong>, <strong>modified</strong></td>
  </tr>
  <tr>
    <th><span class='stixtr'>Optional Common Properties</span></th>
  </tr>
  <tr>
    <td><strong>created_by_ref</strong>, <strong>revoked</strong>, <strong>labels</strong>, <strong>confidence</strong>, <strong>lang</strong>, <strong>external_references</strong>, <strong>object_marking_refs</strong>, <strong>granular_markings</strong>, <strong>extensions</strong></td>
  </tr>
  <tr>
    <th><span class='stixtr'>Not Applicable Common Properties</span></th>
  </tr>
  <tr>
    <td><strong>defanged</strong></td>
  </tr>
  <tr>
    <th><span class='stixtr'>Attack Pattern Specific Properties</span></th>
  </tr>
  <tr>
    <td><strong>name</strong>, <strong>description</strong>, <strong>action</strong></td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6">
  <tr>
    <th><span class='stixtr'>Property Name</span</th>
    <th><span class='stixtr'>Type</span</th>
    <th><span class='stixtr'>Description</span</th>
  </tr>
  <tr>
    <td><strong>type</strong> (required)</td>
    <td><span class="stixtype">string</span></td>
    <td>The value of this property <strong>MUST</strong> be <span class="stixliteral">course-of-action</span>.</td>
  </tr>
  <tr>
    <td><strong>name</strong> (required)</td>
    <td><span class="stixtype">string</span></td>
    <td>A name used to identify the Course of Action.</td>
  </tr>
  <tr>
    <td><strong>description</strong> (optional)</td>
    <td><span class="stixtype">string</span></td>
    <td>A description that provides more details and context about the Course of Action, potentially including its purpose and its key characteristics.</td>
  </tr>
  <tr>
    <td><strong>action</strong> (optional)</td>
    <td><span class="stixtype">RESERVED</span></td>
    <td>RESERVED - To capture structured/automated courses of action.</td>
  </tr>
</table>

### 4.3.2 Relationships <a id="course-of-action-relationships"></a>

These are the relationships explicitly defined between the Course of Action object and other STIX Objects. The first section lists the embedded relationships by property name along with their corresponding target. The rest of the table identifies the relationships that can be made from this object type to another object type by way of the Relationship object. The reverse relationships section illustrates the relationships targeting this object type from another object type. They are included here for convenience. For their definitions, please see the "Source" object.

Relationships are not restricted to those listed below. Relationships can be created between any objects using the <span class="stixliteral">related-to</span> relationship type or, as with open vocabularies, user-defined names.

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th colspan='2'><span class='stixtr'>Embedded Relationships</span></th>
  </tr>
  <tr>
    <td width="50%"><strong>created_by_ref</strong></td>
    <td width="50%"><span class="stixtype">identifier</span> (of type <span class="stixtype">identity</span>)</td>
  </tr>
  <tr>
    <td><strong>object_marking_refs</strong></td>
    <td><span class="stixtype">list</span> of type <span class="stixtype">identifier</span> (of type <span class="stixtype">marking-definition</span>)</td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th><span class='stixtr'>Common Relationships</span></th>
  </tr>
  <tr>
    <td><span class="stixliteral">duplicate-of</span>, <span class="stixliteral">derived-from</span>, <span class="stixliteral">related-to</span></td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6">
  <tr>
    <th width="20%"><span class='stixtr'>Source</span></th>
    <th width="20%""><span class='stixtr'>Relationship Type</span></th>
    <th width="20%"><span class='stixtr'>Target</span></th>
    <th><span class='stixtr'>Description</span></th>
  </tr>
  <tr>
    <td><span class='stixtype'>course-of-action</span></td>
    <td><span class='stixliteral'>investigates</span></td>
    <td><span class='stixtype'>indicator</span></td>
    <td>This Relationship describes that the Course of Action can be used to investigate the Indicator.</td>
  </tr>
  <tr>
    <td><span class='stixtype'>course-of-action</span></td>
    <td><span class='stixliteral'>mitigates</span></td>
    <td><span class='stixtype'>attack-pattern</span>, <span class='stixtype'>indicator</span>, <span class='stixtype'>malware</span>, <span class='stixtype'>tool</span>, <span class='stixtype'>vulnerability</span></td>
    <td>This Relationship describes that the Course of Action can mitigate (e.g. respond to a threat) the related Attack Pattern, Indicator, Malware, Vulnerability, or Tool.<br><br> For example, a <span class='stixliteral'>mitigates</span> Relationship from a Course of Action object to a Malware object indicates that the course of action mitigates the malware.</td>
  </tr>
  <tr>
    <td><span class='stixtype'>course-of-action</span></td>
    <td><span class='stixliteral'>remediates</span></td>
    <td><span class='stixtype'>malware</span>, <span class='stixtype'>vulnerability</span></td>
    <td>This Relationship describes that the Course of Action can be used to remediate (e.g. clean up) the malware or vulnerability</td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th colspan='4'><span class='stixtr'>Reverse Relationships</span></th>
  </tr>
  <tr>
    <td width="20%">—</td>
    <td width="20%"">—</td>
    <td width="20%">—</td>
    <td>—</td>
  </tr>
</table>

**Example**

```JSON
[
  {
    "type": "course-of-action",
    "spec_version": "2.1",
    "id": "course-of-action--8e2e2d2b-17d4-4cbf-938f-98ee46b3cd3f",
    "created_by_ref": "identity--f431f809-377b-45e0-aa1c-6a4751cae5ff",
    "created": "2016-04-06T20:03:48.000Z",
    "modified": "2016-04-06T20:03:48.000Z",
    "name": "Add TCP port 80 Filter Rule to the existing Block UDP 1434 Filter",
    "description": "This is how to add a filter rule to block inbound access to TCP port 80 to the existing UDP 1434 filter ..."
  },
  {
    "type": "relationship",
    "spec_version": "2.1",
    "id": "relationship--44298a74-ba52-4f0c-87a3-1824e67d7fad",
    "created_by_ref": "identity--f431f809-377b-45e0-aa1c-6a4751cae5ff",
    "created": "2016-04-06T20:07:10.000Z",
    "modified": "2016-04-06T20:07:10.000Z",
    "relationship_type": "mitigates",
    "source_ref": "course-of-action--8e2e2d2b-17d4-4cbf-938f-98ee46b3cd3f",
    "target_ref": "malware--31b940d4-6f7f-459a-80ea-9c1f17b5891b"
  },
  {
    "type": "malware",
    "spec_version": "2.1",
    "id": "malware--31b940d4-6f7f-459a-80ea-9c1f17b5891b",
    "created_by_ref": "identity--f431f809-377b-45e0-aa1c-6a4751cae5ff",
    "created": "2016-04-06T20:07:09.000Z",
    "modified": "2016-04-06T20:07:09.000Z",
    "name": "Poison Ivy",
    ...
  }
]
```

## 4.4 Grouping <a id="grouping"></a>


**Type Name:** <span class="stixtype">grouping</span>

A Grouping object explicitly asserts that the referenced STIX Objects have a shared context, unlike a STIX Bundle (which explicitly conveys no context).
A Grouping object should not be confused with an intelligence product, which should be conveyed via a STIX Report.

A STIX Grouping object might represent a set of data that, in time, given sufficient analysis, would mature to convey an incident or threat report as a STIX Report object.
For example, a Grouping could be used to characterize an ongoing investigation into a security event or incident.
A Grouping object could also be used to assert that the referenced STIX Objects are related to an ongoing analysis process, such as when a threat analyst is collaborating with others in their trust community to examine a series of Campaigns and Indicators.
The Grouping SDO contains a list of references to SDOs, SCOs, SROs, and SMOs, along with an explicit statement of the context shared by the content, a textual description, and the name of the grouping.

### 4.4.1 Properties <a id="grouping-properties"></a>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th><span class='stixtr'>Required Common Properties</span></th>
  </tr>
  <tr>
    <td><strong>type</strong>, <strong>spec_version</strong>, <strong>id</strong>, <strong>created</strong>, <strong>modified</strong></td>
  </tr>
  <tr>
    <th><span class='stixtr'>Optional Common Properties</span></th>
  </tr>
  <tr>
    <td><strong>created_by_ref</strong>, <strong>revoked</strong>, <strong>labels</strong>, <strong>confidence</strong>, <strong>lang</strong>, <strong>external_references</strong>, <strong>object_marking_refs</strong>, <strong>granular_markings</strong>, <strong>extensions</strong></td>
  </tr>
  <tr>
    <th><span class='stixtr'>Not Applicable Common Properties</span></th>
  </tr>
  <tr>
    <td><strong>defanged</strong></td>
  </tr>
  <tr>
    <th><span class='stixtr'>Attack Pattern Specific Properties</span></th>
  </tr>
  <tr>
    <td><strong>name</strong>, <strong>description</strong>, <strong>context</strong>, <strong>object_refs</strong></td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6">
  <tr>
    <th><span class='stixtr'>Property Name</span</th>
    <th><span class='stixtr'>Type</span</th>
    <th><span class='stixtr'>Description</span</th>
  </tr>
  <tr>
    <td><strong>type</strong> (required)</td>
    <td><span class="stixtype">string</span></td>
    <td>The value of this property <strong>MUST</strong> be <span class="stixliteral">grouping</span>.</td>
  </tr>
  <tr>
    <td><strong>name</strong> (required)</td>
    <td><span class="stixtype">string</span></td>
    <td>A name used to identify the Grouping.</td>
  </tr>
  <tr>
    <td><strong>description</strong> (optional)</td>
    <td><span class="stixtype">string</span></td>
    <td>A description that provides more details and context about the Grouping, potentially including its purpose and its key characteristics.</td>
  </tr>
  <tr>
    <td><strong>context</strong> (required)</td>
    <td><span class="stixtype">open-vocab</span></td>
    <td>A short descriptor of the particular context shared by the content referenced by the Grouping.<br><br>The value for this property **SHOULD** come from the <span class="stixliteral"><a href="#grouping-context-vocabulary">grouping-context-ov</a></span> open vocabulary.</td>
  </tr>
  <tr>
    <td><strong>object_refs</strong> (required)</td>
    <td><span style="white-space:nowrap"><span class="stixtype">list</span> of type <span class="stixtype">identifier</span></span></td>
    <td>Specifies the STIX Objects that are referred to by this Grouping.</td>
  </tr>
</table>

### 4.4.2 Relationships <a id="grouping-relationships"></a>

There are no relationships explicitly defined between the Grouping object and other STIX Objects, other than those defined as common relationships. The first section lists the embedded relationships by property name along with their corresponding target.

Relationships are not restricted to those listed below. Relationships can be created between any objects using the <span class="stixliteral">related-to</span> relationship type or, as with open vocabularies, user-defined names.

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th colspan='2'><span class='stixtr'>Embedded Relationships</span></th>
  </tr>
  <tr>
    <td width="50%"><strong>created_by_ref</strong></td>
    <td width="50%"><span class="stixtype">identifier</span> (of type <span class="stixtype">identity</span>)</td>
  </tr>
  <tr>
    <td><strong>object_marking_refs</strong></td>
    <td><span class="stixtype">list</span> of type <span class="stixtype">identifier</span> (of type <span class="stixtype">marking-definition</span>)</td>
  </tr>
  <tr>
    <td><strong>object_refs</strong></td>
    <td><span class="stixtype">list</span> of type <span class="stixtype">identifier</span> (of type STIX Object)</td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th><span class='stixtr'>Common Relationships</span></th>
  </tr>
  <tr>
    <td><span class="stixliteral">duplicate-of</span>, <span class="stixliteral">derived-from</span>, <span class="stixliteral">related-to</span></td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6">
  <tr>
    <th width="20%"><span class='stixtr'>Source</span></th>
    <th width="20%""><span class='stixtr'>Relationship Type</span></th>
    <th width="20%"><span class='stixtr'>Target</span></th>
    <th><span class='stixtr'>Description</span></th>
  </tr>
  <tr>
    <td>—</td>
    <td>—</td>
    <td>—</td>
    <td>—</td>
  </tr>
</table>

**Example**

*A standalone Grouping; the consumer may or may not already have access to the referenced STIX Objects.*

```JSON
{
  "type": "grouping",
  "spec_version": "2.1",
  "id": "grouping--84e4d88f-44ea-4bcd-bbf3-b2c1c320bcb3",
  "created_by_ref": "identity--a463ffb3-1bd9-4d94-b02d-74e4f1658283",
  "created": "2015-12-21T19:59:11.000Z",
  "modified": "2015-12-21T19:59:11.000Z",
  "name": "The Black Vine Cyberespionage Group",
  "description": "A simple collection of Black Vine Cyberespionage Group attributed intel",
  "context": "suspicious-activity",
  "object_refs": [
    "indicator--26ffb872-1dd9-446e-b6f5-d58527e5b5d2",
    "campaign--83422c77-904c-4dc1-aff5-5c38f3a2c55c",
    "relationship--f82356ae-fe6c-437c-9c24-6b64314ae68a",
    "file--0203b5c8-f8b6-4ddb-9ad0-527d727f968b"
  ]
}
```

## 4.5 Identity <a id="identity"></a>


**Type Name:** <span class="stixtype">identity</span>

Identities can represent actual individuals, organizations, or groups (e.g., ACME, Inc.) as well as classes of individuals, organizations, systems or groups (e.g., the finance sector).

The Identity SDO can capture basic identifying information, contact information, and the sectors that the Identity belongs to. Identity is used in STIX to represent, among other things, targets of attacks, information sources, object creators, and threat actor identities.

### 4.5.1 Properties <a id="identity-properties"></a>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th><span class='stixtr'>Required Common Properties</span></th>
  </tr>
  <tr>
    <td><strong>type</strong>, <strong>spec_version</strong>, <strong>id</strong>, <strong>created</strong>, <strong>modified</strong></td>
  </tr>
  <tr>
    <th><span class='stixtr'>Optional Common Properties</span></th>
  </tr>
  <tr>
    <td><strong>created_by_ref</strong>, <strong>revoked</strong>, <strong>labels</strong>, <strong>confidence</strong>, <strong>lang</strong>, <strong>external_references</strong>, <strong>object_marking_refs</strong>, <strong>granular_markings</strong>, <strong>extensions</strong></td>
  </tr>
  <tr>
    <th><span class='stixtr'>Not Applicable Common Properties</span></th>
  </tr>
  <tr>
    <td><strong>defanged</strong></td>
  </tr>
  <tr>
    <th><span class='stixtr'>Attack Pattern Specific Properties</span></th>
  </tr>
  <tr>
    <td><strong>name</strong>, <strong>description</strong>, <strong>roles</strong>, <strong>identity_class</strong>, <strong>sectors</strong>, <strong>contact_information</strong></td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6">
  <tr>
    <th><span class='stixtr'>Property Name</span</th>
    <th><span class='stixtr'>Type</span</th>
    <th><span class='stixtr'>Description</span</th>
  </tr>
  <tr>
    <td><strong>type</strong> (required)</td>
    <td><span class="stixtype">string</span></td>
    <td>The value of this property <strong>MUST</strong> be <span class="stixliteral">identity</span>.</td>
  </tr>
  <tr>
    <td><strong>name</strong> (required)</td>
    <td><span class="stixtype">string</span></td>
    <td>A name used to identify the Identity.  When referring to a specific entity (e.g., an individual or organization), this property <strong>SHOULD</strong> contain the canonical name of the specific entity.</td>
  </tr>
  <tr>
    <td><strong>description</strong> (optional)</td>
    <td><span class="stixtype">string</span></td>
    <td>A description that provides more details and context about the Identity, potentially including its purpose and its key characteristics.</td>
  </tr>
  <tr>
    <td><strong>roles</strong> (optional)</td>
    <td><span style="white-space:nowrap"><span class="stixtype">list</span> of type <span class="stixtype">string</span></span></td>
    <td>The list of roles that this Identity performs (e.g., CEO, Domain Administrators, Doctors, Hospital, or Retailer). No open vocabulary is yet defined for this property.</td>
  </tr>
  <tr>
    <td><strong>identity_class</strong> (optional)</td>
    <td><span class="stixtype">open-vocab</span></td>
    <td>The type of entity that this Identity describes, e.g., an individual or organization.<br><br>The value for this property <strong>SHOULD</strong> come from the <span style="white-space:nowrap"><span class="stixliteral"><a href="#identity-class-vocabulary">identity-class-ov</a></span></span> open vocabulary.</td>
  </tr>
  <tr>
    <td><strong>sectors</strong> (optional)</td>
    <td><span style="white-space:nowrap"><span class="stixtype">list</span> of type <span class="stixtype">open-vocab</span></span></td>
    <td>The list of industry sectors that this Identity belongs to.<br><br>The value for this property <strong>SHOULD</strong> come from the <span style="white-space:nowrap"><span class="stixliteral"><a href="#industry-sector-vocabulary">industry-sector-ov</a></span></span> open vocabulary.</td>
  </tr>
  <tr>
    <td><strong>contact_information</strong> (optional)</td>
    <td><span class="stixtype">string</span></td>
    <td>The contact information (e-mail, phone number, etc.) for this Identity. No format for this information is currently defined by this specification.</td>
  </tr>
</table>

### 4.5.2 Relationships <a id="identity-relationships"></a>

These are the relationships explicitly defined between the Identity object and other STIX Objects. The first section lists the embedded relationships by property name along with their corresponding target. The rest of the table identifies the relationships that can be made from this object type to another object type by way of the Relationship object. The reverse relationships section illustrates the relationships targeting this object type from another object type. They are included here for convenience. For their definitions, please see the "Source" object.

Relationships are not restricted to those listed below. Relationships can be created between any objects using the <span class="stixliteral">related-to</span> relationship type or, as with open vocabularies, user-defined names.

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th colspan='2'><span class='stixtr'>Embedded Relationships</span></th>
  </tr>
  <tr>
    <td width="50%"><strong>created_by_ref</strong></td>
    <td width="50%"><span class="stixtype">identifier</span> (of type <span class="stixtype">identity</span>)</td>
  </tr>
  <tr>
    <td><strong>object_marking_refs</strong></td>
    <td><span class="stixtype">list</span> of type <span class="stixtype">identifier</span> (of type <span class="stixtype">marking-definition</span>)</td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th><span class='stixtr'>Common Relationships</span></th>
  </tr>
  <tr>
    <td><span class="stixliteral">duplicate-of</span>, <span class="stixliteral">derived-from</span>, <span class="stixliteral">related-to</span></td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6">
  <tr>
    <th width="20%"><span class='stixtr'>Source</span></th>
    <th width="20%""><span class='stixtr'>Relationship Type</span></th>
    <th width="20%"><span class='stixtr'>Target</span></th>
    <th><span class='stixtr'>Description</span></th>
  </tr>
  <tr>
    <td><span class='stixtype'>identity</span></td>
    <td><span class='stixliteral'>located-at</span></td>
    <td><span class='stixtype'>location</span></td>
    <td>This Relationship describes that the Identity is located at or in the related Location.<br><br>For example, a located-at relationship from the ACME Corporation to a Location representing the United States means that ACME Corporation is located in the United States.</td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th colspan='4'><span class='stixtr'>Reverse Relationships</span></th>
  </tr>
  <tr>
    <td width="20%"><span class='stixtype'>attack-pattern</span>, <span class='stixtype'>campaign</span>, <span class='stixtype'>intrusion-set</span>, <span class='stixtype'>malware</span>, <span class='stixtype'>threat-actor</span>, <span class='stixtype'>tool</td>
    <td width="20%""><span class='stixliteral'>targets</span></td>
    <td width="20%"><span class='stixtype'>identity</span></td>
    <td>See forward relationship for definition.</td>
  </tr>
  <tr>
    <td><span class='stixtype'>threat-actor</span></td>
    <td><span class='stixliteral'>attributed-to</span>, <span class='stixliteral'>impersonates</span></td>
    <td><span class='stixtype'>identity</span></td>
    <td>See forward relationship for definition.</td>
  </tr>
</table>

**Examples**

*An Identity for an individual named John Smith*

```JSON
{
  "type": "identity",
  "spec_version": "2.1",
  "id": "identity--023d105b-752e-4e3c-941c-7d3f3cb15e9e",
  "created_by_ref": "identity--f431f809-377b-45e0-aa1c-6a4751cae5ff",
  "created": "2016-04-06T20:03:00.000Z",
  "modified": "2016-04-06T20:03:00.000Z",
  "name": "John Smith",
  "identity_class": "individual"
}
```

*An Identity for a company named ACME Widget, Inc.*

```JSON
{
  "type": "identity",
  "spec_version": "2.1",
  "id": "identity--e5f1b90a-d9b6-40ab-81a9-8a29df4b6b65",
  "created_by_ref": "identity--f431f809-377b-45e0-aa1c-6a4751cae5ff",
  "created": "2016-04-06T20:03:00.000Z",
  "modified": "2016-04-06T20:03:00.000Z",
  "name": "ACME Widget, Inc.",
  "identity_class": "organization"
}
```

## 4.6 Incident <a id="incident"></a>

**Type Name:** <span class="stixtype">incident</span>

> NOTE: The Incident object in STIX 2.1 is a stub. It is included to support basic use cases but does not contain properties to represent metadata about incidents. Future STIX 2 releases will expand it to include these capabilities. It is suggested that it is used as an extension point for an Incident object defined using the extension facility described in [section 7.3](#extension-definition).

### 4.6.1 Properties <a id="incident-properties"></a>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th><span class='stixtr'>Required Common Properties</span></th>
  </tr>
  <tr>
    <td><strong>type</strong>, <strong>spec_version</strong>, <strong>id</strong>, <strong>created</strong>, <strong>modified</strong></td>
  </tr>
  <tr>
    <th><span class='stixtr'>Optional Common Properties</span></th>
  </tr>
  <tr>
    <td><strong>created_by_ref</strong>, <strong>revoked</strong>, <strong>labels</strong>, <strong>confidence</strong>, <strong>lang</strong>, <strong>external_references</strong>, <strong>object_marking_refs</strong>, <strong>granular_markings</strong>, <strong>extensions</strong></td>
  </tr>
  <tr>
    <th><span class='stixtr'>Not Applicable Common Properties</span></th>
  </tr>
  <tr>
    <td><strong>defanged</strong></td>
  </tr>
  <tr>
    <th><span class='stixtr'>Attack Pattern Specific Properties</span></th>
  </tr>
  <tr>
    <td><strong>name</strong>, <strong>description</strong></td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6">
  <tr>
    <th><span class='stixtr'>Property Name</span</th>
    <th><span class='stixtr'>Type</span</th>
    <th><span class='stixtr'>Description</span</th>
  </tr>
  <tr>
    <td><strong>type</strong> (required)</td>
    <td><span class="stixtype">string</span></td>
    <td>The value of this property <strong>MUST</strong> be <span class="stixliteral">incident</span>.</td>
  </tr>
  <tr>
    <td><strong>name</strong> (required)</td>
    <td><span class="stixtype">string</span></td>
    <td>A name used to identify the Incident.</td>
  </tr>
  <tr>
    <td><strong>description</strong> (optional)</td>
    <td><span class="stixtype">string</span></td>
    <td>A description that provides more details and context about the Incident, potentially including its purpose and its key characteristics.</td>
  </tr>
</table>

### 4.6.2 Relationships <a id="incident-relationships"></a>

These are the relationships explicitly defined between the Incident object and other STIX Objects. The first section lists the embedded relationships by property name along with their corresponding target. The rest of the table identifies the relationships that can be made from this object type to another object type by way of the Relationship object. The reverse relationships section illustrates the relationships targeting this object type from another object type. They are included here for convenience. For their definitions, please see the "Source" object.

Relationships are not restricted to those listed below. Relationships can be created between any objects using the <span class="stixliteral">related-to</span> relationship type or, as with open vocabularies, user-defined names.

This table is left intentionally blank and will be fleshed out in a future release.

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th colspan='2'><span class='stixtr'>Embedded Relationships</span></th>
  </tr>
  <tr>
    <td width="50%"><strong>created_by_ref</strong></td>
    <td width="50%"><span class="stixtype">identifier</span> (of type <span class="stixtype">identity</span>)</td>
  </tr>
  <tr>
    <td><strong>object_marking_refs</strong></td>
    <td><span class="stixtype">list</span> of type <span class="stixtype">identifier</span> (of type <span class="stixtype">marking-definition</span>)</td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th><span class='stixtr'>Common Relationships</span></th>
  </tr>
  <tr>
    <td><span class="stixliteral">duplicate-of</span>, <span class="stixliteral">derived-from</span>, <span class="stixliteral">related-to</span></td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6">
  <tr>
    <th width="20%"><span class='stixtr'>Source</span></th>
    <th width="20%""><span class='stixtr'>Relationship Type</span></th>
    <th width="20%"><span class='stixtr'>Target</span></th>
    <th><span class='stixtr'>Description</span></th>
  </tr>
  <tr>
    <td>—</td>
    <td>—</td>
    <td>—</td>
    <td>—</td>
  </tr>
</table>

**Example**

```JSON
{
  "type": "incident",
  "spec_version": "2.1",
  "id": "incident--8e2e2d2b-17d4-4cbf-938f-98ee46b3cd3f",
  "created_by_ref": "identity--f431f809-377b-45e0-aa1c-6a4751cae5ff",
  "created": "2016-04-06T20:03:48.000Z",
  "modified": "2016-04-06T20:03:48.000Z",
  "name": "Incident 43",
  "description": "This incident addresses APT 28 ..."
}
```

## 4.7 Indicator <a id="indicator"></a>

**Type Name:** <span class="stixtype">indicator</span>

Indicators contain a pattern that can be used to detect suspicious or malicious cyber activity. For example, an Indicator may be used to represent a set of malicious domains and use the STIX Patterning Language (see [section 9](#stix-patterning)) to specify these domains.

The Indicator SDO contains a simple textual description, the Kill Chain Phases that it detects behavior in, a time window for when the Indicator is valid or useful, and a required **pattern** property to capture a structured detection pattern. Conforming STIX implementations **MUST** support the STIX Patterning Language as defined in [section 9](#stix-patterning).

Relationships from the Indicator can describe the malicious or suspicious behavior that it directly detects (Malware, Tool, and Attack Pattern). In addition, it may also imply the presence of a Campaigns, Intrusion Sets, and Threat Actors, etc.

### 4.7.1 Properties <a id="indicator-properties"></a>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th><span class='stixtr'>Required Common Properties</span></th>
  </tr>
  <tr>
    <td><strong>type</strong>, <strong>spec_version</strong>, <strong>id</strong>, <strong>created</strong>, <strong>modified</strong></td>
  </tr>
  <tr>
    <th><span class='stixtr'>Optional Common Properties</span></th>
  </tr>
  <tr>
    <td><strong>created_by_ref</strong>, <strong>revoked</strong>, <strong>labels</strong>, <strong>confidence</strong>, <strong>lang</strong>, <strong>external_references</strong>, <strong>object_marking_refs</strong>, <strong>granular_markings</strong>, <strong>extensions</strong></td>
  </tr>
  <tr>
    <th><span class='stixtr'>Not Applicable Common Properties</span></th>
  </tr>
  <tr>
    <td><strong>defanged</strong></td>
  </tr>
  <tr>
    <th><span class='stixtr'>Attack Pattern Specific Properties</span></th>
  </tr>
  <tr>
    <td><strong>name</strong>, <strong>description</strong>, <strong>indicator_types</strong>, <strong>pattern</strong>, <strong>pattern_type</strong>, <strong>pattern_version</strong>, <strong>valid_from</strong>, <strong>valid_until</strong>, <strong>kill_chain_phases</strong></td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6">
  <tr>
    <th><span class='stixtr'>Property Name</span</th>
    <th><span class='stixtr'>Type</span</th>
    <th><span class='stixtr'>Description</span</th>
  </tr>
  <tr>
    <td><strong>type</strong> (required)</td>
    <td><span class="stixtype">string</span></td>
    <td>The value of this property <strong>MUST</strong> be <span class="stixliteral">indicator</span>.</td>
  </tr>
  <tr>
    <td><strong>name</strong> (optional)</td>
    <td><span class="stixtype">string</span></td>
    <td>A name used to identify the Indicator.<br><br>Producers <strong>SHOULD</strong> provide this property to help products and analysts understand what this Indicator actually does.</td>
  </tr>
  <tr>
    <td><strong>description</strong> (optional)</td>
    <td><span class="stixtype">string</span></td>
    <td>A description that provides more details and context about the Indicator, potentially including its purpose and its key characteristics.<br><br>Producers <strong>SHOULD</strong> provide this property to help products and analysts understand what this Indicator actually does.</td>
  </tr>
  <tr>
    <td><strong>indicator_types</strong> (optional)</td>
    <td><span style="white-space:nowrap"><span class="stixtype">list</span> of type <span class="stixtype">open-vocab</span></span></td>
    <td>A set of categorizations for this indicator.<br><br>The values for this property SHOULD come from the <span style="white-space:nowrap"><span class="stixliteral"><a href="#indicator-type-vocabulary">indicator-type-ov</a></span></span> open vocabulary.</td>
  </tr>
  <tr>
    <td><strong>pattern</strong> (required)</td>
    <td><span class="stixtype">string</span></td>
    <td>The detection pattern for this Indicator <strong>MAY</strong> be expressed as a STIX Pattern as specified in <a href="#stix-patterning">section 9</a> or another appropriate language such as SNORT, YARA, etc.</td>
  </tr>
  <tr>
    <td><strong>pattern_type</strong> (required)</td>
    <td><span class="stixtype">open-vocab</span></td>
    <td>The pattern language used in this indicator.<br><br>The value for this property <strong>SHOULD</strong> come from the <span style="white-space:nowrap"><span class="stixliteral"><a href="#indicator-pattern-type-vocabulary">indicator-pattern-type-ov</a></span></span> open vocabulary.<br><br>The value of this property MUST match the type of pattern data included in the pattern property.</td>
  </tr>
  <tr>
    <td><strong>pattern_version</strong> (optional)</td>
    <td><span class="stixtype">string</span></td>
    <td>The version of the pattern language that is used for the data in the <strong>pattern</strong> property which <strong>MUST</strong> match the type of pattern data included in the <strong>pattern</strong> property.<br><br>For patterns that do not have a formal specification, the build or code version that the pattern is known to work with <strong>SHOULD</strong> be used.<br><br>For the STIX Pattern language, the default value is determined by the specification version of the object.<br><br>For other languages, the default value <strong>SHOULD</strong> be the latest version of the patterning language at the time of this object’s creation.</td>
  </tr>
  <tr>
    <td><strong>valid_from</strong> (required)</td>
    <td><span class="stixtype">timestamp</span></td>
    <td>The time from which this Indicator is considered a valid indicator of the behaviors it is related or represents.</td>
  </tr>
  <tr>
    <td><strong>valid_until</strong> (optional)</td>
    <td><span class="stixtype">timestamp</span></td>
    <td>The time at which this Indicator should no longer be considered a valid indicator of the behaviors it is related to or represents.<br><br>If the <strong>valid_until</strong> property is omitted, then there is no constraint on the latest time for which the Indicator is valid.<br><br>This <strong>MUST</strong> be greater than the timestamp in the <strong>valid_from</strong> property.</td>
  </tr>
  <tr>
    <td><strong>kill_chain_phases</strong> (optional)</td>
    <td><span style="white-space:nowrap"><span class="stixtype">list</span> of type <span class="stixtype">kill-chain-phase</span></span></td>
    <td>The kill chain phase(s) to which this Indicator corresponds.</td>
  </tr>
</table>

### 4.7.2 Relationships <a id="indicator-relationships"></a>

These are the relationships explicitly defined between the Indicator object and other STIX Objects. The first section lists the embedded relationships by property name along with their corresponding target. The rest of the table identifies the relationships that can be made from this object type to another object type by way of the Relationship object. The reverse relationships section illustrates the relationships targeting this object type from another object type. They are included here for convenience. For their definitions, please see the "Source" object.

Relationships are not restricted to those listed below. Relationships can be created between any objects using the related-to relationship type or, as with open vocabularies, user-defined names.

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th colspan='2'><span class='stixtr'>Embedded Relationships</span></th>
  </tr>
  <tr>
    <td width="50%"><strong>created_by_ref</strong></td>
    <td width="50%"><span class="stixtype">identifier</span> (of type <span class="stixtype">identity</span>)</td>
  </tr>
  <tr>
    <td><strong>object_marking_refs</strong></td>
    <td><span class="stixtype">list</span> of type <span class="stixtype">identifier</span> (of type <span class="stixtype">marking-definition</span>)</td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th><span class='stixtr'>Common Relationships</span></th>
  </tr>
  <tr>
    <td><span class="stixliteral">duplicate-of</span>, <span class="stixliteral">derived-from</span>, <span class="stixliteral">related-to</span></td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6">
  <tr>
    <th width="20%"><span class='stixtr'>Source</span></th>
    <th width="20%""><span class='stixtr'>Relationship Type</span></th>
    <th width="20%"><span class='stixtr'>Target</span></th>
    <th><span class='stixtr'>Description</span></th>
  </tr>
  <tr>
    <td><span class='stixtype'>indicator</span></td>
    <td><span class='stixliteral'>indicates</span></td>
    <td><span class='stixtype'>attack-pattern</span>, <span class='stixtype'>campaign</span>, <span class='stixtype'>infrastructure</span>, <span class='stixtype'>intrusion-set</span>, <span class='stixtype'>malware</span>, <span class='stixtype'>threat-actor</span>, <span class='stixtype'>tool</span></td>
    <td>This Relationship describes that the Indicator can detect evidence of the related Attack Pattern, Campaign, Infrastructure, Intrusion Set, Malware, Threat Actor, or Tool. This evidence may not be direct: for example, the Indicator may detect secondary evidence of the Campaign, such as malware or behavior commonly used by that Campaign.<br><br>For example, an <span class='stixliteral'>indicates</span> Relationship from an Indicator to a Campaign object representing Glass Gazelle means that the Indicator is capable of detecting evidence of Glass Gazelle, such as command and control IPs commonly used by that Campaign.</td>
  </tr>
  <tr>
    <td><span class='stixtype'>indicator</span></td>
    <td><span class='stixliteral'>based-on</span></td>
    <td><span class='stixtype'>observed-data</span></td>
    <td>This relationship describes that the indicator was created based on information from an <span class='stixtype'>observed-data</span> object.<br><br>For example, an indicator may be created based upon the observation of a spearphishing email or created based upon analysis performed on a piece of malware or adversary infrastructure.</td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th colspan='4'><span class='stixtr'>Reverse Relationships</span></th>
  </tr>
  <tr>
    <td width="20%"><span class='stixtype'>course-of-action</td>
    <td width="20%""><span class='stixliteral'>investigates</span>, <span class='stixliteral'>mitigates</span></td>
    <td width="20%"><span class='stixtype'>indicastor</span></td>
    <td>See forward relationship for definition.</td>
  </tr>
</table>

**Example**

*Indicator itself, with context*

```JSON
[
  {
    "type": "indicator",
    "spec_version": "2.1",
    "id": "indicator--8e2e2d2b-17d4-4cbf-938f-98ee46b3cd3f",
    "created_by_ref": "identity--f431f809-377b-45e0-aa1c-6a4751cae5ff",
    "created": "2016-04-06T20:03:48.000Z",
    "modified": "2016-04-06T20:03:48.000Z",
    "indicator_types": ["malicious-activity"],
    "name": "Poison Ivy Malware",
    "description": "This file is part of Poison Ivy",
    "pattern": "[ file:hashes.'SHA-256' = '4bac27393bdd9777ce02453256c5577cd02275510b2227f473d03f533924f877' ]",
    "pattern_type": "stix",
    "valid_from": "2016-01-01T00:00:00Z"
  },
  {
    "type": "relationship",
    "spec_version": "2.1",
    "id": "relationship--44298a74-ba52-4f0c-87a3-1824e67d7fad",
    "created_by_ref": "identity--f431f809-377b-45e0-aa1c-6a4751cae5ff",
    "created": "2016-04-06T20:06:37.000Z",
    "modified": "2016-04-06T20:06:37.000Z",
    "relationship_type": "indicates",
    "source_ref": "indicator--8e2e2d2b-17d4-4cbf-938f-98ee46b3cd3f",
    "target_ref": "malware--31b940d4-6f7f-459a-80ea-9c1f17b5891b"
  },
  {
    "type": "malware",
    "spec_version": "2.1",
    "id": "malware--31b940d4-6f7f-459a-80ea-9c1f17b5891b",
    "is_family": true,
    "created": "2016-04-06T20:07:09.000Z",
    "modified": "2016-04-06T20:07:09.000Z",
    "created_by_ref": "identity--f431f809-377b-45e0-aa1c-6a4751cae5ff",
    "name": "Poison Ivy",
    "malware_types": ["trojan"]
  }
]
```

## 4.8 Infrastructure <a id="infrastructure"></a>

**Type Name:** <span class="stixtype">infrastructure</span>

The Infrastructure SDO represents a type of TTP and describes any systems, software services and any associated physical or virtual resources intended to support some purpose (e.g., C2 servers used as part of an attack, device or server that are part of defense, database servers targeted by an attack, etc.).
While elements of an attack can be represented by other SDOs or SCOs, the Infrastructure SDO represents a named group of related data that constitutes the infrastructure.

### 4.8.1 Properties <a id="infrastructure-properties"></a>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th><span class="stixtr">Required Common Properties</span></th>
  </tr>
  <tr>
    <td><strong>type</strong>, <strong>spec_version</strong>, <strong>id</strong>, <strong>created</strong>, <strong>modified</strong></td>
  </tr>
  <tr>
    <th><span class="stixtr">Optional Common Properties></span></th>
  </tr>
  <tr>
    <td><strong>created_by_ref</strong>, <strong>revoked</strong>, <strong>labels</strong>, <strong>confidence</strong>, <strong>lang</strong>, <strong>external_references</strong>, <strong>object_marking_refs</strong>, <strong>granular_markings</strong>, <strong>extensions</strong></td>
  </tr>
  <tr>
    <th><span class="stixtr">Not Applicable Common Properties</span></th>
  </tr>
  <tr>
    <td><strong>defanged</strong></td>
  </tr>
  <tr>
    <th><span class="stixtr">Infrastructure Specific Properties</span></th>
  </tr>
  <tr>
    <td><strong>name</strong>, <strong>description</strong>, <strong>infrastructure_types</strong>, <strong>aliases</strong>, <strong>kill_chain_phases</strong>, <strong>first_seen</strong>, <strong>last_seen</strong></td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6">
  <tr>
    <th><span class="stixtr">Property Name</span></th>
    <th><span class="stixtr">Type</span></th>
    <th><span class="stixtr">Description</span></th>
  </tr>
  <tr>
    <td><strong>type</strong> (required)</td>
    <td><span class="stixtype">string</span></td>
    <td>The value of this property <strong>MUST</strong> be <span class="stixliteral">infrastructure</span>.</td>
  </tr>
  <tr>
    <td><strong>name</strong> (required)</td>
    <td><span class="stixtype">string</span></td>
    <td>A name or characterizing text used to identify the Infrastructure.</td>
  </tr>
  <tr>
    <td><strong>description</strong> (optional)</td>
    <td><span class="stixtype">string</span></td>
    <td>A description that provides more details and context about the Infrastructure, potentially including its purpose, how it is being used, how it relates to other intelligence activities captured in related objects, and its key characteristics.</td>
  </tr>
  <tr>
    <td><strong>infrastructure_types</strong> (optional)</td>
    <td><span style="white-space:nowrap"><span class="stixtype">list</span> of type <span class="stixtype">open-vocab</span></span></td>
    <td>The type of infrastructure being described.<br><br>The values for this property <strong>SHOULD</strong> come from the <a href="#infrastructure-type-vocabulary"><span class="stixliteral">infrastructure-type-ov</span></a> open vocabulary.</td>
  </tr>
  <tr>
    <td><strong>aliases</strong> (optional)</td>
    <td><span style="white-space:nowrap"><span class="stixtype">list</span> of type <span class="stixtype">string</span></span></td>
    <td>Alternative names used to identify this Infrastructure.</td>
  </tr>
  <tr>
    <td><strong>kill_chain_phases</strong> (optional)</td>
    <td><span style="white-space:nowrap"><span class="stixtype">list</span> of type <span class="stixtype">kill-chain-phase</span></span></td>
    <td>The list of Kill Chain Phases for which this Infrastructure is used.</td>
  </tr>
  <tr>
    <td><strong>first_seen</strong> (optional)</td>
    <td><span class="stixtype">timestamp</span></td>
    <td>The time that this Infrastructure was first seen performing malicious activities.</td>
  </tr>
  <tr>
    <td><strong>last_seen</strong> (optional)</td>
    <td><span class="stixtype">timestamp</span></td>
    <td>The time that this Infrastructure was last seen performing malicious activities.<br><br>If this property and the <strong>first_seen</strong> property are both defined, then this property <strong>MUST</strong> be greater than or equal to the timestamp in the <strong>first_seen</strong> property.</td>
  </tr>
</table>

### 4.8.2 Relationships <a id="infrastructure-relationships"></a>

These are the relationships explicitly defined between the Infrastructure object and other STIX Objects. The first section lists the embedded relationships by property name along with their corresponding target. The rest of the table identifies the relationships that can be made from this object type to another object type by way of the Relationship object. The reverse relationships section illustrates the relationships targeting this object type from another object type. They are included here for convenience. For their definitions, please see the "Source" object.

Relationships are not restricted to those listed below. Relationships can be created between any objects using the related-to relationship type or, as with open vocabularies, user-defined names.

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th colspan='2'><span class='stixtr'>Embedded Relationships</span></th>
  </tr>
  <tr>
    <td width="50%"><strong>created_by_ref</strong></td>
    <td width="50%"><span class="stixtype">identifier</span> (of type <span class="stixtype">identity</span>)</td>
  </tr>
  <tr>
    <td><strong>object_marking_refs</strong></td>
    <td><span class="stixtype">list</span> of type <span class="stixtype">identifier</span> (of type <span class="stixtype">marking-definition</span>)</td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th><span class='stixtr'>Common Relationships</span></th>
  </tr>
  <tr>
    <td><span class="stixliteral">duplicate-of</span>, <span class="stixliteral">derived-from</span>, <span class="stixliteral">related-to</span></td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6">
  <tr>
    <th width="20%"><span class='stixtr'>Source</span></th>
    <th width="20%""><span class='stixtr'>Relationship Type</span></th>
    <th width="20%"><span class='stixtr'>Target</span></th>
    <th><span class='stixtr'>Description</span></th>
  </tr>
  <tr>
    <td><span class="stixtype">infrastructure</span></td>
    <td><span class="stixliteral">communicates-with</span></td>
    <td><span class="stixtype">infrastructure</span>, <span class="stixtype">ipv4-addr</span>, <span class="stixtype">ipv6-addr</span>, <span class="stixtype">domain-name</span>, <span class="stixtype">url</span></td>
    <td>This Relationship documents that this infrastructure instance communicates with the defined network addressable resource.<br><br>For example, a botnet could communicate with a crypto-currency mining pool. This does not mean that the pool is a part of this infrastructure.</td>
  </tr>
  <tr>
    <td><span class="stixtype">infrastructure</span></td>
    <td><span class="stixliteral">consists-of</span></td>
    <td><span class="stixtype">infrastructure</span>, <span class="stixtype">observed-data</span>, <span class="stixtype">&ltAll <em>STIX Cyber-observable Objects</em>&gt</span></td>
    <td>This Relationship documents the objects that are used to make up an infrastructure instance, such as <span class="stixtype">ipv4-addr</span>, <span class="stixtype">ipv6-addr</span>, <span class="stixtype">domain-name</span>, <span class="stixtype">url</span>. An infrastructure instance consists of zero or more objects.<br><br>While not all SCO types will make sense as infrastructure, allowing any type of SCO prevents artificially restricting what could be used.</td>
  </tr>
  <tr>
    <td><span class="stixtype">infrastructure</span></td>
    <td><span class="stixliteral">controls</span></td>
    <td><span class="stixtype">infrastructure</span>, <span class="stixtype">malware</span></td>
    <td>This Relationship describes that this infrastructure controls some other infrastructure or a malware instance (or family).</td>
  </tr>
  <tr>
    <td><span class="stixtype">infrastructure</span></td>
    <td><span class="stixliteral">delivers</span></td>
    <td><span class="stixtype">malware</span></td>
    <td>This Relationship describes that this infrastructure is used to actively deliver a malware instance (or family).</td>
  </tr>
  <tr>
    <td><span class="stixtype">infrastructure</span></td>
    <td><span class="stixliteral">has</span></td>
    <td><span class="stixtype">vulnerability</span></td>
    <td>This Relationship describes that this specific Infrastructure has this specific Vulnerability.<br><br>For example, a web server may not have been patched and currently is impacted by a CVE.</td>
  </tr>
  <tr>
    <td><span class="stixtype">infrastructure</span></td>
    <td><span class="stixliteral">hosts</span></td>
    <td><span class="stixtype">tool</span>, <span class="stixtype">malware</span></td>
    <td>This Relationship describes that this infrastructure has a tool running on it or is used to passively host the tool / malware.<br><br>For example, an SSH server may be hosted on a piece of infrastructure.</td>
  </tr>
  <tr>
    <td><span class="stixtype">infrastructure</span></td>
    <td><span class="stixliteral">located-at</span></td>
    <td><span class="stixtype">location</span></td>
    <td>This Relationship describes that the infrastructure originates from the related location.<br><br>For example, a <span class="stixliteral">located-at</span> relationship from the Red Orca C2 infrastructure to a Location representing North America means that the Red Orca C2 Infrastructure appears to originate from or is located in North America.</td>
  </tr>
  <tr>
    <td><span class="stixtype">infrastructure</span></td>
    <td><span class="stixliteral">uses</span></td>
    <td><span class="stixtype">infrastructure</span></td>
    <td>This Relationship describes that this infrastructure uses this other infrastructure to achieve its objectives.</td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th colspan='4'><span class='stixtr'>Reverse Relationships</span></th>
  </tr>
  <tr>
    <td width="20%"><span class="stixtype">campaign</span>, <span class="stixtype">intrusion-set</span>, <span class="stixtype">threat-actor</span></td>
    <td width="20%"><span class="stixliteral">compromises</span></td>
    <td width="20%"><span class="stixtype">infrastructure</span></td>
    <td>See forward relationship for definition.</td>
  </tr>
  <tr>
    <td><span class="stixtype">malware</span></td>
    <td><span class="stixliteral">beacons-to</span>, <span class="stixliteral">exfiltrates-to</span></td>
    <td><span class="stixtype">infrastructure</span></td>
    <td>See forward relationship for definition.</td>
  </tr>
  <tr>
    <td><span class="stixtype">intrusion-set</span>, <span class="stixtype">threat-actor</span></td>
    <td><span class="stixliteral">hosts</span></td>
    <td><span class="stixtype">infrastructure</span></td>
    <td>See forward relationship for definition.</td>
  </tr>
  <tr>
    <td><span class="stixtype">indicator</span></td>
    <td><span class="stixliteral">indicates</span></td>
    <td><span class="stixtype">infrastructure</span></td>
    <td>See forward relationship for definition.</td>
  </tr>
  <tr>
    <td><span class="stixtype">intrusion-set</span>, <span class="stixtype">threat-actor</span></td>
    <td><span class="stixliteral">owns</span></td>
    <td><span class="stixtype">infrastructure</span></td>
    <td>See forward relationship for definition.</td>
  </tr>
  <tr>
    <td><span class="stixtype">malware</span>, <span class="stixtype">tool</span></td>
    <td><span class="stixliteral">targets</span></td>
    <td><span class="stixtype">infrastructure</span></td>
    <td>See forward relationship for definition.</td>
  </tr>
  <tr>
    <td><span class="stixtype">campaign</span>, <span class="stixtype">intrusion-set</span>, <span class="stixtype">malware</span>, <span class="stixtype">threat-actor</span>, <span class="stixtype">tool</span></td>
    <td><span class="stixliteral">uses</span></td>
    <td><span class="stixtype">infrastructure</span></td>
    <td>See forward relationship for definition.</td>
  </tr>
</table>

**Example (additional example can be found in [Appendix C](#additional-examples))**

*Malware C2 Infrastructure*

<img src="images/malware_c2_infrastructure.png" alt="C2 Infrastructure"  width="50%">

```JSON
[
  {
    "type":"infrastructure",
    "spec_version": "2.1",
    "id":"infrastructure--38c47d93-d984-4fd9-b87b-d69d0841628d",
    "created":"2016-05-07T11:22:30.000Z",
    "modified":"2016-05-07T11:22:30.000Z",
    "name":"Poison Ivy C2",
    "infrastructure_types": ["command-and-control"]
  },
  {
    "type": "relationship",
    "spec_version": "2.1",
    "id": "relationship--7aebe2f0-28d6-48a2-9c3e-b0aaa60266ed",
    "created": "2016-05-09T08:17:27.000Z",
    "modified": "2016-05-09T08:17:27.000Z",
    "relationship_type": "controls",
    "source_ref": "infrastructure--38c47d93-d984-4fd9-b87b-d69d0841628d",
    "target_ref": "malware--16f4f3f9-1b68-4abb-bb66-7639d49f1e30"
  },
  {
    "type": "malware",
    "spec_version": "2.1",
    "id": "malware--16f4f3f9-1b68-4abb-bb66-7639d49f1e30",
    "created": "2016-05-08T14:31:09.000Z",
    "modified": "2016-05-08T14:31:09.000Z",
    "is_family": true,
    "malware_types":[
      "remote-access-trojan"
    ],
    "name": "Poison Ivy"
  },
  {
    "type": "relationship",
    "spec_version": "2.1",
    "id": "relationship--7aebe2f0-28d6-48a2-9c3e-b0aaa60266ef",
    "created": "2016-05-09T08:17:27.000Z",
    "modified": "2016-05-09T08:17:27.000Z",
    "relationship_type": "consists-of",
    "source_ref": "infrastructure--38c47d93-d984-4fd9-b87b-d69d0841628d",
    "target_ref": "ipv4-addr--28bb3599-77cd-5a82-a950-b5bc3caf07c4"
  },
  {
    "type": "relationship",
    "spec_version": "2.1",
    "id": "relationship--b82b2819-3b86-4bd5-afb3-fa36cfbc3f18",
    "created": "2016-05-09T08:17:27.000Z",
    "modified": "2016-05-09T08:17:27.000Z",
    "relationship_type": "consists-of",
    "source_ref": "infrastructure--38c47d93-d984-4fd9-b87b-d69d0841628d",
    "target_ref": "ipv4-addr--84445275-e371-444b-baea-ac7d07a180fd"
  },
  {
    "type": "ipv4-addr",
    "spec_version": "2.1",
    "id": "ipv4-addr--28bb3599-77cd-5a82-a950-b5bc3caf07c4",
    "value": "198.51.100.3"
  },
  {
    "type": "ipv4-addr",
    "spec_version": "2.1",
    "id": "ipv4-addr--055987b7-7d94-5326-8e20-c3dad8241976",
    "value": "198.52.200.4"
  }
]
```

## 4.9 Intrusion Set <a id="intrusion-set"></a>

**Type Name:** <span class="stixtype">intrusion-set</span>

An Intrusion Set is a grouped set of adversarial behaviors and resources with common properties that is believed to be orchestrated by a single organization. An Intrusion Set may capture multiple Campaigns or other activities that are all tied together by shared attributes indicating a commonly known or unknown Threat Actor. New activity can be attributed to an Intrusion Set even if the Threat Actors behind the attack are not known.
Threat Actors can move from supporting one Intrusion Set to supporting another, or they may support multiple Intrusion Sets.

Where a Campaign is a set of attacks over a period of time against a specific set of targets to achieve some objective, an Intrusion Set is the entire attack package and may be used over a very long period of time in multiple Campaigns to achieve potentially multiple purposes.

While sometimes an Intrusion Set is not active, or changes focus, it is usually difficult to know if it has truly disappeared or ended. Analysts may have varying level of fidelity on attributing an Intrusion Set back to Threat Actors.

### 4.9.1 Properties <a id="intrusion-set-properties"></a>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th><span class="stixtr">Required Common Properties</span></th>
  </tr>
  <tr>
    <td><strong>type</strong>, <strong>spec_version</strong>, <strong>id</strong>, <strong>created</strong>, <strong>modified</strong></td>
  </tr>
  <tr>
    <th><span class="stixtr">Optional Common Properties></span></th>
  </tr>
  <tr>
    <td><strong>created_by_ref</strong>, <strong>revoked</strong>, <strong>labels</strong>, <strong>confidence</strong>, <strong>lang</strong>, <strong>external_references</strong>, <strong>object_marking_refs</strong>, <strong>granular_markings</strong>, <strong>extensions</strong></td>
  </tr>
  <tr>
    <th><span class="stixtr">Not Applicable Common Properties</span></th>
  </tr>
  <tr>
    <td><strong>defanged</strong></td>
  </tr>
  <tr>
    <th><span class="stixtr">Intrusion Set Specific Properties</span></th>
  </tr>
  <tr>
    <td><strong>name</strong>, <strong>description</strong>, <strong>aliases</strong>, <strong>first_seen</strong>, <strong>last_seen</strong>, <strong>goals</strong>, <strong>resource_level</strong>, <strong>primary_motivation</strong>, <strong>secondary_motivations</strong></td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6">
  <tr>
    <th><span class="stixtr">Property Name</span></th>
    <th><span class="stixtr">Type</span></th>
    <th><span class="stixtr">Description</span></th>
  </tr>
  <tr>
    <td><strong>type</strong> (required)</td>
    <td><span class="stixtype">string</span></td>
    <td>The value of this property <strong>MUST</strong> be <span class="stixliteral">intrusion-set</span>.</td>
  </tr>
  <tr>
    <td><strong>name</strong> (required)</td>
    <td><span class="stixtype">string</span></td>
    <td>A name or characterizing text used to identify the Intrusion Set.</td>
  </tr>
  <tr>
    <td><strong>description</strong> (optional)</td>
    <td><span class="stixtype">string</span></td>
    <td>A description that provides more details and context about the Intrusion Set, potentially including its purpose and its key characteristics.</td>
  </tr>
  <tr>
    <td><strong>aliases</strong> (optional)</td>
    <td><span style="white-space:nowrap"><span class="stixtype">list</span> of type <span class="stixtype">string</span></span></td>
    <td>Alternative names used to identify this Intrusion Set.</td>
  </tr>
  <tr>
    <td><strong>first_seen</strong> (optional)</td>
    <td><span class="stixtype">timestamp</span></td>
    <td>The time that this Intrusion Set was first seen.<br><br>A summary property of data from sightings and other data that may or may not be available in STIX. If new sightings are received that are earlier than the first seen timestamp, the object may be updated to account for the new data.</td>
  </tr>
  <tr>
    <td><strong>last_seen</strong> (optional)</td>
    <td><span class="stixtype">timestamp</span></td>
    <td>The time that this Intrusion Set was last seen.<br><br>This property is a summary property of data from sightings and other data that may or may not be available in STIX. If new sightings are received that are later than the last seen timestamp, the object may be updated to account for the new data.<br><br>If this property and the <strong>first_seen</strong> property are both defined, then this property <strong>MUST</strong> be greater than or equal to the timestamp in the <strong>first_seen</strong> property.</td>
  </tr>
  <tr>
    <td><strong>goals</strong> (optional)</td>
    <td><span style="white-space:nowrap"><span class="stixtype">list</span> of type <span class="stixtype">string</span></span></td>
    <td>The high-level goals of this Intrusion Set, namely, <em>what</em> are they trying to do. For example, they may be motivated by personal gain, but their goal is to steal credit card numbers. To do this, they may execute specific Campaigns that have detailed objectives like compromising point of sale systems at a large retailer.<br><br>Another example: to gain information about latest merger and IPO information from ACME Bank.</td>
  </tr>
  <tr>
    <td><strong>resource_level</strong> (optional)</td>
    <td><span class="stixtype">open-vocab</span></td>
    <td>This property specifies the organizational level at which this Intrusion Set typically works, which in turn determines the resources available to this Intrusion Set for use in an attack.<br><br>The value for this property <strong>SHOULD</strong> come from the <span class="stixliteral"><a href="#attack-resource-level-vocabulary">attack-resource-level-ov</a></span> open vocabulary.</td>
  </tr>
  <tr>
    <td><strong>primary_motivation</strong> (optional)</td>
    <td><span class="stixtype">open-vocab</span></td>
    <td>The primary reason, motivation, or purpose behind this Intrusion Set. The motivation is <em>why</em> the Intrusion Set wishes to achieve the goal (what they are trying to achieve).<br><br>The value for this property <strong>SHOULD</strong> come from the <span class="stixliteral"><a href="#attack-motivation-vocabulary">attack-motivation-ov</a></span> open vocabulary.</td>
  </tr>
  <tr>
    <td><strong>secondary_motivations</strong> (optional)</td>
    <td><span style="white-space:nowrap"><span class="stixtype">list</span> of type <span class="stixtype">open-vocab</span></span></td>
    <td>The secondary reasons, motivations, or purposes behind this Intrusion Set. These motivations can exist as an equal or near-equal cause to the primary motivation. However, it does not replace or necessarily magnify the primary motivation, but it might indicate additional context. The position in the list has no significance.<br><br>The values for this property <strong>SHOULD</strong> come from the <span class="stixliteral"><a href="#attack-motivation-vocabulary">attack-motivation-ov</a></span> open vocabulary.</td>
  </tr>
</table>

### 4.9.2 Relationships <a id="intrusion-set-relationships"></a>

These are the relationships explicitly defined between the Intrusion Set object and other STIX Objects.
The first section lists the embedded relationships by property name along with their corresponding target.
The rest of the table identifies the relationships that can be made from this object type to another object type by way of the Relationship object.
The reverse relationships section illustrates the relationships targeting this object type from another object type.
They are included here for convenience.
For their definitions, please see the "Source" object.

Relationships are not restricted to those listed below.
Relationships can be created between any objects using the <span class="stixliteral">related-to</span> relationship type or, as with open vocabularies, user-defined names.

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th colspan='2'><span class='stixtr'>Embedded Relationships</span></th>
  </tr>
  <tr>
    <td width="50%"><strong>created_by_ref</strong></td>
    <td width="50%"><span class="stixtype">identifier</span> (of type <span class="stixtype">identity</span>)</td>
  </tr>
  <tr>
    <td><strong>object_marking_refs</strong></td>
    <td><span class="stixtype">list</span> of type <span class="stixtype">identifier</span> (of type <span class="stixtype">marking-definition</span>)</td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th><span class='stixtr'>Common Relationships</span></th>
  </tr>
  <tr>
    <td><span class="stixliteral">duplicate-of</span>, <span class="stixliteral">derived-from</span>, <span class="stixliteral">related-to</span></td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6">
  <tr>
    <th width="20%"><span class='stixtr'>Source</span></th>
    <th width="20%""><span class='stixtr'>Relationship Type</span></th>
    <th width="20%"><span class='stixtr'>Target</span></th>
    <th><span class='stixtr'>Description</span></th>
  </tr>
  <tr>
    <td><span class="stixtype">intrusion-set</span></td>
    <td><span class="stixliteral">attributed-to</span></td>
    <td><span class="stixtype">threat-actor</span></td>
    <td>This Relationship describes that the related Threat Actor is involved in carrying out the Intrusion Set.<br><br>For example, an <span class="stixliteral">attributed-to</span> Relationship from the Red Orca Intrusion Set to the Urban Fowl Threat Actor means that the actor carried out or was involved in some of the activity described by the Intrusion Set.</td>
  </tr>
  <tr>
    <td><span class="stixtype">intrusion-set</span></td>
    <td><span class="stixliteral">compromises</span></td>
    <td><span class="stixtype">infrastructure</span></td>
    <td>This Relationship describes that the Intrusion Set compromises the related Infrastructure.</td>
  </tr>
  <tr>
    <td><span class="stixtype">intrusion-set</span></td>
    <td><span class="stixliteral">hosts</span>, <span class="stixliteral">owns</span></td>
    <td><span class="stixtype">infrastructure</span></td>
    <td>This Relationship describes that the Intrusion Set hosts or owns the related Infrastructure (e.g. an actor that rents botnets to other threat actors).</td>
  </tr>
  <tr>
    <td><span class="stixtype">intrusion-set</span></td>
    <td><span class="stixliteral">originates-from</span></td>
    <td><span class="stixtype">location</span></td>
    <td>This Relationship describes that the Intrusion Set originates from the related location and <strong>SHOULD NOT</strong> be used to define attribution.<br><br>For example, an <span class="stixliteral">originates-from</span> relationship from the Red Orca Intrusion Set to a Location representing North America means that the Red Orca Intrusion Set appears to originate from or is located in North America.</td>
  </tr>
  <tr>
    <td><span class="stixtype">intrusion-set</span></td>
    <td><span class="stixliteral">targets</span></td>
    <td><span class="stixtype">identity</span>, <span class="stixtype">location</span>, <span class="stixtype">vulnerability</span></td>
    <td>This Relationship describes that the Intrusion Set uses exploits of the related Vulnerability or targets the type of victims described by the related Identity or Location.<br><br>For example, a <span class="stixliteral">targets</span> Relationship from the Red Orca Intrusion Set to a Vulnerability in a blogging platform indicates that attacks performed as part of Red Orca often exploit that Vulnerability.<br><br>Similarly, a <span class="stixliteral">targets</span> Relationship from the Red Orca Intrusion Set to an Identity describing the energy sector in the United States means that the Intrusion Set typically carries out attacks against targets in that sector.</td>
  </tr>
  <tr>
    <td><span class="stixtype">intrusion-set</span></td>
    <td><span class="stixliteral">uses</span></td>
    <td><span class="stixtype">attack-pattern</span>, <span class="stixtype">infrastructure</span>, <span class="stixtype">malware</span>, <span class="stixtype">tool</span></td>
    <td>This Relationship describes that attacks carried out as part of the Intrusion Set typically use the related Attack Pattern, Infrastructure, Malware, or Tool.<br><br>For example, a <span class="stixliteral">uses</span> Relationship from the Red Orca Intrusion Set to the xInject Malware indicates that xInject is often used during attacks attributed to that Intrusion Set.</td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th colspan='4'><span class='stixtr'>Reverse Relationships</span></th>
  </tr>
  <tr>
    <td width="20%"><span class="stixtype">campaign</span></td>
    <td width="20%"><span class="stixliteral">attributed-to</span></td>
    <td width="20%"><span class="stixtype">intrusion-set</span></td>
    <td>See forward relationship for definition.</td>
  </tr>
  <tr>
    <td><span class="stixtype">malware</span></td>
    <td><span class="stixliteral">authored-by</span></td>
    <td><span class="stixtype">intrusion-set</span></td>
    <td>See forward relationship for definition.</td>
  </tr>
  <tr>
    <td><span class="stixtype">indicator</span></td>
    <td><span class="stixliteral">indicates</span></td>
    <td><span class="stixtype">intrusion-set</span></td>
    <td>See forward relationship for definition.</td>
  </tr>
</table>

**​Example**

```JSON
{
  "type": "intrusion-set",
  "spec_version": "2.1",
  "id": "intrusion-set--4e78f46f-a023-4e5f-bc24-71b3ca22ec29",
  "created_by_ref": "identity--f431f809-377b-45e0-aa1c-6a4751cae5ff",
  "created": "2016-04-06T20:03:48.000Z",
  "modified": "2016-04-06T20:03:48.000Z",
  "name": "Bobcat Breakin",
  "description": "Incidents usually feature a shared TTP of a bobcat being released within the building containing network access, scaring users to leave their computers without locking them first. Still determining where the threat actors are getting the bobcats.",
  "aliases": ["Zookeeper"],
  "goals": ["acquisition-theft", "harassment", "damage"]
}
```

## 4.10 Location <a id="location"></a>

**Type Name:** <span class="stixtype">location</span>

A Location represents a geographic location. The location may be described as any, some or all of the following: region (e.g., North America), civic address (e.g. New York, US), latitude and longitude.

Locations are primarily used to give context to other SDOs. For example, a Location could be used in a relationship to describe that the Bourgeois Swallow intrusion set originates from Eastern Europe.

The Location SDO can be related to an Identity or Intrusion Set to indicate that the identity or intrusion set is located in that location. It can also be related from a malware or attack pattern to indicate that they target victims in that location. The Location object describes geographic areas, not governments, even in cases where that area might have a government. For example, a Location representing the United States describes the United States as a geographic area, not the federal government of the United States.

At least one of the following properties/sets of properties **MUST** be provided:

* **region**
* **country**
* **latitude** and **longitude**

When a combination of properties is provided (e.g. a **region** and a **latitude** and **longitude**) the more precise properties are what the location describes. In other words, if a location contains both a region of <span class="stixliteral">northern-america</span> and a country of <span class="stixliteral">us</span>, then the location describes the United States, not all of North America. In cases where a latitude and longitude are specified without a precision, the location describes the most precise other value.

If precision is specified, then the datum for **latitude** and **longitude** **MUST** be [WGS 84](#wgs-84). Organizations specifying a designated location using **latitude** and **longitude** **SHOULD** specify the precision which is appropriate for the scope of the location being identified. The scope is defined by the boundary as outlined by the precision around the coordinates.

### 4.10.1 Properties <a id="location-properties"></a>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th><span class="stixtr">Required Common Properties</span></th>
  </tr>
  <tr>
    <td><strong>type</strong>, <strong>spec_version</strong>, <strong>id</strong>, <strong>created</strong>, <strong>modified</strong></td>
  </tr>
  <tr>
    <th><span class="stixtr">Optional Common Properties></span></th>
  </tr>
  <tr>
    <td><strong>created_by_ref</strong>, <strong>revoked</strong>, <strong>labels</strong>, <strong>confidence</strong>, <strong>lang</strong>, <strong>external_references</strong>, <strong>object_marking_refs</strong>, <strong>granular_markings</strong>, <strong>extensions</strong></td>
  </tr>
  <tr>
    <th><span class="stixtr">Not Applicable Common Properties</span></th>
  </tr>
  <tr>
    <td><strong>defanged</strong></td>
  </tr>
  <tr>
    <th><span class="stixtr"> Specific Properties</span></th>
  </tr>
  <tr>
    <td><strong>name</strong>, <strong>description</strong>, <strong>latitude</strong>, <strong>longitude</strong>, <strong>precision</strong>, <strong>region</strong>, <strong>country</strong>, <strong>administrative_area</strong>, <strong>city</strong>, <strong>street_address</strong>, <strong>postal_code</strong></td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6">
  <tr>
    <th><span class="stixtr">Property Name</span></th>
    <th><span class="stixtr">Type</span></th>
    <th><span class="stixtr">Description</span></th>
  </tr>
  <tr>
    <td><strong>type</strong> (required)</td>
    <td><span class="stixtype">string</span></td>
    <td>The value of this property <strong>MUST</strong> be <span class="stixliteral">location</span>.</td>
  </tr>
  <tr>
    <td><strong>name</strong> (optional)</td>
    <td><span class="stixtype">string</span></td>
    <td>A name used to identify the Location.</td>
  </tr>
  <tr>
    <td><strong>description</strong> (optional)</td>
    <td><span class="stixtype">string</span></td>
    <td>A textual description of the Location.</td>
  </tr>
  <tr>
    <td><strong>latitude</strong> (optional)</td>
    <td><span class="stixtype">float</span></td>
    <td>The latitude of the Location in decimal degrees. Positive numbers describe latitudes north of the equator, and negative numbers describe latitudes south of the equator. The value of this property <strong>MUST</strong> be between -90.0 and 90.0, inclusive.<br><br>If the <strong>longitude</strong> property is present, this property <strong>MUST</strong> be present.</td>
  </tr>
  <tr>
    <td><strong>longitude</strong> (optional)</td>
    <td><span class="stixtype">float</span></td>
    <td>The longitude of the Location in decimal degrees. Positive numbers describe longitudes east of the prime meridian and negative numbers describe longitudes west of the prime meridian. The value of this property <strong>MUST</strong> be between -180.0 and 180.0, inclusive.<br><br>If the <strong>latitude</strong> property is present, this property <strong>MUST</strong> be present.</td>
  </tr>
  <tr>
    <td><strong>precision</strong> (optional)</td>
    <td><span class="stixtype">float</span></td>
    <td>Defines the precision of the coordinates specified by the <strong>latitude</strong> and <strong>longitude</strong> properties. This is measured in meters. The actual Location may be anywhere up to <strong>precision</strong> meters from the defined point.<br><br>If this property is not present, then the precision is unspecified.<br><br>If this property is present, the <strong>latitude</strong> and <strong>longitude</strong> properties <strong>MUST</strong> be present.</td>
  </tr>
  <tr>
    <td><strong>region</strong> (optional)</td>
    <td><span class="stixtype">open-vocab</span></td>
    <td>The region that this Location describes.<br><br>The value for this property <strong>SHOULD</strong> come from the <span class="stixliteral"><a href="#region-vocabulary">region-ov</a></span> open vocabulary.</td>
  </tr>
  <tr>
    <td><strong>country</strong> (optional)</td>
    <td><span class="stixtype">string</span></td>
    <td>The country that this Location describes. This property <strong>SHOULD</strong> contain a valid ISO 3166-1 ALPHA-2 Code [<a href="#iso3166-1">ISO3166-1</a>].</td>
  </tr>
  <tr>
    <td><strong>administrative_area</strong> (optional)</td>
    <td><span class="stixtype">string</span></td>
    <td>The state, province, or other sub-national administrative area that this Location describes.<br><br>This property SHOULD contain a valid ISO 3166-2 Code [<a href="#iso3166-2">ISO3166-2</a>].</td>
  </tr>
  <tr>
    <td><strong>city</strong> (optional)</td>
    <td><span class="stixtype">string</span></td>
    <td>The city that this Location describes.</td>
  </tr>
  <tr>
    <td><strong>street_address</strong> (optional)</td>
    <td><span class="stixtype">string</span></td>
    <td>The street address that this Location describes. This property includes all aspects or parts of the street address. For example, some addresses may have multiple lines including a mailstop or apartment number.</td>
  </tr>
  <tr>
    <td><strong>postal_code</strong> (optional)</td>
    <td><span class="stixtype">string</span></td>
    <td>The postal code for the Location.</td>
  </tr>
</table>

### 4.10.2 Relationships <a id="location-relationships"></a>

These are the relationships explicitly defined between the Location object and other STIX Objects. The first section lists the embedded relationships by property name along with their corresponding target. The rest of the table identifies the relationships that can be made from this object type to another object type by way of the Relationship object. The reverse relationships section illustrates the relationships targeting this object type from another object type. They are included here for convenience. For their definitions, please see the "Source" object.

Relationships are not restricted to those listed below. Relationships can be created between any objects using the related-to relationship type or, as with open vocabularies, user-defined names.

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th colspan='2'><span class='stixtr'>Embedded Relationships</span></th>
  </tr>
  <tr>
    <td width="50%"><strong>created_by_ref</strong></td>
    <td width="50%"><span class="stixtype">identifier</span> (of type <span class="stixtype">identity</span>)</td>
  </tr>
  <tr>
    <td><strong>object_marking_refs</strong></td>
    <td><span class="stixtype">list</span> of type <span class="stixtype">identifier</span> (of type <span class="stixtype">marking-definition</span>)</td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th><span class='stixtr'>Common Relationships</span></th>
  </tr>
  <tr>
    <td><span class="stixliteral">duplicate-of</span>, <span class="stixliteral">derived-from</span>, <span class="stixliteral">related-to</span></td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th width="20%"><span class='stixtr'>Source</span></th>
    <th width="20%""><span class='stixtr'>Relationship Type</span></th>
    <th width="20%"><span class='stixtr'>Target</span></th>
    <th><span class='stixtr'>Description</span></th>
  </tr>
  <tr>
    <td>—</td>
    <td>—</td>
    <td>—</td>
    <td>—</td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th colspan='4'><span class='stixtr'>Reverse Relationships</span></th>
  </tr>
  <tr>
    <td width="20%"><span class="stixtype">identity</span>, <span class="stixtype">infrastructure</span>, <span class="stixtype">threat-actor</span></td>
    <td width="20%"><span class="stixliteral">located-at</span></td>
    <td width="20%"><span class="stixtype">location</span></td>
    <td>See forward relationship for definition.</td>
  </tr>
  <tr>
    <td><span class="stixtype">campaign</span>, <span class="stixtype">intrusion-set</span>, <span class="stixtype">malware</span></td>
    <td><span class="stixliteral">originates-from</span></td>
    <td><span class="stixtype">location</span></td>
    <td>See forward relationship for definition.</td>
  </tr>
  <tr>
    <td><span class="stixtype">attack-pattern</span>, <span class="stixtype">campaign</span>, <span class="stixtype">intrusion-set</span>, <span class="stixtype">malware</span>, <span class="stixtype">threat-actor</span>, <span class="stixtype">tool</span></td>
    <td><span class="stixliteral">targets</span></td>
    <td><span class="stixtype">location</span></td>
    <td>See forward relationship for definition.</td>
  </tr>
</table>

**Example**

```JSON
  [
    {
    "type": "location",
    "spec_version": "2.1",
    "id": "location--a6e9345f-5a15-4c29-8bb3-7dcc5d168d64",
    "created_by_ref": "identity--f431f809-377b-45e0-aa1c-6a4751cae5ff",
    "created": "2016-04-06T20:03:00.000Z",
    "modified": "2016-04-06T20:03:00.000Z",
    "region": "northern-america"
  }
  {
    "type": "location",
    "spec_version": "2.1",
    "id": "location--a6e9345f-5a15-4c29-8bb3-7dcc5d168d64",
    "created_by_ref": "identity--f431f809-377b-45e0-aa1c-6a4751cae5ff",
    "created": "2016-04-06T20:03:00.000Z",
    "modified": "2016-04-06T20:03:00.000Z",
    "region": "south-eastern-asia",
    "country": "th",
    "administrative_area": "Tak",
    "postal_code": "63170"
  }
  {
    "type": "location",
    "spec_version": "2.1",
    "id": "location--a6e9345f-5a15-4c29-8bb3-7dcc5d168d64",
    "created_by_ref": "identity--f431f809-377b-45e0-aa1c-6a4751cae5ff",
    "created": "2016-04-06T20:03:00.000Z",
    "modified": "2016-04-06T20:03:00.000Z",
    "latitude": "48.8566",
    "longitude": "2.3522"
  }
]
```

## 4.11 Malware <a id="malware"></a>

**Type Name:** <span class="stixtype">malware</span>

Malware is a type of TTP that represents malicious code. It generally refers to a program that is inserted into a system, usually covertly. The intent is to compromise the confidentiality, integrity, or availability of the victim's data, applications, or operating system (OS) or otherwise annoy or disrupt the victim.

The Malware SDO characterizes, identifies, and categorizes malware instances and families from data that may be derived from analysis. This SDO captures detailed information about how the malware works and what it does. This SDO captures contextual data relevant to sharing Malware data without requiring the full analysis provided by the Malware Analysis SDO.

The Indicator SDO provides intelligence producers with the ability to define, using the STIX Pattern Grammar in a standard way to identify and detect behaviors associated with malicious activities. Although the Malware SDO provides vital intelligence on a specific instance or malware family, it does not provide a standard grammar that the Indicator SDO provides to identify those properties in security detection systems designed to process the STIX Pattern grammar. We strongly encourage the use of STIX Indicators for the detection of actual malware, due to its use of the STIX Patterning language and the clear semantics that it provides.

To minimize the risk of a consumer compromising their system in parsing malware samples, producers **SHOULD** consider sharing defanged content (archive and password-protected samples) instead of raw, base64-encoded malware samples.

### 4.11.1 Properties <a id="malware-properties"></a>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th><span class="stixtr">Required Common Properties</span></th>
  </tr>
  <tr>
    <td><strong>type</strong>, <strong>spec_version</strong>, <strong>id</strong>, <strong>created</strong>, <strong>modified</strong></td>
  </tr>
  <tr>
    <th><span class="stixtr">Optional Common Properties></span></th>
  </tr>
  <tr>
    <td><strong>created_by_ref</strong>, <strong>revoked</strong>, <strong>labels</strong>, <strong>confidence</strong>, <strong>lang</strong>, <strong>external_references</strong>, <strong>object_marking_refs</strong>, <strong>granular_markings</strong>, <strong>extensions</strong></td>
  </tr>
  <tr>
    <th><span class="stixtr">Not Applicable Common Properties</span></th>
  </tr>
  <tr>
    <td><strong>defanged</strong></td>
  </tr>
  <tr>
    <th><span class="stixtr"> Specific Properties</span></th>
  </tr>
  <tr>
    <td><strong>name</strong>, <strong>description</strong>, <strong>malware_types</strong>, <strong>is_family</strong>, <strong>aliases</strong>, <strong>kill_chain_phases</strong>, <strong>first_seen</strong>, <strong>last_seen</strong>, <strong>operating_system_refs</strong>, <strong>architecture_execution_envs</strong>, <strong>implementation_languages</strong>, <strong>capabilities</strong>, <strong>sample_refs</strong></td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6">
  <tr>
    <th><span class="stixtr">Property Name</span></th>
    <th><span class="stixtr">Type</span></th>
    <th><span class="stixtr">Description</span></th>
  </tr>
  <tr>
    <td><strong>type</strong> (required)</td>
    <td><span class="stixtype">string</span></td>
    <td>The value of this property <strong>MUST</strong> be <span class="stixliteral">malware</span>.</td>
  </tr>
  <tr>
    <td><strong>name</strong> (optional)</td>
    <td><span class="stixtype">string</span></td>
    <td>A name used to identify the Malware instance or family, as specified by the producer of the SDO. For a malware family the name <strong>MUST</strong> be defined. If a name for a malware instance is not available, the SHA-256 hash value or sample’s filename <strong>MAY</strong> be used instead.</td>
  </tr>
  <tr>
    <td><strong>description</strong> (optional)</td>
    <td><span class="stixtype">string</span></td>
    <td>A description that provides more details and context about the Malware instance or family, potentially including its purpose and its key characteristics.</td>
  </tr>
  <tr>
    <td><strong>malware_types</strong> (optional)</td>
    <td><span style="white-space: nowrap;"><span class="stixtype">list</span> of type <span class="stixtype">open-vocab</span></span></td>
    <td>A set of categorizations for the malware being described.<br><br>The values for this property <strong>SHOULD</strong> come from the <span class="stixliteral"><a href="malware-type-vocabulary">malware-type-ov</a></span> open vocabulary.</td>
  </tr>
  <tr>
    <td><strong>is_family</strong> (optional)</td>
    <td><span class="stixtype">boolean</span></td>
    <td>Whether the object represents a malware family (if <span class="stixliteral">true</span>) or a malware instance (if <span class="stixliteral">false</span>).</td>
  </tr>
  <tr>
    <td><strong>aliases</strong> (optional)</td>
    <td><span style="white-space: nowrap;"><span class="stixtype">list</span> of type <span class="stixtype">string</span></span></td>
    <td>Alternative names used to identify this malware or malware family.</td>
  </tr>
  <tr>
    <td><strong>kill_chain_phases</strong> (optional)</td>
    <td><span style="white-space: nowrap;"><span class="stixtype">list</span> of type <span class="stixtype">kill-chain-phase</span></span></td>
    <td>The list of Kill Chain Phases for which this malware can be used.</td>
  </tr>
  <tr>
    <td><strong>first_seen</strong> (optional)</td>
    <td><span class="stixtype">timestamp</span></td>
    <td>The time that the malware instance or family was first seen.<br><br>This property is a summary property of data from sightings and other data that may or may not be available in STIX. If new sightings are received that are earlier than the first seen timestamp, the object may be updated to account for the new data.</td>
  </tr>
  <tr>
    <td><strong>last_seen</strong> (optional)</td>
    <td><span class="stixtype">timestamp</span></td>
    <td>The time that the malware family or malware instance was last seen.<br><br>This property is a summary property of data from sightings and other data that may or may not be available in STIX. If new sightings are received that are later than the <strong>last_seen</strong> timestamp, the object may be updated to account for the new data.<br><br>If this property and the <strong>first_seen</strong> property are both defined, then this property <strong>MUST</strong> be greater than or equal to the timestamp in the <strong>first_seen</strong> property.</td>
  </tr>
  <tr>
    <td><strong>operating_system_refs</strong> (optional)</td>
    <td><span style="white-space: nowrap;"><span class="stixtype">list</span> of type <span class="stixtype">identifier</span></td>
    <td>The operating systems that the malware family or malware instance is executable on. This applies to virtualized operating systems as well as those running on bare metal.<br><br>The value of this property <strong>MUST</strong> be the <span class="stixtype">identifier</span> for a SCO <span class="stixtype">software</span> object.</td>
  </tr>
  <tr>
    <td><strong>architecture_execution_envs</strong> (optional)</td>
    <td><span style="white-space: nowrap;"><span class="stixtype">list</span> of type <span class="stixtype">open-vocab</span></td>
    <td>The processor architectures (e.g., x86, ARM, etc.) that the malware instance or family is executable on.<br><br>The values for this property <strong>SHOULD</strong> come from the <span class="stixliteral"><a href="#processor-architecture-vocabulary">processor-architecture-ov</a></span> open vocabulary.</td>
  </tr>
  <tr>
    <td><strong>implementation_languages</strong> (optional)</td>
    <td><span style="white-space: nowrap;"><span class="stixtype">list</span> of type <span class="stixtype">open-vocab</span></td>
    <td>The programming language(s) used to implement the malware instance or family.<br><br>The values for this property <strong>SHOULD</strong> come from the <span class="stixliteral"><a href="#implementation-language-vocabulary">implementation-language-ov</a></span> open vocabulary.</td>
  </tr>
  <tr>
    <td><strong>capabilities</strong> (optional)</td>
    <td><span style="white-space: nowrap;"><span class="stixtype">list</span> of type <span class="stixtype">open-vocab</span></td>
    <td>Any of the capabilities identified for the malware instance or family.<br><br>The values for this property <strong>SHOULD</strong> come from the <span class="stixliteral"><a href="#malware-capabilities-vocabulary">malware-capabilities-ov</a></span> open vocabulary.</td>
  </tr>
  <tr>
    <td><strong>sample_refs</strong> (optional)</td>
    <td><span style="white-space: nowrap;"><span class="stixtype">list</span> of type <span class="stixtype">identifier</span></td>
    <td>The <strong>sample_refs</strong> property specifies a list of <span class="stixtype">identifiers</span> of the SCO <span class="stixtype">file</span> or <span class="stixtype">artifact</span> objects associated with this malware instance(s) or family.<br><br>If <strong>is_family</strong> is <span class="stixliteral">false</span>, then all samples listed in <strong>sample_refs MUST</strong> refer to the same binary data.</td>
  </tr>
</table>

### 4.11.2 Relationships <a id="malware-relationships"></a>

These are the relationships explicitly defined between the Malware object and other STIX Objects. The first section lists the embedded relationships by property name along with their corresponding target. The rest of the table identifies the relationships that can be made from this object type to another object type by way of the Relationship object. The reverse relationships section illustrates the relationships targeting this object type from another object type. They are included here for convenience. For their definitions, please see the "Source" object.

Relationships are not restricted to those listed below. Relationships can be created between any objects using the <span class="stixliteral">related-to</span> relationship type or, as with open vocabularies, user-defined names.

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th colspan='2'><span class='stixtr'>Embedded Relationships</span></th>
  </tr>
  <tr>
    <td width="50%"><strong>created_by_ref</strong></td>
    <td width="50%"><span class="stixtype">identifier</span> (of type <span class="stixtype">identity</span>)</td>
  </tr>
  <tr>
    <td><strong>object_marking_refs</strong></td>
    <td><span class="stixtype">list</span> of type <span class="stixtype">identifier</span> (of type <span class="stixtype">marking-definition</span>)</td>
  </tr>
  <tr>
    <td><strong>operating_system_refs</strong></td>
    <td><span class="stixtype">list</span> of type <span class="stixtype">identifier</span> (of type <span class="stixtype">software</span>)</td>
  <tr>
    <td><strong>sample_refs</strong></td>
    <td><span class="stixtype">list</span> of type <span class="stixtype">identifier</span> (of type <span class="stixtype">file</span> or <span class="stixtype">artifact</span>)</td>
</table>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th><span class='stixtr'>Common Relationships</span></th>
  </tr>
  <tr>
    <td><span class="stixliteral">duplicate-of</span>, <span class="stixliteral">derived-from</span>, <span class="stixliteral">related-to</span></td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6">
  <tr>
    <th width="20%"><span class='stixtr'>Source</span></th>
    <th width="20%""><span class='stixtr'>Relationship Type</span></th>
    <th width="20%"><span class='stixtr'>Target</span></th>
    <th><span class='stixtr'>Description</span></th>
  </tr>
  <tr>
    <td><span class="stixtype">malware</span></td>
    <td><span class="stixliteral">authored-by</span></td>
    <td><span class="stixtype">threat-actor</span>, <span class="stixtype">intrusion-set</span></td>
    <td>This Relationship describes that the malware instance or family was developed by the related threat actor or intrusion set.</td>
  </tr>
  <tr>
    <td><span class="stixtype">malware</span></td>
    <td><span class="stixliteral">beacons-to</span>, <span class="stixliteral">exfiltrates-to</span></td>
    <td><span class="stixtype">infrastructure</span></td>
    <td>This Relationship describes that the malware instance or family beacons to or exfiltrates data to the related Infrastructure.</td>
  </tr>
  <tr>
    <td><span class="stixtype">malware</span></td>
    <td><span class="stixliteral">communicates-with</span></td>
    <td><span class="stixtype">ipv4-addr</span>, <span class="stixtype">ipv6-addr</span>, <span class="stixtype">domain-name</span>, <span class="stixtype">url</span></td>
    <td>This Relationship documents that this malware instance (or family) communicates with (beacons to, connects to, or exfiltrated data to) the defined network addressable resource.</td>
  </tr>
  <tr>
    <td><span class="stixtype">malware</span></td>
    <td><span class="stixliteral">controls</span></td>
    <td><span class="stixtype">malware</span></td>
    <td>This Relationship documents that this malware instance (or family) can control other malware which may be resident on the same system on which it is executing.<br><br>Note that this is not meant to imply or state that the malware instance or family drops other malware (which is covered by the <span class="stixliteral">drops</span> relationship).
Rather, it is meant to state that the malware instance or family is able to subvert or control other malware to achieve its goals.</td>
  </tr>
  <tr>
    <td><span class="stixtype">malware</span></td>
    <td><span class="stixliteral">downloads</span>, <span class="stixliteral">drops</span></td>
    <td><span class="stixtype">malware</span>, <span class="stixtype">tool</span>, <span class="stixtype">file</span></td>
    <td>These Relationships document that this malware instance (or family) downloads or drops another malware instance, tool or file. This is especially common with "first-stage" malware instances such as downloaders and droppers.</td>
  </tr>
  <tr>
    <td><span class="stixtype">malware</span></td>
    <td><span class="stixliteral">exploits</span></td>
    <td><span class="stixtype">vulnerability</span></td>
    <td>This Relationship documents that this malware instance or family exploits or attempts to exploit a particular vulnerability.<br><br>For example, an <span class="stixliteral">exploits</span> Relationship linking a malware instance or family representing a downloader to a Vulnerability for CVE-2016-0001 means that the malware instance or family exploits that vulnerability.</td>
  </tr>
  <tr>
    <td><span class="stixtype">malware</span></td>
    <td><span class="stixliteral">originates-from</span></td>
    <td><span class="stixtype">location</span></td>
    <td>This Relationship documents that this malware instance or family originates from a particular location.</td>
  </tr>
  <tr>
    <td><span class="stixtype">malware</span></td>
    <td><span class="stixliteral">targets</span></td>
    <td><span class="stixtype">identity</span>, <span class="stixtype">infrastructure</span>, <span class="stixtype">location</span>, <span class="stixtype">vulnerability</span></td>
    <td>This Relationship documents that a malware instance or family is being used to target an Identity, Infrastructure, or Location. For malware families, this can be used to capture the full set of identities, infrastructures, or locations targeted by the family.<br><br>Similarly, a <span class="stixliteral">targets</span> Relationship linking a malware instance or family representing a downloader to an Identity representing the energy sector means that downloader is typically used against targets in the energy sector.</td>
  </tr>
  <tr>
    <td><span class="stixtype">malware</span></td>
    <td><span class="stixliteral">uses</span></td>
    <td><span class="stixtype">attack-pattern</span>, <span class="stixtype">infrastructure</span>, <span class="stixtype">malware</span>, <span class="stixtype">tool</span></td>
    <td>This Relationship documents that this malware instance or family uses the attack pattern, infrastructure, malware, or tool to achieve its objectives.<br><br>For example, a <span class="stixliteral">uses</span> Relationship from the jay-sm17h Threat Actor to the xInject Malware indicates that xInject is often used by jay-sm17h.</td>
  </tr>
  <tr>
    <td><span class="stixtype">malware</span></td>
    <td><span class="stixliteral">variant-of</span></td>
    <td><span class="stixtype">malware</span></td>
    <td>This Relationship is used to document that one malware instance or family is a variant of another malware instance or family.<br><br>Only the following uses of this relationship are valid:<br><br>Malware instance → Malware family: a Malware instance is a variant of a Malware family. For example, a particular Zeus version 2 sample is a variant of the broader Zeus family.<br><br>Malware family → Malware family: a Malware family is a variant of another Malware family. For example, the Gameover Zeus family is a variant of the broader Zeus family.<br><br>Malware instance → Malware instance: a Malware instance is a variant of another Malware instance. For example, a particular Cryptolocker instance that is based on an another Cryptolocker instance with minor changes.<br><br>Malware family → Malware instance: this relationship <strong>MUST NOT</strong> be used as it is not semantically valid.</td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th colspan='4'><span class='stixtr'>Reverse Relationships</span></th>
  </tr>
  <tr>
    <td width="20%"><span class="stixtype">attack-pattern</span>, <span class="stixtype">infrastructure</span>, <span class="stixtype">tool</span></td>
    <td width="20%"><span class="stixliteral">delivers</span></td>
    <td width="20%"><span class="stixtype">malware</span></td>
    <td>See forward relationship for definition.</td>
  </tr>
  <tr>
    <td><span class="stixtype">indicator</span></td>
    <td><span class="stixliteral">indicates</span></td>
    <td><span class="stixtype">malware</span></td>
    <td>See forward relationship for definition.</td>
  </tr>
  <tr>
    <td><span class="stixtype">course-of-action</span></td>
    <td><span class="stixliteral">mitigates</span>, <span class="stixliteral">remediates</span></td>
    <td><span class="stixtype">malware</span></td>
    <td>See forward relationship for definition.</td>
  </tr>
  <tr>
    <td><span class="stixtype">attack-pattern</span>, <span class="stixtype">campaign</span>, <span class="stixtype">intrusion-set</span>, <span class="stixtype">threat-actor</span></td>
    <td><span class="stixliteral">uses</span></td>
    <td><span class="stixtype">malware</span></td>
    <td>See forward relationship for definition.</td>
  </tr>
  <tr>
    <td><span class="stixtype">tool</span></td>
    <td><span class="stixliteral">drops</span></td>
    <td><span class="stixtype">malware</span></td>
    <td>See forward relationship for definition.</td>
  </tr>
  <tr>
    <td><span class="stixtype">infrastructure</span></td>
    <td><span class="stixliteral">controls</span></td>
    <td><span class="stixtype">malware</span></td>
    <td>See forward relationship for definition.</td>
  </tr>
  <tr>
    <td><span class="stixtype">malware-analysis</span></td>
    <td><span class="stixliteral">characterizes</span>, <span class="stixliteral">av-analysis-of</span>, <span class="stixliteral">static-analysis-of</span>, <span class="stixliteral">dynamic-analysis-of</span></td>
    <td><span class="stixtype">malware</span></td>
    <td>See forward relationship for definition.</td>
  </tr>
</table>

**Example**

```JSON
{
  "type": "malware",
  "spec_version": "2.1",
  "id": "malware--0c7b5b88-8ff7-4a4d-aa9d-feb398cd0061",
  "created": "2016-05-12T08:17:27.000Z",
  "modified": "2016-05-12T08:17:27.000Z",
  "name": "Cryptolocker",
  "description": "A variant of the cryptolocker family",
  "malware_types": ["ransomware"],
  "is_family": false
}
```

## 4.12 Malware Analysis <a id="malware-analysis"></a>

**Type Name:** <span class="stixtype">malware-analysis</span>

Malware Analysis captures the metadata and results of a particular static or dynamic analysis performed on a malware instance or family.
One of **result** or **analysis_sco_refs** properties **MUST** be provided.

### 4.12.1 Properties <a id="malware-analysis-properties"></a>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th><span class="stixtr">Required Common Properties</span></th>
  </tr>
  <tr>
    <td><strong>type</strong>, <strong>spec_version</strong>, <strong>id</strong>, <strong>created</strong>, <strong>modified</strong></td>
  </tr>
  <tr>
    <th><span class="stixtr">Optional Common Properties></span></th>
  </tr>
  <tr>
    <td><strong>created_by_ref</strong>, <strong>revoked</strong>, <strong>labels</strong>, <strong>confidence</strong>, <strong>lang</strong>, <strong>external_references</strong>, <strong>object_marking_refs</strong>, <strong>granular_markings</strong>, <strong>extensions</strong></td>
  </tr>
  <tr>
    <th><span class="stixtr">Not Applicable Common Properties</span></th>
  </tr>
  <tr>
    <td><strong>defanged</strong></td>
  </tr>
  <tr>
    <th><span class="stixtr"> Specific Properties</span></th>
  </tr>
  <tr>
    <td><strong>product</strong>, <strong>version</strong>, <strong>host_vm_ref</strong>, <strong>operating_system_ref</strong>, <strong>installed_software_refs</strong>, <strong>configuration_version</strong>, <strong>modules</strong>, <strong>analysis_engine_version</strong>, <strong>analysis_definition_version</strong>, <strong>submitted</strong>, <strong>analysis_started</strong>, <strong>analysis_ended</strong>, <strong>result_name</strong>, <strong>result</strong>, <strong>analysis_sco_refs</strong>, <strong>sample_ref</strong></td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6">
  <tr>
    <th><span class="stixtr">Property Name</span></th>
    <th><span class="stixtr">Type</span></th>
    <th><span class="stixtr">Description</span></th>
  </tr>
  <tr>
    <td><strong>type</strong> (required)</td>
    <td><span class="stixtype">string</span></td>
    <td>The value of this property <strong>MUST</strong> be <span class="stixliteral">malware-analysis</span>.</td>
  </tr>
  <tr>
    <td><strong>product</strong> (required)</td>
    <td><span class="stixtype">string</span></td>
    <td>The name of the analysis engine or product that was used. Product names <strong>SHOULD</strong> be all lowercase with words separated by a dash "-".<br><br>For cases where the name of a product cannot be specified, a value of "anonymized" <strong>MUST</strong> be used.</td>
  </tr>
  <tr>
    <td><strong>version</strong> (optional)</td>
    <td><span class="stixtype">string</span></td>
    <td>The version of the analysis product that was used to perform the analysis.</td>
  </tr>
  <tr>
    <td><strong>host_vm_ref</strong> (optional)</td>
    <td><span class="stixtype">identifier</span></td>
    <td>A description of the virtual machine environment used to host the guest operating system (if applicable) that was used for the dynamic analysis of the malware instance or family.<br><br>If this value is not included in conjunction with the <strong>operating_system_ref</strong> property, this means that the dynamic analysis may have been performed on bare metal (i.e. without virtualization) or the information was redacted.<br><br>The value of this property <strong>MUST</strong> be the <span class="stixtype">identifier</span> for a SCO <span class="stixtype">software</span> object.</td>
  </tr>
  <tr>
    <td><strong>operating_system_ref</strong> (optional)</td>
    <td><span class="stixtype">identifier</span></td>
    <td>The operating system used for the dynamic analysis of the malware instance or family. This applies to virtualized operating systems as well as those running on bare metal.<br><br>The value of this property <strong>MUST</strong> be the <span class="stixtype">identifier</span> for a SCO <span class="stixtype">software</span> object.</td>
  </tr>
  <tr>
    <td><strong>installed_software_refs</strong> (optional)</td>
    <td><span style="white-space: nowrap;"><span class="stixtype">list</span> of type <span class="stixtype">identifier</span></span></td>
    <td>Any non-standard software installed on the operating system (specified through the <span class="stixliteral">operating-system</span> value) used for the dynamic analysis of the malware instance or family.<br><br>The value of this property <strong>MUST</strong> be the <span class="stixtype">identifier</span> for a SCO <span class="stixtype">software</span> object.</td>
  </tr>
  <tr>
    <td><strong>configuration_version</strong> (optional)</td>
    <td><span class="stixtype">string</span></td>
    <td>The named configuration of additional product configuration parameters for this analysis run.<br><br>For example, when a product is configured to do full depth analysis of Window™ PE files. This configuration may have a named version and that named version can be captured in this property. This will ensure additional runs can be configured in the same way.</td>
  </tr>
  <tr>
    <td><strong>modules</strong> (optional)</td>
    <td><span style="white-space: nowrap;"><span class="stixtype">list</span> of type <span class="stixtype">string</span></span></td>
    <td>The specific analysis modules that were used and configured in the product during this analysis run.<br><br>For example, configuring a product to support analysis of Dridex.</td>
  </tr>
  <tr>
    <td><strong>analysis_engine_version</strong> (optional)</td>
    <td><span class="stixtype">string</span></td>
    <td>The version of the analysis engine or product (including AV engines) that was used to perform the analysis.</td>
  </tr>
  <tr>
    <td><strong>analysis_definition_version</strong> (optional)</td>
    <td><span class="stixtype">string</span></td>
    <td>The version of the analysis definitions used by the analysis tool (including AV tools).</td>
  </tr>
  <tr>
    <td><strong>submitted</strong> (optional)</td>
    <td><span class="stixtype">timestamp</span></td>
    <td>The date and time that the malware was first submitted for scanning or analysis. This value will stay constant while the scanned date can change. For example, when Malware was submitted to a virus analysis tool.</td>
  </tr>
  <tr>
    <td><strong>analysis_started</strong> (optional)</td>
    <td><span class="stixtype">timestamp</span></td>
    <td>The date and time that the malware analysis was initiated.</td>
  </tr>
  <tr>
    <td><strong>analysis_ended</strong> (optional)</td>
    <td><span class="stixtype">timestamp</span></td>
    <td>The date and time that the malware analysis ended.</td>
  </tr>
  <tr>
    <td><strong>result_name</strong> (optional)</td>
    <td><span class="stixtype">string</span></td>
    <td>The classification result or name assigned to the malware instance by the scanner tool.</td>
  </tr>
  <tr>
    <td><strong>result</strong> (optional)</td>
    <td><span class="stixtype">open-vocab</span></td>
    <td>The classification result as determined by the scanner or tool analysis process.<br><br>The value for this property <strong>SHOULD</strong> come from the <span class="stixliteral"><a href="#malware-result-vocabulary">malware-result-ov</a></span> open vocabulary.</td>
  </tr>
  <tr>
    <td><strong>analysis_sco_refs</strong> (optional)</td>
    <td><span style="white-space: nowrap;"><span class="stixtype">list</span> of type <span class="stixtype">identifier</span></span></td>
    <td>This property contains the references to the STIX Cyber-observable Objects that were captured during the analysis process.</td>
  </tr>
  <tr>
    <td><strong>sample_ref</strong> (optional)</td>
    <td><span class="stixtype">identifier</span></td>
    <td>This property contains the reference to the SCO file, network traffic or artifact object that this malware analysis was performed against.<br><br>Caution should be observed when creating an SRO between Malware and Malware Analysis objects when the Malware <strong>sample_refs</strong> property does not contain the SCO that is included in the Malware Analysis <strong>sample_ref</strong> property.<br><br>Note, this property can also contain a reference to an SCO which is not associated with Malware (i.e., some SCO which was scanned and found to be benign.)</td>
  </tr>
</table>

### 4.12.2 Relationships <a id="malware-analysis-relationships"></a>

These are the relationships explicitly defined between the Malware Analysis object and other STIX Objects. The first section lists the embedded relationships by property name along with their corresponding target. The rest of the table identifies the relationships that can be made from this object type to another object type by way of the Relationship object. The reverse relationships section illustrates the relationships targeting this object type from another object type. They are included here for convenience. For their definitions, please see the "Source" object.

Relationships are not restricted to those listed below. Relationships can be created between any objects using the <span class="stixliteral">related-to</span> relationship type or, as with open vocabularies, user-defined names.

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th colspan='2'><span class='stixtr'>Embedded Relationships</span></th>
  </tr>
  <tr>
    <td width="50%"><strong>created_by_ref</strong></td>
    <td width="50%"><span class="stixtype">identifier</span> (of type <span class="stixtype">identity</span>)</td>
  </tr>
  <tr>
    <td><strong>object_marking_refs</strong></td>
    <td><span class="stixtype">list</span> of type <span class="stixtype">identifier</span> (of type <span class="stixtype">marking-definition</span>)</td>
  </tr>
  <tr>
    <td><strong>host_vm_ref</strong></td>
    <td><span class="stixtype">identifier</span> (of type <span class="stixtype">software</span>)</td>
  </tr>
  <tr>
    <td><strong>operating_system_ref</strong></td>
    <td><span class="stixtype">identifier</span> (of type <span class="stixtype">software</span>)</td>
  </tr>
  <tr>
    <td><strong>installed_software_refs</strong></td>
    <td><span class="stixtype">list</span> of type <span class="stixtype">identifier</span> (of type <span class="stixtype">software</span>)</td>
  </tr>
  <tr>
    <td><strong>analysis_sco_refs</strong></td>
    <td><span class="stixtype">list</span> of type <span class="stixtype">identifier</span> (of type STIX Object)</td>
  </tr>
  <tr>
    <td><strong>sample_ref</strong></td>
    <td><span class="stixtype">identifier</span> (of type <span class="stixtype">file</span>, <span class="stixtype">network-traffic</span>, and <span class="stixtype">artifact</span>)</td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th><span class="stixtr"><strong>Common Relationships</strong></span></th>
  </tr>
  <tr>
    <td><span class="stixliteral">duplicate-of</span>, <span class="stixliteral">derived-from</span>, <span class="stixliteral">related-to</span></td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th width="20%"><span class="stixtr"><strong>Source</strong></span></th>
    <th width="20%"><span class="stixtr"><strong>Relationship Type</strong></span></th>
    <th width="20%"><span class="stixtr"><strong>Target</strong></span></th>
    <th><span class="stixtr"><strong>Description</strong></span></th>
  </tr>
  <tr>
    <td><span class="stixtype">malware-analysis</span></td>
    <td><span class="stixliteral">characterizes</span></td>
    <td><span class="stixtype">malware</span></td>
    <td>This Relationship describes that the malware analysis describes the related malware.</td>
  </tr>
  <tr>
    <td><span class="stixtype">malware-analysis</span></td>
    <td><span class="stixliteral">av-analysis-of</span></td>
    <td><span class="stixtype">malware</span></td>
    <td>This Relationship describes that the malware analysis is results for the related malware.</td>
  </tr>
  <tr>
    <td><span class="stixtype">malware-analysis</span></td>
    <td><span class="stixliteral">static-analysis-of</span></td>
    <td><span class="stixtype">malware</span></td>
    <td>This Relationship describes that the malware analysis is static analysis results for the related malware.</td>
  </tr>
  <tr>
    <td><span class="stixtype">malware-analysis</span></td>
    <td><span class="stixliteral">dynamic-analysis-of</span></td>
    <td><span class="stixtype">malware</span></td>
    <td>This Relationship describes that the malware analysis is dynamic analysis results for the related malware.</td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th colspan='4'><span class='stixtr'>Reverse Relationships</span></th>
  </tr>
  <tr>
    <td width="20%">—</span></td>
    <td width="20%">—</span></td>
    <td width="20%">—</span></td>
    <td>—</td>
  </tr>
</table>

**Example**

```JSON
[
  {
    "type": "malware",
    "spec_version": "2.1",
    "id": "malware--8bcf14e9-2ba2-44ef-9e32-fbbc9d2608b2",
    "created": "2020-01-16T18:52:24.277Z",
    "modified": "2020-01-16T18:52:24.277Z",
    "name": "a92e5b2bae.exe",
    "malware_types": [
      "unknown"
    ],
    "is_family": false,
    "sample_refs": [
      "file--ba8965d8-e4ec-5f9c-a4df-1c460994ca58"
    ]
  }
  {
    "type": "malware-analysis",
    "spec_version": "2.1",
    "id": "malware-analysis--d25167b7-fed0-4068-9ccd-a73dd2c5b07c",
    "created": "2020-01-16T18:52:24.277Z",
    "modified": "2020-01-16T18:52:24.277Z",
    "product": "microsoft",
    "analysis_engine_version": "5.1.0",
    "analysis_definition_version": "053514-0062",
    "analysis_started": "2012-02-11T08:36:14Z",
    "analysis_ended": "2012-02-11T08:36:14Z",
    "result": "malicious"
  }
  {
    "type": "relationship",
    "spec_version": "2.1",
    "id": "relationship--014841f8-eb38-4673-9904-70f67c92dd8b",
    "created": "2020-01-16T18:52:24.277Z",
    "modified": "2020-01-16T18:52:24.277Z",
    "relationship_type": "av-analysis-of",
    "source_ref": "malware-analysis--d25167b7-fed0-4068-9ccd-a73dd2c5b07c",
    "target_ref": "malware--8bcf14e9-2ba2-44ef-9e32-fbbc9d2608b2"
  }
  {
    "type": "file",
    "id": "file--ba8965d8-e4ec-5f9c-a4df-1c460994ca58",
    "spec_version": "2.1",
    "hashes": {
      "MD5": "a92e5b2bae0b4b3a3d81c85610b95cd4",
      "SHA-1": "5374e08903744ceeaedd8f5e1bfc06b2c4688e76"
    },
    "size": 77312,
    "name": "a92e5b2bae.exe",
    "parent_directory_ref": "directory--ab82f84a-5afc-5ea7-8d98-9fcbc277eda6"
  }
  {
    "type": "directory",
    "id": "directory--ab82f84a-5afc-5ea7-8d98-9fcbc277eda6",
    "spec_version": "2.1",
    "path": "C:\\"
  }
]
```

## 4.13 Note <a id="note"></a>

**Type Name:** <span class="stixtype">note</span>

A Note is intended to convey informative text to provide further context and/or to provide additional analysis not contained in the STIX Objects, Marking Definition objects, or Language Content objects which the Note relates to. Notes can be created by anyone (not just the original object creator).

For example, an analyst may add a Note to a Campaign object created by another organization indicating that they've seen posts related to that Campaign on a hacker forum.

Because Notes are typically (though not always) created by human analysts and are comprised of human-oriented text, they contain an additional property to capture the analyst(s) that created the Note. This is distinct from the **created_by_ref** property, which is meant to capture the organization that created the object.

### 4.13.1 Properties <a id="note-properties"></a>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th><span class="stixtr">Required Common Properties</span></th>
  </tr>
  <tr>
    <td><strong>type</strong>, <strong>spec_version</strong>, <strong>id</strong>, <strong>created</strong>, <strong>modified</strong></td>
  </tr>
  <tr>
    <th><span class="stixtr">Optional Common Properties></span></th>
  </tr>
  <tr>
    <td><strong>created_by_ref</strong>, <strong>revoked</strong>, <strong>labels</strong>, <strong>confidence</strong>, <strong>lang</strong>, <strong>external_references</strong>, <strong>object_marking_refs</strong>, <strong>granular_markings</strong>, <strong>extensions</strong></td>
  </tr>
  <tr>
    <th><span class="stixtr">Not Applicable Common Properties</span></th>
  </tr>
  <tr>
    <td><strong>defanged</strong></td>
  </tr>
  <tr>
    <th><span class="stixtr"> Specific Properties</span></th>
  </tr>
  <tr>
    <td><strong>abstract</strong>, <strong>content</strong>, <strong>authors</strong>, <strong>object_refs</strong></td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th><span class="stixtr">Property Name</span></th>
    <th><span class="stixtr">Type</span></th>
    <th><span class="stixtr">Description</span></th>
  </tr>
  <tr>
    <td><strong>type</strong> (required)</td>
    <td><span class="stixtype">string</span></td>
    <td>The value of this property <strong>MUST</strong> be <span class="stixliteral">note</span>.</td>
  </tr>
  <tr>
    <td><strong>abstract</strong> (optional)</td>
    <td><span class="stixtype">string</span></td>
    <td>A brief summary of the note content.</td>
  </tr>
  <tr>
    <td><strong>content</strong> (required)</td>
    <td><span class="stixtype">string</span></td>
    <td>The content of the note.</td>
  </tr>
  <tr>
    <td><strong>authors</strong> (optional)</td>
    <td><span class="stixtype">list</span> of type <span class="stixtype">string</span></td>
    <td>The name of the author(s) of this note (e.g., the analyst(s) that created it).</td>
  </tr>
  <tr>
    <td><strong>object_refs</strong> (required)</td>
    <td><span class="stixtype">list</span> of type <span class="stixtype">identifier</span></td>
    <td>The STIX Objects that the note is being applied to.</td>
  </tr>
</table>

### 4.13.2 Relationships <a id="note-relationships"></a>

There are no relationships explicitly defined between the Note object and other STIX Objects, other than the embedded relationships listed below.
These embedded relationships are listed by property name along with their corresponding target.

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th colspan='2'><span class='stixtr'>Embedded Relationships</span></th>
  </tr>
  <tr>
    <td width="50%"><strong>created_by_ref</strong></td>
    <td width="50%"><span class="stixtype">identifier</span> (of type <span class="stixtype">identity</span>)</td>
  </tr>
  <tr>
    <td><strong>object_marking_refs</strong></td>
    <td><span class="stixtype">list</span> of type <span class="stixtype">identifier</span> (of type <span class="stixtype">marking-definition</span>)</td>
  </tr>
  <tr>
    <td><strong>object_refs</strong></td>
    <td><span class="stixtype">list</span> of type <span class="stixtype">identifier</span> (of type STIX Object)</td>
  </tr>
</table>

**Example**

*A generic Note defining additional context and shows an optional external reference to a ticketing system.*

```JSON
{
  "type": "note",
  "spec_version": "2.1",
  "id": "note--0c7b5b88-8ff7-4a4d-aa9d-feb398cd0061",
  "created": "2016-05-12T08:17:27.000Z",
  "modified": "2016-05-12T08:17:27.000Z",
  "external_references": [
    {
      "source_name": "job-tracker",
      "external_id": "job-id-1234"
    }
  ],
  "abstract": "Tracking Team Note#1",
  "content": "This note indicates the various steps taken by the threat analyst team to investigate this specific campaign. Step 1) Do a scan 2) Review scanned results for identified hosts not known by external intel…etc.",
  "authors": ["John Doe"],
  "object_refs": ["campaign--8e2e2d2b-17d4-4cbf-938f-98ee46b3cd3f"]
}
```

## 4.14 Observed Data <a id="observed-data"></a>

**Type Name:** <span class="stixtype">observed-data</span>

Observed Data conveys information about cyber security related entities such as files, systems, and networks using the STIX Cyber-observable Objects (SCOs). For example, Observed Data can capture information about an IP address, a network connection, a file, or a registry key. Observed Data is not an intelligence assertion, it is simply the raw information without any context for what it means.

Observed Data can capture that a piece of information was seen one or more times. Meaning, it can capture both a single observation of a single entity (file, network connection) as well as the aggregation of multiple observations of an entity. When the **number_observed** property is 1 the Observed Data represents a single entity. When the **number_observed** property is greater than 1, the Observed Data represents several instances of an entity potentially collected over a period of time. If a time window is known, that can be captured using the **first_observed** and **last_observed** properties. When used to collect aggregate data, it is likely that some properties in the SCO (e.g., timestamp properties) will be omitted because they would differ for each of the individual observations.

Observed Data may be used by itself (without relationships) to convey raw data collected from any source including analyst reports, sandboxes, and network and host-based detection tools. An intelligence producer conveying Observed Data **SHOULD** include as much context (e.g. SCOs) as possible that supports the use of the observed data set in systems expecting to utilize the Observed Data for improved security. This includes all SCOs that matched on an Indicator pattern and are represented in the collected observed event (or events) being conveyed in the Observed Data object. For example, a firewall could emit a single Observed Data instance containing a single Network Traffic object for each connection it sees. The firewall could also aggregate data and instead send out an Observed Data instance every ten minutes with an IP address and an appropriate **number_observed** value to indicate the number of times that IP address was observed in that window. A sandbox could emit an Observed Data instance containing a file hash that it discovered.

Observed Data may also be related to other SDOs to represent raw data that is relevant to those objects. For example, the Sighting Relationship object, can relate an Indicator, Malware, or other SDO to a specific Observed Data to represent the raw information that led to the creation of the Sighting (e.g., what was actually seen that suggested that a particular instance of malware was active).

To support backwards compatibility, related SCOs can still be specified using the **objects** properties, either the **objects** property or the **object_refs** property **MUST** be provided, but both **MUST NOT** be present at the same time.

### 4.14.1 Properties <a id="observed-data-properties"></a>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th><span class="stixtr">Required Common Properties</span></th>
  </tr>
  <tr>
    <td><strong>type</strong>, <strong>spec_version</strong>, <strong>id</strong>, <strong>created</strong>, <strong>modified</strong></td>
  </tr>
  <tr>
    <th><span class="stixtr">Optional Common Properties></span></th>
  </tr>
  <tr>
    <td><strong>created_by_ref</strong>, <strong>revoked</strong>, <strong>labels</strong>, <strong>confidence</strong>, <strong>lang</strong>, <strong>external_references</strong>, <strong>object_marking_refs</strong>, <strong>granular_markings</strong>, <strong>extensions</strong></td>
  </tr>
  <tr>
    <th><span class="stixtr">Not Applicable Common Properties</span></th>
  </tr>
  <tr>
    <td><strong>defanged</strong></td>
  </tr>
  <tr>
    <th><span class="stixtr"> Specific Properties</span></th>
  </tr>
  <tr>
    <td><strong>first_observed</strong>, <strong>last_observed</strong>, <strong>number_observed</strong>, <strong>objects</strong>, <strong>object_refs</strong></td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6">
  <tr>
    <th><span class="stixtr">Property Name</span></th>
    <th><span class="stixtr">Type</span></th>
    <th><span class="stixtr">Description</span></th>
  </tr>
  <tr>
    <td><strong>type</strong> (required)</td>
    <td><span class="stixtype">string</span></td>
    <td>The value of this property <strong>MUST</strong> be <span class="stixliteral">observed-data</span>.</td>
  </tr>
  <tr>
    <td><strong>first_observed</strong> (required)</td>
    <td><span class="stixtype">timestamp</span></td>
    <td>The beginning of the time window during which the data was seen.</td>
  </tr>
  <tr>
    <td><strong>last_observed</strong> (required)</td>
    <td><span class="stixtype">timestamp</span></td>
    <td>The end of the time window during which the data was seen.<br><br>This <strong>MUST</strong> be greater than or equal to the timestamp in the <strong>first_observed</strong> property.</td>
  </tr>
  <tr>
    <td><strong>number_observed</strong> (required)</td>
    <td><span class="stixtype">integer</span></td>
    <td>The number of times that each Cyber-observable object represented in the <strong>objects</strong> or <strong>object_refs</strong> property was seen. If present, this <strong>MUST</strong> be an integer between 1 and 999,999,999 inclusive.<br><br>If the <strong>number_observed</strong> property is greater than 1, the data contained in the <strong>objects</strong> or <strong>object_refs</strong> property was seen multiple times. In these cases, object creators <strong>MAY</strong> omit properties of the SCO (such as timestamps) that are specific to a single instance of that observed data.</td>
  </tr>
  <tr>
    <td><strong>objects</strong> (optional - deprecated)</td>
    <td><span style="white-space: nowrap;"><span class="stixtype">observable-container</span></span></td>
    <td>A dictionary of SCO representing the observation. The dictionary <strong>MUST</strong> contain at least one object.<br><br>The cyber observable content <strong>MAY</strong> include multiple objects if those objects are related as part of a single observation. Multiple objects not related to each other via cyber observable Relationships <strong>MUST NOT</strong> be contained within the same Observed Data instance.<br><br>This property <strong>MUST NOT</strong> be present if <strong>object_refs</strong> is provided.<br><br>For example, a Network Traffic object and two IPv4 Address objects related via the <strong>src_ref</strong> and <strong>dst_ref</strong> properties can be contained in the same Observed Data because they are all related and used to characterize that single entity.<br><br>NOTE: this property is now deprecated in favor of object_refs and will be removed in a future version.</td>
  </tr>
  <tr>
    <td><strong>object_refs</strong> (optional)</td>
    <td><span style="white-space: nowrap;"><span class="stixtype">list</span> of type <span class="stixtype">identifier</span></span></td>
    <td>A list of SCOs and SROs representing the observation. The <strong>object_refs MUST</strong> contain at least one SCO reference if defined.<br><br>The <strong>object_refs MAY</strong> include multiple SCOs and their corresponding SROs, if those SCOs are related as part of a single observation.<br><br>For example, a Network Traffic object and two IPv4 Address objects related via the <strong>src_ref</strong> and <strong>dst_ref</strong> properties can be contained in the same Observed Data because they are all related and used to characterize that single entity.<br><br>This property <strong>MUST NOT</strong> be present if <strong>objects</strong> is provided.</td>
  </tr>
</table>

### 4.14.2 Relationships <a id="observed-data-relationships"></a>

There are no forward relationships explicitly defined between the Observed Data object and other STIX Objects, other than those defined as common relationships. The first section lists the embedded relationships by property name along with their corresponding target. The reverse relationships section illustrates the relationships targeting this object type from another object type. They are included here for convenience. For their definitions, please see the "Source" object.

In addition to the relationships created using the generic Relationship object, Observed Data is also a direct target of the Sighting SRO. Sightings represent a relationship between some intelligence entity that was seen (e.g., an Indicator or Malware instance), where it was seen, and what evidence was actually seen. The evidence (or raw data) in that relationship is captured as Observed Data.

Relationships are not restricted to those listed below. Relationships can be created between any objects using the <span class="stixliteral">related-to</span> relationship type or, as with open vocabularies, user-defined names.

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th colspan='2'><span class='stixtr'>Embedded Relationships</span></th>
  </tr>
  <tr>
    <td width="50%"><strong>created_by_ref</strong></td>
    <td width="50%"><span class="stixtype">identifier</span> (of type <span class="stixtype">identity</span>)</td>
  </tr>
  <tr>
    <td><strong>object_marking_refs</strong></td>
    <td><span class="stixtype">list</span> of type <span class="stixtype">identifier</span> (of type <span class="stixtype">marking-definition</span>)</td>
  </tr>
  <tr>
    <td><strong>object_refs</strong></td>
    <td><span class="stixtype">list</span> of type <span class="stixtype">identifier</span> (of type SCO or SRO)</td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th><span class='stixtr'>Common Relationships</span></th>
  </tr>
  <tr>
    <td><span class="stixliteral">duplicate-of</span>, <span class="stixliteral">derived-from</span>, <span class="stixliteral">related-to</span></td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th width="20%"><span class='stixtr'>Source</span></th>
    <th width="20%""><span class='stixtr'>Relationship Type</span></th>
    <th width="20%"><span class='stixtr'>Target</span></th>
    <th><span class='stixtr'>Description</span></th>
  </tr>
  <tr>
    <td>—</td>
    <td>—</td>
    <td>—</td>
    <td>—</td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th colspan='4'><span class='stixtr'>Reverse Relationships</span></th>
  </tr>
  <tr>
    <td width="20%"><span class="stixtype">indicator</span></td>
    <td width="20%"><span class="stixliteral">based-on</span></td>
    <td width="20%"><span class="stixtype">observed-data</span></td>
    <td>See forward relationship for definition.</td>
  </tr>
  <tr>
    <td><span class="stixtype">infrastructure</span></td>
    <td><span class="stixliteral">consists-of</span></td>
    <td><span class="stixtype">observed-data</span></td>
    <td>See forward relationship for definition</td>
  </tr>
</table>

**Example**

*Observed Data that references two SCOs*

```JSON
{
  "type": "observed-data",
  "spec_version": "2.1",
  "id": "observed-data--b67d30ff-02ac-498a-92f9-32f845f448cf",
  "created_by_ref": "identity--f431f809-377b-45e0-aa1c-6a4751cae5ff",
  "created": "2016-04-06T19:58:16.000Z",
  "modified": "2016-04-06T19:58:16.000Z",
  "first_observed": "2015-12-21T19:00:00Z",
  "last_observed": "2015-12-21T19:00:00Z",
  "number_observed": 50,
  "object_refs": [
    "ipv4-addr--28bb3599-77cd-5a82-a950-b5bc3caf07c4",
    "domain-name--bedb4899-d24b-5401-bc86-8f6b4cc18ec7"
  ]
}
{
  "type": "domain-name",
  "spec_version": "2.1",
  "id": "domain-name--bedb4899-d24b-5401-bc86-8f6b4cc18ec7",
  "value": "example.com",
  "resolves_to_refs": ["ipv4-addr--28bb3599-77cd-5a82-a950-b5bc3caf07c4"]
}
{
  "type": "ipv4-addr",
  "spec_version": "2.1",
  "id": "ipv4-addr--28bb3599-77cd-5a82-a950-b5bc3caf07c4",
  "value": "198.51.100.3"
}
```

## 4.15 Opinion <a id="opinion"></a>

**Type Name**: <span class="stixtype">opinion</span>

An Opinion is an assessment of the correctness of the information in a STIX Object produced by a different entity.
The primary property is the **opinion** property, which captures the level of agreement or disagreement using a fixed scale.
That fixed scale also supports a numeric mapping to allow for consistent statistical operations across opinions.

For example, an analyst from a consuming organization might say that they "strongly disagree" with a Campaign object and provide an explanation about why.
In a more automated workflow, a SOC operator might give an Indicator "one star" in their TIP (expressing "strongly disagree") because it is considered to be a false positive within their environment.
Opinions are subjective, and the specification does not address how best to interpret them.
Sharing communities are encouraged to provide clear guidelines to their constituents regarding best practice for the use of Opinion objects within the community.

Because Opinions are typically (though not always) created by human analysts and are comprised of human-oriented text, they contain an additional property to capture the analyst(s) that created the Opinion.
This is distinct from the **created_by_ref** property, which is meant to capture the organization that created the object.

### 4.15.1 Properties <a id="opinion-properties"></a>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th><span class="stixtr">Required Common Properties</span></th>
  </tr>
  <tr>
    <td><strong>type</strong>, <strong>spec_version</strong>, <strong>id</strong>, <strong>created</strong>, <strong>modified</strong></td>
  </tr>
  <tr>
    <th><span class="stixtr">Optional Common Properties></span></th>
  </tr>
  <tr>
    <td><strong>created_by_ref</strong>, <strong>revoked</strong>, <strong>labels</strong>, <strong>confidence</strong>, <strong>lang</strong>, <strong>external_references</strong>, <strong>object_marking_refs</strong>, <strong>granular_markings</strong>, <strong>extensions</strong></td>
  </tr>
  <tr>
    <th><span class="stixtr">Not Applicable Common Properties</span></th>
  </tr>
  <tr>
    <td><strong>defanged</strong></td>
  </tr>
  <tr>
    <th><span class="stixtr"> Specific Properties</span></th>
  </tr>
  <tr>
    <td><strong>explanation</strong>, <strong>authors</strong>, <strong>opinion</strong>, <strong>object_refs</strong></td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6">
  <tr>
    <th><span class="stixtr">Property Name</span></th>
    <th><span class="stixtr">Type</span></th>
    <th><span class="stixtr">Description</span></th>
  </tr>
  <tr>
    <td><strong>type</strong> (required)</td>
    <td><span class="stixtype">string</span></td>
    <td>The value of this property <strong>MUST</strong> be <span class="stixliteral">opinion</span>.</td>
  </tr>
  <tr>
    <td><strong>explanation</strong> (optional)</td>
    <td><span class="stixtype">string</span></td>
    <td>An explanation of why the producer has this Opinion. For example, if an Opinion of strongly-disagree is given, the explanation can contain an explanation of why the Opinion producer disagrees and what evidence they have for their disagreement.</td>
  </tr>
  <tr>
    <td><strong>authors</strong> (optional)</td>
    <td><span style="white-space: nowrap;"><span class="stixtype">list</span> of type <span class="stixtype">string</span></span></td>
    <td>The name of the author(s) of this Opinion (e.g., the analyst(s) that created it).</td>
  </tr>
  <tr>
    <td><strong>opinion</strong> (required)</td>
    <td><span class="stixtype">enum</span></td>
    <td>The opinion that the producer has about all of the STIX Object(s) listed in the <strong>object_refs</strong> property.<br><br>The values of this property <strong>MUST</strong> come from the <span class="stixliteral"><a href="#opinion-enumeration">opinion-enum</a></span> enumeration.</td>
  </tr>
  <tr>
    <td><strong>object_refs</strong> (required)</td>
    <td><span style="white-space: nowrap;"><span class="stixtype">list</span> of type <span class="stixtype">identifier</span></span></td>
    <td>The STIX Objects that the Opinion is being applied to.</td>
  </tr>
</table>

### 4.15.2 Relationships <a id="opinion-relationships"></a>

There are no relationships explicitly defined between the Opinion object and other STIX Objects, other than those defined as common relationships. The first section lists the embedded relationships by property name along with their corresponding target.

Relationships are not restricted to those listed below. Relationships can be created between any objects using the <span class="stixliteral">related-to</span> relationship name or, as with open vocabularies, user-defined names.

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th colspan='2'><span class='stixtr'>Embedded Relationships</span></th>
  </tr>
  <tr>
    <td width="50%"><strong>created_by_ref</strong></td>
    <td width="50%"><span class="stixtype">identifier</span> (of type <span class="stixtype">identity</span>)</td>
  </tr>
  <tr>
    <td><strong>object_marking_refs</strong></td>
    <td><span class="stixtype">list</span> of type <span class="stixtype">identifier</span> (of type <span class="stixtype">marking-definition</span>)</td>
  </tr>
  <tr>
    <td><strong>object_refs</strong></td>
    <td><span class="stixtype">list</span> of type <span class="stixtype">identifier</span> (of type any STIX Object type)</td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th><span class='stixtr'>Common Relationships</span></th>
  </tr>
  <tr>
    <td><span class="stixliteral">duplicate-of</span>, <span class="stixliteral">derived-from</span>, <span class="stixliteral">related-to</span></td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th width="20%"><span class='stixtr'>Source</span></th>
    <th width="20%""><span class='stixtr'>Relationship Type</span></th>
    <th width="20%"><span class='stixtr'>Target</span></th>
    <th><span class='stixtr'>Description</span></th>
  </tr>
  <tr>
    <td>—</td>
    <td>—</td>
    <td>—</td>
    <td>—</td>
  </tr>
</table>

**Example**

```JSON
{
  "type": "opinion",
  "spec_version": "2.1",
  "id": "opinion--b01efc25-77b4-4003-b18b-f6e24b5cd9f7",
  "created_by_ref": "identity--f431f809-377b-45e0-aa1c-6a4751cae5ff",
  "created": "2016-05-12T08:17:27.000Z",
  "modified": "2016-05-12T08:17:27.000Z",
  "object_refs": ["relationship--16d2358f-3b0d-4c88-b047-0da2f7ed4471"],
  "opinion": "strongly-disagree",
  "explanation": "This doesn't seem like it is feasible. We've seen how PandaCat has attacked Spanish infrastructure over the last 3 years, so this change in targeting seems too great to be viable. The methods used are more commonly associated with the FlameDragonCrew."
}
```

## 4.16 Report <a id="report"></a>

**Type Name:** <span class="stixtype">report</span>

Reports are collections of threat intelligence focused on one or more topics, such as a description of a threat actor, malware, or attack technique, including context and related details. They are used to group related threat intelligence together so that it can be published as a comprehensive cyber threat story.

The Report SDO contains a list of references to STIX Objects (the CTI objects included in the report) along with a textual description and the name of the report.

For example, a threat report produced by ACME Defense Corp. discussing the Glass Gazelle campaign should be represented using Report. The Report itself would contain the narrative of the report while the Campaign SDO and any related SDOs (e.g., Indicators for the Campaign, Malware it uses, and the associated Relationships) would be referenced in the report contents.

### 4.16.1 Properties <a id="report-properties"></a>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th><span class="stixtr">Required Common Properties</span></th>
  </tr>
  <tr>
    <td><strong>type</strong>, <strong>spec_version</strong>, <strong>id</strong>, <strong>created</strong>, <strong>modified</strong></td>
  </tr>
  <tr>
    <th><span class="stixtr">Optional Common Properties></span></th>
  </tr>
  <tr>
    <td><strong>created_by_ref</strong>, <strong>revoked</strong>, <strong>labels</strong>, <strong>confidence</strong>, <strong>lang</strong>, <strong>external_references</strong>, <strong>object_marking_refs</strong>, <strong>granular_markings</strong>, <strong>extensions</strong></td>
  </tr>
  <tr>
    <th><span class="stixtr">Not Applicable Common Properties</span></th>
  </tr>
  <tr>
    <td><strong>defanged</strong></td>
  </tr>
  <tr>
    <th><span class="stixtr"> Specific Properties</span></th>
  </tr>
  <tr>
    <td><strong>name</strong>, <strong>description</strong>, <strong>report_types</strong>, <strong>published</strong>, <strong>object_refs</strong></td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6">
  <tr>
    <th><span class="stixtr">Property Name</span></th>
    <th><span class="stixtr">Type</span></th>
    <th><span class="stixtr">Description</span></th>
  </tr>
  <tr>
    <td><strong>type</strong> (required)</td>
    <td><span class="stixtype">string</span></td>
    <td>The value of this property <strong>MUST</strong> be <span class="stixliteral">report</span>.</td>
  </tr>
  <tr>
    <td><strong>name</strong> (required)</td>
    <td><span class="stixtype">string</span></td>
    <td>A name or characterizing text used to identify the Report.</td>
  </tr>
  <tr>
    <td><strong>description</strong> (optional)</td>
    <td><span class="stixtype">string</span></td>
    <td>A description that provides more details and context about the Report, potentially including its purpose and its key characteristics.</td>
  </tr>
  <tr>
    <td><strong>report_types</strong> (optional)</td>
    <td><span style="white-space: nowrap;"><span class="stixtype">list</span> of type <span class="stixtype">open-vocab</span></span></td>
    <td>The primary type(s) of content found in this report.<br><br>The values for this property <strong>SHOULD</strong> come from the <span class="stixliteral"><a href="#report-type-vocabulary">report-type-ov</a></span> open vocabulary.</td>
  </tr>
  <tr>
    <td><strong>published</strong> (required)</td>
    <td><span class="stixtype">timestamp</span></td>
    <td>The date that this Report object was officially published by the creator of this report.<br><br>The publication date (public release, legal release, etc.) may be different than the date the report was created or shared internally (the date in the <strong>created</strong> property).</td>
  </tr>
  <tr>
    <td><strong>object_refs</strong> (required)</td>
    <td><span style="white-space: nowrap;"><span class="stixtype">list</span> of type <span class="stixtype">identifier</span></span></td>
    <td>Specifies the STIX Objects that are referred to by this Report.</td>
  </tr>
</table>

### 4.16.2 Relationships <a id="report-relationships"></a>

There are no relationships explicitly defined between the Report object and other STIX Objects, other than those defined as common relationships. The first section lists the embedded relationships by property name along with their corresponding target.

Relationships are not restricted to those listed below. Relationships can be created between any objects using the <span class="stixliteral">related-to</span> relationship name or, as with open vocabularies, user-defined names.

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th colspan='2'><span class='stixtr'>Embedded Relationships</span></th>
  </tr>
  <tr>
    <td width="50%"><strong>created_by_ref</strong></td>
    <td width="50%"><span class="stixtype">identifier</span> (of type <span class="stixtype">identity</span>)</td>
  </tr>
  <tr>
    <td><strong>object_marking_refs</strong></td>
    <td><span class="stixtype">list</span> of type <span class="stixtype">identifier</span> (of type <span class="stixtype">marking-definition</span>)</td>
  </tr>
  <tr>
    <td><strong>object_refs</strong></td>
    <td><span class="stixtype">list</span> of type <span class="stixtype">identifier</span> (of type any STIX Object type)</td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th><span class='stixtr'>Common Relationships</span></th>
  </tr>
  <tr>
    <td><span class="stixliteral">duplicate-of</span>, <span class="stixliteral">derived-from</span>, <span class="stixliteral">related-to</span></td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th width="20%"><span class='stixtr'>Source</span></th>
    <th width="20%""><span class='stixtr'>Relationship Type</span></th>
    <th width="20%"><span class='stixtr'>Target</span></th>
    <th><span class='stixtr'>Description</span></th>
  </tr>
  <tr>
    <td>—</td>
    <td>—</td>
    <td>—</td>
    <td>—</td>
  </tr>
</table>

**Examples**



*A standalone Report; the consumer may or may not already have access to the referenced STIX Objects.*

```JSON
{
  "type": "report",
  "spec_version": "2.1",
  "id": "report--84e4d88f-44ea-4bcd-bbf3-b2c1c320bcb3",
  "created_by_ref": "identity--a463ffb3-1bd9-4d94-b02d-74e4f1658283",
  "created": "2015-12-21T19:59:11.000Z",
  "modified": "2015-12-21T19:59:11.000Z",
  "name": "The Black Vine Cyberespionage Group",
  "description": "A simple report with an indicator and campaign",
  "published": "2016-01-20T17:00:00.000Z",
  "report_types": ["campaign"],
  "object_refs": [
    "indicator--26ffb872-1dd9-446e-b6f5-d58527e5b5d2",
    "campaign--83422c77-904c-4dc1-aff5-5c38f3a2c55c",
    "relationship--f82356ae-fe6c-437c-9c24-6b64314ae68a"
  ]
}
```

*A Bundle with a Report and the STIX Objects that are referred to by the Report*

```JSON
{
  "type": "bundle",
  "id": "bundle--44af6c39-c09b-49c5-9de2-394224b04982",
  "objects": [
    {
      "type": "identity",
      "spec_version": "2.1",
      "id": "identity--a463ffb3-1bd9-4d94-b02d-74e4f1658283",
      "created": "2015-01-21T19:59:17.000Z",
      "modified": "2015-01-21T19:59:17.000Z",
      "name": "Acme Cybersecurity Solutions"
    },
    {
      "type": "report",
      "spec_version": "2.1",
      "id": "report--84e4d88f-44ea-4bcd-bbf3-b2c1c320bcbd",
      "created_by_ref": "identity--a463ffb3-1bd9-4d94-b02d-74e4f1658283",
      "created": "2015-12-21T19:59:11.000Z",
      "modified": "2016-05-21T19:59:11.000Z",
      "name": "The Black Vine Cyberespionage Group",
      "description": "A simple report with an indicator and campaign",
      "published": "2016-01-20T17:00:00.000Z",
      "report_types": ["campaign"],
      "object_refs": [
        "indicator--26ffb872-1dd9-446e-b6f5-d58527e5b5d2",
        "campaign--83422c77-904c-4dc1-aff5-5c38f3a2c55c",
        "relationship--f82356ae-fe6c-437c-9c24-6b64314ae68a"
      ]
    },
    {
      "type": "indicator",
      "spec_version": "2.1",
      "id": "indicator--26ffb872-1dd9-446e-b6f5-d58527e5b5d2",
      "created": "2015-12-21T19:59:17.000Z",
      "modified": "2016-05-21T19:59:17.000Z",
      "name": "Some indicator",
      "indicator_types": ["malicious-activity"],
      "pattern": "[ file:hashes.MD5 = '3773a88f65a5e780c8dff9cdc3a056f3' ]",
      "valid_from": "2015-12-21T19:59:17Z",
      "created_by_ref": "identity--a463ffb3-1bd9-4d94-b02d-74e4f1658283"
    },
    {
      "type": "campaign",
      "spec_version": "2.1",
      "id": "campaign--83422c77-904c-4dc1-aff5-5c38f3a2c55c",
      "created_by_ref": "identity--a463ffb3-1bd9-4d94-b02d-74e4f1658283",
      "created": "2015-12-21T19:59:17.000Z",
      "modified": "2016-05-21T19:59:17.000Z",
      "name": "Some Campaign"
    },
    {
      "type": "relationship",
      "spec_version": "2.1",
      "id": "relationship--f82356ae-fe6c-437c-9c24-6b64314ae68a",
      "created_by_ref": "identity--a463ffb3-1bd9-4d94-b02d-74e4f1658283",
      "created": "2015-12-21T19:59:17.000Z",
      "modified": "2015-12-21T19:59:17.000Z",
      "source_ref": "indicator--26ffb872-1dd9-446e-b6f5-d58527e5b5d2",
      "target_ref": "campaign--83422c77-904c-4dc1-aff5-5c38f3a2c55c",
      "relationship_type": "indicates"
    }
  ]
}
```

## 4.17 Threat Actor <a id="threat-actor"></a>

**Type Name:** <span class="stixtype">threat-actor</span>

Threat Actors are actual individuals, groups, or organizations believed to be operating with malicious intent. A Threat Actor is not an Intrusion Set but may support or be affiliated with various Intrusion Sets, groups, or organizations over time.

Threat Actors leverage their resources, and possibly the resources of an Intrusion Set, to conduct attacks and run Campaigns against targets.

Threat Actors can be characterized by their motives, capabilities, goals, sophistication level, past activities, resources they have access to, and their role in the organization.

### 4.17.1 Properties <a id="threat-actor-properties"></a>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th><span class="stixtr">Required Common Properties</span></th>
  </tr>
  <tr>
    <td><strong>type</strong>, <strong>spec_version</strong>, <strong>id</strong>, <strong>created</strong>, <strong>modified</strong></td>
  </tr>
  <tr>
    <th><span class="stixtr">Optional Common Properties></span></th>
  </tr>
  <tr>
    <td><strong>created_by_ref</strong>, <strong>revoked</strong>, <strong>labels</strong>, <strong>confidence</strong>, <strong>lang</strong>, <strong>external_references</strong>, <strong>object_marking_refs</strong>, <strong>granular_markings</strong>, <strong>extensions</strong></td>
  </tr>
  <tr>
    <th><span class="stixtr">Not Applicable Common Properties</span></th>
  </tr>
  <tr>
    <td><strong>defanged</strong></td>
  </tr>
  <tr>
    <th><span class="stixtr"> Specific Properties</span></th>
  </tr>
  <tr>
    <td><strong>name</strong>, <strong>description</strong>, <strong>threat_actor_types</strong>, <strong>aliases</strong>, <strong>first_seen</strong>, <strong>last_seen</strong>, <strong>roles</strong>, <strong>goals</strong>, <strong>sophistication</strong>, <strong>resource_level</strong>, <strong>primary_motivation</strong>, <strong>secondary_motivations</strong>, <strong>personal_motivations</strong></td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6">
  <tr>
    <th><span class="stixtr">Property Name</span></th>
    <th><span class="stixtr">Type</span></th>
    <th><span class="stixtr">Description</span></th>
  </tr>
  <tr>
    <td><strong>type</strong> (required)</td>
    <td><span class="stixtype">string</span></td>
    <td>The value of this property <strong>MUST</strong> be <span class="stixliteral">threat-actor</span>.</td>
  </tr>
  <tr>
    <td><strong>name</strong> (required)</td>
    <td><span class="stixtype">string</span></td>
    <td>A name or characterizing text used to identify the Threat Actor or Threat Actor group.</td>
  </tr>
  <tr>
    <td><strong>description</strong> (optional)</td>
    <td><span class="stixtype">string</span></td>
    <td>A description that provides more details and context about the Threat Actor, potentially including its purpose and its key characteristics.</td>
  </tr>
  <tr>
    <td><strong>threat_actor_types</strong> (optional)</td>
    <td><span style="white-space: nowrap;"><span class="stixtype">list</span> of type <span class="stixtype">open-vocab</span></span></td>
    <td>The type(s) of this threat actor.<br><br>The values for this property <strong>SHOULD</strong> come from the <span class="stixliteral"><a href="#threat-actor-type-vocabulary">threat-actor-type-ov</a></span> open vocabulary.</td>
  </tr>
  <tr>
    <td><strong>aliases</strong> (optional)</td>
    <td><span style="white-space: nowrap;"><span class="stixtype">list</span> of type <span class="stixtype">string</span></span></td>
    <td>A list of other names that this Threat Actor is believed to use.</td>
  </tr>
  <tr>
    <td><strong>first_seen</strong> (optional)</td>
    <td><span class="stixtype">timestamp</span></td>
    <td>The time that this Threat Actor was first seen.<br><br>This property is a summary property of data from sightings and other data that may or may not be available in STIX. If new sightings are received that are earlier than the first seen timestamp, the object may be updated to account for the new data.</td>
  </tr>
  <tr>
    <td><strong>last_seen</strong> (optional)</td>
    <td><span class="stixtype">timestamp</span></td>
    <td>The time that this Threat Actor was last seen.<br><br>This property is a summary property of data from sightings and other data that may or may not be available in STIX. If new sightings are received that are later than the last seen timestamp, the object may be updated to account for the new data. If this property and the <strong>first_seen</strong> property are both defined, then this property <strong>MUST</strong> be greater than or equal to the timestamp in the <strong>first_seen</strong> property.</td>
  </tr>
  <tr>
    <td><strong>roles</strong> (optional)</td>
    <td><span style="white-space: nowrap;"><span class="stixtype">list</span> of type <span class="stixtype">open-vocab</span></span></td>
    <td>A list of roles the Threat Actor plays.<br><br>The values for this property <strong>SHOULD</strong> come from the <span class="stixliteral"><a href="#threat-actor-role-vocabulary">threat-actor-role-ov</a></span> open vocabulary.</td>
  </tr>
  <tr>
    <td><strong>goals</strong> (optional)</td>
    <td><span style="white-space: nowrap;"><span class="stixtype">list</span> of type <span class="stixtype">string</span></span></td>
    <td>The high-level goals of this Threat Actor, namely, *what* are they trying to do. For example, they may be motivated by personal gain, but their goal is to steal credit card numbers. To do this, they may execute specific Campaigns that have detailed objectives like compromising point of sale systems at a large retailer.</td>
  </tr>
  <tr>
    <td><strong>sophistication</strong> (optional)</td>
    <td><span class="stixtype">open-vocab</span></td>
    <td>The skill, specific knowledge, special training, or expertise a Threat Actor must have to perform the attack.<br><br>The value for this property <strong>SHOULD</strong> come from the <span class="stixliteral"><a href="#threat-actor-sophistication-vocabulary">threat-actor-sophistication-ov</a></span> open vocabulary.</td>
  </tr>
  <tr>
    <td><strong>resource_level</strong> (optional)</td>
    <td><span class="stixtype">open-vocab</span></td>
    <td>The organizational level at which this Threat Actor typically works, which in turn determines the resources available to this Threat Actor for use in an attack. This attribute is linked to the <strong>sophistication</strong> property — a specific resource level implies that the Threat Actor has access to at least a specific sophistication level.<br><br>The value for this property <strong>SHOULD</strong> come from the <span class="stixliteral"><a href="#attack-resource-level-vocabulary">attack-resource-level-ov</a></span> open vocabulary.</td>
  </tr>
  <tr>
    <td><strong>primary_motivation</strong> (optional)</td>
    <td><span class="stixtype">open-vocab</span></td>
    <td>The primary reason, motivation, or purpose behind this Threat Actor. The motivation is *why* the Threat Actor wishes to achieve the goal (what they are trying to achieve).<br><br>The value for this property <strong>SHOULD</strong> come from the <span class="stixliteral"><a href="#attack-motivation-vocabulary">attack-motivation-ov</a></span> open vocabulary.</td>
  </tr>
  <tr>
    <td><strong>secondary_motivations</strong> (optional)</td>
    <td><span style="white-space: nowrap;"><span class="stixtype">list</span> of type <span class="stixtype">open-vocab</span></span></td>
    <td>This property specifies the secondary reasons, motivations, or purposes behind this Threat Actor.<br><br>These motivations can exist as an equal or near-equal cause to the primary motivation. However, it does not replace or necessarily magnify the primary motivation, but it might indicate additional context. The position in the list has no significance.<br><br>The value for this property <strong>SHOULD</strong> come from the <span class="stixliteral"><a href="#attack-motivation-vocabulary">attack-motivation-ov</a></span> open vocabulary.</td>
  </tr>
  <tr>
    <td><strong>personal_motivations</strong> (optional)</td>
    <td><span style="white-space: nowrap;"><span class="stixtype">list</span> of type <span class="stixtype">open-vocab</span></span></td>
    <td>The personal reasons, motivations, or purposes of the Threat Actor regardless of organizational goals.<br><br>Personal motivation, which is independent of the organization's goals, describes what impels an individual to carry out an attack. Personal motivation may align with the organization's motivation — as is common with activists — but more often it supports personal goals. For example, an individual analyst may join a Data Miner corporation because his or her skills may align with the corporation's objectives. But the analyst most likely performs his or her daily work toward those objectives for personal reward in the form of a paycheck. The motivation of personal reward may be even stronger for Threat Actors who commit illegal acts, as it is more difficult for someone to cross that line purely for altruistic reasons. The position in the list has no significance.<br><br>The values for this property <strong>SHOULD</strong> come from the <span class="stixliteral"><a href="#attack-motivation-vocabulary">attack-motivation-ov</a></span> open vocabulary.</td>
  </tr>
</table>

### 4.17.2 Relationships <a id="threat-actor-relationships"></a>

These are the relationships explicitly defined between the Threat Actor object and other STIX Objects. The first section lists the embedded relationships by property name along with their corresponding target. The rest of the table identifies the relationships that can be made from this object type to another object type by way of the Relationship object. The reverse relationships section illustrates the relationships targeting this object type from another object type. They are included here for convenience. For their definitions, please see the "Source" object.

Relationships are not restricted to those listed below. Relationships can be created between any objects using the <span class="stixliteral">related-to</span> relationship type or, as with open vocabularies, user-defined names.

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th colspan='2'><span class='stixtr'>Embedded Relationships</span></th>
  </tr>
  <tr>
    <td width="50%"><strong>created_by_ref</strong></td>
    <td width="50%"><span class="stixtype">identifier</span> (of type <span class="stixtype">identity</span>)</td>
  </tr>
  <tr>
    <td><strong>object_marking_refs</strong></td>
    <td><span class="stixtype">list</span> of type <span class="stixtype">identifier</span> (of type <span class="stixtype">marking-definition</span>)</td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th><span class='stixtr'>Common Relationships</span></th>
  </tr>
  <tr>
    <td><span class="stixliteral">duplicate-of</span>, <span class="stixliteral">derived-from</span>, <span class="stixliteral">related-to</span></td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6">
  <tr>
    <th width="20%"><span class='stixtr'>Source</span></th>
    <th width="20%""><span class='stixtr'>Relationship Type</span></th>
    <th width="20%"><span class='stixtr'>Target</span></th>
    <th><span class='stixtr'>Description</span></th>
  </tr>
  <tr>
    <td><span class="stixtype">threat-actor</span></td>
    <td><span class="stixliteral">attributed-to</span></td>
    <td><span class="stixtype">identity</span></td>
    <td>This Relationship describes that the Threat Actor's real identity is the related Identity.<br><br>For example, an <span class="stixliteral">attributed-to</span> Relationship from the jay-sm17h Threat Actor to the John Smith Identity means that the actor known as jay-sm17h is John Smith.</td>
  </tr>
  <tr>
    <td><span class="stixtype">threat-actor</span></td>
    <td><span class="stixliteral">compromises</span></td>
    <td><span class="stixtype">infrastructure</span></td>
    <td>This Relationship describes that the Threat Actor compromises the related Infrastructure.</td>
  </tr>
  <tr>
    <td><span class="stixtype">threat-actor</span></td>
    <td><span class="stixliteral">hosts</span>, <span class="stixliteral">owns</span></td>
    <td><span class="stixtype">infrastructure</span></td>
    <td>This Relationship describes that the Threat Actor hosts or owns the related Infrastructure (e.g. an actor that rents botnets to other threat actors).</td>
  </tr>
  <tr>
    <td><span class="stixtype">threat-actor</span></td>
    <td><span class="stixliteral">impersonates</span></td>
    <td><span class="stixtype">identity</span></td>
    <td>This Relationship describes that the Threat Actor impersonates the related Identity.<br><br>For example, an <span class="stixliteral">impersonates</span> Relationship from the gh0st Threat Actor to the ACME Corp. Identity means that the actor known as gh0st impersonates ACME Corp.</td>
  </tr>
  <tr>
    <td><span class="stixtype">threat-actor</span></td>
    <td><span class="stixliteral">located-at</span></td>
    <td><span class="stixtype">location</span></td>
    <td>This Relationship describes that the Threat Actor is located at or in the related Location.<br><br>For example, a <span class="stixliteral">located-at</span> relationship from the gh0st Threat Actor to a Location representing the United States means that ACME Corporation is located in the United States.</td>
  </tr>
  <tr>
    <td><span class="stixtype">threat-actor</span></td>
    <td><span class="stixliteral">targets</span></td>
    <td><span class="stixtype">identity</span>, <span class="stixtype">location</span>, <span class="stixtype">vulnerability</span></td>
    <td>This Relationship describes that the Threat Actor uses exploits of the related Vulnerability or targets the type of victims described by the related Identity or Location.<br><br>For example, a <span class="stixliteral">targets</span> Relationship from the jay-sm17h Threat Actor to a Vulnerability in a blogging platform indicates that attacks performed by John Smith often exploit that Vulnerability.<br><br>Similarly, a <span class="stixliteral">targets</span> Relationship from the jay-sm17h Threat Actor to an Identity describing the energy sector in the United States means that John Smith often carries out attacks against targets in that sector.</td>
  </tr>
  <tr>
    <td><span class="stixtype">threat-actor</span></td>
    <td><span class="stixliteral">uses</span></td>
    <td><span class="stixtype">attack-pattern</span>, <span class="stixtype">infrastructure</span>, <span class="stixtype">malware</span>, <span class="stixtype">tool</span></td>
    <td>This Relationship describes that attacks carried out as part of the Threat Actor typically use the related Attack Pattern, Infrastructure, Malware, or Tool.<br><br>For example, a <span class="stixliteral">uses</span> Relationship from the jay-sm17h Threat Actor to the xInject Malware indicates that xInject is often used by John Smith.<br><br>A campaign, threat actor, intrusion set, malware, or tool takes infrastructure and compromises and/or uses it for their own.</td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th colspan='4'><span class='stixtr'>Reverse Relationships</span></th>
  </tr>
  <tr>
    <td width="20%"><span class="stixtype">campaign</span>, <span class="stixtype">intrusion-set</span></td>
    <td width="20%"><span class="stixliteral">attributed-to</span></td>
    <td width="20%"><span class="stixtype">threat-actor</span></td>
    <td>See forward relationship for definition.</td>
  </tr>
  <tr>
    <td><span class="stixtype">malware</span></td>
    <td><span class="stixliteral">authored-by</span></td>
    <td><span class="stixtype">threat-actor</span></td>
    <td>See forward relationship for definition.</td>
  </tr>
  <tr>
    <td><span class="stixtype">indicator</span></td>
    <td><span class="stixliteral">indicates</span></td>
    <td><span class="stixtype">threat-actor</span></td>
    <td>See forward relationship for definition.</td>
  </tr>
</table>

**Example**

```JSON
{
  "type": "threat-actor",
  "spec_version": "2.1",
  "id": "threat-actor--8e2e2d2b-17d4-4cbf-938f-98ee46b3cd3f",
  "created_by_ref": "identity--f431f809-377b-45e0-aa1c-6a4751cae5ff",
  "created": "2016-04-06T20:03:48.000Z",
  "modified": "2016-04-06T20:03:48.000Z",
  "threat_actor_types": [ "crime-syndicate"],
  "name": "Evil Org",
  "description": "The Evil Org threat actor group",
  "aliases": ["Syndicate 1", "Evil Syndicate 99"],
  "roles": ["director"],
  "goals": ["Steal bank money", "Steal credit cards"],
  "sophistication": "advanced",
  "resource_level": "team",
  "primary_motivation": "organizational-gain"
}
```

## 4.18 Tool <a id="tool"></a>

**Type Name:** <span class="stixtype">tool</span>

Tools are legitimate software that can be used by threat actors to perform attacks. Knowing how and when threat actors use such tools can be important for understanding how campaigns are executed. Unlike malware, these tools or software packages are often found on a system and have legitimate purposes for power users, system administrators, network administrators, or even normal users. Remote access tools (e.g., RDP) and network scanning tools (e.g., Nmap) are examples of Tools that may be used by a Threat Actor during an attack.

The Tool SDO characterizes the properties of these software tools and can be used as a basis for making an assertion about how a Threat Actor uses them during an attack. It contains properties to name and describe the tool, a list of Kill Chain Phases the tool can be used to carry out, and the version of the tool.

This SDO **MUST NOT** be used to characterize malware. Further, Tool **MUST NOT** be used to characterize tools used as part of a course of action in response to an attack.

### 4.18.1 Properties <a id="tool-properties"></a>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th><span class="stixtr">Required Common Properties</span></th>
  </tr>
  <tr>
    <td><strong>type</strong>, <strong>spec_version</strong>, <strong>id</strong>, <strong>created</strong>, <strong>modified</strong></td>
  </tr>
  <tr>
    <th><span class="stixtr">Optional Common Properties></span></th>
  </tr>
  <tr>
    <td><strong>created_by_ref</strong>, <strong>revoked</strong>, <strong>labels</strong>, <strong>confidence</strong>, <strong>lang</strong>, <strong>external_references</strong>, <strong>object_marking_refs</strong>, <strong>granular_markings</strong>, <strong>extensions</strong></td>
  </tr>
  <tr>
    <th><span class="stixtr">Not Applicable Common Properties</span></th>
  </tr>
  <tr>
    <td><strong>defanged</strong></td>
  </tr>
  <tr>
    <th><span class="stixtr"> Specific Properties</span></th>
  </tr>
  <tr>
    <td><strong>name</strong>, <strong>description</strong>, <strong>tool_types</strong>, <strong>aliases</strong>, <strong>kill_chain_phases</strong>, <strong>tool_version</strong></td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6">
  <tr>
    <th><span class="stixtr">Property Name</span></th>
    <th><span class="stixtr">Type</span></th>
    <th><span class="stixtr">Description</span></th>
  </tr>
  <tr>
    <td><strong>type</strong> (required)</td>
    <td><span class="stixtype">string</span></td>
    <td>The value of this property <strong>MUST</strong> be <span class="stixliteral">tool</span>.</td>
  </tr>
  <tr>
    <td><strong>name</strong> (required)</td>
    <td><span class="stixtype">string</span></td>
    <td>A name or characterizing text used to identify the Tool.</td>
  </tr>
  <tr>
    <td><strong>description</strong> (optional)</td>
    <td><span class="stixtype">string</span></td>
    <td>A description that provides more details and context about the Tool, potentially including its purpose and its key characteristics.</td>
  </tr>
  <tr>
    <td><strong>tool_types</strong> (optional)</td>
    <td><span style="white-space: nowrap;"><span class="stixtype">list</span> of type <span class="stixtype">open-vocab</span></span></td>
    <td>The kind(s) of tool(s) being described.<br><br>The values for this property <strong>SHOULD</strong> come from the <span class="stixliteral"><a href="#tool-type-vocabulary">tool-type-ov</a></span> open vocabulary.</td>
  </tr>
  <tr>
    <td><strong>aliases</strong> (optional)</td>
    <td><span style="white-space: nowrap;"><span class="stixtype">list</span> of type <span class="stixtype">string</span></span></td>
    <td>Alternative names used to identify this Tool.</td>
  </tr>
  <tr>
    <td><strong>kill_chain_phases</strong> (optional)</td>
    <td><span style="white-space: nowrap;"><span class="stixtype">list</span> of type <span class="stixtype">kill-chain-phase</span></span></td>
    <td>The list of kill chain phases for which this Tool can be used.</td>
  </tr>
  <tr>
    <td><strong>tool_version</strong> (optional)</td>
    <td><span class="stixtype">string</span></td>
    <td>The version identifier associated with the Tool.</td>
  </tr>
</table>

### 4.18.2 Relationships <a id="tool-relationships"></a>

These are the relationships explicitly defined between the Tool object and other STIX Objects. The first section lists the embedded relationships by property name along with their corresponding target. The rest of the table identifies the relationships that can be made from this object type to another object type by way of the Relationship object. The reverse relationships section illustrates the relationships targeting this object type from another object type. They are included here for convenience. For their definitions, please see the "Source" object.

Relationships are not restricted to those listed below. Relationships can be created between any objects using the <span class="stixliteral">related-to</span> relationship type or, as with open vocabularies, user-defined names.

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th colspan='2'><span class='stixtr'>Embedded Relationships</span></th>
  </tr>
  <tr>
    <td width="50%"><strong>created_by_ref</strong></td>
    <td width="50%"><span class="stixtype">identifier</span> (of type <span class="stixtype">identity</span>)</td>
  </tr>
  <tr>
    <td><strong>object_marking_refs</strong></td>
    <td><span class="stixtype">list</span> of type <span class="stixtype">identifier</span> (of type <span class="stixtype">marking-definition</span>)</td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th><span class='stixtr'>Common Relationships</span></th>
  </tr>
  <tr>
    <td><span class="stixliteral">duplicate-of</span>, <span class="stixliteral">derived-from</span>, <span class="stixliteral">related-to</span></td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6">
  <tr>
    <th width="20%"><span class='stixtr'>Source</span></th>
    <th width="20%""><span class='stixtr'>Relationship Type</span></th>
    <th width="20%"><span class='stixtr'>Target</span></th>
    <th><span class='stixtr'>Description</span></th>
  </tr>
  <tr>
    <td><span class="stixtype">tool</span></td>
    <td><span class="stixliteral">delivers</span></td>
    <td><span class="stixtype">malware</span></td>
    <td>This Relationship describes that this Tool is used to deliver a malware instance (or family).</td>
  </tr>
  <tr>
    <td><span class="stixtype">tool</span></td>
    <td><span class="stixliteral">drops</span></td>
    <td><span class="stixtype">malware</span></td>
    <td>This Relationship documents that this Tool drops a malware instance (or family).</td>
  </tr>
  <tr>
    <td><span class="stixtype">tool</span></td>
    <td><span class="stixliteral">has</span></td>
    <td><span class="stixtype">vulnerability</span></td>
    <td>This Relationship describes that this specific Tool has this specific Vulnerability.<br><br>For example, a tool may not have been patched and currently is impacted by a CVE.</td>
  </tr>
  <tr>
    <td><span class="stixtype">tool</span></td>
    <td><span class="stixliteral">targets</span></td>
    <td><span class="stixtype">identity</span>, <span class="stixtype">infrastructure</span>, <span class="stixtype">location</span>, <span class="stixtype">vulnerability</span></td>
    <td>This Relationship documents that this Tool is being used to target this Identity, Infrastructure, Location, or exploit the Vulnerability.<br><br>For example, a <span class="stixliteral">targets</span> Relationship linking an exploit Tool to a Vulnerability for CVE-2016-0001 means that the tool exploits that vulnerability.<br><br>Similarly, a <span class="stixliteral">targets</span> Relationship linking a DDoS Tool to an Identity representing the energy sector means that Tool is typically used against targets in the energy sector.</td>
  </tr>
  <tr>
    <td><span class="stixtype">tool</span></td>
    <td><span class="stixliteral">uses</span></td>
    <td><span class="stixtype">infrastructure</span></td>
    <td>This Relationship describes that this Tool uses the related Infrastructure.</td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th colspan='4'><span class='stixtr'>Reverse Relationships</span></th>
  </tr>
  <tr>
    <td width="20%"><span class="stixtype">infrastructure</span></td>
    <td width="20%"><span class="stixliteral">hosts</span></td>
    <td width="20%"><span class="stixtype">tool</span></td>
    <td>See forward relationship for definition.</td>
  </tr>
  <tr>
    <td><span class="stixtype">malware</span></td>
    <td><span class="stixliteral">downloads</span>, <span class="stixliteral">drops</span></td>
    <td><span class="stixtype">tool</span></td>
    <td>See forward relationship for definition</td>
  </tr>
  <tr>
    <td><span class="stixtype">indicator</span></td>
    <td><span class="stixliteral">indicates</span></td>
    <td><span class="stixtype">tool</span></td>
    <td>See forward relationship for definition</td>
  </tr>
  <tr>
    <td><span class="stixtype">course-of-action</span></td>
    <td><span class="stixliteral">mitigates</span></td>
    <td><span class="stixtype">tool</span></td>
    <td>See forward relationship for definition</td>
  </tr>
  <tr>
    <td><span class="stixtype">attack-pattern</span>, <span class="stixtype">campaign</span>, <span class="stixtype">intrusion-set</span>, <span class="stixtype">malware</span>, <span class="stixtype">threat-actor</span></td>
    <td><span class="stixliteral">uses</span></td>
    <td><span class="stixtype">tool</span></td>
    <td>See forward relationship for definition</td>
  </tr>
</table>

**Example**

```JSON
{
  "type": "tool",
  "spec_version": "2.1",
  "id": "tool--8e2e2d2b-17d4-4cbf-938f-98ee46b3cd3f",
  "created_by_ref": "identity--f431f809-377b-45e0-aa1c-6a4751cae5ff",
  "created": "2016-04-06T20:03:48.000Z",
  "modified": "2016-04-06T20:03:48.000Z",
  "tool_types": [ "remote-access"],
  "name": "VNC"
}
```

## 4.19 Vulnerability <a id="vulnerability"></a>

**Type Name:** <span class="stixtype">vulnerability</span>

A Vulnerability is a weakness or defect in the requirements, designs, or implementations of the computational logic (e.g., code) found in software and some hardware components (e.g., firmware) that can be directly exploited to negatively impact the confidentiality, integrity, or availability of that system.

CVE is a list of information security vulnerabilities and exposures that provides common names for publicly known problems \[[CVE](#cve)\]. For example, if a piece of malware exploits CVE-2015-12345, a Malware object could be linked to a Vulnerability object that references CVE-2015-12345.

The Vulnerability SDO is primarily used to link to external definitions of vulnerabilities or to describe 0-day vulnerabilities that do not yet have an external definition. Typically, other SDOs assert relationships to Vulnerability objects when a specific vulnerability is targeted and exploited as part of malicious cyber activity. As such, Vulnerability objects can be used as a linkage to the asset management and compliance process.

### 4.19.1 Properties <a id="vulnerability-properties"></a>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th><span class="stixtr">Required Common Properties</span></th>
  </tr>
  <tr>
    <td><strong>type</strong>, <strong>spec_version</strong>, <strong>id</strong>, <strong>created</strong>, <strong>modified</strong></td>
  </tr>
  <tr>
    <th><span class="stixtr">Optional Common Properties></span></th>
  </tr>
  <tr>
    <td><strong>created_by_ref</strong>, <strong>revoked</strong>, <strong>labels</strong>, <strong>confidence</strong>, <strong>lang</strong>, <strong>external_references</strong>, <strong>object_marking_refs</strong>, <strong>granular_markings</strong>, <strong>extensions</strong></td>
  </tr>
  <tr>
    <th><span class="stixtr">Not Applicable Common Properties</span></th>
  </tr>
  <tr>
    <td><strong>defanged</strong></td>
  </tr>
  <tr>
    <th><span class="stixtr"> Specific Properties</span></th>
  </tr>
  <tr>
    <td><strong>name</strong>, <strong>description</strong></td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6">
  <tr>
    <th><span class="stixtr">Property Name</span></th>
    <th><span class="stixtr">Type</span></th>
    <th><span class="stixtr">Description</span></th>
  </tr>
  <tr>
    <td><strong>type</strong> (required)</td>
    <td><span class="stixtype">string</span></td>
    <td>The value of this property <strong>MUST</strong> be <span class="stixliteral">vulnerability</span>.</td>
  </tr>
  <tr>
    <td><strong>external_references</strong> (optional)</td>
    <td><span style="white-space: nowrap;"><span class="stixtype">list</span> of type <span class="stixtype">external-reference</span></span></td>
    <td>A list of external references which refer to non-STIX information. This property <strong>MAY</strong> be used to provide one or more Vulnerability identifiers, such as a CVE ID [<a href="#cve">CVE</a>]. When specifying a CVE ID, the <strong>source_name</strong> property of the external reference <strong>MUST</strong> be set to <span class="stixliteral">cve</span> and the <strong>external_id</strong> property <strong>MUST</strong> be the exact CVE identifier.</td>
  </tr>
  <tr>
    <td><strong>name</strong> (required)</td>
    <td><span class="stixtype">string</span></td>
    <td>A name or characterizing text used to identify the Vulnerability.</td>
  </tr>
  <tr>
    <td><strong>description</strong> (optional)</td>
    <td><span class="stixtype">string</span></td>
    <td>A description that provides more details and context about the Vulnerability, potentially including its purpose and its key characteristics.</td>
  </tr>
</table>

### 4.19.2 Relationships <a id="vulnerability-relationships"></a>

These are the relationships explicitly defined between the Vulnerability object and other STIX Objects. The first section lists the embedded relationships by property name along with their corresponding target. The rest of the table identifies the relationships that can be made from this object type to another object type by way of the Relationship object. The reverse relationships section illustrates the relationships targeting this object type from another object type. They are included here for convenience. For their definitions, please see the "Source" object.

Relationships are not restricted to those listed below. Relationships can be created between any objects using the <span class="stixliteral">related-to</span> relationship type or, as with open vocabularies, user-defined names.

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th colspan='2'><span class='stixtr'>Embedded Relationships</span></th>
  </tr>
  <tr>
    <td width="50%"><strong>created_by_ref</strong></td>
    <td width="50%"><span class="stixtype">identifier</span> (of type <span class="stixtype">identity</span>)</td>
  </tr>
  <tr>
    <td><strong>object_marking_refs</strong></td>
    <td><span class="stixtype">list</span> of type <span class="stixtype">identifier</span> (of type <span class="stixtype">marking-definition</span>)</td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th><span class='stixtr'>Common Relationships</span></th>
  </tr>
  <tr>
    <td><span class="stixliteral">duplicate-of</span>, <span class="stixliteral">derived-from</span>, <span class="stixliteral">related-to</span></td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th width="20%"><span class='stixtr'>Source</span></th>
    <th width="20%""><span class='stixtr'>Relationship Type</span></th>
    <th width="20%"><span class='stixtr'>Target</span></th>
    <th><span class='stixtr'>Description</span></th>
  </tr>
  <tr>
    <td>—</td>
    <td>—</td>
    <td>—</td>
    <td>—</td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th colspan='4'><span class='stixtr'>Reverse Relationships</span></th>
  </tr>
  <tr>
    <td width="20%"><span class="stixtype">attack-pattern</span>, <span class="stixtype">campaign</span>, <span class="stixtype">intrusion-set</span>, <span class="stixtype">malware</span>, <span class="stixtype">threat-actor</span>, <span class="stixtype">tool</span></td>
    <td width="20%"><span class="stixliteral">targets</span></td>
    <td width="20%"><span class="stixtype">vulnerability</span></td>
    <td>See forward relationship for definition.</td>
  </tr>
  <tr>
    <td><span class="stixtype">malware</span></td>
    <td><span class="stixliteral">exploits</span></td>
    <td><span class="stixtype">vulnerability</span></td>
    <td>See forward relationship for definition.</td>
  </tr>
  <tr>
    <td><span class="stixtype">course-of-action</span></td>
    <td><span class="stixliteral">mitigates</span>, <span class="stixliteral">remediates</span></td>
    <td><span class="stixtype">vulnerability</span></td>
    <td>See forward relationship for definition.</td>
  </tr>
  <tr>
    <td><span class="stixtype">infrastructure</span></td>
    <td><span class="stixliteral">has</span></td>
    <td><span class="stixtype">vulnerability</span></td>
    <td>See forward relationship for definition.</td>
  </tr>
</table>

**Example**

```JSON
{
  "type": "vulnerability",
  "spec_version": "2.1",
  "id": "vulnerability--0c7b5b88-8ff7-4a4d-aa9d-feb398cd0061",
  "created": "2016-05-12T08:17:27.000Z",
  "modified": "2016-05-12T08:17:27.000Z",
  "created_by_ref": "identity--f431f809-377b-45e0-aa1c-6a4751cae5ff",
  "name": "CVE-2016-1234",
  "external_references": [
    {
      "source_name": "cve",
      "external_id": "CVE-2016-1234"
    }
  ]
}
```

# 5. STIX Relationship Objects <a id="stix-relationship-objects"></a>

STIX Relationship Objects (SROs) represent types of relationships used to describe CTI. The Generic Relationship SRO is used to describe many varied types of relationships, while the specific Sighting SRO contains additional properties to represent Sighting relationships.

Property information, relationship information, and examples are provided for each SRO defined below. Property information includes common properties as well as properties that are specific to each SRO. Because SROs cannot be the source or target of other SROs, relationship information is included but only to describe embedded relationships (e.g., **created_by_ref**).

## 5.1 Relationship <a id="relationship"></a>

**Type Name:** <span class="stixtype">relationship</span>

The Relationship object is used to link together two SDOs or SCOs in order to describe how they are related to each other. If SDOs and SCOs are considered "nodes" or "vertices" in the graph, the Relationship Objects (SROs) represent "edges".

STIX defines many relationship types to link together SDOs and SCOs. These relationships are contained in the "Relationships" table under each SDO and SCO definition. Relationship types defined in the specification **SHOULD** be used to ensure consistency. An example of a specification-defined relationship is that an <span class="stixtype">indicator</span> <span class="stixliteral">indicates</span> a <span class="stixtype">campaign</span>. That relationship type is listed in the Relationships section of the Indicator SDO definition.

STIX also allows relationships from any SDO or SCO to any SDO or SCO that have not been defined in this specification. These relationships **MAY** use the <span class="stixliteral">related-to</span> relationship type or **MAY** use a user-defined relationship type. As an example, a user might want to link <span class="stixtype">malware</span> directly to a <span class="stixtype">tool</span>. They can do so using <span class="stixliteral">related-to</span> to say that the Malware is related to the Tool but not describe how, or they could use <span class="stixliteral">delivered-by</span> (a user-defined name they determined) to indicate more detail.

Note that some relationships in STIX may seem like "shortcuts". For example, an Indicator doesn't really detect a Campaign: it detects activity (Attack Patterns, Malware, Infrastructure, etc.) that are often used by that campaign. While some analysts might want all of the source data and think that shortcuts are misleading, in many cases it's helpful to provide just the key points (shortcuts) and leave out the low-level details. In other cases, the low-level analysis may not be known or sharable, while the high-level analysis is. For these reasons, relationships that might appear to be "shortcuts" are not excluded from STIX.

### 5.1.1 Specification-Defined Relationships Summary <a id="relationship-specification-defined-relationships-summary"></a>


A relationship summary table for all specification-defined relationships can be found in [Appendix B](#relationship-summary-table) of this document. The relationship summary table is provided as a convenience. If there is a discrepancy between the table and the relationships defined with each of the SDOs, then the relationships defined with the SDOs **MUST** be viewed as authoritative.​

### 5.1.2 Properties <a id="relationship-properties"></a>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th><span class="stixtr">Required Common Properties</span></th>
  </tr>
  <tr>
    <td><strong>type</strong>, <strong>spec_version</strong>, <strong>id</strong>, <strong>created</strong>, <strong>modified</strong></td>
  </tr>
  <tr>
    <th><span class="stixtr">Optional Common Properties></span></th>
  </tr>
  <tr>
    <td><strong>created_by_ref</strong>, <strong>revoked</strong>, <strong>labels</strong>, <strong>confidence</strong>, <strong>lang</strong>, <strong>external_references</strong>, <strong>object_marking_refs</strong>, <strong>granular_markings</strong>, <strong>extensions</strong></td>
  </tr>
  <tr>
    <th><span class="stixtr">Not Applicable Common Properties</span></th>
  </tr>
  <tr>
    <td><strong>defanged</strong></td>
  </tr>
  <tr>
    <th><span class="stixtr"> Specific Properties</span></th>
  </tr>
  <tr>
    <td><strong>relationship_type</strong>, <strong>description</strong>, <strong>source_ref</strong>, <strong>target_ref</strong>, <strong>start_time</strong>, <strong>stop_time</strong></td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6">
  <tr>
    <th><span class="stixtr">Property Name</span></th>
    <th><span class="stixtr">Type</span></th>
    <th><span class="stixtr">Description</span></th>
  </tr>
  <tr>
    <td><strong>type</strong> (required)</td>
    <td><span class="stixtype">string</span></td>
    <td>The value of this property <strong>MUST</strong> be <span class="stixliteral">relationship</span>.</td>
  </tr>
  <tr>
    <td><strong>relationship_type</strong> (required)</td>
    <td><span class="stixtype">string</span></td>
    <td>The name used to identify the type of Relationship. This value <strong>SHOULD</strong> be an exact value listed in the relationships for the source and target SDO, but <strong>MAY</strong> be any string. The value of this property <strong>MUST</strong> be in ASCII and is limited to characters a-z (lowercase ASCII), 0-9, and hyphen (-).</td>
  </tr>
  <tr>
    <td><strong>description</strong> (optional)</td>
    <td><span class="stixtype">string</span></td>
    <td>A description that provides more details and context about the Relationship, potentially including its purpose and its key characteristics.</td>
  </tr>
  <tr>
    <td><strong>source_ref</strong> (required)</td>
    <td><span class="stixtype">identifier</span></td>
    <td>The <strong>id</strong> of the source (from) object. The value <strong>MUST</strong> be an ID reference to an SDO or SCO (i.e., it cannot point to an SRO, Bundle, Language Content, or Marking Definition).</td>
  </tr>
  <tr>
    <td><strong>target_ref</strong> (required)</td>
    <td><span class="stixtype">identifier</span></td>
    <td>The <strong>id</strong> of the target (to) object. The value <strong>MUST</strong> be an ID reference to an SDO or SCO (i.e., it cannot point to an SRO, Bundle, Language Content, or Marking Definition).</td>
  </tr>
  <tr>
    <td><strong>start_time</strong> (optional)</td>
    <td><span class="stixtype">timestamp</span></td>
    <td>This optional timestamp represents the earliest time at which the Relationship between the objects exists. If this property is a future timestamp, at the time the <strong>start_time</strong> property is defined, then this represents an estimate by the producer of the intelligence of the earliest time at which relationship will be asserted to be true.<br><br>If it is not specified, then the earliest time at which the relationship between the objects exists is not defined.</td>
  </tr>
  <tr>
    <td><strong>stop_time</strong> (optional)</td>
    <td><span class="stixtype">timestamp</span></td>
    <td>The latest time at which the Relationship between the objects exists. If this property is a future timestamp, at the time the <strong>stop_time</strong> property is defined, then this represents an estimate by the producer of the intelligence of the latest time at which relationship will be asserted to be true.<br><br>If <strong>start_time</strong> and <strong>stop_time</strong> are both defined, then <strong>stop_time MUST</strong> be later than the <strong>start_time</strong> value.<br><br>If <strong>stop_time</strong> is not specified, then the latest time at which the relationship between the objects exists is either not known, not disclosed, or has no defined stop time.</td>
  </tr>
</table>

### 5.1.3 Relationships <a id="relationship-relationships"></a>

There are no relationships explicitly defined between the Relationship object and other STIX Objects, other than the embedded relationships listed below. These embedded relationships are listed by property name along with their corresponding target.

The only type of relationship that can point to a Relationship Object is the embedded relationship on the Note, Opinion, and Language Content Objects.

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th colspan='2'><span class='stixtr'>Embedded Relationships</span></th>
  </tr>
  <tr>
    <td width="50%"><strong>created_by_ref</strong></td>
    <td width="50%"><span class="stixtype">identifier</span> (of type <span class="stixtype">identity</span>)</td>
  </tr>
  <tr>
    <td><strong>object_marking_refs</strong></td>
    <td><span class="stixtype">list</span> of type <span class="stixtype">identifier</span> (of type <span class="stixtype">marking-definition</span>)</td>
  </tr>
</table>

## 5.2 Sighting <a id="sighting"></a>


**Type Name:** <span class="stixtype">sighting</span>

A Sighting denotes the belief that something in CTI (e.g., an indicator, malware, tool, threat actor, etc.) was seen. Sightings are used to track who and what are being targeted, how attacks are carried out, and to track trends in attack behavior.

The Sighting relationship object is a special type of SRO; it is a relationship that contains extra properties not present on the Generic Relationship object. These extra properties are included to represent data specific to sighting relationships (e.g., **count**, representing how many times something was seen), but for other purposes a Sighting can be thought of as a Relationship with a name of "sighting-of". Sighting is captured as a relationship because you cannot have a sighting unless you have something that has been sighted. Sighting does not make sense without the relationship to what was sighted.

Sighting relationships relate three aspects of the sighting:
- What was sighted, such as the Indicator, Malware, Campaign, or other SDO (**sighting_of_ref**)
- Who sighted it and/or where it was sighted, represented as an Identity (**where_sighted_refs**)
- What was actually seen on systems and networks, represented as Observed Data (**observed_data_refs**)

What was sighted is required; a sighting does not make sense unless you say what you saw. Who sighted it, where it was sighted, and what was actually seen are optional. In many cases it is not necessary to provide that level of detail in order to provide value.

Sightings are used whenever any SDO has been "seen". In some cases, the object creator wishes to convey very little information about the sighting; the details might be sensitive, but the fact that they saw a malware instance or threat actor could still be very useful. In other cases, providing the details may be helpful or even necessary; saying exactly which of the 1000 IP addresses in an indicator were sighted is helpful when tracking which of those IPs is still malicious.

Sighting is distinct from Observed Data in that Sighting is an intelligence assertion ("I saw this threat actor") while Observed Data is simply information ("I saw this file"). When you combine them by including the linked Observed Data (**observed_data_refs**) from a Sighting, you can say "I saw this file, and that makes me think I saw this threat actor".

### 5.2.1 Properties <a id="sighting-properties"></a>

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th><span class="stixtr">Required Common Properties</span></th>
  </tr>
  <tr>
    <td><strong>type</strong>, <strong>spec_version</strong>, <strong>id</strong>, <strong>created</strong>, <strong>modified</strong></td>
  </tr>
  <tr>
    <th><span class="stixtr">Optional Common Properties></span></th>
  </tr>
  <tr>
    <td><strong>created_by_ref</strong>, <strong>revoked</strong>, <strong>labels</strong>, <strong>confidence</strong>, <strong>lang</strong>, <strong>external_references</strong>, <strong>object_marking_refs</strong>, <strong>granular_markings</strong>, <strong>extensions</strong></td>
  </tr>
  <tr>
    <th><span class="stixtr">Not Applicable Common Properties</span></th>
  </tr>
  <tr>
    <td><strong>defanged</strong></td>
  </tr>
  <tr>
    <th><span class="stixtr"> Specific Properties</span></th>
  </tr>
  <tr>
    <td><strong>description</strong>, <strong>first_seen</strong>, <strong>last_seen</strong>, <strong>count</strong>, <strong>sighting_of_ref</strong>, <strong>observed_data_refs</strong>, <strong>where_sighted_refs</strong>, <strong>summary</strong></td>
  </tr>
</table>

<table border="1" cellspacing="0" cellpadding="6">
  <tr>
    <th><span class="stixtr">Property Name</span></th>
    <th><span class="stixtr">Type</span></th>
    <th><span class="stixtr">Description</span></th>
  </tr>
  <tr>
    <td><strong>type</strong> (required)</td>
    <td><span class="stixtype">string</span></td>
    <td>The value of this property <strong>MUST</strong> be <span class="stixliteral">sighting</span>.</td>
  </tr>
  <tr>
    <td><strong>description</strong> (optional)</td>
    <td><span class="stixtype">string</span></td>
    <td>A description that provides more details and context about the Sighting.</td>
  </tr>
  <tr>
    <td><strong>first_seen</strong> (optional)</td>
    <td><span class="stixtype">timestamp</span></td>
    <td>The beginning of the time window during which the SDO referenced by the <strong>sighting_of_ref</strong> property was sighted.</td>
  </tr>
  <tr>
    <td><strong>last_seen</strong> (optional)</td>
    <td><span class="stixtype">timestamp</span></td>
    <td>The end of the time window during which the SDO referenced by the <strong>sighting_of_ref</strong> property was sighted.<br><br>If this property and the <strong>first_seen</strong> property are both defined, then this property <strong>MUST</strong> be greater than or equal to the timestamp in the <strong>first_seen</strong> property.</td>
  </tr>
  <tr>
    <td><strong>count</strong> (optional)</td>
    <td><span class="stixtype">integer</span></td>
    <td>If present, this <strong>MUST</strong> be an integer between 0 and 999,999,999 inclusive and represents the number of times the SDO referenced by the <strong>sighting_of_ref</strong> property was sighted.<br><br>Observed Data has a similar property called <strong>number_observed</strong>, which refers to the number of times the data was observed. These counts refer to different concepts and are distinct.<br><br>For example, a single sighting of a DDoS bot might have many millions of observations of the network traffic that it generates. Thus, the Sighting <strong>count</strong> would be 1 (the bot was observed once) but the Observed Data <strong>number_observed</strong> would be much higher.<br><br>As another example, a sighting with a count of 0 can be used to express that an indicator was not seen at all.</td>
  </tr>
  <tr>
    <td><strong>sighting_of_ref</strong> (required)</td>
    <td><span class="stixtype">identifier</span></td>
    <td>An ID reference to the SDO that was sighted (e.g., Indicator or Malware).<br><br>For example, if this is a Sighting of an Indicator, that Indicator’s ID would be the value of this property.<br><br>This property <strong>MUST</strong> reference only an SDO.</td>
  </tr>
  <tr>
    <td><strong>observed_data_refs</strong> (optional)</td>
    <td><span style="white-space: nowrap;"><span class="stixtype">list</span> of type <span class="stixtype">identifier</span></span></td>
    <td>A list of ID references to the Observed Data objects that contain the raw cyber data for this Sighting.<br><br>For example, a Sighting of an Indicator with an IP address could include the Observed Data for the network connection that the Indicator was used to detect.<br><br>This property <strong>MUST</strong> reference only Observed Data SDOs.</td>
  </tr>
  <tr>
    <td><strong>where_sighted_refs</strong> (optional)</td>
    <td><span style="white-space: nowrap;"><span class="stixtype">list</span> of type <span class="stixtype">identifier</span></span></td>
    <td>A list of ID references to the Identity or Location objects describing the entities or types of entities that saw the sighting.<br><br>Omitting the <strong>where_sighted_refs</strong> property does not imply that the sighting was seen by the object creator. To indicate that the sighting was seen by the object creator, an Identity representing the object creator should be listed in <strong>where_sighted_refs</strong>.<br><br>This property <strong>MUST</strong> reference only Identity or Location SDOs.</td>
  </tr>
  <tr>
    <td><strong>summary</strong> (optional)</td>
    <td><span class="stixtype">string</span></td>
    <td>The <strong>summary</strong> property indicates whether the Sighting should be considered summary data. Summary data is an aggregation of previous Sightings reports and should not be considered primary source data. Default value is <span class="stixliteral">false</span>.</td>
  </tr>
</table>

### 5.2.2 Relationships <a id="sighting-relationships"></a>

There are no relationships explicitly defined between the Sighting object and other STIX Objects, other than the embedded relationships listed below. These embedded relationships are listed by property name along with their corresponding target.

The only type of relationship that can point to a Sighting Object is the embedded relationship on the Note, Opinion, and Language Content Objects.

<table border="1" cellspacing="0" cellpadding="6" width="100%">
  <tr>
    <th colspan='2'><span class='stixtr'>Embedded Relationships</span></th>
  </tr>
  <tr>
    <td width="50%"><strong>created_by_ref</strong></td>
    <td width="50%"><span class="stixtype">identifier</span> (of type <span class="stixtype">identity</span>)</td>
  </tr>
  <tr>
    <td><strong>object_marking_refs</strong></td>
    <td><span class="stixtype">list</span> of type <span class="stixtype">identifier</span> (of type <span class="stixtype">marking-definition</span>)</td>
  </tr>
  <tr>
    <td><strong>sighting_of_ref</strong></td>
    <td><span class="stixtype">identifier</span> (of type SDO)</td>
  </tr>
  <tr>
    <td><strong>observed_data_refs</strong></td>
    <td><span class="stixtype">list</span> of type <span class="stixtype">identifier</span> (of type <span class="stixtype">observed-data</span>)</td>
  </tr>
  <tr>
    <td><strong>where_sighted_refs</strong></td>
    <td><span class="stixtype">list</span> of type <span class="stixtype">identifier</span> (of type <span class="stixtype">identity</span>)</td>
  </tr>
</table>

**Examples**

*Sighting of Indicator, without Observed Data*

```JSON


{
  "type": "sighting",
  "spec_version": "2.1",
  "id": "sighting--ee20065d-2555-424f-ad9e-0f8428623c75",
  "created_by_ref": "identity--f431f809-377b-45e0-aa1c-6a4751cae5ff",
  "created": "2016-04-06T20:08:31.000Z",
  "modified": "2016-04-06T20:08:31.000Z",
  "sighting_of_ref": "indicator--8e2e2d2b-17d4-4cbf-938f-98ee46b3cd3f"
}
```

*Sighting of Indicator, with Observed Data (what exactly was seen) and where it was seen*

```JSON
[
  {
    "type": "sighting",
    "spec_version": "2.1",
    "id": "sighting--ee20065d-2555-424f-ad9e-0f8428623c75",
    "created_by_ref": "identity--f431f809-377b-45e0-aa1c-6a4751cae5ff",
    "created": "2016-04-06T20:08:31.000Z",
    "modified": "2016-04-06T20:08:31.000Z",
    "first_seen": "2015-12-21T19:00:00Z",
    "last_seen": "2015-12-21T19:00:00Z",
    "count": 50,
    "sighting_of_ref": "indicator--8e2e2d2b-17d4-4cbf-938f-98ee46b3cd3f",
    "observed_data_refs": ["observed-data--b67d30ff-02ac-498a-92f9-32f845f448cf"],
    "where_sighted_refs": ["identity--b67d30ff-02ac-498a-92f9-32f845f448ff"]
  },
  {
    "type": "observed-data",
    "spec_version": "2.1",
    "id": "observed-data--b67d30ff-02ac-498a-92f9-32f845f448cf",
    "created_by_ref": "identity--f431f809-377b-45e0-aa1c-6a4751cae5ff",
    "created": "2016-04-06T19:58:16.000Z",
    "modified": "2016-04-06T19:58:16.000Z",
    "first_observed": "2015-12-21T19:00:00Z",
    "last_observed": "2016-04-06T19:58:16Z",
    "number_observed": 50,
    "object_refs": [
      "file--30038539-3eb6-44bc-a59e-d0d3fe84695a"
    ]
  }
]
```
