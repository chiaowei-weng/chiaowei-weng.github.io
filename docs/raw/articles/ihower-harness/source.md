---
marp: true
theme: default
paginate: true
size: 16:9

---

<style>
:root {
  --ink: #1d1d1f;
  --sub: #6e6e73;
  --blue: #0071e3;
  --panel: #f5f5f7;
  --line: #e3e3e6;
  --green: #2fa84f;
  --red: #d9405a;
  /* 從部落格文章帶過來的 SVG 圖表用變數 (light mode) */
  --bg: #ffffff;
  --surface: #f6f8fa;
  --border: #d1d9e0;
  --text: #1f2328;
  --text-secondary: #656d76;
  --accent: #0969da;
  --tag-bg: #ddf4ff;
}

section {
  font-family: -apple-system, "SF Pro Text", "Helvetica Neue", "PingFang TC", "Noto Sans TC", sans-serif;
  background: #ffffff;
  color: var(--ink);
  font-size: 26px;
  line-height: 1.5;
  padding: 60px 70px;
}

h1 { font-size: 60px; font-weight: 700; letter-spacing: -0.02em; }
h2 { font-size: 38px; font-weight: 700; letter-spacing: -0.01em; margin-bottom: 0.4em; }
h3 { font-size: 28px; font-weight: 600; color: var(--ink); }
a { color: var(--blue); text-decoration: none; }
strong { color: var(--ink); font-weight: 700; }
em { color: var(--blue); font-style: normal; font-weight: 600; }

ul, ol { margin-top: 0.2em; }
li { margin: 0.28em 0; }
code {
  font-family: "SF Mono", "JetBrains Mono", Menlo, monospace;
  background: var(--panel);
  border-radius: 6px;
  padding: 1px 7px;
  font-size: 0.86em;
}
pre {
  background: var(--panel);
  border: 1px solid var(--line);
  border-radius: 14px;
  padding: 22px 26px;
  font-size: 0.7em;
  line-height: 1.45;
}
pre code { background: none; padding: 0; }

section::after {
  color: var(--sub);
  font-size: 16px;
}

/* footer brand */
section footer { color: var(--sub); font-size: 16px; }

