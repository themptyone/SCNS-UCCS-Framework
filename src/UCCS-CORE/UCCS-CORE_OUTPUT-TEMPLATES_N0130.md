# SCNS ID: $UCCS-BB:DOC:UCCS-CORE:OUTPUT-TEMPLATES:N0130$

---

### **Block 14: Core Output, UIP Framework, and Templates**
*Copy the content below into a file (e.g., `14_core_output_and_templates.md`).*

---

## Core Output: File-SCNS Cross-Reference Table

**SCNS ID:** `$UCCS-CORE:OUTPUT:FILE:SCNS:CROSS-REFERENCE:N0230$`

-----

## UIP Integration Framework

**SCNS ID:** `$UCCS-CORE:FRAMEWORK:UIP:INTEGRATION:FRAMEWORK:N0240$`

### Block-by-Block Organization Process

GENERATE → VALIDATE → ITERATE → GENERATE → VALIDATE...


**Every organizational action follows UIP:**

1.  **GENERATE**: Create organizational structure/update
2.  **SUMMARIZE**: Explain what was organized and why
3.  **PREVIEW**: Show table/matrix changes before applying
4.  **CONFIRM**: "Proceed? (Y / N / Modify)"
5.  **ITERATE**: Apply changes or modify based on user input

### Granular Control Points

**File Registration UIP**
  - Individual file SCNS ID assignment requires confirmation
  - Batch operations show summary table before applying
  - Relationship detection presents findings for validation

**Cross-Reference UIP**
  - Each detected relationship requires user confirmation
  - Conflicting references trigger resolution workflow
  - Matrix updates show before/after comparison

**Maintenance UIP**
  - File changes trigger organization review process
  - Broken references require user decision (fix/ignore/defer)
  - Status changes validated before updating master registry

-----

## Protocol Implementation Templates

**SCNS ID:** `$UCCS-CORE:IMPL:PROTOCOL:TEMPLATES:IMPLEMENTATION:N0250$`

### User Prompt Templates

**Initialize File Organization**
Execute UCCS-ORG-INITIALIZE for workspace: [path/description]
Please discover all files, assign preliminary SCNS IDs, and present the master registry table for confirmation. Follow UIP: Generate → Preview → Confirm → Iterate


**Update Cross-References**
Execute UCCS-ORG-STRUCTURE analysis on current file registry. Map all RTAG relationships and update the cross-reference matrix. Show relationship changes and request validation via UIP.


**Maintenance Check**
Execute UCCS-ORG-MAINTAIN to sync file registry with current workspace state. Identify any broken references, missing files, or SCNS ID conflicts. Present maintenance report and recommended actions for UIP confirmation.


### AI System Behavior

The AI must always:
  - Present organizational changes in table format before applying
  - Require explicit user confirmation for SCNS ID assignments
  - Show relationship matrix updates with clear before/after views
  - Validate all cross-references and flag inconsistencies
  - Maintain organization audit trail with timestamps