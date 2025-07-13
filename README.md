# The Minimal Light Theme

[![LICENSE](https://img.shields.io/github/license/Marquis03/minimal-light?style=flat-square&logo=creative-commons&color=EF9421)](https://github.com/Marquis03/minimal-light/blob/main/LICENSE)

[[Demo the theme](https://marquis03.github.io/minimal-light)] [[简体中文](./README_zh_Hans.md)]

*This is the source code of my homepage. I build this website based on [minimal](https://github.com/orderedlist/minimal).*

*Feel free to use and share the source code anywhere you like.*

## Features

- Simple and elegant personal homepage theme
- Jekyll theme, automatically deployed by GitHub Pages
- Basic search engine optimization
- Mobile friendly
- Supporting Markdown
- Supporting dark mode

## Project Architecture

```text
.
├── _data
|   ├── competitions.yml                      # the YAML file for competitions
|   ├── publications.yml                      # the YAML file for publications
|   └── services.yml                          # the YAML file for services
├── _includes
|   ├── competitions.html                     # the HTML file for competitions
|   ├── publications.html                     # the HTML file for publications
|   └── services.html                         # the HTML file for services
├── _layouts
|   └── homepage.html                         #  the HTML template for the homepage
├── _sass
|   ├── minimal-light.scss                    #  this file will be compiled into a CSS file to control the style of the page
|   └── minimal-light-no-dark-mode.scss       #  this file is similar to minimal-light.scss with the dark mode disabled
├── assets                                    #  some files
├── .gitignore                                #  this file specifies intentionally untracked files that Git should ignore
├── CNAME                                     #  the custom domain, will be used by GitHub page sevice
├── Gemfile                                   #  a RubyGems related file
├── LICENSE                                   #  the license file
├── README.md                                 #  the readme file (English)
├── README_zh_Hans.md                         #  the readme file (Simplified Chinese)
├── _config.yml                               #  the Jekyll configuration file, including some options of the page
└── index.md                                  #  the content of the index page, using Markdown
```

## Getting Started

This template can be used in the following two ways:

- **Using with the GitHub Pages Service.** GitHub will provide you with a server to generate and host web pages.
- **Using locally with Jekyll.** You may install Jekyll on your own computer and generate static web pages (i.e., HTML files) with this template. After that, you may upload the HTML files to your server.

The detailed instructions are available below.

### Using with the GitHub Pages Service

There are two ways to use this template on GitHub:

#### Fork this repository

- Fork this repository (or [use this repository as a template](https://docs.github.com/en/github/creating-cloning-and-archiving-repositories/creating-a-repository-from-a-template)) and change the name to `your-username.github.io`.

- Enable the GitHub pages for that repository following the steps [here](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site#creating-your-site).

#### Using this repository as a remote theme

To use this theme, add the following to your repository's `_config.yml`:

```yaml
remote_theme: Marquis03/minimal-light
```

Please note that adding the above line will directly apply all the default settings in this repository to yours.

If you hope to edit any files (e.g., `index.md`), you still need to copy them to your repository.

### Using Locally with Jekyll

First, install [Ruby](https://www.ruby-lang.org/en/) and [Jekyll](https://jekyllrb.com/). The install instructions can be found here: <https://jekyllrb.com/docs/installation/#guides>

Then, clone this repository:

```bash
git clone https://github.com/Marquis03/minimal-light.git
cd minimal-light
```

Install and run:

```bash
bundle install
bundle add webrick
bundle exec jekyll server
```

View the live page using `localhost`:
<http://localhost:4000>. You can get the HTML files in `_site` folder.

## Customizing

### Configuration variables

The Minimal Light theme will respect the following variables, if set in your site's `_config.yml`:

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

# Google Analytics ID
# Please remove this if you don't use Google Analytics
google_analytics: UA-111540567-4
  ```

### Edit `index.md`

Create `index.md` and add your personal information. It supports **Markdown** and **HTML** syntax.

### Edit included files

There are three html files included in `_layouts/homepage.html`. They are `_includes/competitions.html`, `_includes/publications.html` and `_includes/service.html`, respectively. If you don't hope to include these three files, you may remove the following lines in `_data/competitions.yml`, `_data/publications.yml` and `_data/services.yml`:

<https://github.com/Marquis03/minimal-light/blob/e7880e3fbcf28d52d35467db6e3580140fe0c650/_data/competitions.yml#L1-L20>

<https://github.com/Marquis03/minimal-light/blob/e7880e3fbcf28d52d35467db6e3580140fe0c650/_data/publications.yml#L1-L18>

If you hope to edit these lists without changing the format, you may edit `_data/competitions.yml`, `_data/publications.yml` and `_data/services.yml`.

### Stylesheet

If you'd like to add your own custom styles, you may edit `_sass/minimal-light.scss`.

### Layouts

If you'd like to change the theme's HTML layout, you may edit `_layout/homepage.html`.

## License

This work is licensed under a [Creative Commons Zero v1.0 Universal](https://github.com/Marquis03/minimal-light/blob/main/LICENSE) License.

## Acknowledgements

Our project uses the source code from the following repositories:

- [Xiao-Chenguang/minimal-light](https://github.com/Xiao-Chenguang/minimal-light)
- [yaoyao-liu/minimal-light](https://github.com/yaoyao-liu/minimal-light)
- [pages-themes/minimal](https://github.com/pages-themes/minimal)
- [orderedlist/minimal](https://github.com/orderedlist/minimal)
- [al-folio](https://github.com/alshedivat/al-folio)
