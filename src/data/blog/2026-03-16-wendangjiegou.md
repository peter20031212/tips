---
title: "文档结构"
description: "AstroPaper的文档结构"
pubDatetime: 2026-03-16T12:00:00.000Z
tags: ["blog", "astro"]
featured: true  # 想上首頁就加這行
---

###文档结构
```
src/
├── pages/                    ← ✅ 主頁在這裡！
│   ├── index.astro          ← 網站首頁
│   ├── posts/
│   │   └── [...page].astro  ← 博客列表頁
│   └── about.md            ← 關於頁面
└── data/
    └── blog/               ← ✅ 純資料，沒有頁面！
        ├── 2026-03-16-first-post.md
        └── other-post.md
```
### 详细说明
| 位置                                    | 作用       | URL                           |
| ------------------------------------- | -------- | ----------------------------- |
| src/pages/index.astro                 | 網站首頁     | /                             |
| src/pages/posts/[...page].astro       | 博客列表     | /posts/、/posts/2/             |
| src/data/blog/*.md                    | 文章內容（資料） | 無對應頁面                         |
| src/pages/posts/[...slug]/index.astro | 單篇文章     | /posts/2026-03-16-first-post/ |
