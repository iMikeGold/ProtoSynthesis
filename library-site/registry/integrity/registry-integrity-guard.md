# ProtoSynthesis Registry Integrity Guard v1.1

Authority Level: Library Internal System Rule  
Status: Active  
Scope: /library-site/registry/  
Version: 1.1  

---

# 1. PURPOSE

The Registry Integrity Guard defines structural validity rules for all registry.json files used within the ProtoSynthesis Library system.

Its purpose is to ensure:

- valid machine-readable JSON structure  
- consistent registry schema usage  
- predictable UI rendering behaviour  
- prevention of system-level rendering failure  

This document governs structure only.  
It does NOT define content meaning.

---

# 2. SCOPE

This rule set applies only to:

- /library-site/registry/registry.json  
- all future registry files within /library-site/registry/  

It does NOT apply to:

- architecture layer files  
- G01DN system definitions  
- content files (books, articles, whitepapers)  
- external systems  

---

# 3. CORE RULE: JSON VALIDITY

All registry files MUST be valid JSON.

This includes:

- correct array formatting  
- proper comma separation between objects  
- no trailing invalid characters  
- no missing structural delimiters  

If JSON parsing fails:

→ The registry system is considered FAILED  
→ No partial rendering is allowed  
→ No fallback auto-repair is permitted  

---

# 4. REQUIRED COLLECTION STRUCTURE

Each registry category MUST follow this format:

```json
"books": [
  {
    "id": "book-001",
    "title": "Example Title",
    "path": "/content/books/example.html",
    "status": "draft",
    "visibility": "public",
    "tags": ["foundation"]
  }
]
```

---

# 5. REQUIRED ITEM CONTRACT (STRICT)

Each item MUST include:

- id (string, globally unique)  
- title (string)  
- path (string, valid route)  

Optional fields:

- status  
- visibility  
- tags  

No additional undefined fields should be introduced without schema extension.

---

# 6. FAILURE BEHAVIOUR

If registry.json is invalid or fails to parse:

The system MUST:

1. Stop registry rendering immediately  
2. Prevent partial UI rendering  
3. Enter explicit FAIL state  

Fallback message:

> Registry not found or failed to load.

---

# 7. DATA INTEGRITY RULES

The registry is a deterministic system input.

Therefore:

- No malformed JSON is permitted  
- No best-effort parsing in production  
- No automatic correction or inference  
- No silent degradation modes  

System must behave as:

✔ fully valid  
✖ fully failed  

No intermediate state is allowed.

---

# 8. EXTENSION RULE

New registry sections (ebooks, articles, whitepapers, datasets, etc.) MUST:

- follow identical structural rules  
- remain backward compatible  
- not modify existing schema behaviour  
- not introduce breaking changes without version increment  

---

# 9. UI COMPATIBILITY RULE

Frontend rendering assumes:

- each category is a valid array  
- each item contains required fields  
- schema structure remains stable across versions  

If schema changes:

→ UI behaviour is considered undefined until updated  

---

# 10. VERSIONING RULE

Any change that affects:

- required fields  
- structural rules  
- failure behaviour  
- parsing expectations  

MUST increment version (v1.x → v1.y)

Patch changes must NOT alter schema contract.

---

# 11. INTEGRITY PRINCIPLE

The registry is a:

> Machine-readable structural truth layer for the Library system

It is NOT:

- a flexible document  
- a human-formatted note file  
- a schema-optional dataset  

---

# 12. STATUS

Active and enforced within:

/library-site/registry/

© ProtoSynthesis Library System
