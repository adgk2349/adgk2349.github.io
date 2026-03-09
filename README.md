# adgk2349.github.io

Personal blog and portfolio site for `adgk2349`, built with Jekyll + Chirpy and deployed on GitHub Pages.

- Live site: <https://adgk2349.github.io>
- Theme base: <https://github.com/cotes2020/jekyll-theme-chirpy>

## Overview

This repository contains:

- Dev blog posts (`_posts`)
- Static pages (`_tabs`)
- Site configuration (`_config.yml`)
- GitHub Actions workflow for build and deploy (`.github/workflows/pages-deploy.yml`)

## Tech Stack

- Jekyll (Ruby 3.3)
- Chirpy theme
- GitHub Pages
- Giscus comments

## Local Development

### Prerequisites

- Ruby 3.3
- Bundler

### Run locally

```bash
bundle install
bundle exec jekyll s --livereload
```

Then open:

- <http://127.0.0.1:4000>

## Build and Validate

```bash
bundle exec jekyll b
bundle exec htmlproofer _site --disable-external
```

## Writing a New Post

Create a markdown file under `_posts`:

```text
_posts/YYYY-MM-DD-title.md
```

Use front matter like:

```yaml
---
title: "Post Title"
date: 2026-03-09 10:00:00 +0900
categories: [Dev, Notes]
tags: [jekyll, chirpy]
---
```

## Deployment

Push to `main` and GitHub Actions builds/deploys the site automatically.

Workflow file:

- `.github/workflows/pages-deploy.yml`

Note:

- Changes to `README.md`, `LICENSE`, and `.gitignore` are ignored by deploy trigger.

## Directory Notes

- `_posts`: blog posts
- `_tabs`: static menu pages
- `assets`: images/fonts/static assets
- `_config.yml`: site metadata and behavior
- `_site`: generated output

## License

This repository is distributed under the MIT License. See `LICENSE` for details.
