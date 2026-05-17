---
title: 用 utterances 把 GitHub Issues 變成留言板
published: 2026-05-17
description: '在靜態部落格加上留言功能，不需要後端、不需要資料庫。'
image: ''
tags: ['開發', 'Astro', 'utterances']
category: '開發'
draft: false
lang: 'zh-TW'
---

## 為什麼選 utterances

靜態部落格要加留言，常見方案有 Disqus（有廣告）、Giscus（用 GitHub Discussions）、utterances（用 GitHub Issues）。

選 utterances 的理由很單純：Issues 夠用、無廣告、設定最少。

## 實作方式

新增 `src/components/misc/Comments.astro`，裡面放 utterances 的 `<script>` 標籤，然後掛到 `src/pages/posts/[...slug].astro` 的文章內容後面。

```astro
<script
  src="https://utteranc.es/client.js"
  repo="chiaowei-weng/chiaowei-weng.github.io"
  issue-term="pathname"
  theme="github-light"
  crossorigin="anonymous"
  async
></script>
```

`issue-term="pathname"` 代表每篇文章的 Issue 標題用頁面路徑命名，留言自動分類，不需要手動建 Issue。

## 深色模式同步

utterances 載入後是一個 `<iframe>`，要切換主題需要用 `postMessage` 傳訊息進去。用 `MutationObserver` 監聽 `document.documentElement` 的 class 變化，偵測到 `dark` 加上或移除時就發訊：

```js
const observer = new MutationObserver(() => {
  const isDark = document.documentElement.classList.contains('dark')
  iframe.contentWindow?.postMessage(
    { type: 'set-theme', theme: isDark ? 'github-dark' : 'github-light' },
    'https://utteranc.es'
  )
})
observer.observe(document.documentElement, {
  attributes: true,
  attributeFilter: ['class'],
})
```

## 啟用前提

到 [github.com/apps/utterances](https://github.com/apps/utterances) 安裝 GitHub App，授權給對應的 repo，留言功能才會正常運作。
