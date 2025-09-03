# SCNS ID: $UCCS-BB:DOC:UCCS-CORE:RTAGS:N0050$

---

## Cross-Reference System (RTAGs)

**SCNS ID:** `$UCCS-CORE:CONCEPT:RTAGS:CROSS-REFERENCE:SYSTEM:N0110$`

### Core RTAGs

REF       – neutral reference (See X)
DEPENDS   – requires X before Y
CALLS     – invokes or uses X
RANGE     – marks span (Replace N0100–N0200)


-   **REF**: For neutral navigation.
-   **DEPENDS**: For dependency ordering.
-   **CALLS**: For function/method invocation links.
-   **RANGE**: For batch edits or replacements.

> Note: `CALLED_BY` is derivable via reverse index of `CALLS`. Keeps RTAG set lean and parse-friendly.