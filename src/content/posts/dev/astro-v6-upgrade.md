---
title: 部落格框架大升級：Astro v6、Svelte v5、Tailwind v4
published: 2026-05-16
description: '一次升三個主版本的紀錄，以及途中踩到的坑。'
image: ''
tags: ['開發', 'Astro', 'Svelte', 'Tailwind']
category: '開發'
draft: false
lang: 'zh-TW'
---

## 升級範圍

| 套件 | 升級前 | 升級後 |
|---|---|---|
| Astro | 4.16 | 6.3 |
| Svelte | 4.2 | 5.55（Runes） |
| Tailwind CSS | 3.4 | 4.3 |
| @astrojs/svelte | 5.7 | 8.1 |
| Biome | 1.8 | 2.4 |

## 主要 Breaking Changes

### Tailwind v4

`tailwind.config.cjs` 整個移除，改用 CSS-based config。`@tailwind base/components/utilities` 換成 `@import "tailwindcss"`，`@layer components {}` 換成 `@utility {}`。`@astrojs/tailwind` 整合也改用 `@tailwindcss/vite`。

### Svelte v5 Runes

所有 `let x` 響應式變數改為 `$state(x)`，`$:` 改為 `$effect()`，`on:event` 改為 `onevent`，具名 `<slot>` 改為 `{@render snippet()}`。

### Astro v5 → v6

Content Collection 新增 `glob()` loader，`src/content/config.ts` 換成 `src/content.config.ts`。API 也有異動：`entry.render()` 改為 `render(entry)`，`entry.slug` 改為 `entry.id`。

## 踩到的坑

**`ButtonLink.astro` 的 `<a><button>` 無效 HTML**

升完之後跑全站巡查，發現側邊欄分類連結點了都跑回首頁。最後追到根因：`<a>` 包 `<button>` 是無效 HTML（interactive 元素不能巢狀），瀏覽器把 `<a>` 渲染成只有 19px 高，按鈕卻有 40px 往外溢出，Swup 的 click 攔截因此失效。把 `<button>` 移掉，樣式直接套到 `<a>` 上，就好了。

**CI Node.js 版本不符**

Workflow 裝 pnpm `latest`（v10），但 Node.js 只有 v20，pnpm v10 要求 v22.13+。升 Node 到 22，改用 `pnpm/action-setup@v4` 自動讀 `packageManager` 欄位，解決。
