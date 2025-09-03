# SCNS ID: $UCCS-BB:DOC:UCCS-CORE:IMPL-SCNS:N0040$

---

## Part 2: Core System Implementation

**SCNS ID:** `$UCCS-CORE:IMPL:SYSTEM:CORE:IMPLEMENTATION:N0080$`

The UCCS architecture is realized through a set of core JavaScript classes that manage coordinates, protocols, and system execution. SCNS treats code as spatially organized rather than line-bound. Logical relationships map to coordinates, ensuring stability across refactors and enabling automation. Natural spatial patterns: **Trees, Pipelines, Graphs, Layers**.

AI uses *value-driven automation* to optimize code safely. The SCNS-V4 is a domain-agnostic spatial addressing system.

V4 Standard: [DOMAIN]:[AREA]:[COMPONENT]:[ELEMENT]:[TAG]:[SEQUENCE][:VERSION][:STATE]

### 2.1 SCNS Coordinate Engine (`SCNSCoordinate`)

**SCNS ID:** `$UCCS-CORE:IMPL:SCNS:COORDINATE:ENGINE:N0090$`

**SCNS-V4 Coordinate Format**
**SCNS ID:** `$UCCS-CORE:SPEC:FRAMEWORK:SCNS-V4-FORMAT:FORMAT:N0100$`

#### Summary
SCNS-V4 is a universal, domain-agnostic coordinate system designed to support the principle of Universal Addressability. It uses a six-part hierarchical structure and optional dimensional tags for versioning and state to give any piece of information a precise, queryable address.

#### Elaboration
The SCNS-V4 is the spatial addressing system within the UCCS framework. To support Universal Addressability, its format is abstracted to be domain-agnostic. The standard format consists of six hierarchical components:
* DOMAIN: The highest-level project or system domain (e.g., FINAPP, COGNITION).
* AREA: A major functional area or context within the domain.
* COMPONENT: A specific module, service, or subject.
* ELEMENT: The discrete, self-contained block of information.
* TAG: A classification based on the block's functional.
* SEQUENCE: A hierarchical numeric identifier, often incremented by 10 for spacing.

The addition of optional dimensional tags at the end of the coordinate to track an information block's lifecycle (...:[SEQUENCE][:VERSION][:STATE]). These include a :VERSION tag for tracking revisions and a :STATE tag to denote its lifecycle status (e.g., :DRAFT, :ACTIVE, :PASS). For practical project implementation, a simplified format like PROJECT:MODULE:FUNCTION:VERSION:STATE is often used.

This class is the foundation of universal addressability. It parses, validates, and manages SCNS coordinates.

* **Function**: Takes a raw coordinate string (e.g., `$UCCS-CORE:PROTO:ORG:SPEC:N0210$`).
* **Parsing**: Splits the string into its six components: `domain`, `area`, `component`, `element`, `tag`, and `sequence`.
* **Validation**: Ensures the coordinate adheres to the SCNS-V4-FORMAT specification, including checking for six parts and a sequence number that starts with 'N' followed by digits.