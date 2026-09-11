# Marketplace

> **A multi-sided platform subtype that intermediates transactions between distinct actor groups.**

```yaml
semantic_id: wsf:Marketplace
preferred_name: Marketplace
aliases: [Multi-sided Platform (transaction subtype)]
status: Baseline
version: 0.1.0
classification: Tier 3 (Specialisation)
parent: wsf:Platform
domain: Structure
```

## Definition

**Short:** A Platform subtype that intermediates transactions between distinct actor groups, monetising via take rates.

**Intuition:** A transaction venue — eBay, Amazon Marketplace, App Store, OTCHERE Marketplace.

## Necessary conditions

1. All Platform necessary conditions (inherited).
2. **Multi-sided intermediation** — MUST connect at least two distinct actor groups in a transaction relationship.
3. **Take-rate monetisation** — MUST extract value via per-transaction fees (or equivalent monetisation mechanism).

## Relationships

- **Specialises:** `wsf:Platform`
- **Related to:** `wsf:Multi-sided Market`, `wsf:Gatekeeper`, `wsf:Network Effect (Indirect/Cross-Side)`, `wsf:Trust Mechanisms`

---

*Marketplace is a Tier 3 specialisation of Platform. Status: Baseline.*
