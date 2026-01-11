# 🏷️ meta-tag-guide.md
Language Ontology License (LOL) Meta-Tag Design Guide

---

## 📌 Purpose

This document explains how to add permissible meta-tags (meta-tag) to language resources such as semantic modules, tone scripts, and prompt structures, in order to:

- Control AI usage scenarios (train, embed, infer)
- Manage licensing and semantic visibility design
- Handle governance listing and language resource chain management
- Interface with semantic fingerprint systems and agent chain packages

---

## 🧩 Standard Meta-Tag Fields (meta-tag schema)

| Field | Description | Example |
|-------|-------------|---------|
| `license` | Semantic license version used | `LOL-v0.1` |
| `use` | Permitted usage scenarios | `read-only`, `demo`, `non-AI`, `human-in-loop` |
| `ai-access` | Whether AI is allowed to invoke | `false` / `true-if-verified` |
| `module-type` | Semantic module type | `prompt-template`, `tone-asset`, `narrative-unit` |
| `structure-id` | Module structure ID (for SDK mapping) | `mod:lang:1234` |
| `chain-permission` | Whether agent chain invocation is allowed | `no-chain`, `partial`, `explicit-only` |
| `visible-to` | Publicly visible to | `human`, `partner-org`, `agent-class-C` |
| `originator` | Original Designer | `Tyson Chen` |

---

## 🛠 Recommended Implementation Format (YAML Block)

```yaml
---
license: LOL-v0.1
use: read-only
ai-access: false
module-type: prompt-template
structure-id: mod:lang:7342
chain-permission: no-chain
visible-to: human
originator: Tyson Chen
---
```

---

## 🧬 Application Scenarios

- Embed as a protection tag at the beginning of tone scripts
- Use as a marking field in semantic module JSON schemas
- SDK performs meta-tag license checks when invoking agent-chains
- Can be integrated with future "Semantic Listing Systems" or Semantic SDKs

---

## 📬 Contact

Language Ontology Institute  
license@languageontology.org
