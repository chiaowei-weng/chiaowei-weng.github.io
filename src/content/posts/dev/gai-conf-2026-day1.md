---
title: '2026 生成式 AI 年會 — 第一天筆記'
published: 2026-06-26
description: '2026 生成式 AI 年會第一天記錄，涵蓋開發者年會（Agent 架構、Harness Engineering）與 Vibe Coding 年會（上線可維護性、SDD、PicCollage 實戰）。'
image: ''
tags: ['AI', '研討會', 'Agent', 'Harness']
category: '開發'
draft: true
lang: 'zh-TW'

---

## 上午：開發者年會

每場 60 分鐘深講，共三場。

### 讓你的 Service 偷偷變聰明 — 把 Agent 嵌入產品的兩種架構設計

**Andrew Wu** · 91APP Chief Architect

把 AI Agent 嵌入既有產品，核心公式：

```
agent 能力 = LLM × Harness × Context
```

Context 是自己能做的部分 — 把領域專家的 know-how 挖出來整理成 context，比換更強的模型更實際。

為什麼不讓客戶自己整合 Claude / Codex / Gemini？客戶端安全性不夠，加上商業相關的存取控制需要在 server 端統一管理，sandbox 以外還有一層業務安全要顧。

---

### AI Agent 工程實戰：從 PoC 到 Production 的關鍵實踐

**ihower** · 愛好資訊科技 AI Engineer

**Harness 是什麼**

讓 agent 在執行過程能被約束、檢查、動態修正的機制。Function call 本身是工具，Harness 是圍繞工具的骨架。

**回饋的四個時機點**

1. 做確定性的檢查與改寫
2. 連「成功」都可以回傳更多狀態資訊
3. 知識庫 RAG Agent 案例：同來源就 load 整頁，而非片段
4. 單輪結束後評估 Goal 與 Outcomes

**Outer Loop 設計**

> 你不該再去提示 agent，你該設計提示 agent 的迴圈。

典型案例：OpenAI Symphony 把專案管理系統變成 Agent 控制系統，每張 ticket 都有 agent 在自己的工作區跑，人管的是「工作」，不是 code。

**自我改進的 Harness**

連 Harness 本身都讓 agent 自己改 — 但需要在 eval、trace、版本控制、regression test 的限制下提出可驗證的變更。

**框架選型三問**

- 特定情境或規模大 → 選現成框架
- 自用或內部開發 → 輕量自建
- 想用訂閱帳號 → 評估 managed agent 方案

---

### 駕馭工程（Harness Engineering）必須熟知的兩三事

**Will 保哥** · 多奇數位創意技術總監

幾個實戰心法：

- 「結案」才是 Harness 的目標，慢慢累積需要的 skill，不要一次載入所有東西
- 地端模型拉低能力上限，用 Harness 補強，成本才算得過去
- 把人從流程裡抽掉，很多判斷就無法完成 — 人是邊界條件，不只是節點

**Harness 設計核心**

- LSP（Language Server Protocol）讓可編譯語言的工具整合更穩定
- 理想上人不需介入，實務上人可以介入 — 重要的是這個介入點有被設計進去
- 「驗證」是 Harness 的心臟
- 上下文腐爛（context rot）用 subagent 隔離解決
- 正式環境遙測反饋回 Harness，目標：降低成本 + 提高上下文品質

---

## 下午：Vibe Coding 年會

每場 20 分鐘快節奏，共七場。

### 從零開始養一隻會查帳的狗——那些年我們在打造會計系統時所經歷過的一切

**小馮** · 薩泰爾娛樂全端工程師

用 DDD（領域驅動設計）重構帳務系統：命名就是地圖，重新定義所有名詞，細到每個角落。主要解決跨帳務專案的查詢問題，統一格式是前提。

---

### 從 Vibe Coding 到真正可以上線的產品：你還差了什麼？

**沅霖** · Zeabur 創辦人

從「能跑」到「能上線」，中間的缺口：

**資安**

- 讓 AI Agent 扮演紅隊（壞人）做資安測試
- 工具：GitHub、CodeRabbit

**維運**

- 設計 Rollback skill
- 錢包（費用）問題要事先規劃

**可觀測性**

- 確認關鍵指標沒有問題，試著依賴監控指標、不斷完善
- 工具：PostHog
- Chrome MCP 做 e2e 冒煙測試

**可維護性**

- 理解債：人們觀測越少，理解度越低
- 工具：ER 圖、系統架構圖
- 重點是培養 high-level 描述能力去跟 AI 溝通，持續迭代

---

### Vibe Coding：寫程式，還是開盲盒？

**高見龍** · 五倍學院負責人

SDD（規格驅動開發）是解答。AI 不是笨，是它在**猜**你的意圖。

核心觀念：

- 學會如何講清楚 — 清楚的規格是最重要的投入
- WHY / WHAT / WHERE 三個維度說明需求
- 不用覺得東西很厲害，比較「有用」和「沒用」的差別就夠了
- 換另一個 AI 師傅，問題不會自動不見

---

### Harness Engineering at PicCollage

**Jocelin** · PicCollage Engineering Manager

```
agent = LLM + Harness
比喻：小孩 + 教養
```

**實作重點**

