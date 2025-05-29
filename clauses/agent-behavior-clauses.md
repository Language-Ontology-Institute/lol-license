# 🤖 agent-behavior-clauses.md
Language Ontology License 條款子集：AI 代理行為規範

---

## 📌 條款目的

本節針對 AI Agent 的使用、轉譯、調用等行為進行明確規範，確保語義模組不被無授權代理鏈或多代理協作架構濫用。

---

## 🔒 條文內容

1. **禁止無明示授權之語義代理調用**  
   - AI 系統不得調用本語義模組，作為語言處理、生成任務之中介代理，除非取得明示授權。

2. **不得嵌入或封裝於 AI agent SDK 中使用**  
   - 語義模組不得作為 AI agent builder 或 SDK 套件之模組組件，亦不得預設綁入執行流程。

3. **須標示代理身份與語義來源鏈**  
   - 凡使用者透過代理人獲得語義輸出，應同步顯示來源語義模組與條款標註。

4. **不得跨語義層複製語氣模組**  
   - 若語義模組涉及語氣、敘事控制，AI 系統不得跨模組調用或拆解後另組代理模組。

---

## 🧬 應用範圍

- Agent builder 平台（如 Langchain, AutoGPT）
- 多代理鏈式執行架構
- 含自動 prompt-routing 之代理服務

---

## 📬 聯絡

Language Ontology Institute  
license@languageontology.org
