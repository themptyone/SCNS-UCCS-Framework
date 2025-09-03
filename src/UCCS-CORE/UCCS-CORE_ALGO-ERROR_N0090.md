# SCNS ID: $UCCS-BB:DOC:UCCS-CORE:ALGO-ERROR:N0090$

---

## Error Handling and Validation

**SCNS ID:** `$UCCS-CORE:ALGO:ERROR:HANDLING:VALIDATION:N0160$`

### Malformed Address Detection

**Algorithm:** Validate SCNS address format and detect common errors.
```javascript
function validateAddress(address) {
    const errors = [];

    // Format validation
    const scnsPattern = /^[A-Z0-9]{4,8}:[A-Z]{2}:L\d{4,}$/;
    if (!scnsPattern.test(address)) {
        errors.push({
            type: 'INVALID_FORMAT',
            message: 'Address must follow PID:FK:L#### format',
            severity: 'HIGH'
        });
    }

    // Component validation
    const [pid, fk, lineNum] = address.split(':');
    if (pid && (pid.length < 4 || pid.length > 8)) {
        errors.push({
            type: 'INVALID_PID_LENGTH',
            message: 'Project ID must be 4-8 characters',
            severity: 'MEDIUM'
        });
    }

    if (fk && !STANDARD_FILE_KEYS.includes(fk)) {
        errors.push({
            type: 'UNKNOWN_FILE_KEY',
            message: `File key '${fk}' not in standard library`,
            severity: 'MEDIUM'
        });
    }

    return {
        isValid: errors.length === 0,
        errors: errors
    };
}
```
###Consistency Checking

**Algorithm:** Ensure address consistency across project files.

JavaScript

function checkConsistency(projectFiles) {
    const issues = [];
    const addressRegistry = new Map();

    // Build complete address registry
    projectFiles.forEach(file => {
        file.addresses.forEach(addr => {
            if (addressRegistry.has(addr.id)) {
                issues.push({
                    type: 'DUPLICATE_ADDRESS',
                    address: addr.id,
                    files: [addressRegistry.get(addr.id).file, file.name]
                });
            }
            addressRegistry.set(addr.id, {
                address: addr,
                file: file.name
            });
        });
    });
    // Check reference integrity
    addressRegistry.forEach((entry, addressId) => {
        const refs = extractReferences(entry.address.comment);
        refs.forEach(refId => {
            if (!addressRegistry.has(refId)) {
                issues.push({
                    type: 'BROKEN_REFERENCE',
                    source: addressId,
                    target: refId,
                    file: entry.file
                });
            }
        });
    });
    return issues;
}