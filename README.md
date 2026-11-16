# Nan 的博客

网址：https://cx330-nn77.github.io/

用 [Hugo](https://gohugo.io/) + [PaperMod](https://github.com/adityatelange/hugo-PaperMod) 主题搭建，推送到 `main` 后由 GitHub Actions 自动构建并发布到 GitHub Pages（约 1 分钟）。

## 写一篇新文章

```bash
hugo new content posts/文章英文名.md
```

打开 `content/posts/文章英文名.md`，修改开头信息：

```toml
+++
title = '文章标题'
date = '2026-11-16T20:00:00+08:00'
draft = false               # true 是草稿，不会发布
categories = ['论文笔记']    # 论文笔记 / 实验记录 / 工具配置
tags = ['RSI', '智能体']
summary = '一句话简介'
+++
```

下面用 Markdown 写正文。图片放在 `static/images/`，文中写 `![说明](/images/图片.png)`。

## 本地预览

```bash
hugo server -D
```

浏览器打开 http://localhost:1313/ ，保存后自动刷新。

## 发布

```bash
git add -A
git commit -m "新文章：标题"
git push
```

## 目录说明

| 路径 | 作用 |
| --- | --- |
| `content/posts/` | 文章 |
| `content/about.md` | “关于”页面 |
| `hugo.toml` | 网站标题、菜单、首页介绍等设置 |
| `static/` | 图片等静态文件 |
| `themes/PaperMod/` | 主题（git 子模块，不要直接改） |
| `.github/workflows/hugo.yml` | 自动部署配置 |

## 备注

- 本仓库已设置走本机代理 `127.0.0.1:7897` 推送（仅对本仓库生效）。若关闭了代理导致推送失败，运行 `git config --unset http.proxy` 取消。
- 重新克隆本仓库时需带上主题：`git clone --recursive https://github.com/Cx330-nn77/Cx330-nn77.github.io.git`
