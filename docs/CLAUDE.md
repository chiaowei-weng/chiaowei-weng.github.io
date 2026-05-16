# Blog 專案知識庫

> Schema 文件 — 每次作業開始時，請同時閱讀本檔與 `wiki/index.md`。
> 每次重大 compile、批次 ingest 或結構變更後請更新本檔。

## 範疇

### 涵蓋

本 wiki 記錄 **[Fuwari](https://github.com/saicaca/fuwari) 部落格專案** 的所有面向：

- **技術架構**：Astro 框架、Svelte 元件、Tailwind CSS、build pipeline
- **內容系統**：Markdown 撰寫規範、frontmatter 欄位、content collection 設定
- **自訂套件**：remark / rehype 外掛（摘錄、閱讀時間、directive、KaTeX、GitHub Card）
- **功能模組**：全文搜尋（Pagefind）、RSS、Sitemap、頁面切換動畫（Swup）
- **UI 元件**：Navbar、PostCard、ArchivePanel、Search、LightDarkSwitch 等
- **i18n**：多語系架構與語言設定
- **部署**：GitHub Pages、Vercel、build 指令與靜態輸出
- **開發流程**：新增文章、格式化（Biome）、型別檢查

### 不涵蓋

- 文章本身的內容（那是部落格的產出，不是知識庫的對象）
- Astro 或 Tailwind 的官方文件全文（僅記錄本專案的使用方式與踩坑）
- 與本專案無關的 LLM / AI 研究

## 操作

本 wiki 遵循 llm-wiki skill 的五種操作：`compile`、`ingest`、`query`、`lint`、`audit`。
每次操作均在 `log/YYYYMMDD.md` 追加一筆記錄。

## 命名規範

- **概念頁**（`wiki/concepts/`）：Title Case 名詞短語，繁體中文或英文皆可視主題而定
- **資料夾分割**（`wiki/concepts/<topic>/`）：主題超過 ~1200 字時使用，含 `index.md` + 各面向子頁
- **實體頁**（`wiki/entities/`）：套件名稱、工具名稱、人名等專有名詞
- **摘要頁**（`wiki/summaries/`）：kebab-case 來源 slug

所有頁面需有 YAML frontmatter：`title`、`type`、`created`、`updated`、`sources`、`tags`。

### 圖表與公式

- 所有流程圖、架構圖 → **mermaid**，禁止 ASCII art
- 所有公式 → **KaTeX**（行內 `$...$`，區塊 `$$...$$`）

### 原始檔政策

- 小型文字來源 → 複製到 `raw/<子資料夾>/`
- 大型二進位檔 → 在 `raw/refs/<slug>.md` 建立指標檔（含 `kind: ref` 與 `external_path`），不複製本體

## 現有文章

*尚無 — 每次 compile 後更新此清單*

### 概念
*(無)*

### 實體
*(無)*

### 摘要
*(無)*

## 待研究問題

- Swup 頁面切換動畫與 Astro View Transitions 的差異與選擇理由？
- Pagefind 全文搜尋的 build 流程與索引原理？
- `rehype-components` 的自訂 directive 擴充機制？
- OKLCH 色彩轉換在 Stylus 中的 `oklchToHex` 函式用途？

## 研究缺口

待 ingest 的來源：

- [ ] `src/plugins/` 目錄下各外掛原始碼 — 理解自訂 remark/rehype 的實作
- [ ] `src/content/spec/about.md` — 了解 about 頁規範
- [ ] `astro.config.mjs` — 完整的 build 設定文件化
- [ ] `tailwind.config.cjs` — 主題色設定與 OKLCH 機制

## Audit 待辦

*(無 — 執行 `python3 scripts/audit_review.py <wiki-root> --open` 以更新)*

## LLM 作業備註

- **語言**：繁體中文（技術名詞、套件名稱保留英文原文）
- **語調**：由淺入深 — 先給概覽與用途，再展開實作細節
- **深度**：讀者假設為「懂網頁開發但剛接觸此專案」
- **矛盾處理**：並列兩種說法，各自引用來源，加入「待研究問題」追蹤
