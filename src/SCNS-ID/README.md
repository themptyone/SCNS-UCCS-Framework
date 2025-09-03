# SCNS V4 - Spatial Code Navigation System

This repository contains the complete definitions and documentation for **SCNS V4**, a revolutionary approach to organizing and navigating information that treats code, documents, and data as **spatial entities** rather than linear text.

---

## 📌 What is SCNS?

SCNS is like a **GPS system for your information**.  
Instead of relying on fragile file paths and line numbers that break when code is refactored, SCNS assigns a **stable, hierarchical coordinate** to every discrete unit of information.  

This foundational principle is called **Universal Addressability**.

---

## ❌ The Problem

Traditional file systems and references break down when:

- Files are reorganized or renamed
- Code is refactored across multiple files
- Teams need to collaborate on complex projects
- AI systems need to understand relationships between components

---

## ✅ The SCNS Solution

SCNS provides **stable coordinates** that survive changes to the underlying structure.

**Example:**

- Traditional Path:  
  `folder1/subfolder1/file1.txt (line 47)`
- SCNS Coordinate:  
  `$MYPROJECT:AUTH:LOGIN:VALIDATION:N0010$`

Even if the file is moved or refactored, the SCNS coordinate remains the same.

---

## 🪜 The Three Pillars of SCNS

1. **Spatial Intelligence** → Information has relationships and positioning, not just content.  
2. **Coordinate Stability** → Addresses survive refactoring, reorganization, and evolution.  
3. **Universal Compatibility** → Any system, language, or tool can adopt SCNS addressing.  

---

## 🧩 SCNS V4 Format Specification

SCNS-V4 uses a **six-part hierarchical coordinate system**:

$DOMAIN:AREA:COMPONENT:ELEMENT:TAG:SEQUENCE$


### Component Breakdown

- **DOMAIN** → Highest-level project/system (e.g., `WEBAPP`, `FINTECH`)  
- **AREA** → Major functional area (e.g., `AUTH`, `UI`, `API`)  
- **COMPONENT** → Specific module/service (e.g., `LOGIN`, `DATABASE`)  
- **ELEMENT** → Self-contained block of info (e.g., `VALIDATION`, `RENDER`)  
- **TAG** → Functional role (e.g., `FUNC`, `DATA`, `CTRL`, `ERR`)  
- **SEQUENCE** → Numeric identifier for ordering (`N0010`, `N0020`)  

### Optional Dimensional Tags

- **Version Tag** → Tracks revisions (e.g., `:V1.2.3`)  
- **State Tag** → Lifecycle status (e.g., `:DRAFT`, `:ACTIVE`, `:DEPRECATED`)  

---

## 🛠 Practical Example

Embed SCNS coordinates directly in code for spatial context:

```javascript
// SCNS: $WEBAPP:AUTH:VALIDATION:EMAIL:N0010$
function validateUser(email) {
  return email.includes('@');
}
```
If this function is moved from src/auth/login.js to lib/security/auth.ts,
its SCNS coordinate remains the same, ensuring all references stay intact.

# 🏛 Core Architectural Principles

SCNS is governed by **8 universal principles**:

1. **Conservation of Context** – Every element has coordinates.  
2. **Persistence Through Change** – Coordinates survive refactoring and evolution.  
3. **Relational Integrity** – Relationships between blocks are explicit and trackable.  
4. **Purpose Primacy** – Classification based on functional intent, not implementation.  
5. **Hierarchical Harmony** – Coordinates reflect logical architecture.  
6. **Universal Accessibility** – Works with any system, language, or paradigm.  
7. **User Sovereignty** – Major changes require explicit user validation.  
8. **Universal Addressability** – Any discrete unit of information can be assigned a coordinate.  

---

# 📊 Comparison With Traditional Systems

| Feature                | File Paths | Git Hashes | UUIDs | SCNS V4 |
|-------------------------|------------|------------|-------|---------|
| Survives refactors      | ❌         | ✅         | ✅    | ✅      |
| Human-readable          | ✅         | ❌         | ❌    | ✅      |
| Expresses hierarchy     | ✅         | ❌         | ❌    | ✅      |
| Universal across tools  | ❌         | ❌         | ✅    | ✅      |

---
