# adgk2349.github.io

[English](README.md) · [한국어](README.ko.md) · [日本語](README.ja.md)

`adgk2349` の個人ブログ/ポートフォリオ用リポジトリです。Jekyll + Chirpy で構築し、GitHub Pages で配信します。

- 公開サイト: <https://adgk2349.github.io>
- テーマベース: <https://github.com/cotes2020/jekyll-theme-chirpy>

## 概要

このリポジトリには以下が含まれます。

- 開発ブログ記事 (`_posts`)
- 静的ページ (`_tabs`)
- サイト設定 (`_config.yml`)
- ビルド/デプロイ用 GitHub Actions ワークフロー (`.github/workflows/pages-deploy.yml`)

## 技術スタック

- Jekyll (Ruby 3.3)
- Chirpy テーマ
- GitHub Pages
- Giscus コメント

## ローカル開発

### 前提条件

- Ruby 3.3
- Bundler

### ローカル実行

```bash
bundle install
bundle exec jekyll s --livereload
```

起動後:

- <http://127.0.0.1:4000>

## ビルドと検証

```bash
bundle exec jekyll b
bundle exec htmlproofer _site --disable-external
```

## 新規投稿の作成

`_posts` 配下に Markdown ファイルを作成します。

```text
_posts/YYYY-MM-DD-title.md
```

フロントマター例:

```yaml
---
title: "Post Title"
date: 2026-03-09 10:00:00 +0900
categories: [Dev, Notes]
tags: [jekyll, chirpy]
---
```

## デプロイ

`main` ブランチへ push すると、GitHub Actions が自動でビルド/デプロイします。

ワークフローファイル:

- `.github/workflows/pages-deploy.yml`

注意:

- `README.md`、`LICENSE`、`.gitignore` の変更はデプロイトリガー対象外です。

## ディレクトリメモ

- `_posts`: ブログ記事
- `_tabs`: 静的メニューページ
- `assets`: 画像/フォント/静的アセット
- `_config.yml`: サイトメタデータと動作設定
- `_site`: ビルド出力

## ライセンス

このリポジトリは MIT ライセンスで公開されています。詳細は `LICENSE` を参照してください。
