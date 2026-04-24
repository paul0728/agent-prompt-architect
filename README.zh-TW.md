# Agent Prompt Architect

> [English](./README.md)

一個教會 AI 程式碼助手如何使用 CO-STAR 框架生成結構化 Agent System Prompt 的 Skill。

這是一個 **Skill** — 一組指令，安裝後讓你的 AI 助手具備協助你互動式撰寫更好 Agent Prompt 的專業能力。

## 運作方式

1. 將 `skill/SKILL.md` 複製到你的 AI 工具的 skill/rules 目錄
2. 向 AI 助手請求協助：「幫我寫一個 agent 的 system prompt」
3. 助手依照 Skill 執行 — 訪談你、套用 CO-STAR、生成 prompt

## 安裝方式

```bash
npx skills add paul0728/agent-prompt-architect
```

或手動將 `skill/` 目錄複製到你的 AI 工具的 skills 位置：

| 工具 | 目標位置 |
|------|----------|
| Kiro | `.kiro/skills/agent-prompt-architect/` |
| Claude Code | `.claude/skills/agent-prompt-architect/` |
| Cursor | `.cursor/skills/agent-prompt-architect/` |
| GitHub Copilot | `.github/skills/agent-prompt-architect/` |
| Cline | `.cline/skills/agent-prompt-architect/` |
| Windsurf | `.windsurf/skills/agent-prompt-architect/` |

## Skill 教會了什麼

安裝後，你的 AI 助手會獲得以下能力：

1. **訪談你** — 詢問 agent 的角色、工具、約束條件和輸出格式
2. **套用 CO-STAR 框架** — 以 Context、Objective、Style、Tools、Anti-patterns、Response、Examples 結構化 prompt
3. **生成 few-shot 範例** — 用 ✅/❌ 對比取代冗長的規則描述
4. **執行品質檢查** — 驗證無硬編碼值、無衝突規則、輸出格式正確
5. **處理多 Agent 專案** — 建議檔案組織方式和各 agent 的慣例

## CO-STAR 框架

| 區段 | 用途 |
|------|------|
| **C**ontext（情境） | 執行時變數（時間、時區）— 動態注入 |
| **O**bjective（目標） | Agent 的角色和主要目標 |
| **S**tyle（風格） | 行為規則（何時呼叫工具 vs. 文字回應） |
| **T**ools（工具） | 可用工具及描述 |
| **A**nti-patterns（反模式） | 明確的「禁止」規則，附正確/錯誤範例 |
| **R**esponse（回應） | 輸出格式規範 |
| + **Examples**（範例） | 2-3 個具體的 input→output 對 |

## 架構支援

Skill 知道如何為以下架構撰寫 prompt：

- **ReAct Agent** — 帶推理的工具呼叫迴圈
- **Plan-then-Execute Agent** — 規劃器 + 循序執行器
- **Summary / 後處理 Agent** — 從工具輸出生成報告
- **多 Agent 協調器** — 路由和結果聚合

## 授權

MIT
