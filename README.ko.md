# adgk2349.github.io

[English](README.md) · [한국어](README.ko.md) · [日本語](README.ja.md)

`adgk2349`의 개인 블로그/포트폴리오 사이트 저장소입니다. Jekyll + Chirpy 기반이며 GitHub Pages로 배포됩니다.

- 라이브 사이트: <https://adgk2349.github.io>
- 테마 베이스: <https://github.com/cotes2020/jekyll-theme-chirpy>

## 개요

이 저장소에는 다음이 포함됩니다.

- 개발 블로그 글 (`_posts`)
- 정적 페이지 (`_tabs`)
- 사이트 설정 (`_config.yml`)
- 빌드/배포 GitHub Actions 워크플로 (`.github/workflows/pages-deploy.yml`)

## 기술 스택

- Jekyll (Ruby 3.3)
- Chirpy 테마
- GitHub Pages
- Giscus 댓글

## 로컬 개발

### 사전 준비

- Ruby 3.3
- Bundler

### 로컬 실행

```bash
bundle install
bundle exec jekyll s --livereload
```

실행 후 접속:

- <http://127.0.0.1:4000>

## 빌드 및 검증

```bash
bundle exec jekyll b
bundle exec htmlproofer _site --disable-external
```

## 새 글 작성

`_posts` 아래에 마크다운 파일을 생성합니다.

```text
_posts/YYYY-MM-DD-title.md
```

프론트 매터 예시:

```yaml
---
title: "Post Title"
date: 2026-03-09 10:00:00 +0900
categories: [Dev, Notes]
tags: [jekyll, chirpy]
---
```

## 배포

`main` 브랜치에 푸시하면 GitHub Actions가 자동으로 빌드/배포합니다.

워크플로 파일:

- `.github/workflows/pages-deploy.yml`

참고:

- `README.md`, `LICENSE`, `.gitignore` 변경은 배포 트리거에서 제외됩니다.

## 디렉터리 노트

- `_posts`: 블로그 글
- `_tabs`: 정적 메뉴 페이지
- `assets`: 이미지/폰트/정적 자산
- `_config.yml`: 사이트 메타데이터 및 동작 설정
- `_site`: 빌드 결과물

## 라이선스

이 저장소는 MIT 라이선스로 배포됩니다. 자세한 내용은 `LICENSE`를 참고하세요.
