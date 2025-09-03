# SCNS ID: $UCCS-BB:DOC:UCCS-CORE:PROTO-DESC:N0190$

---

### `$UCCS-CORE:PROTO:INF:SPEC:N0600$` - UCCS-INF (AI-Human Collaboration)

**SCNS ID:** `$UCCS-CORE:PROTO:INF:COLLABORATION:PROTOCOL:N0730$`

  * **Purpose**: The master protocol for structured AI-human collaboration via the Universal Interaction Process (UIP) loop.
  * **Architectural Role**: The parent protocol for all AI-driven generation and processing tasks. It embodies the "Process Over Product" philosophy, ensuring that AI-generated content is reviewed, refined, and confirmed in a structured manner. Its state machine (`GENERATE` → `SUMMARIZE` → `PREVIEW` → `CONFIRM` → `ITERATE`) is a foundational pattern.
  * **Execution Example**: A cascading execution where user approval triggers subsequent protocols.
    ```
    Trigger: User Input "Add social login feature"

    1. UCCS-INF Execution:
       - GENERATE: Feature requirements analysis.
       - SUMMARIZE: Integration summary.
       - PREVIEW: Implementation approach.
       - CONFIRM: User approval received.
    2. Cascade Trigger: Approval cascades to UCCS-NAV for impact analysis.
    ```

### `$UCCS-CORE:PROTO:NAV:SPEC:N0220$` - UCCS-NAV (Spatial Navigation)

**SCNS ID:** `$UCCS-CORE:PROTO:NAV:NAVIGATION:PROTOCOL:N0740$`

  * **Purpose**: Enables spatial navigation and dependency graph traversal.
  * **Architectural Role**: Provides the system with spatial intelligence. It builds a spatial index for efficient lookups and offers capabilities like dependency chain traversal, impact analysis, circular reference detection, and finding related coordinates (siblings, neighbors).
  * **Execution Example**: Analyzing the impact of changing a core component.
    ```
    COORDINATE: $UCCS-CORE:PROTO:NAV:SPEC:N0220$
    INPUT: "$MYAPP:AUTH:SYSTEM:LOGIN:VALIDATE:N0001$" // Coordinate to analyze
    ACTION: "ANALYZE_IMPACT"

    EXECUTION RESULT: {
      "directDependents": 12,
      "riskLevel": "HIGH"
    }
    ```

### `$UCCS-APP:LIFECYCLE:CODE:SPEC:N1200$` - UCCS-CODE (Code Lifecycle Management)

**SCNS ID:** `$UCCS-APP:LIFECYCLE:CODE:MANAGEMENT:PROTOCOL:N0750$`

  * **Purpose**: Code analysis, generation, and SCNS compliance validation.
  * **Architectural Role**: Implements a dual-engine system for code quality. A `CodeFixEngine` suggests and applies fixes for compliance violations, while a `CodeVerificationEngine` validates the changes. It calculates metrics like coordinate density and complexity.
  * **Execution Example**: Analyzing a source code file for compliance.
    ```
    COORDINATE: $UCCS-APP:LIFECYCLE:CODE:SPEC:N1200$
    INPUT: {
      "sourceCode": "/** SCNS: $MYAPP:AUTH:LOGIN:N0001$ */ function login() { ... }",
      "operation": "ANALYZE_AND_FIX"
    }

    EXECUTION RESULT:
    - SCNS Compliance: 95%
    - Quality Metrics: LOC=15, Complexity=3
    - Verification Engine: PASSED
    ```

### `$UCCS-APP:LIFECYCLE:QA:SPEC:N0900$` - UCCS-QA (Quality Assurance)

**SCNS ID:** `$UCCS-APP:LIFECYCLE:QA:ASSURANCE:PROTOCOL:N0760$`

  * **Purpose**: Manages the quality assurance lifecycle, including test plans, test cases, and bug reports.
  * **Architectural Role**: Enables spatial test mapping by linking test artifacts directly to the source code coordinates they validate. This ensures that any change to a component immediately highlights the relevant tests.
  * **Execution Example**: Creating a test plan spatially linked to a feature coordinate.
    ```
    COORDINATE: $UCCS-APP:LIFECYCLE:QA:SPEC:N0900$
    INPUT: {
      "action": "CREATE_SPATIAL_TEST_PLAN",
      "target": "$MYAPP:AUTH:SYSTEM:LOGIN:VALIDATE:N0001$",
      "testTypes": ["UNIT", "INTEGRATION"]
    }
    ```

### `$UCCS-CORE:PROTO:CONTEXT-METER:SPEC:N0700$` - UCCS-Context-Meter

**SCNS ID:** `$UCCS-CORE:PROTO:CONTEXT:METER:PROTOCOL:N0770$`

  * **Purpose**: Provides AI token usage tracking and cost transparency reporting.
  * **Architectural Role**: A critical utility for managing the operational costs of AI interactions. It tracks metrics for multi-protocol sessions, offering optimization suggestions to improve efficiency.
  * **Execution Example**: Reporting the cost of a complex, multi-protocol task.
    ```
    📊 Resource Usage Report:
    ┌─────────────────────────────────────────────────────────┐
    │ Protocol                   │ Tokens │ Cost   │ Duration │
    ├─────────────────────────────────────────────────────────┤
    │ UCCS-INF (UIP Loops)       │ 2,450  │ $0.025 │ 145s     │
    │ UCCS-CODE (Analysis)       │ 890    │ $0.009 │ 67s      │
    ├─────────────────────────────────────────────────────────┤
    │ TOTAL SESSION              │ 3,340  │ $0.034 │ 212s     │
    └─────────────────────────────────────────────────────────┘
    ```