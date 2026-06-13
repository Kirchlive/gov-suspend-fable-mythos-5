# Anthropic Fable 5 / Mythos 5 — Suspension Dossier

A single-page, static research dossier on the **US export-control directive (June 12, 2026)** that suspended access to Anthropic's Claude **Fable 5** and **Mythos 5** models. Built to be hosted on **GitHub Pages**.

> **Unofficial research compilation. Not affiliated with Anthropic.** All third-party statements are paraphrased and link back to public primary sources. This is a developing story — verify against the linked sources before relying on any detail.

---

## What's inside

| File | Purpose |
|------|---------|
| `index.html` | The full dossier as a self-contained page (inline CSS + minimal vanilla JS, no build step, no dependencies except web fonts). |
| `README.md` | This file. |
| `.gitignore` | Blocks OS junk files (`.DS_Store`, `Thumbs.db`, …) and common editor/tooling cruft. |

The page covers, in 11 numbered sections: core facts · timeline · the models (Fable 5 / Mythos 5, safeguards, benchmarks, pricing) · the suspension itself · the jailbreak dispute · the Pentagon background conflict · reactions on Reddit, X and in the news · open questions · full source list.

---

## Features

- **Self-contained** — one HTML file, no framework, no build.
- **Light / dark theme** — follows `prefers-color-scheme`, with a manual toggle persisted via `localStorage`.
- **Sticky section index** with scroll-spy (IntersectionObserver) and a reading-progress bar.
- **Responsive** down to mobile; visible keyboard focus; `prefers-reduced-motion` respected.
- Typography: IBM Plex **Serif / Sans / Mono** (loaded from Google Fonts, with system fallbacks).

---

## Run locally

It's a static file — just open it, or serve the folder:

```bash
# Python
python3 -m http.server 8000
# then visit http://localhost:8000

# or Node
npx serve .
```

---

## Deploy to GitHub Pages

1. Create a repo and push these files to the `main` branch root:

   ```bash
   git init
   git add .
   git commit -m "Add Fable 5 / Mythos 5 suspension dossier"
   git branch -M main
   git remote add origin https://github.com/<user>/<repo>.git
   git push -u origin main
   ```

2. In the repo: **Settings → Pages → Build and deployment → Source: Deploy from a branch**, then pick **Branch: `main` / `/ (root)`** and save.

3. The site goes live at:

   ```
   https://<user>.github.io/<repo>/
   ```

   For a user/organization site, name the repo `<user>.github.io` and it will serve at `https://<user>.github.io/`.

> No Jekyll processing is needed (it's plain HTML). If you ever add files that start with `_`, drop an empty `.nojekyll` file in the root to bypass Jekyll.

---

## Editing

All content lives in `index.html`. Sections are plain `<section class="block" id="sec-N">` elements; the theme is driven entirely by CSS custom properties at the top of the `<style>` block (`--paper`, `--ink`, `--signal`, …) — change those to re-skin the whole page.

---

## Sourcing & accuracy notes

- Primary sources (Anthropic statement + launch blog, SecurityWeek, Axios reporting, the March court ruling coverage) were read directly.
- The Reddit thread list is taken from the Techmeme aggregation; only the **r/LocalLLaMA** thread was analyzed at the comment level. Other subreddit comment content is unverified.
- Some crypto-news outlets report conflicting dates (June 1 / June 11); the authoritative figure is Anthropic's own: **June 12, 2026, 17:21 ET**.
- Anthropic announced further technical detail "over the next 24 hours" after the statement — not yet incorporated.

## License / use

Source code (HTML/CSS/JS) is free to reuse and adapt. The dossier text is a compiled summary of public reporting; quoted/paraphrased material remains the property of the respective publishers. No warranty — see the in-page disclaimer.