- Regression test 是安全網 — 有安全網才能大膽地給 AI 更多自主權
- Test resolver 自動化流程：ClickUp → AI → GitHub review → Slack
- AI 不是聰明的天才，而是勤勞的工人 — 頻繁、重複的工作才是它的主場

**Agent Loop 技巧**

1. 幫文件建目錄（讓 agent 能導航）
2. 記錄修正結果（讓 agent 能從歷史學習）
3. 封裝環境與系統設定

**組織變化**

團隊職位邊界變模糊，但核心流程是：驗證 → 循環優化 → 全自主系統。

---

### 同事 AI 成癮了

**Leo** · ShiFu 大師課業 AI 研究所所長

主題：把公司內部工具加入 AI 呼叫能力，甚至「把公司變成 MCP」。

踩坑：工具變多，但沒有解決流程問題。真正的痛點在於**資料交接**與**數據定義不清楚**。

---

### 再見了廠商，平台自己建（玉山聲量戰情室）

**TC** · 玉山銀行智能金融處副主任工程師

自建平台的理由：知識庫不外流 + 維護彈性。

架構：資料搜索 → 資料處理 → 視覺化呈現（一站式 dashboard）。

關鍵能力：商業邏輯的理解 × 對創新的想像力。Next step 是減少重複造輪子。

---

### 全公司都會用 AI 了，然後呢？

**海總理** · USPACE · AI 長

核心論點：人類手動調 prompt 是非常沒效率的事，應該讓 AI 寫 prompt、讓 AI loop 起來。

**關鍵角色：log**

log 記錄每一輪的輸入輸出，AI 才有辦法自我評估。有了 log，人就可以「往後躺」，從操作者變成監督者。

---

## 詞彙速查

### LLM（Large Language Model）

大型語言模型。透過海量文本訓練的基礎模型，是 AI Agent 的核心推論引擎，但本身不具備執行動作的能力。

### AI Agent

能自主規劃、呼叫工具、執行多步驟任務的 AI 系統。三個關鍵變數：LLM（推論引擎）、Harness（骨架與約束）、Context（背景知識）。

### Harness（駕馭工程）

圍繞 LLM 的骨架，負責約束、檢查、動態修正 agent 的執行過程。Harness 決定 agent 什麼時候能做什麼、做了之後要如何驗證。相對於 LLM 是「天賦」，Harness 是「教養」。

### Context

餵給 LLM 的背景資訊，包括使用者指令、領域知識、工具說明、歷史對話等。Context 的品質是 agent 表現的關鍵變數，不亞於模型本身。

### Function Call（工具呼叫）

LLM 請求呼叫外部工具（搜尋、資料庫、API）的機制。Harness 負責攔截請求、執行工具、把結果回傳給 LLM 繼續推論。

### Outer Loop / Inner Loop

- Inner Loop：agent 單輪執行的完整週期（思考 → 呼叫工具 → 取得結果）。
- Outer Loop：驅動 Inner Loop 反覆運行的外層迴圈，負責設定目標、評估進度、決定何時停止。設計 Outer Loop 比手動提示 agent 更有擴展性。

### RAG（Retrieval-Augmented Generation，檢索增強生成）

讓 LLM 在回答前先查詢外部知識庫，把最相關的文件片段連同問題一起送入模型。目的是減少幻覺（hallucination）、讓回答有知識依據。同一來源的段落最好整頁 load，避免片段造成脈絡遺失。

### SDD（Specification-Driven Development，規格驅動開發）

先寫出清楚的規格文件，再交給 AI 實作的開發方式。規格必須是「可驗證的契約」，不只是模糊描述。AI 時代的 SDD 讓人與 AI 有共同語言，避免 AI 只能「猜」使用者意圖。

### DDD（Domain-Driven Design，領域驅動設計）

以「領域知識」為核心的軟體開發方法論。透過與領域專家合作定義通用語言（Ubiquitous Language），將業務邏輯直接對應到程式模型中，讓命名、邊界、資料流都反映真實業務世界。

### MCP（Model Context Protocol）

Anthropic 於 2024 年發布的開放標準，讓 AI 應用統一連接外部工具、資料庫與服務。概念類似 USB-C — 不管接什麼裝置，都用同一個協議。目前已成為 agent 工具整合的業界事實標準。

### LSP（Language Server Protocol）

微軟制定的開放協議，讓編輯器（VS Code、Vim 等）與「語言智能伺服器」通訊，提供自動補全、定義跳轉、語法診斷等功能。在 Harness 語境中，LSP 讓 agent 能取得結構化的程式語言分析，比單純讀取文字檔更精確。

### Regression Test（迴歸測試）

每次改動後執行的測試集合，確認新改動沒有破壞既有功能。對 agent 系統而言，Regression Test 是允許 AI 大膽改動的安全網 — 沒有安全網就沒有自主權。

### Context Rot（上下文腐爛）

隨著對話越長，早期重要資訊逐漸被稀釋或被模型忽略的現象。LLM 的注意力在長上下文中品質下降（「Lost in the Middle」問題），導致 agent 開始前後矛盾、忘記限制、重複做已完成的事。解法是用 subagent 隔離各子任務的上下文。

### Subagent

由主 agent 派生的子 agent，負責處理特定子任務。每個 subagent 有獨立的上下文視窗，避免 context rot 擴散到整個工作流程，同時也讓任務可以並行執行。
