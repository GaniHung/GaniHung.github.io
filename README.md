# GaniHung.github.io

Personal bilingual (English / Chinese) research website for Guohui Li (李国辉), hosted on GitHub Pages.

## Purpose

This site presents undergraduate research, publications, selected projects, awards, and personal interests for academic applications and long-term maintenance. It replaces the previous blog with a lightweight static layout.

## Structure

```text
index.html              English homepage
zh/index.html           Chinese homepage
assets/css/styles.css   Shared styles
assets/js/main.js       Navigation and smooth scroll
assets/images/          Site images and favicon
assets/videos/          Project and performance videos
assets/documents/       CV PDFs (when available)
404.html                Not-found page
robots.txt, sitemap.xml SEO files
.nojekyll               Disable Jekyll processing
```

Original media files live in `Sources/` locally. That folder is gitignored; copy processed assets into `assets/` before committing.

## Local preview

From the repository root:

```bash
python -m http.server 8000
```

Open `http://localhost:8000/` for English and `http://localhost:8000/zh/` for Chinese.

## Updating content

### Papers

Edit the Publications section in both `index.html` and `zh/index.html`. Replace disabled “Coming soon” buttons with real links when paper, code, or manuscript URLs are available.

### CV

Place PDFs in `assets/documents/` as:

- `Guohui_Li_CV_English.pdf`
- `Guohui_Li_CV_Chinese.pdf`

Then add CV buttons in the hero section of each language page.

### Projects

Add a new project card under `#projects` in both language files. Include one real screenshot in `assets/images/`, a short description, and a GitHub link.

### Images and videos

1. Add source files to `Sources/` (local only).
2. Process or compress as needed.
3. Copy outputs to `assets/images/` or `assets/videos/`.
4. Reference them with root-relative paths such as `/assets/images/example.jpg`.

### Bilingual text

Keep English and Chinese pages structurally aligned, but write Chinese copy naturally rather than translating word-for-word.

## GitHub Pages deployment

This repository is configured for user/organization Pages at `https://ganihung.github.io/`.

1. Commit changes on `main`.
2. Push to `origin main`.
3. In the repository settings, ensure Pages is enabled for the `main` branch (root `/`).
4. Wait for the deployment workflow to finish, then verify the live site.

## Backup

A legacy snapshot of the previous blog should be kept on branch `backup/legacy-site-20260620` before major rebuilds.
