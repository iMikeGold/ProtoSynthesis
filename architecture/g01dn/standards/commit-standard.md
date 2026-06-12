# PROTOSYNTHESIS COMMIT STANDARD v1.1

Authority Level: Standard (L2)
Status: Canonical
Classification: Internal Development Standard
Location: /architecture/g01dn/standards/commit-standard.md
Depends On: G01DN Layer Definition Specification

---

# 0. VERSION NOTE

v1.1 introduces:

- strict commit structure enforcement
- architectural traceability requirements
- formal change classification system
- elimination of non-structured commit messages

---

# 1. PURPOSE

This standard defines how all Git commits within ProtoSynthesis must be written.

Commits are architectural records, not activity logs.

They must ensure:

- traceability
- consistency
- structural clarity
- architectural history integrity

---

# 2. COMMIT STRUCTURE

All commits MUST follow:

type(scope): description

---

# 3. COMMIT TYPES

Allowed types:

- feat → new structural addition
- fix → structural correction
- refactor → structural reorganisation
- docs → documentation-only changes
- chore → maintenance / non-architectural updates
- lock → finalised or immutable definitions

---

# 4. SCOPE RULE

Scope must reflect architectural domain:

Valid:
- root
- g01dn
- constitutional
- protocol
- standards
- reference
- naming
- commit
- ip

Invalid:
- vague labels ("stuff", "update", "misc")

---

# 5. DESCRIPTION RULE

Descriptions must be:

- concise
- declarative
- structural in meaning
- non-narrative

Forbidden:
- emotional language
- personal commentary
- vague summaries

---

# 6. CHANGE CLASSIFICATION

Each commit must represent:

- structural addition
- structural modification
- structural correction
- structural clarification
- structural lock

---

# 7. EXAMPLES

Correct:

feat(g01dn): formalise inheritance rules  
fix(standards): resolve naming conflict  
lock(root): finalise identity boundary  
docs(reference): update system reference view  

Incorrect:

- "fixed stuff again"
- "cleaned things up"
- "idk reorganised it"

---

# 8. SYSTEM RULE

Commits represent system history.

Not developer intent.

Not narrative logs.

They are structural truth records.

---

# 9. STATUS

Canonical Commit Standard v1.1
All commits must conform.

© ProtoSynthesis 2026–Present