/* ---------- COVER ---------- */
section.cover {
  background: linear-gradient(180deg, #ffffff 0%, #f5f5f7 100%);
  padding: 80px 90px;
  justify-content: center;
}
section.cover h1 { font-size: 64px; line-height: 1.08; margin-bottom: 0.3em; }
section.cover .kicker { color: var(--blue); font-weight: 700; font-size: 24px; letter-spacing: 0.04em; }
section.cover .by { color: var(--sub); font-size: 26px; margin-top: 1.2em; }

/* ---------- SECTION DIVIDER ---------- */
section.section {
  background: var(--ink);
  color: #ffffff;
  justify-content: center;
}
section.section h1 { color: #ffffff; font-size: 70px; }
section.section .kicker { color: #6cb4ff; font-weight: 700; font-size: 26px; letter-spacing: 0.08em; }
section.section p { color: #c7c7cc; font-size: 26px; }
section.section::after { color: #6e6e73; }

/* ---------- LEAD (big statement) ---------- */
section.lead { justify-content: center; }
section.lead h2 { font-size: 50px; line-height: 1.25; }
section.lead p { font-size: 28px; color: var(--sub); }
.big { font-size: 46px; font-weight: 700; line-height: 1.3; letter-spacing: -0.01em; }

/* ---------- TWO COLUMNS ---------- */
.cols { display: grid; grid-template-columns: 1fr 1fr; gap: 36px; align-items: start; }
.cols-3 { display: grid; grid-template-columns: 1fr 1fr 1fr; gap: 24px; align-items: start; }

/* ---------- CARD / PANEL ---------- */
.card {
  background: var(--panel);
  border-radius: 18px;
  padding: 22px 26px;
}
.card h3 { margin: 0 0 0.3em 0; }
.card.blue { background: #eef6ff; }
.card.green { background: #eef9f0; }
.card.red { background: #fdeef1; }

.gap { margin-top: 36px; }
.gap-sm { margin-top: 24px; }

/* ---------- QUOTE ---------- */
.quote {
  margin-top: 40px;
  font-size: 30px;
  font-weight: 600;
  line-height: 1.4;
  border-left: 5px solid var(--blue);
  padding-left: 24px;
  color: var(--ink);
}
.cite { color: var(--sub); font-size: 20px; margin-top: 8px; }

/* ---------- TABLE ---------- */
table { font-size: 0.82em; border-collapse: collapse; width: 100%; }
th { background: var(--ink); color: #fff; font-weight: 600; padding: 10px 14px; text-align: left; }
td { padding: 9px 14px; border-bottom: 1px solid var(--line); }
tr:nth-child(even) td { background: var(--panel); }

.pass { color: var(--green); font-weight: 700; }
.fail { color: var(--red); font-weight: 700; }

.small { font-size: 0.82em; color: var(--sub); }
.tag { display:inline-block; background: var(--blue); color:#fff; border-radius: 999px; padding: 2px 14px; font-size: 18px; font-weight: 600; }
.center { text-align: center; }
img { border-radius: 12px; }
</style>

<!-- _class: cover -->
<!-- _paginate: false -->

<div class="cols">
<div>

<span class="kicker">給 Agent 開發者的</span>

# Harness + Loop Engineering

<div class="by">2026/6/26<br><strong>ihower</strong> @ 生成式 AI 開發者年會</div>

</div>
<div class="center">

![w:280](harness-qrcode.jpg)

<div class="small">投影片<br><a href="https://ihower.tw/presentation/harness.html">https://ihower.tw/presentation/harness.html</a></div>

</div>
</div>

---

## 我是誰

<div class="cols">
<div>

**張文鈿**，網路暱稱 *ihower*

- 2002 年起從事 Web 軟體開發
- 2005 年 個人部落格 <https://ihower.tw>
- 2018 年 自行開業「愛好資訊科技」<https://aihao.tw>
- 2023 年 開始經營 **AI Engineer 電子報**
- 開源貢獻: [OpenAI Agents SDK](https://github.com/openai/openai-agents-python/pulls?q=is%3Apr+author%3Aihower+)
- 我的課程「大語言模型 LLM 應用開發工作坊」<https://aihao.tw/llm>

</div>
<div class="center">

![w:320](photo3.jpg)

</div>
</div>

---

## Agenda

<div class="cols">
<div>

1. Recap: 什麼是 Deep Agent<br>
2. **什麼是 Harness Engineering** 🎯<br>
3. **時機 ①: 工具執行內**<br>
4. **時機 ②: request 之間注入**<br>
5. **時機 ③: 單輪結束（stop hook）**<br>
6. **時機 ④: 外層 Loop**<br>
7. 進階: 自我改進的 Harness<br>
8. 收尾: 會過期的 Harness<br>
9. 番外: 自建 Agent 的框架選型<br>

</div>
<div class="center">

![h:430](blog-list.jpg)

</div>
</div>

<div class="small gap-sm">📚 搭配有 9 篇的 blog 系列《給 Agent 開發者的駕馭工程》長篇文章 👉 <a href="https://blog.aihao.tw">blog.aihao.tw</a></div>

---

## 👥 預期聽眾

多數談 Harness Engineering 是在講 Claude Code、Codex 來做軟體開發流程。

本場<strong>不是</strong>這個角度，而是站在「**自行開發 AI Agent**」的切入點。你要做的可能是 Text-to-SQL Agent、知識庫 RAG Agent，場景各式各樣，用途不一定是軟體開發。

<div class="quote">
Harness Engineering 可以適用於<strong>開發任何場景的 AI Agent</strong>
</div>

---

<!-- _class: section -->
<!-- _paginate: false -->

<span class="kicker">PART 1</span>

# Recap:<br>什麼是 Deep Agent

---

## 複習 Agent 1.0 迴圈

![w:980 Agent 迴圈: Input → LLM 挑選工具 → Tools → 執行得到 Tool Result → 觀察結果回到 LLM，呼叫工具 N 次後輸出 Output](agent-loop.jpg)

<div class="small center gap-sm">呼叫工具 N 次、每次都把結果讀回來，直到沒有工具要呼叫才輸出</div>

---

## Agent 2.0 (Deep Agent) 的六項能力

這些能力讓 Agent 應付更大更複雜的任務，技術上都是用到 **Function Calling** 來實現的

| 能力 | 做什麼 |
|---|---|
| **Plan & Todos** | 拆解大任務，依序執行 |
| **Filesystem & Bash** | 操作檔案、執行程式（搭配 sandbox） |
| **Sub-Agent** | 把耗 token 的任務分給子代理人，隔離 context |
| **Memory** | 跨 session 記得使用者與專案的長期資訊 |
| **Skills** | 按需動態載入的技能 prompt |
| **更多工具** | MCP、Browser、Computer Use |

<div class="cite">代表產品: <a href="https://www.claude.com/product/claude-code">Claude Code</a>、<a href="https://github.com/openai/codex">Codex</a>、<a href="https://github.com/google-gemini/gemini-cli">Gemini CLI</a>、LangChain <a href="https://blog.langchain.com/deep-agents/">Deep Agents</a></div>

---

## Deep Agent 內建能力 ①: Plan & Todos

<div class="cols">
<div class="card">

### 🎯 它解決什麼問題

- 只靠 in-context 規劃，思路容易被中間步驟干擾、遺失
- 改用工具維護外部 todo list，**不會忘記**沒做完的事

</div>
<div class="card blue">

### 🔧 技術上怎麼辦到

透過 Function Calling 提供工具:

- `TaskCreate` 建立任務項目
- `TaskGet` 取得任務詳情
- `TaskUpdate` 更新任務狀態
- `TaskList` 列出所有任務

</div>
</div>

---

## Deep Agent 內建能力 ②: Filesystem & Bash

<div class="cols">
<div class="card">

### 🎯 它解決什麼問題

- **Filesystem** 讀寫改檔，**Bash** 執行任意 shell 指令
- 讓 Agent 真的**動手做事**:編譯、跑測試、git、裝套件

</div>
<div class="card blue">

### 🔧 技術上怎麼辦到

透過 Function Calling 提供工具:

- `Read`／`Edit`／`Write` 讀寫檔案
- `Bash` 執行 CLI 指令
- `Glob`／`Grep` 搜尋檔案

</div>
</div>

---

## Deep Agent 內建能力 ③: Sub-Agent

<div class="cols">
<div class="card">

### 🎯 它解決什麼問題

- 主 agent 派子代理去研究、查找、驗證
- 子 agent 是**獨立 context** 跑，只回精簡摘要（**context 隔離**）
- 可**平行化**:多個子 agent 同時工作

</div>
<div class="card blue">

### 🔧 技術上怎麼辦到

透過 Function Calling 提供工具:

- 一個叫做 `Agent` 的工具
- 工具內就是**呼叫另一個 Agent** 執行，把子 agent 輸出回傳給主 agent

</div>
</div>

---

## Deep Agent 內建能力 ④: Memory

<div class="cols">
<div class="card">

### 🎯 它解決什麼問題

- 把**重要資訊存起來**，下次再開 agent，**它還記得**
- 例:Claude Code 的 `CLAUDE.md`、Codex 的 `AGENTS.md`、長期 memory 儲存

</div>
<div class="card blue">

### 🔧 技術上怎麼辦到

- Agent 一啟動就**預設載入** `AGENTS.md`
- 使用者可以自己要求**更新** `AGENTS.md`
- 可自行設計記憶行為:記什麼、存在哪些目錄檔案、什麼時候回憶哪些內容

</div>
</div>

---

## Deep Agent 內建能力 ⑤: Skills

<div class="cols">
<div class="card">

### 🎯 它解決什麼問題

- 為特定任務打包的 **prompt ＋工具配置＋程式碼**
- **不全部塞進 context**，用到才載入；寫 markdown 就能新增
- 例:翻譯 skill、寫部落格 skill、處理 PDF skill

</div>
<div class="card blue">

### 🔧 技術上怎麼辦到

- 預設 system prompt 只載入 **skills 列表**
- 使用者需要某個 skill 時，Agent 才用讀檔工具**載入完整 skill 內容**

</div>
</div>

---

## Deep Agent 內建能力 ⑥: 更多工具

<div class="cols">
<div class="card">

### 🎯 它解決什麼問題

- **MCP**: 接外部 Slack、Gmail、Notion、自建 API…
- **Browser**: 瀏覽網頁、填表單、點按鈕，能上網做事或用網頁驗證自己的產出
- **Computer Use**: 直接操作桌面 GUI（看螢幕、移動滑鼠、敲鍵盤）

</div>
<div class="card blue">

### 🔧 技術上怎麼辦到

- Browser 與 Computer Use 需要**多模態模型**:讓 AI 看截圖判斷下一步該點哪裡
- MCP 標準化工具協議

</div>
</div>

---

## 但有能力 ≠ 把事情做好

<div class="cols gap-sm">
<div class="card green">

### ✓ 能力給了你能不能做

能讀檔、跑指令、開子代理、記憶、用工具。

</div>
<div class="card" style="background:#fff8c5;">

### ? 但是做得對不對 · 做完了沒

這一步的產出對嗎？整個任務做完了沒？怎麼穩定地做好、做完？

</div>
</div>

---
<!-- _class: section -->
<!-- _paginate: false -->

<span class="kicker">PART 2</span>

# 什麼是<br>Harness Engineering

---

## 「做完了」誰說了算?

<div class="cols">
<div>

- Agent 自信地宣稱完成，但東西是壞的
- 測試沒跑、需求沒做完，它說「已全部完成 ✅」
- 你指出問題，它道歉，然後再犯

</div>
<div class="card red">

### 這不是個案

Anthropic 整理長時間執行 agent 的失敗模式，**第一名就是「過早宣告完成」**。

</div>
</div>

<div class="cite">參考:Anthropic <a href="https://www.anthropic.com/engineering/effective-harnesses-for-long-running-agents">Effective harnesses for long-running agents</a></div>

---

## 什麼是 Harness? ➡️ Agent = Model + Harness

<div class="cols">
<div>

這是網路上常見的定義

**模型以外的一切**（system prompt、工具、編排、hooks）都算 harness。

</div>
<div class="card red">

### 小小吐槽 🤷

這定義有點偷懶

> 就像說「整體 = 核心 + 其他」

這個其他到底是什麼，我們需要**更可以操作的技術拆解**!

</div>
</div>

<div class="cite">定義出自: <a href="https://www.langchain.com/blog/the-anatomy-of-an-agent-harness">The Anatomy of an Agent Harness</a>（Viv Trivedy）</div>

---

## 首先，harness 不只是技術功能列表

<div class="cols">
<div class="card red">

### ❌ 不是這個

Skills、Sub-Agent、Hooks、Filesystem、worktree

這些都只是**手段**，不是 Harness Engineering 的思維核心。

</div>
<div class="card blue">

### ✅ 真正的主軸

是如何讓 agent 在**執行過程**能被**約束、檢查、動態修正**

</div>
</div>

---

## 回顧 Prompt、Context、Harness 三層

常被講成一條「演進」之路，但其實技術累加的都會用上，只是各自凸顯一個新的工程焦點:

| | 核心問題 | 技術功能 |
|---|---|---|
| **Prompt Engineering** | 怎麼讓模型**這一次**答得更好 | system prompt、few-shot、evals |
| **Context Engineering** | 在 context window 限制下**選擇**該放的資訊 | RAG、memory、compaction、tool offload |
| **Harness Engineering** | 怎麼在**執行過程**中約束、檢查、動態修正 | skills、filesystem、hooks |

<p>並沒有「XXX 已死」這回事，後者是基於前者的發展之上，而非取而代之。</p>

---

## Harness 核心策略: 先 generate，再 verify

核心策略就是: **驗證 (verification)**，廣義的說就是 **回饋(feedback)**

<div class="cols">
<div class="card red">

### 常見失敗

agent 輸出答案 → agent 覺得「看起來沒問題」→ 就停了。

</div>
<div class="card blue">

### 解法: generate → verify → fix

模型有自我修正的能力，但我們需要讓 Agent 順利觸發進入「輸出 → 回饋驗證 → 修正」這個流程。

</div>
</div>

<div class="small gap-sm">那工程上怎麼確保 verify「真的會發生」？</div>

---

## 兩個軸把 harness 拆解

Thoughtworks 用兩個軸拆解 harness 作法: **方向**×**型態**:

| | 運算式 Computational（確定性、程式工具）| 推論式 Inferential（LLM 生成）|
|---|---|---|
| **前饋 Feedforward**<br>引導器 Guides（行動前引導）| 用程式工具產生的 code metadata 與約束：LSP、Codemod／ast-grep、架構規則（ArchUnit 等）| **system prompt**、AGENTS.md、Skills、bootstrap instructions、how-to 文件 |
| **回饋 Feedback**<br>感測器 Sensors（行動後修正）| 測試、linter、type checker、靜態分析（eslint、semgrep）、pre-commit hook | **LLM as Judge**、AI code review、Review Skills |

<div class="small gap-sm">原文是針對 coding agent 場景，但此框架被我延伸到非 coding agent 上</div>

<div class="cite">參考:Birgitta Böckeler（Thoughtworks）<a href="https://martinfowler.com/articles/harness-engineering.html">Harness engineering for coding agent users</a></div>

---

## 好的 Harness 做兩件事

<div class="cols">
<div class="card">

### 🧭 Guides 前饋

**提高「一次做對」的機率**

文件、skills、範例、架構約束。

軟性引導，做不做最後還是要看 agent

</div>
<div class="card blue">

### 📡 Sensors 回饋

**輸出之後，感測提供回饋，引導 Agent 自我修正**

測試、linter、judge、AI review。

用程式自動觸發，不靠 Agent 自覺。

</div>
</div>

<div class="quote">好的 harness 同時做兩件事: 提高「一次做對」的機率，並在出錯時能自我修正。</div>

---

## 前饋 Guides

你的 system／developer prompt，要把「什麼是好的結果」以及「驗證流程」寫清楚。
例如 AGENTS.md／CLAUDE.md 都會要求 Agent 要去做驗證

<div class="cols">
<div class="card">

### Claude Code

> 「**非常重要**:完成任務時你**必須**執行 lint 和 typecheck（npm run lint、ruff…），確保程式碼正確。」

</div>
<div class="card">

### Codex

> 「如果 AGENTS.md 裡有可程式化的檢查，你**必須**全部執行並盡力驗證通過。即使只是改文件也一樣。」

</div>
</div>

<div class="cite">參考:敏捷三叔公 <a href="https://agile3uncles.com/2026/04/15/claude-code-harness-web-to-do-list/">最小可行 harness</a>、<a href="https://blog.aihao.tw/2026/05/03/agents-md-research-and-practices/">AGENTS.md 該寫什麼</a></div>

---

## 前饋的限制

前饋終究是**軟性、機率性**的引導

你在 AGENTS.md 寫十遍「一定要驗證」，模型還是有可能跳過 😢

---

## 回饋 Sensors: 把 verify 變成自動執行

前饋是軟性引導；回饋則用程式**自動執行**，不靠模型自覺

這可以插在 Agent lifecycle 的不同位置，來給 Agent 回饋。

本場將深入講解回饋的四個時機點

<div class="cols gap-sm">
<div class="card">

**① 工具執行內**（Part 3）

**② request 之間注入**（Part 4）

</div>
<div class="card blue">

**③ 單輪結束 · Stop hook**（Part 5）

**④ 外層 Loop**（Part 6）

</div>
</div>

---

## 當然，前饋和回饋缺一不可

<div class="cols">
<div class="card red">

### 若只有回饋、沒有前饋

agent 寫 code → 測試失敗 → 改 → 再失敗，跑好幾輪還是超時。

通常不是回饋不夠，是 agent 從頭就不知道「好的執行過程跟結果」該有的樣子。

</div>
<div class="card red">

### 若只有前饋、沒有回饋

Agent 可能跳過驗證流程，可能沒有確實做好驗證。不知道做的對不對、不確定做完了沒

</div>
</div>

<div class="quote">
    Agent 需要前饋一開始走對方向，也需要回饋負責把關修正。兩者缺一不可。
</div>

---

<!-- _class: lead -->

<div class="big">Harness Engineering:<br>讓 Agent 依目標<strong>持續、正確地動作</strong>的工程。</div>

<p class="gap-sm">本場將重點講「回饋訊號」:要有東西能判斷<strong>做得好不好、做得對不對、做完了沒</strong>。</p>

---

## 回饋的四個時機點

把 agent 的迴圈由內而外拆解，回饋有四個時機點:

| 時機 | 多久觸發一次 | 成本 | 修正粒度 | 對應的 hook |
|---|---|---|---|---|
| **① 工具執行內** | 每次 tool call | 毫秒，最便宜 | 單一動作 | Pre／PostToolUse |
| **② request 之間注入** | 使用者或程式想注入時 | 趨近零 | 當前這一輪的方向 | 無專屬 hook |
| **③ 單輪結束** | 每一輪 | 秒級 | 整輪的產出 | Stop hook |
| **④ 外層 Loop** | 每個 session | 分鐘到小時 | 整個任務 | 排程／外迴圈 |

---

## 回饋的四個時機 ①②③④

<svg viewBox="0 0 720 342" style="width:100%;max-width:1040px;height:auto;display:block;margin:6px auto 0;font-family:-apple-system,'PingFang TC','Noto Sans TC',Helvetica,Arial,sans-serif;" xmlns="http://www.w3.org/2000/svg">
<defs>
<marker id="he2arr" viewBox="0 0 10 10" refX="8" refY="5" markerWidth="7" markerHeight="7" orient="auto-start-reverse"><path d="M0,0 L10,5 L0,10 z" style="fill:var(--text-secondary)"/></marker>
<marker id="he2arrA" viewBox="0 0 10 10" refX="8" refY="5" markerWidth="7" markerHeight="7" orient="auto-start-reverse"><path d="M0,0 L10,5 L0,10 z" style="fill:var(--accent)"/></marker>
</defs>
<rect x="10" y="40" width="700" height="296" rx="14" style="fill:var(--bg);stroke:var(--text-secondary);stroke-width:1.5;stroke-dasharray:6 5"/>
<rect x="26" y="27" width="332" height="27" rx="13.5" style="fill:var(--bg);stroke:var(--text-secondary);stroke-width:1.5"/>
<text x="40" y="45" style="fill:var(--text);font-size:13px;font-weight:700">④ 外層 Loop</text>
<text x="118" y="45" style="fill:var(--text-secondary);font-size:11.5px">· 每個 session · 分鐘~小時 · 修正整個任務</text>
<rect x="34" y="78" width="652" height="154" rx="12" style="fill:var(--surface);stroke:var(--accent);stroke-width:1.5"/>
<rect x="50" y="65" width="170" height="26" rx="13" style="fill:var(--surface);stroke:var(--accent);stroke-width:1.5"/>
<text x="63" y="82" style="fill:var(--accent);font-size:12.5px;font-weight:700">③ 一輪 Turn</text>
<text x="138" y="82" style="fill:var(--text-secondary);font-size:11px">· 秒級</text>
<text x="52" y="111" style="fill:var(--text-secondary);font-size:11px">使用者輸入</text>
<line x1="52" y1="117" x2="52" y2="138" style="stroke:var(--text-secondary);stroke-width:1.4" marker-end="url(#he2arr)"/>
<rect x="48" y="138" width="86" height="40" rx="7" style="fill:var(--bg);stroke:var(--border);stroke-width:1.3"/>
<text x="91" y="155" text-anchor="middle" style="fill:var(--text);font-size:12px;font-weight:600">模型</text>
<text x="91" y="170" text-anchor="middle" style="fill:var(--text-secondary);font-size:10px">request 1</text>
<line x1="134" y1="158" x2="168" y2="158" style="stroke:var(--text-secondary);stroke-width:1.4" marker-end="url(#he2arr)"/>
<rect x="170" y="138" width="86" height="40" rx="7" style="fill:var(--tag-bg);stroke:var(--accent);stroke-width:1.3"/>
<text x="213" y="155" text-anchor="middle" style="fill:var(--accent);font-size:12px;font-weight:600">🔧 tool calls</text>
<text x="213" y="170" text-anchor="middle" style="fill:var(--accent);font-size:10px;font-weight:700">①</text>
<line x1="256" y1="158" x2="290" y2="158" style="stroke:var(--text-secondary);stroke-width:1.4" marker-end="url(#he2arr)"/>
<rect x="292" y="138" width="86" height="40" rx="7" style="fill:var(--bg);stroke:var(--border);stroke-width:1.3"/>
<text x="335" y="155" text-anchor="middle" style="fill:var(--text);font-size:12px;font-weight:600">模型</text>
<text x="335" y="170" text-anchor="middle" style="fill:var(--text-secondary);font-size:10px">request 2</text>
<line x1="378" y1="158" x2="412" y2="158" style="stroke:var(--text-secondary);stroke-width:1.4" marker-end="url(#he2arr)"/>
<rect x="414" y="138" width="86" height="40" rx="7" style="fill:var(--tag-bg);stroke:var(--accent);stroke-width:1.3"/>
<text x="457" y="155" text-anchor="middle" style="fill:var(--accent);font-size:12px;font-weight:600">🔧 tool calls</text>
<text x="457" y="170" text-anchor="middle" style="fill:var(--accent);font-size:10px;font-weight:700">①</text>
<line x1="500" y1="158" x2="534" y2="158" style="stroke:var(--text-secondary);stroke-width:1.4" marker-end="url(#he2arr)"/>
<rect x="536" y="138" width="92" height="40" rx="7" style="fill:var(--bg);stroke:var(--border);stroke-width:1.3"/>
<text x="582" y="155" text-anchor="middle" style="fill:var(--text);font-size:12px;font-weight:600">模型</text>
<text x="582" y="170" text-anchor="middle" style="fill:var(--text-secondary);font-size:10px">輸出答案</text>
<line x1="628" y1="158" x2="648" y2="158" style="stroke:var(--accent);stroke-width:1.5" marker-end="url(#he2arrA)"/>
<rect x="650" y="134" width="22" height="48" rx="6" style="fill:var(--tag-bg);stroke:var(--accent);stroke-width:1.6"/>
<text x="661" y="164" text-anchor="middle" style="fill:var(--accent);font-size:14px;font-weight:800">③</text>
<rect x="206" y="95" width="334" height="22" rx="11" style="fill:var(--surface);stroke:var(--accent);stroke-width:1.2"/>
<text x="373" y="110" text-anchor="middle" style="fill:var(--accent);font-size:10.5px;font-weight:700">② request 之間注入 (人 steer 或程式)</text>
<path d="M 284 117 L 284 150" style="fill:none;stroke:var(--accent);stroke-width:1.2;stroke-dasharray:3 2" marker-end="url(#he2arrA)"/>
<path d="M 518 117 L 518 150" style="fill:none;stroke:var(--accent);stroke-width:1.2;stroke-dasharray:3 2" marker-end="url(#he2arrA)"/>
<text x="320" y="197" text-anchor="middle" style="fill:var(--text-secondary);font-size:10.5px">① 工具執行內 · 修正單一動作</text>
<path d="M 650 182 L 650 212 Q 650 218 644 218 L 99 218 Q 91 218 91 212 L 91 180" style="fill:none;stroke:var(--accent);stroke-width:1.3;stroke-dasharray:4 3" marker-end="url(#he2arrA)"/>
<rect x="252" y="208" width="216" height="19" rx="9.5" style="fill:var(--surface);stroke:var(--accent);stroke-width:1"/>
<text x="360" y="221" text-anchor="middle" style="fill:var(--accent);font-size:10.5px">Stop hook 沒過 → 同份 context 再跑一輪</text>
<text x="360" y="254" text-anchor="middle" style="fill:var(--text);font-size:11.5px">一輪 (Turn) = 多次「模型 request → tool calls」反覆，直到模型輸出答案</text>
<path d="M 672 182 L 672 302 Q 672 310 664 310 L 42 310 Q 30 310 30 300 L 30 168 Q 30 158 40 158 L 46 158" style="fill:none;stroke:var(--text-secondary);stroke-width:1.6" marker-end="url(#he2arr)"/>
<rect x="150" y="300" width="424" height="20" rx="10" style="fill:var(--bg);stroke:var(--text-secondary);stroke-width:1.3"/>
<text x="362" y="314" text-anchor="middle" style="fill:var(--text);font-size:11px;font-weight:600">④ 通過後這個 session 收掉，換上全新 context 再跑一圈</text>
</svg>

---
<!-- _class: section -->
<!-- _paginate: false -->

<span class="kicker">PART 3 · 時機 ①</span>

# 在工具執行內

---

## Tool Call 裡面

工具呼叫內，有三個可以設計的地方:

<div class="cols-3">
<div class="card">

### 執行前: 驗證輸入

確定性檢查參數與內容，
擋掉危險或無效的呼叫

</div>
<div class="card">

### 執行後: 檢查結果

對結果做品質檢查，
必要時就地修復或重試

</div>
<div class="card blue">

### 工具回傳值+夾帶指引

tool response 不只回資料，**還夾帶指示與 metadata**，引導 Agent 的下一步

</div>
</div>

---

<!-- _class: lead -->

## 工具輸出不只是 function output，<br>是你寫給 Agent 的回饋

<p>寫程式習慣把回傳值當「資料」: 查到什麼回什麼，出錯就回傳 error code</p>

<div class="big gap-sm">但對 Agent 來說，<strong>tool response 也是一個對話訊息</strong>:<br>你可以在裡面夾帶指示、更多資訊 metadata，<br>甚至告訴 Agent 下一步怎麼做。</div>

---

## 案例: Text-to-SQL Agent

<div class="cols">
<div class="card">

### 場景

使用者用自然語言問財務數據，

Agent 基於 DB schema 產生 SQL

用 `execute_sql(sql_query)` 工具查詢。

</div>
<div class="card red">

### LLM 生成 SQL 的風險

- **幻覺**不存在的表格和欄位
- 生成查詢以外的危險語法
- 忘記**分頁**，回傳爆量資料
- SQL dialect 語法不同

</div>
</div>

<div class="small gap-sm">
我們會在 system prompt 插入 table schema 說明有哪些 tables/columns，以及各種 SQL 限制，這是前饋要先寫好。</div>

---

## 在工具內: 把 SQL 解析成語法樹(AST)，做確定性的檢查和改寫

```python
import sqlglot
from sqlglot import exp

tree = sqlglot.parse_one(sql_query, dialect="postgres")

# 1. 只允許 SELECT（擋下來）
if not isinstance(tree, exp.Select):
    return "只允許 SELECT 查詢"

# 2. 資料表白名單（擋下來）
for table in tree.find_all(exp.Table):
    if table.name not in ALLOWED_TABLES:
        return f"資料表 {table.name} 不在允許範圍，可用：{ALLOWED_TABLES}"

# 3. 沒 LIMIT 就補安全上限（補強）
if tree.args.get("limit") is None:
    tree = tree.limit(200)

safe_sql = tree.sql(dialect="postgres") # 確保輸出 postgres 語法
```

---

## 工具回饋的設計

驗證沒過時，tool response 的品質決定 Agent 自我修正的能力

<div class="cols gap-sm">
<div class="card red">

### ❌ 爛 error

```text
ERROR: column "revenue_growth"
does not exist
```

Agent 只能瞎猜重試，越改越歪。

</div>
<div class="card green">

### ✅ 好 error

```text
欄位 revenue_growth 不存在。
financial_metrics table 可用欄位有：
revenue, revenue_yoy, gross_margin…
和 revenue_growth 最相似的欄位有 revenue_yoy, revenue_qoq
```

下一步直接被導正。

</div>
</div>

<div class="quote">每個失敗訊息都是引導模型再次做對的<strong>好機會</strong></div>

---

## 連「成功」都可以回傳更多狀態資訊

<div class="cols">
<div class="card red">

### ❌ 陽春的成功 flag

`{"success": true}` 或 `{"count": 0}`

- 查詢成功但 0 筆，是真的沒有結果，還是查詢不正確?
- 是改了幾筆，也看不出來

</div>
<div class="card green">

### ✅ 回傳更多狀態資訊

把規模與範圍寫清楚:

- 影響幾筆、動了哪些欄位或區塊
- 有沒有碰到不該碰的

更多資訊，Agent 才有依據判斷「這次結果合不合理」，是否要修正

</div>
</div>

<div class="quote">錯誤要設計，成功也要設計。一個陽春的成功 flag，也可能是「假完成」的訊號</div>

---

## 工具回傳的引導訊息

各種純運算式(Computational)的檢查，回傳的是對應的固定訊息:

```python
def collect_feedback(output, source):
    # 純運算式檢查:規則直接判定,不靠 LLM,沒過就回寫死的固定訊息
    msgs = []
    if count_words(output) > 500:
        msgs.append("摘要超過 500 字，請縮短")
    if missing_required_terms(output):
        msgs.append("漏掉必留的專有名詞，請補回")
    if cosine_similarity(output, source) < 0.8:
        msgs.append("與原文語意偏離，請貼近來源重寫")
    return msgs
```

<div class="cols gap-sm">
<div class="card">

### 運算式檢查（固定訊息）

回**事先寫死**的固定字串:又快又穩又可重現。

</div>
<div class="card blue">

### 語意 judge（當場生成）

若沒辦法用純運算式的檢查，也可用 LLM 當 judge，附上回饋的 **reasoning** 理由。

</div>
</div>

---

## 設計回傳值的另一個重點: 需要有意識地控制 context window

注意控制別塞滿 context。context 過了某個門檻，模型會變笨(context rot)

別忘了 [Context Engineering](https://ihower.tw/blog/12817-context-engineering) 的整套策略，各種縮減 context 的技術:

<div class="cols-3 gap-sm">
<div class="card">

### Context Offloading

**硬性工具輸出上限**、**頭尾保留** (切頭切尾)、**卸載到檔案** (只留預覽 ＋ 路徑，有需要 Agent 再打開看)

</div>
<div class="card">

### 檢索技術

關鍵字、向量檢索、reranker 等，只挑選相關的 context

</div>
<div class="card">

### Sub-Agent

龐大的中間過程交給 sub-agent 在獨立 context 跑，只回傳結論

</div>
</div>

---

## 案例: 知識庫 RAG Agent

知識庫問答 Agent 會配一個 `search_knowledge(query)` 工具 (關鍵字搜尋＋向量搜尋 等)

工具不只回傳搜尋結果，我們還可以回傳以下資訊，回饋給 Agent 更多資訊:

<div class="cols-3 gap-sm">
<div class="card">

### 1️⃣ 標註來源與分數

回傳時標上來源和相關度分數，讓 Agent 有依據判斷哪些該引用、哪些該丟

</div>
<div class="card">

### 2️⃣ 同源就 load 整頁

好幾個 chunk 都來自同一份文件 → 暗示整份相關。**可以指示 Agent 直接把整頁讀回來**，比散落片段好用

</div>
<div class="card blue">

### 3️⃣ 看見 top-k 以外的資訊

回傳不只 top-k 搜尋結果，還夾帶整個資料集的統計

</div>
</div>

<div class="cite">參考:Jason Liu <a href="https://jxnl.co/writing/2025/08/27/facets-context-engineering/">Beyond Chunks: Why Context Engineering is the Future of RAG</a></div>

---

## 工具回傳除了 top-k，還夾帶統計與指示

```xml
<results query="API timeout issues">
  <ticket id="LIN-1247" status="Done">…</ticket>
  <ticket id="LIN-1189" status="Done">…</ticket>
</results>
<facets>
  <status_facet> <value name="Done" count="6"/> <value name="Open" count="5"/> </status_facet>
</facets>
<system-instruction>
  回傳的 2 筆全是 Done。facets 顯示另有 5 筆 Open 沒進 top-k，請改用 search(query, status="Open") 追查進行中的問題。
</system-instruction>
```

<div class="cols gap-sm">
<div class="card">

### `<facets>` 揭露隱藏資料

告訴 Agent:符合的不只你看到這 2 筆，還有 5 筆 Open 沒進 top-k

</div>
<div class="card blue">

### `<system-instruction>` 額外的指示

直接在工具輸出裡告訴 Agent 下一步該怎麼搜

</div>
</div>

---

## 語意 judge: 把回饋交給另一個模型

呼叫另一個模型做 review，把回饋當 tool response 帶回來。從主迴圈看，這仍是一次普通的 tool call。

```python
@function_tool
async def consult_model(question, files, model):
    """遇到難題、想確認方向、或要 review 產出時呼叫，
    交給另一個模型給獨立回饋。"""
    ...
```

例如: RAG Agent 生成答案後，用另一個模型檢查有沒有幻覺。

---

## 案例: Claude Code ＋ Codex plugin

這種做法在 coding agent 上也蠻常見

<div class="card blue">

`/codex:review`: Claude 把本地 git 改動交給 **Codex（GPT）** 做 code review，並說明「只做 review、不准順手改」。一個寫 code、一個分析審查。

</div>

這是人工觸發，也可以寫進前饋規則，說明「在流程中何時、遇到哪類情況就呼叫」

---

## 工具層 Harness 的設計原則

<div class="cols">
<div class="card">

### 1️⃣ 能確定性檢查最好

例如 SQL 語法驗證用 SQLGlot，又快又穩

</div>
<div class="card">

### 2️⃣ 語意判斷才用 LLM Judge

細緻品質好不好沒有確定性 assert 可寫，
使用 LLM judge 補規則型檢查的不足

</div>
</div>
<div class="cols gap-sm">
<div class="card">

### 3️⃣ 回饋最好可行動

錯誤訊息要附「該怎麼辦」，不是只丟一個程式 error code。

</div>
<div class="card">

### 4️⃣ 延遲預算內完成

工具層回饋在 tool call 內發生，要注意 latency，別拖慢整個迴圈。

</div>
</div>

---

<!-- _class: section -->
<!-- _paginate: false -->

<span class="kicker">PART 4 · 時機 ②</span>

# 兩次 model request 之間，<br>把訊息注入執行中的 agent

---

## 這個時機在哪:兩次 model request 之間

一輪 (Turn) 不是「一問一答」，而是「模型 request → tool calls → 模型 request → …」反覆，直到輸出答案。注入就發生在這個迴圈內部、**還沒輸出答案前**:

<svg viewBox="0 0 720 248" style="width:100%;max-width:1000px;height:auto;display:block;margin:6px auto 0;font-family:-apple-system,'PingFang TC','Noto Sans TC',Helvetica,Arial,sans-serif;" xmlns="http://www.w3.org/2000/svg">
<defs>
<marker id="s2arr" viewBox="0 0 10 10" refX="8" refY="5" markerWidth="7" markerHeight="7" orient="auto-start-reverse"><path d="M0,0 L10,5 L0,10 z" style="fill:var(--text-secondary)"/></marker>
<marker id="s2arrA" viewBox="0 0 10 10" refX="8" refY="5" markerWidth="7" markerHeight="7" orient="auto-start-reverse"><path d="M0,0 L10,5 L0,10 z" style="fill:var(--accent)"/></marker>
</defs>
<rect x="10" y="56" width="700" height="150" rx="12" style="fill:var(--surface);stroke:var(--accent);stroke-width:1.5"/>
<rect x="26" y="44" width="250" height="24" rx="12" style="fill:var(--surface);stroke:var(--accent);stroke-width:1.5"/>
<text x="40" y="61" style="fill:var(--accent);font-size:12px;font-weight:700">一輪 Turn (agent 還在進行中)</text>
<rect x="196" y="74" width="328" height="22" rx="11" style="fill:var(--tag-bg);stroke:var(--accent);stroke-width:1.2"/>
<text x="360" y="89" text-anchor="middle" style="fill:var(--accent);font-size:10.5px;font-weight:700">↓ 在這裡注入訊息 (人 steer 或程式)</text>
<path d="M 268 96 L 268 116" style="fill:none;stroke:var(--accent);stroke-width:1.2;stroke-dasharray:3 2" marker-end="url(#s2arrA)"/>
<path d="M 524 96 L 524 116" style="fill:none;stroke:var(--accent);stroke-width:1.2;stroke-dasharray:3 2" marker-end="url(#s2arrA)"/>
<rect x="30" y="120" width="92" height="44" rx="7" style="fill:var(--bg);stroke:var(--border);stroke-width:1.3"/>
<text x="76" y="138" text-anchor="middle" style="fill:var(--text);font-size:12px;font-weight:600">模型</text>
<text x="76" y="153" text-anchor="middle" style="fill:var(--text-secondary);font-size:10px">request 1</text>
<line x1="122" y1="142" x2="156" y2="142" style="stroke:var(--text-secondary);stroke-width:1.4" marker-end="url(#s2arr)"/>
<rect x="158" y="120" width="92" height="44" rx="7" style="fill:var(--tag-bg);stroke:var(--accent);stroke-width:1.3"/>
<text x="204" y="146" text-anchor="middle" style="fill:var(--accent);font-size:12px;font-weight:600">🔧 tool calls</text>
<line x1="250" y1="142" x2="284" y2="142" style="stroke:var(--text-secondary);stroke-width:1.4" marker-end="url(#s2arr)"/>
<rect x="286" y="120" width="92" height="44" rx="7" style="fill:var(--bg);stroke:var(--border);stroke-width:1.3"/>
<text x="332" y="138" text-anchor="middle" style="fill:var(--text);font-size:12px;font-weight:600">模型</text>
<text x="332" y="153" text-anchor="middle" style="fill:var(--text-secondary);font-size:10px">request 2</text>
<line x1="378" y1="142" x2="412" y2="142" style="stroke:var(--text-secondary);stroke-width:1.4" marker-end="url(#s2arr)"/>
<rect x="414" y="120" width="92" height="44" rx="7" style="fill:var(--tag-bg);stroke:var(--accent);stroke-width:1.3"/>
<text x="460" y="146" text-anchor="middle" style="fill:var(--accent);font-size:12px;font-weight:600">🔧 tool calls</text>
<line x1="506" y1="142" x2="540" y2="142" style="stroke:var(--text-secondary);stroke-width:1.4;stroke-dasharray:4 3" marker-end="url(#s2arr)"/>
<rect x="542" y="120" width="100" height="44" rx="7" style="fill:var(--bg);stroke:var(--border);stroke-width:1.3;stroke-dasharray:4 3"/>
<text x="592" y="138" text-anchor="middle" style="fill:var(--text-secondary);font-size:12px;font-weight:600">模型</text>
<text x="592" y="153" text-anchor="middle" style="fill:var(--text-secondary);font-size:10px">輸出答案 (還沒到)</text>
<text x="360" y="186" text-anchor="middle" style="fill:var(--text);font-size:11px">注入發生在每個「tool calls → 下一個 model request」之間 (圖中標記處)</text>
<text x="360" y="200" text-anchor="middle" style="fill:var(--text-secondary);font-size:10.5px">agent 還沒到「輸出答案」這一步，就把新訊息插進這一輪</text>
</svg>

<div class="small gap-sm">不是等 agent 執行完才注入（那是時機③單輪結束），而是在它還在迴圈中間、還沒輸出答案時就插進去。來源可以是人 (steer)，也可以是程式。</div>

---

## 同一個注入點，兩種用途

Agent 還在反覆呼叫工具、還沒輸出答案時，就把新訊息插進去，馬上影響它接下來的動作

<div class="cols">
<div class="card blue">

### 🧑 用途一: 人中途 steer

使用者就主動輸入一段話介入，叫做 **steering** 轉向/引導。

在 **Codex、Claude Code** 這類互動式 coding agent 最常見，是內建功能。

</div>
<div class="card">

### ⚙️ 用途二: 程式注入

例如背景工具程式跑完送回結果、外部事件 (webhook、告警) 要讓 agent 知道。

目前**較少框架實作**，少數像 **Pydantic AI** 做成通用機制。

</div>
</div>

---

## 只能在 requests 之間: 這是 API 後端的限制

已經發出 tool calls 但還沒拿到結果，這時若添加 user message 回傳，API 會錯誤

<div class="cols gap-sm">
<div class="card red">

### ❌ 不合法

assistant 發了 tool calls → 還沒等到所有工具結果 → 直接加 user message 回傳。下一個 request 送出就 400。

</div>
<div class="card green">

### ✅ 合法

assistant 發了 tool calls → **每個 call 的結果都補齊** → 再加 user message → 下一個 request。

</div>
</div>

<div class="small gap-sm">OpenAI、Anthropic 模型發出的<strong>每一個 tool call 都必須先補上對應結果</strong>，中間不能插別的訊息。所以必須等當前 tool 全部執行完、湊成 API 合法狀態，才能在<strong>下一個 model request 之前</strong>注入你的訊息。</div>

---

## 用途一: 人中途 steer

最常見的用途是人主動介入。steering 和 interrupt 都是 **Codex、Claude Code** 的內建功能。這跟 human-in-the-loop 不一樣:

<div class="cols">
<div class="card">

### 🛑 Human-in-the-loop

你**刻意設計一個等待點**，讓 agent 跑到那裡停下來問你 (最典型: 執行某工具前先請使用者確認)。

是 **agent 停下來問你**。

</div>
<div class="card blue">

### 🧭 Steering

agent **沒有等待點、也不打算停**，是你在它還在執行時主動輸入 (通常因為「需求變了」)。

是**你主動介入**。

</div>
</div>

---

## 當用戶中途輸入訊息時，還可以細分兩種: steering 與 interrupt

<div class="cols gap-sm">
<div class="card blue">

### 🧭 不中斷: steering

訊息先排進佇列，等當前 tool calls 結果到齊、正要發下一個 model request 前才注入。

agent 沒中斷，只是下一步多了你的訊息，**已建立的 context 全部保留**。

</div>
<div class="card red">

### 🛑 強制中斷: interrupt

取消正在執行的工具，沒答完的 tool call 硬塞 `tool_result`，內容是固定字串 `aborted` ，維持對話 API 合法。

</div>
</div>

---

## 用途二: 程式注入

用途常見有:

<div class="cols-3 gap-sm">
<div class="card">

### 🔧 背景工具結果

長時間工具在背景跑完，把結果送回 agent。

</div>
<div class="card">

### 📡 外部事件

webhook、錯誤告警、聊天平台訊息主動送進來。

</div>

</div>

<div class="small gap-sm">有提供這個注入點的框架不多: OpenAI Agents SDK、Google ADK 都沒有。少數例外是 Pydantic AI v1.101.0（2026 年 5 月）的 <code>enqueue</code>，兩種模式: <code>asap</code>（盡快插入，就是這篇的時機點）與 <code>when_idle</code>（整輪結束後才插入）。</div>

<div class="cite">參考:<a href="https://pydantic.dev/docs/ai/core-concepts/message-history/#injecting-messages-mid-run">Pydantic AI: Injecting messages mid-run</a></div>

---

## 背景工具結果怎麼送回 agent

它分兩步:

<div class="cols gap-sm">
<div class="card blue">

### 第一步: 當工具被呼叫時

tool call 後不等跑完，馬上回 `tool_result`，內容是固定的:

<div style="font-family:'SF Mono',Menlo,monospace;font-size:0.6em;background:var(--panel);border-radius:8px;padding:10px 12px;margin-top:8px;color:var(--sub);line-height:1.5;">Tool 'X' is running in background (task N). You will receive the result automatically when it completes.</div>

</div>
<div class="card green">

### 第二步: 當背景任務完成時

只能用 user message 插入:

<div style="font-family:'SF Mono',Menlo,monospace;font-size:0.6em;background:var(--panel);border-radius:8px;padding:10px 12px;margin-top:8px;color:var(--sub);line-height:1.5;">Background tool 'X' (task N) completed. Result: …</div>

注意不能用 `tool_result` 訊息了，因為 API 的 tool call 跟 tool result 是一對一配對的。

</div>
</div>

---

<!-- _class: lead -->

<!-- _class: section -->
<!-- _paginate: false -->

<span class="kicker">PART 5 · 時機 ③</span>

# 單輪結束的<br>Goal 與 Outcomes

---

## 單輪結束的時機 ③ Agent 連續呼叫工具後，最後輸出文字答案時

<svg viewBox="0 0 720 342" style="width:100%;max-width:1040px;height:auto;display:block;margin:6px auto 0;font-family:-apple-system,'PingFang TC','Noto Sans TC',Helvetica,Arial,sans-serif;" xmlns="http://www.w3.org/2000/svg">
<defs>
<marker id="he2arr" viewBox="0 0 10 10" refX="8" refY="5" markerWidth="7" markerHeight="7" orient="auto-start-reverse"><path d="M0,0 L10,5 L0,10 z" style="fill:var(--text-secondary)"/></marker>
<marker id="he2arrA" viewBox="0 0 10 10" refX="8" refY="5" markerWidth="7" markerHeight="7" orient="auto-start-reverse"><path d="M0,0 L10,5 L0,10 z" style="fill:var(--accent)"/></marker>
</defs>
<rect x="10" y="40" width="700" height="296" rx="14" style="fill:var(--bg);stroke:var(--text-secondary);stroke-width:1.5;stroke-dasharray:6 5"/>
<rect x="26" y="27" width="332" height="27" rx="13.5" style="fill:var(--bg);stroke:var(--text-secondary);stroke-width:1.5"/>
<text x="40" y="45" style="fill:var(--text);font-size:13px;font-weight:700">④ 外層 Loop</text>
<text x="118" y="45" style="fill:var(--text-secondary);font-size:11.5px">· 每個 session · 分鐘~小時 · 修正整個任務</text>
<rect x="34" y="78" width="652" height="154" rx="12" style="fill:var(--surface);stroke:var(--accent);stroke-width:1.5"/>
<rect x="50" y="65" width="170" height="26" rx="13" style="fill:var(--surface);stroke:var(--accent);stroke-width:1.5"/>
<text x="63" y="82" style="fill:var(--accent);font-size:12.5px;font-weight:700">③ 一輪 Turn</text>
<text x="138" y="82" style="fill:var(--text-secondary);font-size:11px">· 秒級</text>
<text x="52" y="111" style="fill:var(--text-secondary);font-size:11px">使用者輸入</text>
<line x1="52" y1="117" x2="52" y2="138" style="stroke:var(--text-secondary);stroke-width:1.4" marker-end="url(#he2arr)"/>
<rect x="48" y="138" width="86" height="40" rx="7" style="fill:var(--bg);stroke:var(--border);stroke-width:1.3"/>
<text x="91" y="155" text-anchor="middle" style="fill:var(--text);font-size:12px;font-weight:600">模型</text>
<text x="91" y="170" text-anchor="middle" style="fill:var(--text-secondary);font-size:10px">request 1</text>
<line x1="134" y1="158" x2="168" y2="158" style="stroke:var(--text-secondary);stroke-width:1.4" marker-end="url(#he2arr)"/>
<rect x="170" y="138" width="86" height="40" rx="7" style="fill:var(--tag-bg);stroke:var(--accent);stroke-width:1.3"/>
<text x="213" y="155" text-anchor="middle" style="fill:var(--accent);font-size:12px;font-weight:600">🔧 tool calls</text>
<text x="213" y="170" text-anchor="middle" style="fill:var(--accent);font-size:10px;font-weight:700">①</text>
<line x1="256" y1="158" x2="290" y2="158" style="stroke:var(--text-secondary);stroke-width:1.4" marker-end="url(#he2arr)"/>
<rect x="292" y="138" width="86" height="40" rx="7" style="fill:var(--bg);stroke:var(--border);stroke-width:1.3"/>
<text x="335" y="155" text-anchor="middle" style="fill:var(--text);font-size:12px;font-weight:600">模型</text>
<text x="335" y="170" text-anchor="middle" style="fill:var(--text-secondary);font-size:10px">request 2</text>
<line x1="378" y1="158" x2="412" y2="158" style="stroke:var(--text-secondary);stroke-width:1.4" marker-end="url(#he2arr)"/>
<rect x="414" y="138" width="86" height="40" rx="7" style="fill:var(--tag-bg);stroke:var(--accent);stroke-width:1.3"/>
<text x="457" y="155" text-anchor="middle" style="fill:var(--accent);font-size:12px;font-weight:600">🔧 tool calls</text>
<text x="457" y="170" text-anchor="middle" style="fill:var(--accent);font-size:10px;font-weight:700">①</text>
<line x1="500" y1="158" x2="534" y2="158" style="stroke:var(--text-secondary);stroke-width:1.4" marker-end="url(#he2arr)"/>
<rect x="536" y="138" width="92" height="40" rx="7" style="fill:var(--bg);stroke:var(--border);stroke-width:1.3"/>
<text x="582" y="155" text-anchor="middle" style="fill:var(--text);font-size:12px;font-weight:600">模型</text>
<text x="582" y="170" text-anchor="middle" style="fill:var(--text-secondary);font-size:10px">輸出答案</text>
<line x1="628" y1="158" x2="648" y2="158" style="stroke:var(--accent);stroke-width:1.5" marker-end="url(#he2arrA)"/>
<rect x="650" y="134" width="22" height="48" rx="6" style="fill:var(--tag-bg);stroke:var(--accent);stroke-width:1.6"/>
<text x="661" y="164" text-anchor="middle" style="fill:var(--accent);font-size:14px;font-weight:800">③</text>
<rect x="206" y="95" width="334" height="22" rx="11" style="fill:var(--surface);stroke:var(--accent);stroke-width:1.2"/>
<text x="373" y="110" text-anchor="middle" style="fill:var(--accent);font-size:10.5px;font-weight:700">② request 之間注入 (人 steer 或程式)</text>
<path d="M 284 117 L 284 150" style="fill:none;stroke:var(--accent);stroke-width:1.2;stroke-dasharray:3 2" marker-end="url(#he2arrA)"/>
<path d="M 518 117 L 518 150" style="fill:none;stroke:var(--accent);stroke-width:1.2;stroke-dasharray:3 2" marker-end="url(#he2arrA)"/>
<text x="320" y="197" text-anchor="middle" style="fill:var(--text-secondary);font-size:10.5px">① 工具執行內 · 修正單一動作</text>
<path d="M 650 182 L 650 212 Q 650 218 644 218 L 99 218 Q 91 218 91 212 L 91 180" style="fill:none;stroke:var(--accent);stroke-width:1.3;stroke-dasharray:4 3" marker-end="url(#he2arrA)"/>
<rect x="252" y="208" width="216" height="19" rx="9.5" style="fill:var(--surface);stroke:var(--accent);stroke-width:1"/>
<text x="360" y="221" text-anchor="middle" style="fill:var(--accent);font-size:10.5px">Stop hook 沒過 → 同份 context 再跑一輪</text>
<text x="360" y="254" text-anchor="middle" style="fill:var(--text);font-size:11.5px">一輪 (Turn) = 多次「模型 request → tool calls」反覆，直到模型輸出答案</text>
<path d="M 672 182 L 672 302 Q 672 310 664 310 L 42 310 Q 30 310 30 300 L 30 168 Q 30 158 40 158 L 46 158" style="fill:none;stroke:var(--text-secondary);stroke-width:1.6" marker-end="url(#he2arr)"/>
<rect x="150" y="300" width="424" height="20" rx="10" style="fill:var(--bg);stroke:var(--text-secondary);stroke-width:1.3"/>
<text x="362" y="314" text-anchor="middle" style="fill:var(--text);font-size:11px;font-weight:600">④ 通過後這個 session 收掉，換上全新 context 再跑一圈</text>
</svg>

---

## 設計 Goal 可驗證的停止條件，強迫模型自動再一輪

<div class="cols">
<div>

給 Agent 一個目標:

- 希望的**最終狀態**是什麼
- 用什麼**證據**驗證
- 有哪些**限制**要遵守

讓 Agent 持續修正，直到通過為止。

這是 Codex 和 Claude Code 的內建功能。

</div>
<div class="card blue">

### 核心精神

> 不能因為「模型**覺得**大概做完了」
> 就算數。

完成與否，要對著**停止條件**驗證，
沒過就繼續做。

</div>
</div>

---

## Goal 合約模板

好的 Goal 不一定是更長的 prompt，而是一份**精簡的契約**:

```text
/goal <desired end state>                 ← 期望的最終狀態
      verified by <specific evidence>     ← 用什麼證據驗證
      while preserving <constraints>.     ← 同時要保住什麼
Use <allowed inputs, tools, boundaries>.  ← 允許的工具與邊界
Between iterations, <how to choose the next best action>.
If blocked or no valid paths remain,
      <what to report and what would unlock progress>.
```

<div class="small gap-sm">範例:「將 p95 latency 降到 120ms 以下，用壓力測試做驗證，並保持測試套件都要通過」</div>

<div class="card blue gap-sm">

🤖 **讓 AI 幫你寫**:任務夠清楚時，直接 `Help me turn this into a strong /goal: <任務描述>`

</div>

<div class="cite">出處: <a href="https://developers.openai.com/cookbook/examples/codex/using_goals_in_codex">OpenAI Cookbook: Using Goals in Codex</a></div>

---

## 不適合用 Goal 的時候

<div class="cols">
<div class="card red">

### ❌ 完成條件模糊

- 「把這個變得**更好**」
- 「**重構**這段程式碼」

沒有可靠的完成條件，

</div>
<div class="card green">

### ✅ 先定義，再開工

- 預期的**最終狀態**
- 驗證用的**測試**
- 要保住的**限制**

定義不出來？那問題不在工具，
在你還不知道自己要什麼。

</div>
</div>

---

## 使用者的角色轉變: turn → round

<div class="cols">
<div>

藏在 Goal 背後的，是交付物的轉變:

- 你交付的不再是一句 **prompt**，而是一份「**目標 ＋ 邊界**」的契約
- 然後讓 Agent 持續去跑: **prompt → 判斷完成沒 → 再 prompt** 讓 agent 繼續做
- 思考單位，從「一次對話 **turn**」換成「一輪工作 **round/loop**」

</div>
<div class="card blue">

### 那這迴圈怎麼判斷「做完了沒」？

有各種不同實作，讓我幫你分析。

</div>
</div>

---

## 深入研究三種產品實作，沿著「驗證的 Judge 有多獨立」來看

<div class="cols-3 gap-sm">
<div class="card">

### Codex 的 Goal

由**主模型自我審計**，自己呼叫 `update_goal` 宣告

</div>
<div class="card">

### Claude Code 的 Gooal

每輪結束，交給獨立的 **Haiku** 小模型裁決

</div>
<div class="card blue">

### Claude Managed Agents 的 Outcome

由獨立的 grader agent 拿 rubric 評分標準，去檢查產出物做驗收

</div>
</div>

---

## 實作一: Codex /goal，沒有裁判的自我審計

Codex 沒有第二個模型在做判定，是自我審計

<div class="cols gap-sm">
<div class="card">

### Agent loop 像是確定性狀態機

- 當判斷完成時，主模型呼叫 `update_goal(complete)`更新狀態
- 如果狀態還是 Active，就重新注入同一份 <a href="https://github.com/openai/codex/blob/main/codex-rs/prompts/templates/goals/continuation.md">continuation.md</a> prompt 強迫 Agent 繼續跑下一輪

</div>
<div class="card blue">

### 判定者就是主模型自己

- 完成 = 模型呼叫 `update_goal(complete)`
- Agent 帶著完整的對話紀錄和推理脈絡繼續下一輪

</div>
</div>

---

## Codex /goal:自我審計迴圈

<svg viewBox="0 0 700 268" style="width:100%;max-width:1060px;max-height:470px;height:auto;display:block;margin:14px auto" xmlns="http://www.w3.org/2000/svg" role="img" aria-label="Codex /goal 自我審計迴圈示意圖">
<defs>
<marker id="cdxB" markerWidth="10" markerHeight="8" refX="8" refY="3" orient="auto"><path d="M0,0 L8,3 L0,6 Z" style="fill:var(--accent)"/></marker>
<marker id="cdxG" markerWidth="10" markerHeight="8" refX="8" refY="3" orient="auto"><path d="M0,0 L8,3 L0,6 Z" style="fill:#1a7f37"/></marker>
</defs>
<rect x="462" y="8" width="160" height="34" rx="8" style="fill:#dafbe1;stroke:#1a7f37;stroke-width:1.5"/>
<text x="542" y="30" text-anchor="middle" style="fill:#1a7f37;font-size:11.5px;font-weight:700">update_goal(complete) ✅</text>
<rect x="18" y="62" width="168" height="60" rx="8" style="fill:var(--surface);stroke:var(--border);stroke-width:1.5"/>
<text x="102" y="88" text-anchor="middle" style="fill:var(--text);font-size:12.5px;font-weight:700">注入 continuation.md</text>
<text x="102" y="107" text-anchor="middle" style="fill:var(--text-secondary);font-size:11px">每輪同一份合約 prompt</text>
<rect x="236" y="62" width="176" height="60" rx="8" style="fill:var(--tag-bg);stroke:var(--accent);stroke-width:1.5"/>
<text x="324" y="88" text-anchor="middle" style="fill:var(--text);font-size:12.5px;font-weight:700">主 agent 跑一輪</text>
<text x="324" y="107" text-anchor="middle" style="fill:var(--text-secondary);font-size:11px">推理 + 工具呼叫</text>
<rect x="462" y="56" width="160" height="72" rx="8" style="fill:var(--surface);stroke:var(--border);stroke-width:1.5"/>
<text x="542" y="86" text-anchor="middle" style="fill:var(--text);font-size:12.5px;font-weight:700">自我審計</text>
<text x="542" y="105" text-anchor="middle" style="fill:var(--text-secondary);font-size:11px">達成目標?</text>
<line x1="186" y1="92" x2="232" y2="92" style="stroke:var(--accent);stroke-width:1.5" marker-end="url(#cdxB)"/>
<line x1="412" y1="92" x2="458" y2="92" style="stroke:var(--accent);stroke-width:1.5" marker-end="url(#cdxB)"/>
<line x1="542" y1="56" x2="542" y2="46" style="stroke:#1a7f37;stroke-width:1.5" marker-end="url(#cdxG)"/>
<text x="552" y="54" style="fill:#1a7f37;font-size:10.5px">是</text>
<path d="M542,128 V196 H102 V126" style="fill:none;stroke:var(--accent);stroke-width:1.5" marker-end="url(#cdxB)"/>
<text x="324" y="189" text-anchor="middle" style="fill:var(--text-secondary);font-size:10.5px">否: 沒呼叫 update_goal → thread idle 且 goal.status = Active → 再注入</text>
<text x="350" y="230" text-anchor="middle" style="fill:var(--text);font-size:11.5px;font-weight:600">判定者就是主 agent 自己, 全程沒有第二個模型</text>
</svg>

---

## Codex 怎麼防「過早宣告完成」

判定權在主模型手上，Codex 用 prompt 要求以「當前 worktree 與外部狀態」去自查

<div class="cols gap-sm">
<div class="card">

### Tool description

<a href="https://github.com/openai/codex/blob/main/codex-rs/ext/goal/src/spec.rs">update_goal 的 description</a> 寫好寫滿:

> Set status to `complete` **only when the objective has actually been achieved** and no required work remains.

</div>
<div class="card blue">

### 每輪注入的 Continuation prompt

要求模型逐項找證據:

> "treat completion as **unproven** and verify it against the actual current state"
> "The audit must **prove** completion, not merely fail to find obvious remaining work"

每輪注入的 prompt 都一樣 (只有 Budget 數字不同)

</div>
</div>

---

## 別只看名字，要看實作

<div class="cols">
<div class="card red">

### 流傳的誤解

有些技術文章寫: Codex 的 Goal「用一個獨立小模型每回合評分」

</div>
<div class="card green">

### 翻原始碼跟文件才知道

沒有第二個 model、沒有額外的 grader

</div>
</div>

<div class="quote">harness 的實作細節，不能靠幻覺想像那是怎麼做的</div>

---

## 實作二: Claude Code 的 Goal，獨立 Haiku 讀刪減 transcript

Claude Code 把判定交給**另一個模型**。當主迴圈（Opus）輸出答案時，harness 不交還控制權，而是發一個 request 把整段對話交給一個獨立小模型來審計 (類似 fork):

```text
Based on the conversation transcript above,
has the following stopping condition been satisfied?

<stopping condition>

Answer based on transcript evidence only.
```

<div class="card red gap-sm">

⚠️ 注意: 這只會看對話紀錄，審計是不會呼叫工具打開檔案、實際檢查 artifact 產出物

</div>

---

## Claude Code /goal 的三個細節

<div class="cols-3 gap-sm">
<div class="card">

### 獨立的小模型

預設 **Haiku**，用另一份 system prompt

</div>
<div class="card">

### transcript 是重組副本

保留對話紀錄、工具呼叫紀錄，**移除** thinking、移除整包 claudeMd 環境、tool metadata 等

</div>
<div class="card">

### structured output

回覆 `{ok, reason, impossible}`，包括回饋理由，以及是否不可能辦到(此時應該放行，避免無窮迴圈卡死)。

</div>
</div>

<div class="cols gap-sm">
<div class="card green">

### 判「是」

目標完成，把最後答案輸出給你

</div>
<div class="card blue">

### 判「否」

擋下，把 Haiku 寫的 `reason` 注入主 agent，強迫跑下一輪

</div>
</div>

---

## Claude Code /goal:Haiku 裁判流程

<svg viewBox="0 0 700 324" style="width:100%;max-width:1060px;max-height:470px;height:auto;display:block;margin:14px auto" xmlns="http://www.w3.org/2000/svg" role="img" aria-label="Claude Code /goal fork 判定示意圖">
<defs>
<marker id="ccB" markerWidth="10" markerHeight="8" refX="8" refY="3" orient="auto"><path d="M0,0 L8,3 L0,6 Z" style="fill:var(--accent)"/></marker>
<marker id="ccG" markerWidth="10" markerHeight="8" refX="8" refY="3" orient="auto"><path d="M0,0 L8,3 L0,6 Z" style="fill:#1a7f37"/></marker>
<marker id="ccR" markerWidth="10" markerHeight="8" refX="8" refY="3" orient="auto"><path d="M0,0 L8,3 L0,6 Z" style="fill:#cf222e"/></marker>
</defs>
<rect x="24" y="20" width="194" height="56" rx="8" style="fill:var(--tag-bg);stroke:var(--accent);stroke-width:1.5"/>
<text x="121" y="44" text-anchor="middle" style="fill:var(--text);font-size:12.5px;font-weight:700">主 agent 跑一輪 (Opus)</text>
<text x="121" y="62" text-anchor="middle" style="fill:var(--text-secondary);font-size:11px">自認達成, 要結束</text>
<rect x="262" y="20" width="120" height="56" rx="8" style="fill:var(--surface);stroke:var(--border);stroke-width:1.5"/>
<text x="322" y="44" text-anchor="middle" style="fill:var(--text);font-size:12.5px;font-weight:700">Stop hook</text>
<text x="322" y="62" text-anchor="middle" style="fill:var(--text-secondary);font-size:11px">攔下結束</text>
<line x1="218" y1="48" x2="258" y2="48" style="stroke:var(--accent);stroke-width:1.5" marker-end="url(#ccB)"/>
<line x1="322" y1="76" x2="322" y2="112" style="stroke:var(--accent);stroke-width:1.5" marker-end="url(#ccB)"/>
<text x="338" y="94" style="fill:var(--text-secondary);font-size:10.5px">複製刪減版 transcript</text>
<text x="338" y="108" style="fill:var(--text-secondary);font-size:10.5px">(剝除 thinking)</text>
<rect x="232" y="116" width="180" height="64" rx="8" style="fill:#fff8c5;stroke:#9a6700;stroke-width:1.5"/>
<text x="322" y="142" text-anchor="middle" style="fill:#9a6700;font-size:12.5px;font-weight:700">獨立 Haiku 裁判</text>
<text x="322" y="161" text-anchor="middle" style="fill:var(--text-secondary);font-size:10.5px">另一個模型, 只讀 transcript</text>
<path d="M412,148 H575 V244" style="fill:none;stroke:#1a7f37;stroke-width:1.5" marker-end="url(#ccG)"/>
<text x="486" y="140" text-anchor="middle" style="fill:#1a7f37;font-size:10.5px">ok: true</text>
<path d="M232,148 H170 V244" style="fill:none;stroke:#cf222e;stroke-width:1.5" marker-end="url(#ccR)"/>
<text x="198" y="140" text-anchor="middle" style="fill:#cf222e;font-size:10.5px">ok: false</text>
<rect x="470" y="246" width="210" height="54" rx="8" style="fill:#dafbe1;stroke:#1a7f37;stroke-width:1.5"/>
<text x="575" y="270" text-anchor="middle" style="fill:var(--text);font-size:12px;font-weight:700">目標完成, 交還控制 ✅</text>
<text x="575" y="288" text-anchor="middle" style="fill:var(--text-secondary);font-size:10.5px">goal 達成</text>
<rect x="20" y="246" width="300" height="54" rx="8" style="fill:#ffebe9;stroke:#cf222e;stroke-width:1.5"/>
<text x="170" y="270" text-anchor="middle" style="fill:var(--text);font-size:12px;font-weight:700">reason 注入回主 thread</text>
<text x="170" y="288" text-anchor="middle" style="fill:var(--text-secondary);font-size:10.5px">針對性診斷 → 主 agent 繼續下一輪</text>
<path d="M20,273 H10 V48 H24" style="fill:none;stroke:var(--accent);stroke-width:1.5" marker-end="url(#ccB)"/>
</svg>

---

## 判「沒完成」之後，兩家差在哪

| | Codex /goal | Claude Code /goal |
|---|---|---|
| **回饋形式** | 重播同一份 continuation.md，只有 budget 數字在動 | Haiku 寫的針對性診斷，指出 transcript 缺了什麼 |
| **下一步依據** | 環境證據(測試失敗、compile error等)＋自己保留的 reasoning | 外部裁判指出缺口 |
| **成本代價** | 每輪多累積一份 prompt，但會有 prompt cache | 每輪多一次 Haiku call，主 thread 只增加一小段 reason |
| **失效模式** | 模型有盲點時無外部視角打破，可能連錯好幾輪 | Haiku 誤判:會被自信的收尾語言騙過 |

---

## 實作三: Claude Managed Agents 的 Outcome

<div class="cols">
<div>

第三種最為獨立，獨立 Agent 拿著 rubric 操作 artifact 做檢查:

- Grader 在**全新 context window**:只拿 rubric 與產出物，**看不到主 agent 的推理與敘事**
- 不只「看」:而是有工具操作，可以像真實使用者**實際操作** artifact 產出物，開檔、點 UI、打 API、查 DB 等
- Rubric **逐條可評分**;沒過就帶著**逐條缺失**進下一輪
- `max_iterations` 預設 3、最多 20

</div>
<div class="card">

### Rubric 評分條件 範例

```markdown
# Outcome: 研究報告完成
- [ ] 涵蓋 7 項必查數據，各附來源
- [ ] 每個引用 [n] 連到有效 URL，
      且原文逐字支持該主張
- [ ] 財務數字出自 10-K / 10-Q 正式文件
```

</div>
</div>

<div class="cite">參考:<a href="https://platform.claude.com/docs/en/managed-agents/define-outcomes">Claude: Define outcomes</a>、Anthropic <a href="https://www.anthropic.com/engineering/harness-design-long-running-apps">Harness design for long-running apps</a></div>

---

## Outcome:獨立 grader 操作 artifact

<svg viewBox="0 0 700 282" style="width:100%;max-width:1060px;max-height:470px;height:auto;display:block;margin:14px auto" xmlns="http://www.w3.org/2000/svg" role="img" aria-label="Managed Agents Outcome 獨立 grader 示意圖">
<defs>
<marker id="ocB" markerWidth="10" markerHeight="8" refX="8" refY="3" orient="auto"><path d="M0,0 L8,3 L0,6 Z" style="fill:var(--accent)"/></marker>
<marker id="ocG" markerWidth="10" markerHeight="8" refX="8" refY="3" orient="auto"><path d="M0,0 L8,3 L0,6 Z" style="fill:#1a7f37"/></marker>
<marker id="ocR" markerWidth="10" markerHeight="8" refX="8" refY="3" orient="auto"><path d="M0,0 L8,3 L0,6 Z" style="fill:#cf222e"/></marker>
</defs>
<rect x="14" y="40" width="140" height="58" rx="8" style="fill:var(--tag-bg);stroke:var(--accent);stroke-width:1.5"/>
<text x="84" y="65" text-anchor="middle" style="fill:var(--text);font-size:12.5px;font-weight:700">主 agent</text>
<text x="84" y="83" text-anchor="middle" style="fill:var(--text-secondary);font-size:11px">(generator)</text>
<rect x="224" y="36" width="140" height="66" rx="8" style="fill:var(--bg);stroke:var(--text-secondary);stroke-width:1.5"/>
<text x="294" y="62" text-anchor="middle" style="fill:var(--text);font-size:12.5px;font-weight:700">artifact</text>
<text x="294" y="80" text-anchor="middle" style="fill:var(--text-secondary);font-size:11px">(檔案 / app)</text>
<rect x="486" y="36" width="200" height="66" rx="8" style="fill:var(--surface);stroke:var(--accent);stroke-width:1.5;stroke-dasharray:5 3"/>
<text x="586" y="60" text-anchor="middle" style="fill:var(--text);font-size:12.5px;font-weight:700">獨立 grader agent</text>
<text x="586" y="78" text-anchor="middle" style="fill:var(--text-secondary);font-size:10.5px">全新 context + rubric</text>
<line x1="154" y1="69" x2="222" y2="69" style="stroke:var(--accent);stroke-width:1.5" marker-end="url(#ocB)"/>
<text x="188" y="60" text-anchor="middle" style="fill:var(--text-secondary);font-size:10.5px">產出</text>
<line x1="486" y1="69" x2="366" y2="69" style="stroke:var(--accent);stroke-width:1.5" marker-end="url(#ocB)"/>
<text x="426" y="60" text-anchor="middle" style="fill:var(--text-secondary);font-size:10.5px">拿 rubric 操作</text>
<text x="426" y="88" text-anchor="middle" style="fill:var(--text-secondary);font-size:10.5px">點 UI / 打 API / 查 DB</text>
<line x1="586" y1="102" x2="586" y2="198" style="stroke:#1a7f37;stroke-width:1.5" marker-end="url(#ocG)"/>
<text x="604" y="150" style="fill:#1a7f37;font-size:10.5px">satisfied</text>
<path d="M520,102 V150 H180 V198" style="fill:none;stroke:#cf222e;stroke-width:1.5" marker-end="url(#ocR)"/>
<text x="350" y="143" text-anchor="middle" style="fill:#cf222e;font-size:10.5px">needs_revision</text>
<rect x="486" y="200" width="200" height="48" rx="8" style="fill:#dafbe1;stroke:#1a7f37;stroke-width:1.5"/>
<text x="586" y="229" text-anchor="middle" style="fill:var(--text);font-size:12px;font-weight:700">交付 ✅</text>
<rect x="24" y="200" width="312" height="48" rx="8" style="fill:#ffebe9;stroke:#cf222e;stroke-width:1.5"/>
<text x="180" y="222" text-anchor="middle" style="fill:var(--text);font-size:11.5px;font-weight:700">逐條缺失回饋</text>
<text x="180" y="239" text-anchor="middle" style="fill:var(--text-secondary);font-size:10.5px">主 agent 再改一輪</text>
<path d="M24,224 H10 V69 H14" style="fill:none;stroke:var(--accent);stroke-width:1.5" marker-end="url(#ocB)"/>
<text x="350" y="272" text-anchor="middle" style="fill:var(--text);font-size:11.5px;font-weight:600">裁判完全獨立: 不看 transcript, 直接對成品逐條驗收</text>
</svg>

---

## 相比自評，獨立驗收是最準確的

<div class="cols">
<div class="card red">

### Agent 會自我吹捧

要 agent 評自己做的東西，它傾向**自信地稱讚**，哪怕在人眼中品質明顯普通。

而且 context 裡的錯誤推理會**不斷累積**，前面說服了自己「方向對」，後面就一路錯下去。

</div>
<div class="card blue">

### 問題在於「誰來批判」

同一個 agent 較難對自己的產出下得了手，換一個全新 context 獨立評審，比較容易做出準確的 Judge。

</div>
</div>

<div class="quote">「調出一個挑剔的獨立 evaluator，比教會 agent 自我批判容易得多。」</div>

<div class="cite">出處: Anthropic <a href="https://www.anthropic.com/engineering/harness-design-long-running-apps">Harness design for long-running apps</a></div>

---

## 學界研究表示: 越獨立、越會動手，判定越可信

<div class="cols gap-sm">
<div class="card red">

### 自我評審

- **純自我修正**: 缺乏外部回饋時容易失敗
- **只讀文字的 judge**: 偵測假性完成(false success)能力有限，容易被「自信的收尾語言」帶著走

</div>
<div class="card green">

### 獨立評審

- **環境／執行回饋**: 看測試與執行結果，不看語言宣稱
- **rubric 分解**: 把驗收拆成逐條標準
- **Agent-as-a-Judge**: 能讀檔、跑指令的裁判，可靠度接近人類

</div>
</div>

<div class="small gap-sm">越往獨立、越會實際操作的那端，判定越可信。</div>

---

## 三種實作的總比較

| | Codex 的 Goal | Claude Code 的 Goal | Claude Managed Agents Outcomes |
|---|---|---|---|
| **誰來判定** | **主模型自我審計** | 獨立的 Haiku | 全新 context 的 grader agent |
| **harness 角色** | 不判斷，閒置時重播合約 prompt | 每輪結束送 transcript 裁決 | 自動配置 grader 評估迴圈 |
| **看什麼證據** | 自己 context 裡的一切(含 reasoning) | **刪減版 transcript** | **只看 artifact，實際操作驗收** |
| **怎麼宣告完成** | 主模型呼叫 `update_goal` | yes／no ＋診斷 reason | rubric 逐條 pass／fail |
| **沒完成時的回饋** | 沒有診斷，只重播同一份模板 | 一段針對性診斷，指出缺什麼 | 逐條列出缺失，最具體 |

<div class="quote">獨立性:  Codex Goal < Claude Code goal < Managed Agents Outcomes</div>

---

## 但是對工程師來說，一切都有 tradeoff: 成本和獨立性的代價

獨立性換來可靠度，但要付出代價。差別不只是「單次評估多少錢」，也要看「錯誤多久才被發現」

| | 獨立性／可靠度 | 單次評估成本 | 錯誤多久被發現 |
|---|---|---|---|
| **Codex 自我審計** | 低:主模型自評 | 趨近零:只查狀態 | 靠模型自己就先發現 |
| **Claude Code Haiku** | 中:獨立小模型讀 transcript | 小:約 1-2 秒 | 每 turn 一次 |
| **Outcome grader** | 高:獨立 agent 操作 artifact | 高:數十倍、約 8 分鐘 | 整個 iteration 做完才抓到 |

<div class="quote">越獨立越可靠，但需要用到更多 tokens 來分析，錯誤也是在整個流程中越晚被發現，導致總成本較貴也較慢</div>

---

## OpenAI Codex goal 為什麼不用獨立裁判?

<div class="cols gap-sm">
<div class="card">

### 有兩層可以裁判

- **harness 層**: 用獨立裁判，就像 Claude 作法
- **模型層**: 要靠模型本身的驗證、自我審計能力行不行

</div>
<div class="card blue">

### 我個人推測

- 我推測 OpenAI 有特別加強 update_goal 的 post-training 模型訓練，強化模型自我審計的能力
- **比較節省執行 tokens 的總成本**

</div>
</div>

<div class="small gap-sm">兩家方向不同: OpenAI 偏向加強模型訓練 goal、把自評 prompt 寫好。Claude 則用 harness 層的獨立裁判來做。</div>

---

## 如果是自行開發 agent，該怎麼選

<div class="cols-3 gap-sm">
<div class="card">

### 自我審計(Codex 式)

<strong>調教難度較高。</strong>高度依賴模型的自律，一般模型容易過早宣告完成。

適合: 重視 Latency 和成本的中短任務。

</div>
<div class="card">

### Transcript 裁判(Claude Code 式)

<strong>折衷做法。</strong>小模型判 transcript，好實作、好評估(輸入輸出都是文字)。

適合:中程任務，在 transcript 中就能看到可信的證明。

</div>
<div class="card blue">

### 獨立 verify(Outcome 式)

<strong>效果最好，但成本最高、latency 是最大弱點。</strong>每次驗收要把 artifact 跑起來操作。

適合:長時間、以交付物為終點，價值高到值得花評估開銷。

</div>
</div>

---

## 綜合案例: 使用者訪談 Agent，結合兩家的做法

<div class="cols">
<div>

需求: 按訪綱逐題訪問用戶

挑戰: 但什麼時候該換下一題？這題問夠了沒？

模型會偏向「覺得差不多了就想往下走」，跟第二篇的**過早宣告完成**是同一個問題，只是這裏是「這**一題**問完了沒」。

</div>
<div class="card red">

### 我的做法

- 借 **Claude Code** 的 transcript judge 把關「這題問夠了沒」
- 借 **Codex** 每輪重新注入 prompt 的做法，讓訪談持續往前

</div>
</div>

---

## 借 Claude Code 的做法: 提供換題工具，裡面做 transcript judge

agent 想跳下一題時，呼叫 `switch_next_question_workflow` 工具，裡面是一個獨立 Judge 審核:

```python
@function_tool
async def switch_next_question_workflow(reason: str, user_requested_next: bool) -> str:
    """當你判斷目前這題已取得足夠答案、或使用者要求跳題時呼叫。"""
    # 真正的判定在 server 端，工具只是把請求轉過去
    ...
```

<div class="small gap-sm">prompt 寫說:「回傳 Y／已切換才代表進到下一題」、「回傳 N 你 <strong>MUST</strong> 繼續聚焦同一題，換問法追問」</div>

---

## Judge 看什麼: 每題有不同的 rubric，根據逐字稿判斷

不同題目有不同的完成標準(rubric)，用小模型根據逐字稿來判斷:

<div class="cols">
<div>

```python
QUESTION_WORKFLOW = [
  { "title": "最近一次使用情境",
    "completion_criteria":
      "需含最近一次使用的具體情境，"
      "至少提到使用的功能與當時任務。" },
  { "title": "替代方案",
    "completion_criteria":
      "需提到至少一個替代方案，"
      "最好指出最常用者與原因。" },
  # …其餘題目
]
```

</div>
<div>

```text
You are a user interview quality reviewer.
Use only the transcript below. Do not infer
facts that are not in the transcript.

Current question: {question}
Completion criteria: {completion_criteria}
Transcript: {transcript}

Return exactly one character:
Y if complete. N if not.
```

</div>
</div>

---

## 沒過時的回傳值: 還是要可行動

Judge 回 N 時，工具不是只回一個 false，而是回一段**可行動的指令**，順便附上這是第幾次被退:

```text
N: 仍停留在第 1 題「最近一次使用情境」。這是第一次追問。
請換一種問法追問目前這題，不要切換題目。
```

---

## 借 Codex 的做法: time_control 每輪注入動態狀態

每輪推動 agent 往對的方向走: 「現在過幾分鐘了、第幾題了」的狀態也傳給 Agent

```text
<time_control>已過 7 分鐘 / 共 15 分鐘</time_control>
<current_question>第 2 / 5 題: 題目....</current_question>
```

<div class="small gap-sm">每輪動態注入<strong>當下狀態</strong>，提醒目前在哪一題，以及用這個訊號調節奏:時間充裕就從容追問，時間不夠了就加速減少追問。</div>

---

## 訪談 Agent:time_control 推進度，Judge 把關

<svg viewBox="0 0 700 400" style="width:100%;max-width:1060px;max-height:480px;height:auto;display:block;margin:10px auto" xmlns="http://www.w3.org/2000/svg" role="img" aria-label="使用者訪談 agent 組合 time_control 與 Judge 示意圖">
<defs>
<marker id="uiB" markerWidth="10" markerHeight="8" refX="8" refY="3" orient="auto"><path d="M0,0 L8,3 L0,6 Z" style="fill:var(--accent)"/></marker>
<marker id="uiG" markerWidth="10" markerHeight="8" refX="8" refY="3" orient="auto"><path d="M0,0 L8,3 L0,6 Z" style="fill:#1a7f37"/></marker>
<marker id="uiR" markerWidth="10" markerHeight="8" refX="8" refY="3" orient="auto"><path d="M0,0 L8,3 L0,6 Z" style="fill:#cf222e"/></marker>
</defs>
<rect x="160" y="14" width="380" height="54" rx="8" style="fill:var(--surface);stroke:var(--border);stroke-width:1.5"/>
<text x="350" y="38" text-anchor="middle" style="fill:var(--text);font-size:12.5px;font-weight:700">time_control: 每輪注入動態狀態 (時間 / 題號)</text>
<text x="350" y="57" text-anchor="middle" style="fill:var(--text-secondary);font-size:11px">Codex 式 · 前饋: 給模型它自己算不出的當下狀態</text>
<rect x="235" y="96" width="230" height="58" rx="8" style="fill:var(--tag-bg);stroke:var(--accent);stroke-width:1.5"/>
<text x="350" y="120" text-anchor="middle" style="fill:var(--text);font-size:12.5px;font-weight:700">訪談 agent 跑一輪</text>
<text x="350" y="139" text-anchor="middle" style="fill:var(--text-secondary);font-size:11px">逐題問答 · 判斷這題問夠了沒</text>
<rect x="205" y="192" width="290" height="62" rx="8" style="fill:#fff8c5;stroke:#9a6700;stroke-width:1.5"/>
<text x="350" y="216" text-anchor="middle" style="fill:#9a6700;font-size:12.5px;font-weight:700">獨立 Judge · 只讀 transcript + 該題 rubric</text>
<text x="350" y="235" text-anchor="middle" style="fill:var(--text-secondary);font-size:11px">Claude Code 式 · 回饋: 把關「這題能不能換」</text>
<rect x="395" y="298" width="215" height="48" rx="8" style="fill:#dafbe1;stroke:#1a7f37;stroke-width:1.5"/>
<text x="502" y="320" text-anchor="middle" style="fill:var(--text);font-size:12px;font-weight:700">進到下一題 ✅</text>
<text x="502" y="337" text-anchor="middle" style="fill:var(--text-secondary);font-size:10.5px">harness 推進到下一題</text>
<rect x="70" y="298" width="250" height="48" rx="8" style="fill:#ffebe9;stroke:#cf222e;stroke-width:1.5"/>
<text x="195" y="320" text-anchor="middle" style="fill:var(--text);font-size:12px;font-weight:700">留在本題, 換問法追問</text>
<text x="195" y="337" text-anchor="middle" style="fill:var(--text-secondary);font-size:10.5px">回傳可行動指令 + 第幾次被退</text>
<line x1="350" y1="68" x2="350" y2="94" style="stroke:var(--accent);stroke-width:1.5" marker-end="url(#uiB)"/>
<text x="358" y="86" style="fill:var(--text-secondary);font-size:10.5px">影響何時換題</text>
<line x1="350" y1="154" x2="350" y2="190" style="stroke:var(--accent);stroke-width:1.5" marker-end="url(#uiB)"/>
<text x="360" y="177" style="fill:var(--text-secondary);font-size:10.5px">想換題: 呼叫 switch 工具</text>
<path d="M495,210 H575 V296" style="fill:none;stroke:#1a7f37;stroke-width:1.5" marker-end="url(#uiG)"/>
<text x="537" y="203" text-anchor="middle" style="fill:#1a7f37;font-size:10.5px">Y: 切換</text>
<path d="M205,210 H150 V296" style="fill:none;stroke:#cf222e;stroke-width:1.5" marker-end="url(#uiR)"/>
<text x="150" y="203" text-anchor="middle" style="fill:#cf222e;font-size:10.5px">N: 留本題</text>
<path d="M70,325 H32 V125 H233" style="fill:none;stroke:var(--accent);stroke-width:1.5" marker-end="url(#uiB)"/>
<path d="M610,325 H665 V41 H542" style="fill:none;stroke:var(--accent);stroke-width:1.5" marker-end="url(#uiB)"/>
<text x="640" y="200" text-anchor="middle" style="fill:var(--text-secondary);font-size:10.5px">下一輪</text>
<path d="M195,346 V362 H503 V348" style="fill:none;stroke:#1a7f37;stroke-width:1.3;stroke-dasharray:5 3" marker-end="url(#uiG)"/>
<text x="349" y="359" text-anchor="middle" style="fill:var(--text-secondary);font-size:10.5px">退 3 次 / 使用者喊跳 → 強制放行</text>
<text x="350" y="382" text-anchor="middle" style="fill:var(--text);font-size:11.5px;font-weight:600">time_control 推進度, Judge 把關: 一前一後讓限時訪談問得深又跑得完</text>
</svg>

---

<!-- _class: section -->
<!-- _paginate: false -->

<span class="kicker">PART 6 · 時機 ④</span>

# 外層 Outer Loop

---

## Agent 輸出一輪完整答案之後 ④ 外層 Harness

<svg viewBox="0 0 720 342" style="width:100%;max-width:1040px;height:auto;display:block;margin:6px auto 0;font-family:-apple-system,'PingFang TC','Noto Sans TC',Helvetica,Arial,sans-serif;" xmlns="http://www.w3.org/2000/svg">
<defs>
<marker id="he2arr" viewBox="0 0 10 10" refX="8" refY="5" markerWidth="7" markerHeight="7" orient="auto-start-reverse"><path d="M0,0 L10,5 L0,10 z" style="fill:var(--text-secondary)"/></marker>
<marker id="he2arrA" viewBox="0 0 10 10" refX="8" refY="5" markerWidth="7" markerHeight="7" orient="auto-start-reverse"><path d="M0,0 L10,5 L0,10 z" style="fill:var(--accent)"/></marker>
</defs>
<rect x="10" y="40" width="700" height="296" rx="14" style="fill:var(--bg);stroke:var(--text-secondary);stroke-width:1.5;stroke-dasharray:6 5"/>
<rect x="26" y="27" width="332" height="27" rx="13.5" style="fill:var(--bg);stroke:var(--text-secondary);stroke-width:1.5"/>
<text x="40" y="45" style="fill:var(--text);font-size:13px;font-weight:700">④ 外層 Loop</text>
<text x="118" y="45" style="fill:var(--text-secondary);font-size:11.5px">· 每個 session · 分鐘~小時 · 修正整個任務</text>
<rect x="34" y="78" width="652" height="154" rx="12" style="fill:var(--surface);stroke:var(--accent);stroke-width:1.5"/>
<rect x="50" y="65" width="170" height="26" rx="13" style="fill:var(--surface);stroke:var(--accent);stroke-width:1.5"/>
<text x="63" y="82" style="fill:var(--accent);font-size:12.5px;font-weight:700">③ 一輪 Turn</text>
<text x="138" y="82" style="fill:var(--text-secondary);font-size:11px">· 秒級</text>
<text x="52" y="111" style="fill:var(--text-secondary);font-size:11px">使用者輸入</text>
<line x1="52" y1="117" x2="52" y2="138" style="stroke:var(--text-secondary);stroke-width:1.4" marker-end="url(#he2arr)"/>
<rect x="48" y="138" width="86" height="40" rx="7" style="fill:var(--bg);stroke:var(--border);stroke-width:1.3"/>
<text x="91" y="155" text-anchor="middle" style="fill:var(--text);font-size:12px;font-weight:600">模型</text>
<text x="91" y="170" text-anchor="middle" style="fill:var(--text-secondary);font-size:10px">request 1</text>
<line x1="134" y1="158" x2="168" y2="158" style="stroke:var(--text-secondary);stroke-width:1.4" marker-end="url(#he2arr)"/>
<rect x="170" y="138" width="86" height="40" rx="7" style="fill:var(--tag-bg);stroke:var(--accent);stroke-width:1.3"/>
<text x="213" y="155" text-anchor="middle" style="fill:var(--accent);font-size:12px;font-weight:600">🔧 tool calls</text>
<text x="213" y="170" text-anchor="middle" style="fill:var(--accent);font-size:10px;font-weight:700">①</text>
<line x1="256" y1="158" x2="290" y2="158" style="stroke:var(--text-secondary);stroke-width:1.4" marker-end="url(#he2arr)"/>
<rect x="292" y="138" width="86" height="40" rx="7" style="fill:var(--bg);stroke:var(--border);stroke-width:1.3"/>
<text x="335" y="155" text-anchor="middle" style="fill:var(--text);font-size:12px;font-weight:600">模型</text>
<text x="335" y="170" text-anchor="middle" style="fill:var(--text-secondary);font-size:10px">request 2</text>
<line x1="378" y1="158" x2="412" y2="158" style="stroke:var(--text-secondary);stroke-width:1.4" marker-end="url(#he2arr)"/>
<rect x="414" y="138" width="86" height="40" rx="7" style="fill:var(--tag-bg);stroke:var(--accent);stroke-width:1.3"/>
<text x="457" y="155" text-anchor="middle" style="fill:var(--accent);font-size:12px;font-weight:600">🔧 tool calls</text>
<text x="457" y="170" text-anchor="middle" style="fill:var(--accent);font-size:10px;font-weight:700">①</text>
<line x1="500" y1="158" x2="534" y2="158" style="stroke:var(--text-secondary);stroke-width:1.4" marker-end="url(#he2arr)"/>
<rect x="536" y="138" width="92" height="40" rx="7" style="fill:var(--bg);stroke:var(--border);stroke-width:1.3"/>
<text x="582" y="155" text-anchor="middle" style="fill:var(--text);font-size:12px;font-weight:600">模型</text>
<text x="582" y="170" text-anchor="middle" style="fill:var(--text-secondary);font-size:10px">輸出答案</text>
<line x1="628" y1="158" x2="648" y2="158" style="stroke:var(--accent);stroke-width:1.5" marker-end="url(#he2arrA)"/>
<rect x="650" y="134" width="22" height="48" rx="6" style="fill:var(--tag-bg);stroke:var(--accent);stroke-width:1.6"/>
<text x="661" y="164" text-anchor="middle" style="fill:var(--accent);font-size:14px;font-weight:800">③</text>
<rect x="206" y="95" width="334" height="22" rx="11" style="fill:var(--surface);stroke:var(--accent);stroke-width:1.2"/>
<text x="373" y="110" text-anchor="middle" style="fill:var(--accent);font-size:10.5px;font-weight:700">② request 之間注入 (人 steer 或程式)</text>
<path d="M 284 117 L 284 150" style="fill:none;stroke:var(--accent);stroke-width:1.2;stroke-dasharray:3 2" marker-end="url(#he2arrA)"/>
<path d="M 518 117 L 518 150" style="fill:none;stroke:var(--accent);stroke-width:1.2;stroke-dasharray:3 2" marker-end="url(#he2arrA)"/>
<text x="320" y="197" text-anchor="middle" style="fill:var(--text-secondary);font-size:10.5px">① 工具執行內 · 修正單一動作</text>
<path d="M 650 182 L 650 212 Q 650 218 644 218 L 99 218 Q 91 218 91 212 L 91 180" style="fill:none;stroke:var(--accent);stroke-width:1.3;stroke-dasharray:4 3" marker-end="url(#he2arrA)"/>
<rect x="252" y="208" width="216" height="19" rx="9.5" style="fill:var(--surface);stroke:var(--accent);stroke-width:1"/>
<text x="360" y="221" text-anchor="middle" style="fill:var(--accent);font-size:10.5px">Stop hook 沒過 → 同份 context 再跑一輪</text>
<text x="360" y="254" text-anchor="middle" style="fill:var(--text);font-size:11.5px">一輪 (Turn) = 多次「模型 request → tool calls」反覆，直到模型輸出答案</text>
<path d="M 672 182 L 672 302 Q 672 310 664 310 L 42 310 Q 30 310 30 300 L 30 168 Q 30 158 40 158 L 46 158" style="fill:none;stroke:var(--text-secondary);stroke-width:1.6" marker-end="url(#he2arr)"/>
<rect x="150" y="300" width="424" height="20" rx="10" style="fill:var(--bg);stroke:var(--text-secondary);stroke-width:1.3"/>
<text x="362" y="314" text-anchor="middle" style="fill:var(--text);font-size:11px;font-weight:600">④ 通過後這個 session 收掉，換上全新 context 再跑一圈</text>
</svg>

---

## 為什麼需要外層迴圈?

<div class="cols gap-sm">
<div class="card">

### 三種情況

- **① 單一 context 能力有限**: 大任務得拆段，每段用乾淨 context 重新開始、表現不受前一段影響（塞滿、失敗推理污染、Goal 跨不過 session）
- **② 是另一個不相關的新任務**: 本來就該各自開乾淨 context，並管理多條平行的 agent
- **③ 要由外部事件自動觸發**: webhook、新郵件、排程、CI 失敗一來就啟動

</div>
<div class="card green">

### 共同的解法

需要一個在單輪 agent 之外的工程迴圈，也就是 **外層 harness**

它決定何時觸發、每件事開獨立 agent、多條 agent 怎麼協調。

進度不靠 context 記憶，會寫到檔案系統共享。

</div>
</div>

---

## 思路: 設計提示 Agent 的迴圈

<div class="cols">
<div>

這一層最近在社群很熱門:

- 龍蝦爸 Peter Steinberger:「你不該再去提示 agent，你該**設計提示 agent 的迴圈**」講了好幾個月
- Claude 的 Boris Cherny、Andrej Karpathy 大神也講過類似的話
- 最近出現 **loop engineering** 新詞

</div>
<div class="card blue">

### 具體來說

其實就是強調 Outer loop (Outer harness) 這一層，讓我們看具體實作案例，拆解給你看

</div>
</div>

<div class="cite">參考: <a href="https://x.com/steipete/status/2063697162748260627">Peter Steinberger</a>: You should be designing loops that prompt your agents.</div>

---

## 外層 Loop 的三種實作案例

<div class="cols-3 gap-sm">
<div class="card">

### 🔁 Ralph

**bash 蠻力重跑**

每圈全新 context，同一份 prompt 反覆送進去直到做完

</div>
<div class="card">

### 🎼 OpenAI Symphony

**看板協調器**

專案管理工具當控制平面，每張開啟的 ticket 配一個 agent

</div>
<div class="card">

### ⏰ 自動排程

**定時觸發**

時間到就跑一輪；依 context 是否沿用，再分「獨立」與「heartbeat」兩種

</div>
</div>

---

## Ralph:最笨也最有名的 Loop

```bash
while :; do
  cat PROMPT.md | claude-code
done
```

- 一個 bash 無窮迴圈，每圈把同一份 prompt 再送進去一次
- **每一圈都是全新的 context**:每圈歸零，只從固定幾份檔案重新讀起
- **完成才跳出**:當 AI 認為所有任務都完成，輸出 `COMPLETE` 代表完成，就脫離無窮迴圈

<div class="cite">出處: <a href="https://ghuntley.com/ralph/">ghuntley.com/ralph</a>（2025 就有了）</div>

---

## 跨圈記憶: 進度全靠外部狀態

Ralph 拆成三個檔案:

<div class="cols-3">
<div class="card">

### 📜 git history

完成的工作就是 commit，

新 agent 開圈先看歷史

</div>
<div class="card">

### 📝 progress.txt

每圈追加學到的事:

陷阱、模式、決策

</div>
<div class="card">

### ☑️ prd.json

任務清單與 `passes` 狀態:

每圈挑最高優先且未完成的

</div>
</div>

<div class="card gap-sm">

**ralph 的每一圈**:

讀 prd.json／progress.txt → 挑最高優先尚未完成的 story → 只實作這一個 → 跑 typecheck 和測試 → 過了 commit 標記完成 → learning 追加進 progress.txt → 下一圈。

</div>

---

## Ralph:一圈的樣子

<svg viewBox="0 0 700 300" style="width:100%;max-width:1060px;max-height:470px;height:auto;display:block;margin:14px auto" xmlns="http://www.w3.org/2000/svg" role="img" aria-label="Ralph 運作原理示意圖">
<defs>
<marker id="rlpA" markerWidth="10" markerHeight="8" refX="8" refY="3" orient="auto"><path d="M0,0 L8,3 L0,6 Z" style="fill:var(--accent)"/></marker>
<marker id="rlpS" markerWidth="10" markerHeight="8" refX="8" refY="3" orient="auto"><path d="M0,0 L8,3 L0,6 Z" style="fill:var(--text-secondary)"/></marker>
</defs>
<path d="M524,108 V46 H86 V104" style="fill:none;stroke:var(--accent);stroke-width:1.5;stroke-dasharray:5 3" marker-end="url(#rlpA)"/>
<text x="305" y="38" text-anchor="middle" style="fill:var(--accent);font-size:11.5px;font-weight:600">每圈結束 → context 整個丟掉, 開全新一圈</text>
<rect x="22" y="108" width="130" height="64" rx="8" style="fill:var(--surface);stroke:var(--border);stroke-width:1.5"/>
<text x="87" y="135" text-anchor="middle" style="fill:var(--text);font-size:12px;font-weight:700">prompt.md</text>
<text x="87" y="154" text-anchor="middle" style="fill:var(--text-secondary);font-size:10.5px">每圈用同一份</text>
<rect x="212" y="102" width="158" height="76" rx="8" style="fill:var(--tag-bg);stroke:var(--accent);stroke-width:1.5"/>
<text x="291" y="133" text-anchor="middle" style="fill:var(--text);font-size:12.5px;font-weight:700">全新 context 的 agent</text>
<text x="291" y="152" text-anchor="middle" style="fill:var(--text-secondary);font-size:10.5px">乾淨的 context, 跑一圈</text>
<rect x="430" y="108" width="186" height="64" rx="8" style="fill:var(--surface);stroke:var(--border);stroke-width:1.5"/>
<text x="523" y="134" text-anchor="middle" style="fill:var(--text);font-size:12px;font-weight:700">挑一個 story 做</text>
<text x="523" y="153" text-anchor="middle" style="fill:var(--text-secondary);font-size:10px">過 typecheck/測試才 commit</text>
<line x1="152" y1="140" x2="210" y2="140" style="stroke:var(--accent);stroke-width:1.5" marker-end="url(#rlpA)"/>
<line x1="370" y1="140" x2="428" y2="140" style="stroke:var(--accent);stroke-width:1.5" marker-end="url(#rlpA)"/>
<rect x="206" y="246" width="300" height="46" rx="8" style="fill:#fff8c5;stroke:#9a6700;stroke-width:1.5"/>
<text x="356" y="266" text-anchor="middle" style="fill:#9a6700;font-size:11.5px;font-weight:700">檔案狀態 (跨圈不丟)</text>
<text x="356" y="283" text-anchor="middle" style="fill:var(--text-secondary);font-size:10px">git history · progress.txt · prd.json</text>
<path d="M268,246 V182" style="fill:none;stroke:var(--text-secondary);stroke-width:1.5" marker-end="url(#rlpS)"/>
<text x="260" y="214" text-anchor="end" style="fill:var(--text-secondary);font-size:10px">① 開圈先讀</text>
<path d="M452,172 V246" style="fill:none;stroke:var(--text-secondary);stroke-width:1.5" marker-end="url(#rlpS)"/>
<text x="460" y="208" style="fill:var(--text-secondary);font-size:10px">② commit、</text>
<text x="460" y="222" style="fill:var(--text-secondary);font-size:10px">記下學到的</text>
</svg>

---

## Claude Code 的 ralph-wiggum Plugin: 別只看名字，要看內部實作

名字叫 Ralph，但讀完 code，它的機制跟原版不同:

<div class="cols">
<div class="card">

### 原版 Ralph

bash 外迴圈，**每圈整個重來**:全新 context、靠檔案傳遞進度。是「**換新 context**」的設計。

</div>
<div class="card blue">

### ralph-wiggum plugin

用 **Stop hook** 在**同一個 session** 內攔住結束，進行完成判定。

</div>
</div>

<div class="quote">「同一條 thread 延續」＋「完成與否主模型自己決定」＝ 其實是 <strong>Codex /goal</strong> 作法，而不是原版 Ralph。</div>

<div class="cite">參考:<a href="https://github.com/anthropics/claude-code/tree/main/plugins/ralph-wiggum">claude-code/plugins/ralph-wiggum</a></div>

---

## 對 Ralph 的批評

<div class="card red">

- **無狀態重跑**: prompt 每圈不變，progress.txt 只是軟性筆記、缺結構化記憶
- **暴力跑，收斂困難**: 弱模型的權宜之計，靠大量 token 硬做、可能把關不足
- **執行成本**: 可能卡住一直耗 token

</div>

<div class="quote">心得: 驗證 (goal) 應該在內層 harness 就要做好，而不能只靠外層一直重跑。只依靠外層既耗 token，也很難對大範圍做好驗證。</div>

<div class="cite">參考:Steinberger <a href="https://x.com/steipete/status/2011422781137707112">「slop in a loop」</a>、<a href="https://dev.to/thesystemistsimon/ralph-loop-is-innovative-i-wouldnt-use-it-for-anything-that-matters-4d99">Ralph Loop Is Innovative…</a></div>

---

## OpenAI Symphony: 把專案管理系統變成 Agent 控制系統

OpenAI 開源的 harness 外層系統(以Spec形式): 以任務為中心，將 Linear 當做控制平面，每張開啟的 ticket 都有一個 agent 在自己工作區跑（有新 ticket 就派工)

<div class="cols gap-sm">
<div class="card">

### 專案看板就是狀態機

- ticket 狀態驅動:進 Todo 派 agent、進 Rework 帶 review 重做、進終態收掉
- 任務 DAG:沒被 block 的就開 agents 平行跑
- agent 自己開 ticket、交付 **proof of work** 成果（CI、review、示範影片等）

</div>
<div class="card blue">

### 人管理的是「工作」，不是 code

- 有些 ticket 純調查分析，從頭到尾不碰 codebase
- Agent 的目標不只是「寫完 code」，而是要「說服人類把這段程式碼合併」

</div>
</div>

<div class="cite">參考:OpenAI <a href="https://openai.com/index/open-source-codex-orchestration-symphony/">An open-source spec for Codex orchestration: Symphony</a>（2026/4）</div>

---

## Symphony:看板就是狀態機

<svg viewBox="0 0 700 252" style="width:100%;max-width:1060px;max-height:470px;height:auto;display:block;margin:14px auto" xmlns="http://www.w3.org/2000/svg" role="img" aria-label="OpenAI Symphony 運作原理示意圖">
<defs>
<marker id="symA" markerWidth="11" markerHeight="9" refX="9" refY="3.2" orient="auto"><path d="M0,0 L9,3.2 L0,6.4 Z" style="fill:var(--text-secondary)"/></marker>
</defs>
<rect x="22" y="8" width="656" height="34" rx="8" style="fill:var(--tag-bg);stroke:var(--accent);stroke-width:1.5"/>
<text x="350" y="30" text-anchor="middle" style="fill:var(--text);font-size:10.5px;font-weight:700">🎼 Symphony: 看板當控制平面, 每張開啟的 ticket 都配一個 agent 在自己的 workspace 跑</text>
<rect x="24" y="54" width="150" height="24" rx="5" style="fill:var(--surface);stroke:var(--border);stroke-width:1"/>
<text x="99" y="70" text-anchor="middle" style="fill:var(--text-secondary);font-size:11px;font-weight:600">Todo</text>
<rect x="184" y="54" width="166" height="24" rx="5" style="fill:var(--surface);stroke:var(--border);stroke-width:1"/>
<text x="267" y="70" text-anchor="middle" style="fill:var(--text-secondary);font-size:11px;font-weight:600">In Progress</text>
<rect x="360" y="54" width="150" height="24" rx="5" style="fill:var(--surface);stroke:var(--border);stroke-width:1"/>
<text x="435" y="70" text-anchor="middle" style="fill:var(--text-secondary);font-size:11px;font-weight:600">Review</text>
<rect x="520" y="54" width="156" height="24" rx="5" style="fill:var(--surface);stroke:var(--border);stroke-width:1"/>
<text x="598" y="70" text-anchor="middle" style="fill:var(--text-secondary);font-size:11px;font-weight:600">Done</text>
<rect x="32" y="86" width="134" height="40" rx="6" style="fill:var(--bg);stroke:var(--border);stroke-width:1.2"/>
<text x="99" y="103" text-anchor="middle" style="fill:var(--text);font-size:10.5px;font-weight:600">TICKET-12</text>
<text x="99" y="118" text-anchor="middle" style="fill:var(--text-secondary);font-size:9.5px">待派工</text>
<rect x="32" y="132" width="134" height="40" rx="6" style="fill:var(--bg);stroke:var(--border);stroke-width:1.2"/>
<text x="99" y="149" text-anchor="middle" style="fill:var(--text);font-size:10.5px;font-weight:600">TICKET-13</text>
<text x="99" y="164" text-anchor="middle" style="fill:var(--text-secondary);font-size:9.5px">待派工</text>
<rect x="192" y="86" width="150" height="40" rx="6" style="fill:var(--tag-bg);stroke:var(--accent);stroke-width:1.4"/>
<text x="267" y="103" text-anchor="middle" style="fill:var(--text);font-size:10.5px;font-weight:600">TICKET-9</text>
<text x="267" y="118" text-anchor="middle" style="fill:var(--accent);font-size:9.5px;font-weight:600">🤖 agent A 實作中</text>
<rect x="192" y="132" width="150" height="40" rx="6" style="fill:var(--tag-bg);stroke:var(--accent);stroke-width:1.4"/>
<text x="267" y="149" text-anchor="middle" style="fill:var(--text);font-size:10.5px;font-weight:600">TICKET-10</text>
<text x="267" y="164" text-anchor="middle" style="fill:var(--accent);font-size:9.5px;font-weight:600">🤖 agent B 實作中</text>
<rect x="368" y="86" width="134" height="40" rx="6" style="fill:#fff8c5;stroke:#9a6700;stroke-width:1.4"/>
<text x="435" y="103" text-anchor="middle" style="fill:var(--text);font-size:10.5px;font-weight:600">TICKET-7</text>
<text x="435" y="118" text-anchor="middle" style="fill:#9a6700;font-size:9px">PR + 證明影片, 等人審</text>
<rect x="528" y="86" width="140" height="40" rx="6" style="fill:#dafbe1;stroke:#1a7f37;stroke-width:1.4"/>
<text x="598" y="103" text-anchor="middle" style="fill:var(--text);font-size:10.5px;font-weight:600">TICKET-3</text>
<text x="598" y="118" text-anchor="middle" style="fill:#1a7f37;font-size:9.5px">✓ merged</text>
<line x1="40" y1="200" x2="660" y2="200" style="stroke:var(--text-secondary);stroke-width:1.5" marker-end="url(#symA)"/>
<text x="350" y="220" text-anchor="middle" style="fill:var(--text-secondary);font-size:10.5px">ticket 狀態由左往右流動 = 狀態機; 沒被 block 的各配一個 agent 平行跑</text>
</svg>

---

## 自動排程(cron): 最輕量、最通用的觸發

<div class="cols">
<div>

設定觸發條件，條件一到就自動把一段 prompt 丟出去跑一輪。

Claude Code、Codex 都已**內建**（`/loop`、Routines、Automations），設定就能用，是最容易上手的。

</div>
<div class="card">

### 觸發的節奏

- **定時**: cron 排程，時間到就跑
- **動態**: 讓 agent 自己決定下次何時跑
- **事件**: webhook、新郵件、CI 失敗才觸發

</div>
</div>

例如

```text
/loop 5m 檢查 deploy 狀態，失敗就修        ← 固定間隔
/loop 盯著 CI，紅了就處理                  ← 動態間隔：模型自己決定
```

---

## 設計重點: 要不要沿用 context ?

<div class="cols gap-sm">
<div class="card">

### 每次獨立 context

每次開**全新的 agent**。乾淨 context、進度靠外部狀態。

例如 Codex 的 standalone automation 模式 、Claude Code 的 Routines 功能

</div>
<div class="card blue">

### 沿用 context: Heartbeat

把 prompt 打到**同一個長駐 session**。記憶連續、反應快，但 context 會持續變大。

例如 Codex 的 thread automation 模式、Claude Code 的 in-session `/loop`功能

</div>
</div>

---

## 兩種觸發:獨立 context vs heartbeat

<svg viewBox="0 0 700 300" style="width:100%;max-width:1060px;max-height:470px;height:auto;display:block;margin:14px auto" xmlns="http://www.w3.org/2000/svg" role="img" aria-label="Cron 排程兩種模式: 獨立 context 與 heartbeat">
<defs>
<marker id="crnA" markerWidth="10" markerHeight="8" refX="8" refY="3" orient="auto"><path d="M0,0 L8,3 L0,6 Z" style="fill:var(--accent)"/></marker>
<marker id="crnS" markerWidth="10" markerHeight="8" refX="8" refY="3" orient="auto"><path d="M0,0 L8,3 L0,6 Z" style="fill:var(--text-secondary)"/></marker>
</defs>
<circle cx="58" cy="150" r="26" style="fill:var(--surface);stroke:var(--accent);stroke-width:1.6"/>
<line x1="58" y1="150" x2="58" y2="134" style="stroke:var(--accent);stroke-width:1.6"/>
<line x1="58" y1="150" x2="70" y2="150" style="stroke:var(--accent);stroke-width:1.6"/>
<text x="58" y="196" text-anchor="middle" style="fill:var(--text);font-size:10.5px;font-weight:600">cron 觸發</text>
<text x="58" y="210" text-anchor="middle" style="fill:var(--text-secondary);font-size:9px">時間到就跑</text>
<path d="M84,138 C122,116 144,94 180,86" style="fill:none;stroke:var(--accent);stroke-width:1.4;stroke-dasharray:4 3" marker-end="url(#crnA)"/>
<text x="120" y="104" text-anchor="middle" style="fill:var(--text-secondary);font-size:9.5px">開新的</text>
<path d="M84,162 C122,186 144,208 180,216" style="fill:none;stroke:var(--accent);stroke-width:1.4;stroke-dasharray:4 3" marker-end="url(#crnA)"/>
<text x="120" y="210" text-anchor="middle" style="fill:var(--text-secondary);font-size:9.5px">回同一條</text>
<text x="430" y="28" text-anchor="middle" style="fill:var(--text);font-size:11.5px;font-weight:700">每次獨立 context (cron + headless / 雲端排程)</text>
<rect x="192" y="56" width="120" height="44" rx="7" style="fill:var(--tag-bg);stroke:var(--accent);stroke-width:1.3"/>
<text x="252" y="76" text-anchor="middle" style="fill:var(--text);font-size:10.5px;font-weight:600">t1 全新 run</text>
<text x="252" y="92" text-anchor="middle" style="fill:var(--text-secondary);font-size:9px">乾淨的 context</text>
<rect x="362" y="56" width="120" height="44" rx="7" style="fill:var(--tag-bg);stroke:var(--accent);stroke-width:1.3"/>
<text x="422" y="76" text-anchor="middle" style="fill:var(--text);font-size:10.5px;font-weight:600">t2 全新 run</text>
<text x="422" y="92" text-anchor="middle" style="fill:var(--text-secondary);font-size:9px">乾淨的 context</text>
<rect x="532" y="56" width="120" height="44" rx="7" style="fill:var(--tag-bg);stroke:var(--accent);stroke-width:1.3"/>
<text x="592" y="76" text-anchor="middle" style="fill:var(--text);font-size:10.5px;font-weight:600">t3 全新 run</text>
<text x="592" y="92" text-anchor="middle" style="fill:var(--text-secondary);font-size:9px">乾淨的 context</text>
<text x="430" y="120" text-anchor="middle" style="fill:var(--text-secondary);font-size:9.5px">各自了結, 結果送出後 context 就丟掉; 進度靠外部狀態傳遞</text>
<line x1="150" y1="144" x2="668" y2="144" style="stroke:var(--border);stroke-width:1;stroke-dasharray:3 3"/>
<text x="430" y="172" text-anchor="middle" style="fill:var(--text);font-size:11.5px;font-weight:700">Heartbeat: 沿用 context (/loop · thread automation)</text>
<text x="252" y="192" text-anchor="middle" style="fill:var(--text-secondary);font-size:9px">t1</text>
<text x="430" y="192" text-anchor="middle" style="fill:var(--text-secondary);font-size:9px">t2</text>
<text x="608" y="192" text-anchor="middle" style="fill:var(--text-secondary);font-size:9px">t3</text>
<path d="M252,196 V215" style="fill:none;stroke:var(--text-secondary);stroke-width:1.4" marker-end="url(#crnS)"/>
<path d="M430,196 V215" style="fill:none;stroke:var(--text-secondary);stroke-width:1.4" marker-end="url(#crnS)"/>
<path d="M608,196 V215" style="fill:none;stroke:var(--text-secondary);stroke-width:1.4" marker-end="url(#crnS)"/>
<rect x="190" y="216" width="478" height="60" rx="8" style="fill:var(--surface);stroke:var(--accent);stroke-width:1.5"/>
<text x="210" y="237" style="fill:var(--text);font-size:10.5px;font-weight:600">同一條 session 一直活著</text>
<polygon points="206,268 206,258 648,248 648,268" style="fill:rgba(9,105,218,.15);stroke:var(--accent);stroke-width:0.8"/>
<text x="427" y="264" text-anchor="middle" style="fill:var(--text-secondary);font-size:9px">context 每次都更長 →</text>
</svg>

---

## Loop 和 Goal 可以一起用

| | 管什麼 | 回答的問題 |
|---|---|---|
| **外層 Loop** | scheduling 排程 | **什麼時候**跑、多久跑一次 |
| **Goal** | termination 終止 | 做到**什麼程度**才能停 |

<div class="cols gap-sm">
<div class="card green">

### 作法一

排程內的 Agent 就直接用上 Goal 把事情做完
</div>
<div class="card">

### 作法二

在排程內，把工作丟到某個 queue 就結束。另外有真正做事帶 goal 的 Agent 去執行

</div>
</div>

---

## 案例: 龍蝦爸爸的 Loop 自動維護 Repo

Steinberger 開源的 maintainer-orchestrator skill 每隔 5 分鐘醒來執行

<div class="cols gap-sm">
<div class="card">

### 🕰️ Cron ＋ Orchestrator 協調分配任務

- orchestrator 本身只當**控制平面**:定時檢查、派工、監控、需要時問人決策
- 每 5 分鐘 **heartbeat** 醒來讀各 worker 現況
- 實作全部下放給平行跑的 **worker thread**；worker **不准再往下委派**

</div>
<div class="card blue">

### 🗂️ 先過一道 triage 分類

github-project-triage 把進來的 queue 分三類:

- **Autonomous**:可重現、有界、可驗證 → 直接派工
- **Needs owner**:產品決策、安全、缺權限
- **Defer／close**:過期、重複 → 附證據處置

</div>
</div>

<div class="cite">出處:<a href="https://x.com/steipete/status/2064998499780084154">@steipete</a>（2026/6），skills 開源於 <a href="https://github.com/steipete/agent-scripts">agent-scripts</a></div>

---

## 外層 Loop 核心三個問題

<div class="cols-3 gap-sm">
<div class="card">

### 1️⃣ 怎麼被觸發

固定 cron、動態間隔，還是事件（webhook、新郵件、CI 失敗、看板多一張 ticket）？

</div>
<div class="card">

### 2️⃣ 醒來看什麼

要讀哪些 context 之外的狀態，才知道進度到哪、有沒有新工作？

例如 Ralph 讀 git／progress.txt、Symphony 讀專案看板等等

</div>
<div class="card">

### 3️⃣ 結果送去哪

開 PR、寄一封簡報、丟進 triage 收件匣，還是安靜歸檔？

</div>
</div>

---

![w:860 loopcraft: 由內到外五層巢狀迴圈，從 token 到開放探索](loopcraft.png)

<div class="small center gap-sm">出自 Shawn "swyx" Wang 電子報，其中 loop engineering 最想強調的是第 ④ 層 <strong>MetaLoop</strong>(生迴圈的迴圈)</div>

---

<!-- _class: section -->
<!-- _paginate: false -->

<span class="kicker">PART 7 · 進階</span>

# 自我改進的<br>Harness

---

## 把「改 harness」這件事交給 agent

<div class="cols">
<div>

**連 harness 本身，都讓 agent 自己改。** 讓 agent 根據自己跑出來的 trace 與 eval，回頭改自己的 harness，包括 system prompt, skills 甚至 code 。

<div class="card blue gap-sm">

自我改進不是讓 agent 想改什麼就改什麼

需要在 eval、trace、版本控制、regression test 的限制下，提出可驗證的變更。

不然，「自我改進」和「把 harness 改壞」就分不出來了。
</div>

</div>
<div>

<div class="card">

### 📡 方法一: 讀 Production Traces

</div>
<div class="card gap-sm">

### 🔧 方法二: 用 Agent 當優化器改 code

</div>
<div class="card gap-sm">

### 📚 方法三: Self-Improving 改 Skills

</div>

<div class="small gap-sm">💡 詳見 blog.aihao.tw 文章: 自我改進 Harness, Meta-Harness 與爬坡 </div>

</div>
</div>

---

<!-- _class: section -->
<!-- _paginate: false -->

<span class="kicker">PART 8 · 收尾</span>

# 會過期的 Harness

<p>Model-Harness-Fit</p>

---

## 模型一升級，harness 會怎樣?

<div class="cols gap-sm">
<div class="card blue">

### 🔗 沒有一套 harness 適用所有模型

- 同一套 harness 換個模型，效果**不一樣**
- 小模型要更複雜精巧的 harness，大模型需要的 harness 可以較輕薄

</div>
<div class="card" style="background:#fff8c5;">

### ⏳ harness 會過期

模型每次變強，某些當初**補強它的元件**就不再有用，該被移除。

每次升級時可以檢查之前的 prompt 約束、workflow 還有必要嗎？

</div>
</div>

> Terminal-Bench 2.0 排行榜排的不是「模型」，而是「**harness ＋ 模型**」的配對。同一個模型配不同 harness，分數差好幾個百分點，差距甚至大過一個模型世代的升級。

---

## 設計 Harness 架構時，應考慮模型升級

<div class="cols gap-sm">
<div class="card red">

### ⏳ 會過期

**各種 harness 做法與補強措施**

Bitter Lesson: 能隨算力擴大的通用方法，終究勝過手工規則。很多會隨更強的模型逐步不再需要。

</div>
<div class="card green">

### ♾️ 不會過期

**定義「什麼叫做好」＋ 驗證**

就算模型強到能完美自我驗證，它驗證的，仍然是一個「由你定義的目標」。定義什麼是「好」，是無論模型多強都得自己做的核心。

Harness 應該設計得**容易替換元件、更容易測量性能**: 模型一變強，你才拆得掉。

</div>
</div>

<div class="small gap-sm">💡 詳見 blog.aihao.tw 文章: 會過期的 Harness, Model-Harness-Fit 與 Bitter Lesson</div>

---
<!-- _class: section -->
<!-- _paginate: false -->

<span class="kicker">PART 9 · 動手做</span>

# 自建 Agent 的<br>框架選型

---

## 該從哪個開發框架開始?

<div class="cols gap-sm">
<div class="card blue">

### 路線一: 從功能完整的 Deep Agent 開始

**起點高**: 一開始就有能跑的 agent，但相對不好改。

**✅ 優點**: 馬上能跑；harness 原廠針對自家模型調過。

**⚠️ 缺點**: 會帶用不到的 context／工具；可控性／可維護性受限；常綁特定供應商。

</div>
<div class="card">

### 路線二: 從基礎構建

**起點低**: 要自己接的多，但彈性與可控性好，能一步步朝想要的設計走。

**✅ 優點**: 完全可控，貼著任務分布拿掉無關 context／工具；model 無關、好換供應商、好控成本。

**⚠️ 缺點**: 前期工程量較大。

</div>
</div>

---

## 框架舉例

<div class="cols">
<div class="card blue">

### 路線一: 全套 Deep Agent

- [Codex SDK / app server](https://developers.openai.com/codex/sdk/)）Apache 2.0 開源，可用 ChatGPT 訂閱帳號登入
- [Claude Agent SDK](https://code.claude.com/docs/en/agent-sdk/overview)（Anthropic）核心閉源，第三方只能用 API key
- [LangChain deepagents](https://github.com/langchain-ai/deepagents) MIT 開源

</div>
<div class="card">

### 路線二: 從基礎構建（opinionated 高 → 低）

- [AWS Strands Agents](https://strandsagents.com/)
- [Google ADK](https://adk.dev/)
- [Microsoft Agent Framework](https://github.com/microsoft/agent-framework)
- [OpenAI Agents SDK](https://openai.github.io/openai-agents-python/)
- [Pydantic AI](https://ai.pydantic.dev/)
- [LangGraph](https://github.com/langchain-ai/langgraph)

</div>
</div>

---

## 那到底該選哪個?

<div class="cols-3 gap-sm">
<div class="card">

### 🔹 特定情境／規模大

特定情境，或使用者多 → **從基礎構建**。貼近單一任務分布的 vertical agent 更有效率: token 成本低、延遲低，也能換供應商、精算成本。

</div>
<div class="card">

### 🔹 自用／內部開發

要打造團隊用的 harness 與 outer loop → **從現成 deep agent**。

要的本來就是強的通用開發 agent，原廠已調好內層，先有能跑的東西、疊上 outer loop 最快。

</div>
<div class="card blue">

### 🔹 想用訂閱帳號

要讓使用者帶自己的 ChatGPT 帳號 → **看 Codex SDK 或 Codex app server**。

支援訂閱帳號登入，不必 API key 計費；Claude Agent SDK 第三方只能用 API key。

</div>
</div>

<div class="small gap-sm">💡 詳見 blog.aihao.tw 文章: 自建 Agent 的框架選型: 全套 Deep Agent 還是從基礎構建?</div>

---
<!-- _class: section -->
<!-- _paginate: false -->

<span class="kicker">CONCLUSION</span>

# 總結

<p>Takeaways</p>

---

## 給 Agent 開發者的駕馭工程 系列九篇

1. **Part 1**｜六項 Deep Agent 能力
2. **Part 2**｜Harness = 在**執行迴圈**裡約束、檢查、修正；agent 要**回饋迴路**，不是完美 prompt
3. **Part 3 · 時機①**｜**工具裡**閉合最小迴圈: 驗證、改寫、回傳值夾帶指示
4. **Part 4 · 時機②**｜**request 之間注入**: 人 steer／interrupt，或程式注入背景工具結果
5. **Part 5 · 時機③**｜**單輪結束**驗收 Goal／Outcomes；三種 judge 不同實作分析
6. **Part 6 · 時機④**｜**外層 Loop** 跨 session: Ralph／Symphony／cron，**把自己移出迴圈**
7. **Part 7 · 進階**｜讓 agent **自己改自己的 harness**
8. **Part 8 · 收尾**｜Harness **綁模型、會過期**；不過期的是 **Eval 與 Judge**
9. **Part 9 · 番外**｜框架兩條路:**全套 Deep Agent／從基礎構建**

<div class="small gap-sm">📚 歡迎到 <a href="https://blog.aihao.tw">blog.aihao.tw</a> 看全篇內容。</div>

---

<!-- _class: cover -->
<!-- _paginate: false -->

<span class="kicker">Thank You</span>

# 謝謝，請多指教 🙏

<div class="by">

- 個人部落格 <https://ihower.tw>
- Facebook [ihower](https://www.facebook.com/ihower)
- Threads [@ihower](https://www.threads.net/@ihower)
- Twitter [@ihower](https://twitter.com/ihower)

</div>
