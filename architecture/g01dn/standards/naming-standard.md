# PROTOSYNTHESIS NAMING STANDARD v1.1

Authority Level: Standard (L2)
Status: Canonical
Classification: Internal Architecture Standard
Location: /architecture/g01dn/standards/naming-standard.md
Depends On: G01DN Layer Definition Specification

---

# 0. VERSION NOTE

v1.1 introduces:

- strict elimination of naming ambiguity
- enforced structural naming consistency
- separation of conceptual vs filesystem naming
- standardised layer and artefact naming patterns

---

# 1. PURPOSE

This standard defines how all ProtoSynthesis architectural artefacts must be named.

It ensures:

- consistency across repository structure
- elimination of naming drift
- traceability of system components
- alignment between conceptual layers and filesystem representation

---

# 2. CORE PRINCIPLE

Naming is structural, not stylistic.

Every name must reflect:

- its layer role
- its functional purpose
- its position in the architecture

Names are deterministic identifiers, not creative expressions.

---

# 3. LAYER NAMING FORMAT

All G01DN-related files MUST follow:

layer-name-descriptor.md

Examples:

constitutional-form.md  
authority-model.md  
layer-definition.md  
protocol-definition.md  
naming-standard.md  

Rules:

- lowercase only
- hyphen-separated tokens
- no abbreviations unless formally defined
- no duplicate semantic meaning across files

---

# 4. DIRECTORY NAMING RULES

Directories represent structural domains only:

Allowed:
- constitutional/
- protocol/
- standards/
- reference/
- frameworks/

Not allowed:
- mixed-purpose folders
- ambiguous conceptual groupings
- duplicate semantic domains

---

# 5. CONCEPTUAL VS FILESYSTEM SEPARATION

A concept is NOT a folder.

- Concept = logical architecture definition  
- Folder = physical representation of governance domain  

They must remain separate in interpretation.

---

# 6. INVALID NAMING PATTERNS

- camelCase
- random abbreviations (gdn1, protoX)
- duplicate semantic naming (protocol-protocol.md)
- mixed-layer filenames (root-protocol-standard.md)
- UI or narrative-style naming

---

# 7. SYSTEM CONSISTENCY RULE

All naming must be:

- deterministic
- traceable
- layer-aligned
- semantically unique

Any ambiguity is a structural violation.

---

# 8. STATUS

Canonical Naming Standard v1.1
All naming must conform.

© ProtoSynthesis 2026–Present
