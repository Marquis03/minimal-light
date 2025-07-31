# Minimal Light 主题

[![LICENSE](https://img.shields.io/github/license/Marquis03/minimal-light?style=flat-square&logo=creative-commons&color=EF9421)](https://github.com/Marquis03/minimal-light/blob/main/LICENSE)

[[主题演示](https://marquis03.github.io/minimal-light)] [[English](./README.md)]

这是我的个人主页模板源代码。我基于 [minimal](https://github.com/orderedlist/minimal) 主题构建了这个网站。

*你可以在任何地方自由使用和分享此源代码。*

## 功能特点

- 简洁优雅的个人主页主题
- Jekyll 主题，由 GitHub Pages 自动部署
- 基本的搜索引擎优化
- 移动设备友好
- 支持 Markdown
- 支持自动的深色模式

## 项目架构

```text
.
├── _data
|   ├── competitions.yml                      # 竞赛信息的YAML文件
|   ├── publications.yml                      # 发表论文的YAML文件
|   └── services.yml                          # 服务信息的YAML文件
├── _includes
|   ├── competitions.html                     # 竞赛信息的HTML文件
|   ├── publications.html                     # 论文信息的HTML文件
|   └── services.html                         # 服务信息的HTML文件
├── _layouts
|   └── homepage.html                         # 主页的HTML模板
├── _sass
|   ├── minimal-light.scss                    # 此文件将被编译为CSS文件，控制页面样式
|   └── minimal-light-no-dark-mode.scss       # 此文件与minimal-light.scss类似，但禁用了深色模式
├── assets                                    # 静态文件
├── .gitignore                                # 指定Git应忽略的未跟踪文件
├── CNAME                                     # 自定义域名，供GitHub Pages服务使用
├── Gemfile                                   # RubyGems相关文件
├── LICENSE                                   # 许可证文件
├── README.md                                 # 自述文件（英文）
├── README_zh_Hans.md                         # 自述文件（简体中文）
├── _config.yml                               # Jekyll配置文件，包含页面的一些选项
└── index.md                                  # 首页内容，使用Markdown格式
```

## 快速开始

这个模板可以通过以下两种方式使用：

- **使用 GitHub Pages 服务**：GitHub 将为你提供一个服务器来生成和托管网页。
- **在本地使用 Jekyll**：你可以在自己的计算机上安装 Jekyll，使用此模板生成静态网页（即 HTML 文件）。然后，你可以将 HTML 文件上传到自己的服务器。

详细说明如下。

### 使用 GitHub Pages 服务

在 GitHub 上使用此模板有两种方法：

#### 方法一：Fork 这个仓库

- Fork 这个仓库（或者[使用这个仓库作为模板](https://docs.github.com/en/github/creating-cloning-and-archiving-repositories/creating-a-repository-from-a-template)），并将名称更改为 `your-username.github.io`。

- 按照[这里](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site#creating-your-site)的步骤为该仓库启用 GitHub Pages。

#### 方法二：使用此仓库作为远程主题

要使用此主题，请在你的仓库的 `_config.yml` 中添加以下内容：

```yaml
remote_theme: Marquis03/minimal-light
```

请注意，添加上述行会直接将此仓库中的所有默认设置应用到你的仓库。

如果你希望编辑任何文件（例如 `index.md`），仍需要将它们复制到你的仓库中。

### 在本地使用 Jekyll

首先，安装 [Ruby](https://www.ruby-lang.org/en/) 和 [Jekyll](https://jekyllrb.com/)。安装说明可以在这里找到：<https://jekyllrb.com/docs/installation/#guides>

然后，克隆这个仓库：

```bash
git clone https://github.com/Marquis03/minimal-light.git
cd minimal-light
```

安装并运行：

```bash
bundle install
bundle add webrick
bundle exec jekyll server
```

使用 `localhost` 查看实时页面：
<http://localhost:4000>。你可以在 `_site` 文件夹中获取 HTML 文件。

## 自定义设置

### 配置变量

Minimal Light 主题有以下的变量, 你可以在 `_config.yml` 文件中修改：

```yaml
# Basic Information
title: Your Name
position: Master Student
affiliation: Your Affiliation
affiliation_link: https://marquis03.github.io/minimal-light
email: yourname (at) example.edu

# Search Engine Optimization (SEO)
# The following information is used to improve the website traffic from search engines, e.g., Google.
keywords: minimal light
description: The Minimal Light is a simple and elegant jekyll theme for academic personal homepage.
canonical: https://marquis03.github.io/minimal-light

# Links
# If you don't need one of them, you may delete the corresponding line.
google_scholar: https://scholar.google.com/
cv_link: assets/files/curriculum_vitae.pdf
github_link: https://github.com/
kaggle_link: https://www.kaggle.com/
linkedin: https://www.linkedin.com/
twitter: https://twitter.com/

# Images (e.g., your profile picture and your website's favicon)
# "favicon" and "favicon_dark" are used for the light and dark modes, respectively.
avatar: ./assets/img/avatar.png
favicon: ./assets/img/favicon.svg
favicon_dark: ./assets/img/favicon.svg

# Footnote
# You may use the option to disable the footnote, "Powered by Jekyll and Minimal Light theme."
enable_footnote: true

# Auto Dark Mode
# You may use the option to disable the automatic dark theme
auto_dark_mode: true

# Font
# You can use this option to choose between Serif or Sans Serif fonts.
font: "Serif" # or "Sans Serif"

# Baidu Analytics ID
# Please remove this if you don't use Baidu Analytics
baidu_analytics:

# Google Analytics ID
# Please remove this if you don't use Google Analytics
google_analytics: UA-XXXXXXXXX-X
```

### 编辑 `index.md`

创建 `index.md` 并添加你的个人信息。它支持 **Markdown** 和 **HTML** 语法。

### 编辑包含文件

在 `index.md` 中包含了三个 HTML 文件，分别是 `_includes/competitions.html`、`_includes/publications.html` 和 `_includes/services.html`。如果你不希望包含这三个文件，可以删除 `index.md` 中的相应行：

```markdown
{% include publications.html %}

{% include services.html %}

{% include competitions.html %}
```

如果你希望在不更改格式的情况下编辑这些列表，可以编辑 `_data/competitions.yml`、`_data/publications.yml` 和 `_data/services.yml`。

### 样式表（CSS）

如果你想添加自己的自定义样式，可以编辑 `_sass/minimal-light.scss`。

### 布局（HTML）

如果你想更改主题的 HTML 布局，可以编辑 `_layout/homepage.html`。

## 许可证

这个项目使用 [Creative Commons Zero v1.0 Universal](https://github.com/Marquis03/minimal-light/blob/main/LICENSE) 许可证。

## 致谢

我们的项目使用了以下仓库的源代码：

- [Xiao-Chenguang/minimal-light](https://github.com/Xiao-Chenguang/minimal-light)
- [yaoyao-liu/minimal-light](https://github.com/yaoyao-liu/minimal-light)
- [pages-themes/minimal](https://github.com/pages-themes/minimal)
- [orderedlist/minimal](https://github.com/orderedlist/minimal)
- [al-folio](https://github.com/alshedivat/al-folio)
