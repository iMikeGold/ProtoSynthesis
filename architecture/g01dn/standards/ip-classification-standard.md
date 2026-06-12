
# PROTOSYNTHESIS INTELLECTUAL PROPERTY CLASSIFICATION STANDARD v1.1

Authority Level: Standard (L2)
Status: Canonical
Classification: Internal Architecture Governance Standard
Location: /architecture/g01dn/standards/ip-classification-standard.md
Depends On: G01DN Layer Definition Specification

---

# 0. VERSION NOTE

v1.1 introduces:

- structural alignment with G01DN layer system
- clarified distinction between architecture vs asset ownership
- reinforced classification enforcement rules
- improved repository governance mapping

---

# 1. PURPOSE

This standard defines the governance model for intellectual property within ProtoSynthesis.

It controls:

- visibility
- access
- ownership classification
- distribution rights
- derivative relationships

It ensures structural and commercial integrity across the system.

---

# 2. SCOPE

Applies to ALL ProtoSynthesis assets:

- architecture files
- standards
- protocols
- implementations
- research
- media
- systems
- derivatives

Across all repositories and deployment environments.

---

# 3. CLASSIFICATION MODEL

## 🟢 P — Public

Unrestricted access.

Includes:

- public documentation
- published architecture views
- external-facing content

Ownership remains intact.

---

## 🔵 I — Internal

Restricted to authorised contributors.

Includes:

- working architecture files
- internal drafts
- system design documents

Not for public distribution.

---

## 🟡 D — Derivative

Systems derived from ProtoSynthesis architecture.

Defines lineage, not visibility.

Examples:

- educational systems
- frameworks built on ProtoSynthesis
- applied implementations

May also carry P / I / R / K classification.

---

## 🟠 R — Restricted

Sensitive operational or commercial content.

Includes:

- strategy
- business logic
- operational systems
- private documentation

Access controlled.

---

## 🔴 K — Kernel

Highest sensitivity level.

Includes:

- core system logic
- proprietary architectures
- monetisable engines
- protected algorithms

Must NOT be publicly exposed.

---

# 4. CLASSIFICATION RULES

- Every asset MUST have a classification
- Highest applicable classification applies by default
- Downgrading classification requires explicit review
- Mixed classification is permitted (e.g. D+I, D+P)

---

# 5. DERIVATION RULES

Derivation defines lineage, not visibility.

A system may be:

- derived (D)
- but public (P)
- or restricted (R)
- or kernel-protected (K)

Derivation ≠ access level

---

# 6. REPOSITORY GOVERNANCE RULES

## Public Repositories
May contain:
- P assets only

## Internal Repositories
May contain:
- P, I, D, R assets

## Kernel Repositories
May contain:
- K assets only

---

# 7. STRUCTURAL RULE

No classification overrides architectural hierarchy.

G01DN and Root Specification remain above classification logic.

---

# 8. STEWARDSHIP PRINCIPLE

All assets must maintain:

- traceability
- controlled access
- architectural integrity
- ownership clarity

---

# 9. INVALID PATTERNS

- hiding K assets in public repos
- mislabelling internal assets as public
- breaking derivation traceability
- mixing classification rules across domains

---

# 10. STATUS

This document is the canonical IP Classification Standard v1.1.

All ProtoSynthesis assets must conform to it.

© ProtoSynthesis 2026–Present
