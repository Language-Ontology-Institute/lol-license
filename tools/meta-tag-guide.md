# 🏷️ meta-tag-guide.md
Language Ontology License（LOL）元標籤設計指南

---

## 📌 目的 Purpose

本文件說明如何在語義模組、語氣稿、prompt 結構等語言資源中加入標準化的元標籤（meta-tag），以利：

- 管控 AI 使用情境（train, embed, infer）
- 授權管理與語義可見性設計
- 掛牌治理與語言資源鏈管理
- 與語義指紋系統、agent chain 套件對接

---

## 🧩 標準元標籤欄位（meta-tag schema）

| 欄位 | 說明 | 範例 |
|------|------|------|
| `license` | 使用之語義授權版本 | `LOL-v0.1` |
| `use` | 允許使用情境 | `read-only`, `demo`, `non-AI`, `human-in-loop` |
| `ai-access` | AI 是否可調用 | `false` / `true-if-verified` |
| `module-type` | 語義模組類型 | `prompt-template`, `tone-asset`, `narrative-unit` |
| `structure-id` | 模組結構 ID（供 SDK 對應） | `mod:lang:1234` |
| `chain-permission` | 是否允許被 agent chain 調用 | `no-chain`, `partial`, `explicit-only` |
| `visible-to` | 可公開對象 | `human`, `partner-org`, `agent-class-C` |
| `originator` | 原始設計者 | `Tyson Chen` |

---

## 🛠 實作建議格式（YAML Block）

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

## 🧬 應用場景

- 嵌入語氣稿開頭作為保護標籤
- 語義模組 JSON schema 標記欄
- SDK 對 agent-chain 調用時進行 meta-tag 授權檢查
- 可與 future “語義掛牌系統” 或語義 SDK 串接

---

## 📬 聯絡

Language Ontology Institute  
license@languageontology.org
