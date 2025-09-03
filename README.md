# SCNS-UCCS: Spatial Code Navigation System & Universal Code Coordinate System

**SCNS ID:** `$GITHUB:SCNS-UCCS:README:MAIN:DOC:N0010$`

This repository contains the core framework, specifications, and protocols for the **Spatial Code Navigation System (SCNS)** and the **Universal Code Coordinate System (UCCS)**. UCCS is a domain-agnostic spatial addressing system designed to create stable, hierarchical, and contextually-aware coordinates for any discrete unit of information, transforming chaotic data into a machine-navigable structure.

## Table of Contents

- [Core Philosophy: Universal Addressability](#core-philosophy-universal-addressability)
- [The SCNS-V4 Coordinate Format](#the-scns-v4-coordinate-format)
- [The Universal Interaction Protocol (UIP)](#the-universal-interaction-protocol-uip)
- [System Architecture & Core Protocols](#system-architecture--core-protocols)
- [Key Use Cases](#key-use-cases)
- [Getting Started](#getting-started)

## Core Philosophy: Universal Addressability

**SCNS ID:** `$GITHUB:SCNS-UCCS:README:PHILOSOPHY:CORE:N0100$`

The foundational principle of UCCS is **Universal Addressability**. This principle establishes that any discrete block of information—a function, a paragraph, a requirement—can be assigned a stable and unique coordinate that persists through refactoring and system evolution. By treating information spatially, UCCS establishes a framework where component relationships are explicit, traceable, and resilient.

## The SCNS-V4 Coordinate Format

**SCNS ID:** `$GITHUB:SCNS-UCCS:README:FORMAT:SPEC:N0200$`

The SCNS-V4 coordinate is a six-part hierarchical address for information blocks.

### Format Structure

```
$DOMAIN:AREA:COMPONENT:ELEMENT:TAG:SEQUENCE$
```

### Component Definitions

- **`DOMAIN`**: The highest-level project or system (e.g., `FINAPP`)
- **`AREA`**: A major functional area within the domain (e.g., `API`, `ARCH`)
- **`COMPONENT`**: A specific module, service, or subject (e.g., `AUTH`)
- **`ELEMENT`**: The discrete, self-contained block of information
- **`TAG`**: A functional classification of the block’s purpose (e.g., `SPEC`, `IMPL`)
- **`SEQUENCE`**: A hierarchical numeric identifier, incremented by 10 to allow insertions (e.g., `N0010`)

Optional dimensional tags for `:VERSION` and `:STATE` can be appended for lifecycle tracking.

## The Universal Interaction Protocol (UIP)

**SCNS ID:** `$GITHUB:SCNS-UCCS:README:UIP:PROTOCOL:N0300$`

The **Universal Interaction Protocol (UIP)** is the mandatory, non-negotiable pattern for all significant AI-driven actions, ensuring **User Sovereignty** by requiring explicit user validation for any change.

### Five-Step Control Flow

1. **GENERATE**: The AI agent creates the content for a discrete work unit
1. **SUMMARIZE**: The AI provides a concise, 1-3 line summary of the work
1. **PREVIEW**: The complete result is shown to the user for review
1. **CONFIRM**: The AI pauses at a **UIP Gate** and asks for validation with the mandatory prompt: “**Proceed? (Y/N/Modify)**”
1. **ITERATE**: The AI continues, stops, or re-works based on user input

The protocol’s intensity is adjustable via the **User Proficiency Level (UPL)**.

## System Architecture & Core Protocols

**SCNS ID:** `$GITHUB:SCNS-UCCS:README:ARCHITECTURE:PROTOCOLS:N0400$`

UCCS is organized into hierarchical layers. The **Protocol Layer** contains the foundational infrastructure for AI-human collaboration and governance.

### Core Protocol Components

- **`UCCS-INF`**: The master protocol for AI-human collaboration, governing all interactions via the UIP loop. It is the parent to model-specific implementations like `UCCS-INF-GPT`
- **`UCCS-NAV`**: Provides spatial intelligence for dependency graph traversal, impact analysis, and circular reference detection
- **`UCCS-CODE`**: Manages the code lifecycle, including analysis, compliant generation, and validation
- **`UCCS-QA`**: Spatially links test artifacts (plans, cases, bug reports) directly to source code coordinates for full traceability
- **`UCCS-Context-Meter`**: A utility providing transparency into AI token usage and costs to support User Sovereignty

## The main Usecases7
 
**SCNS ID:** `$GITHUB:SCNS-UCCS:README:USECASES:KEY:N0500$`

### Business & Enterprise

#### AI-Driven Software Development

Structure the entire software lifecycle from requirements to QA, enabling automated impact analysis across dependencies.

#### Advanced Knowledge Management

Convert enterprise documentation into a navigable knowledge graph using relational tags (`RTAGs`) like `REF` and `DEPENDS`.

#### Audit and Compliance

Generate an immutable audit trail where every decision is logged via UIP and every artifact is tied to a permanent SCNS coordinate.

### Day-to-Day Productivity

#### Structured Project Management

Break down projects into SCNS-addressed tasks for absolute clarity on status and dependencies (e.g., `$PROJ-X:PHASE1:DESIGN:UI-MOCKUP:TODO:N0010:DRAFT$`).

#### Personal Knowledge Graphs

Apply UCCS to note-taking to create a resilient personal knowledge base where links do not break when files are moved or renamed.

#### Collaborative Document Editing

Assign persistent coordinates to paragraphs, allowing comments and edits to remain anchored to the correct content block during revisions.

## Getting Started

**SCNS ID:** `$GITHUB:SCNS-UCCS:README:GETTING-STARTED:GUIDE:N0600$`

Implementation begins with conceptual alignment.

### Quick Start Steps

1. **Define Your Space**: Establish the `DOMAIN` and primary `AREA`s for any new project to create its foundational structure
1. **Interact Spatially**: Structure requests to a UCCS-compliant AI with a clear `TASK_GOAL` and set your `USER_PROFICIENCY_LEVEL`
1. **Use a Starter Prompt**: Initiate a project with a structured command:
   
   ```
   Execute UCCS-ORG-INITIALIZE for workspace: [path/description].
   Please discover all files, assign preliminary SCNS IDs, and present the master registry table for confirmation.
   ```

-----

## Contributing

We welcome contributions to the SCNS-UCCS project. Please ensure all contributions follow the UCCS coordinate system and adhere to the Universal Interaction Protocol.

## License

This project is licensed under the terms specified in the LICENSE file.

## Support

For questions, issues, or feature requests, please open an issue in this repository.