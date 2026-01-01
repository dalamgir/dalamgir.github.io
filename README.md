# dalamgir.github.io

Personal blog powered by Hugo + PaperMod, deployed via GitHub Pages.

## Writing posts

Add Markdown files under `content/posts/` (you can nest in folders). Example front matter:

```yaml
---
title: "Post title"
date: 2025-01-01T00:00:00Z
tags: ["ai", "physics"]
description: "Optional short summary"
draft: false
---
```

## Local preview (no Ruby required)

- With Docker (no host install):

  ```bash
  docker run --rm -it -p 1313:1313 \
    -v "$PWD":/src \
    -w /src \
    klakegg/hugo:0.146.0-ext-alpine \
    server --bind 0.0.0.0 --baseURL http://localhost -D
  ```

- If you have Hugo locally, run `hugo server -D`.

## Deployment

GitHub Actions workflow (`.github/workflows/gh-pages.yml`) builds and deploys to GitHub Pages on pushes to `main`. Ensure Pages is set to "GitHub Actions" in repository settings.
