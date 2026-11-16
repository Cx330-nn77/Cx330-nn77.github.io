+++
title = '第一篇文章：这个博客怎么写'
date = '2026-11-16T20:00:00+08:00'
draft = false
categories = ['工具配置']
tags = ['Hugo', 'GitHub Pages']
summary = '用 Hugo + GitHub Pages 搭建个人博客，以及之后怎么新增文章。'
+++

这是博客的第一篇文章，也是一份写作备忘。

## 新建一篇文章

在博客目录运行：

```bash
hugo new content posts/my-first-note.md
```

会在 `content/posts/` 下生成一个文件，开头是这样的“文章信息”：

```toml
+++
title = 'my first note'
date = '2026-11-16T20:00:00+08:00'
draft = true          # 写完改成 false 才会发布
categories = ['论文笔记']
tags = ['RSI']
summary = '一句话简介'
+++
```

下面直接用 Markdown 写正文就行。

## 本地预览

```bash
hugo server -D
```

浏览器打开 <http://localhost:1313/>，保存文件后页面会自动刷新。`-D` 表示草稿也显示。

## 发布

```bash
git add -A
git commit -m "新文章：xxx"
git push
```

推送后 GitHub Actions 会自动构建，大约一分钟后网站更新。

## Markdown 常用写法

- **加粗**、*斜体*、`行内代码`
- 链接：[GitHub](https://github.com/Cx330-nn77)
- 图片：把图片放到 `static/images/`，然后写 `![说明](/images/xxx.png)`
- 表格：

| 方法 | 准确率 |
| ---- | ------ |
| 基线 | 70%    |
| 改进 | 75%    |

> 引用块适合写论文原文摘录。
