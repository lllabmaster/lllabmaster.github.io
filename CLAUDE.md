# BrookJI 的博客站点

这是一个基于 Jekyll 的个人博客网站，托管在 GitHub Pages 上。

## 项目概览

- **类型**: Jekyll 静态站点 / GitHub Pages
- **主题**: 基于 onevcat 的 Jekyll 主题
- **语言**: 中文博客为主
- **Ruby 版本**: 使用 Jekyll 3.6.3+

## 项目结构

```
├── _config.yml          # Jekyll 配置文件
├── _includes/           # 可复用的 HTML 组件
│   ├── head.html       # 页面头部
│   ├── footer.html     # 页脚
│   ├── side-panel.html # 侧边栏
│   ├── comments.html   # 评论系统
│   └── ...
├── _layouts/            # 页面布局模板
│   ├── default.html    # 默认布局
│   ├── post.html       # 文章布局
│   ├── page.html       # 页面布局
│   └── category.html   # 分类页面布局
├── _posts/             # 博客文章存放目录
├── _sass/              # Sass 样式文件
├── css/                # 编译后的 CSS
├── js/                 # JavaScript 文件
├── assets/             # 静态资源
├── Gemfile             # Ruby 依赖
├── index.html          # 首页
└── categories.html     # 分类索引页面
```

## 开发工作流

### 本地预览

```bash
# 安装依赖
bundle install

# 启动本地服务器
bundle exec jekyll serve

# 访问 http://localhost:4000
```

### 创建新文章

1. 在 `_posts/` 目录下创建新文件
2. 文件命名格式: `YYYY-MM-DD-title.markdown` 或 `YYYY-MM-DD-title.md`
3. 使用以下 front matter 模板:

```yaml
---
layout: post
title: 文章标题
date: YYYY-MM-DD
categories: category-name
comments: true
---
```

### 重要配置

- **permalink**: `/:year/:month/:day/:title/`
- **paginate**: 每页 10 篇文章
- **cover_color**: 红色主题
- **评论系统**: Disqus (lllabmaster)

### 分类功能

博客支持文章分类功能（使用 Jekyll 原生 + 前端 JavaScript 实现）：

1. **在文章中设置分类** - 在 front matter 中添加 `categories` 字段：

```yaml
---
layout: post
title: 文章标题
date: 2026-07-10
categories: diary
comments: true
---
```

支持多个分类：
```yaml
categories: [diary, tech]
```

2. **查看分类** - 访问 `/categories/` 查看所有分类及文章列表

3. **分类浏览** - 点击分类标签可查看该分类下的所有文章，使用 URL hash 实现切换（如 `/categories/#diary`）

**说明**：此方案不依赖 GitHub Actions 或额外脚本，分类数据由 Jekyll 原生生成，前端 JavaScript 处理分类切换。

## 内容规范

- 文章主要使用 Markdown 格式
- 代码高亮使用 Rouge
- 主题技术栈: 深度学习、TensorFlow、PyTorch、Spark、Scala 等

## 部署

- 推送到 `master` 分支后，GitHub Pages 自动构建部署
- 站点地址: `https://lllabmaster.github.io`

## 注意事项

1. 文章日期会出现在 URL 中，确保文件名日期准确
2. 中文文件名在 URL 中会被编码，建议使用拼音或英文
3. Disqus 评论需要在文章中设置 `comments: true`
