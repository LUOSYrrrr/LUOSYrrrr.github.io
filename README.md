# LUOSYrrrr.github.io

Personal homepage for **Siyuan Luo (骆思缘)**, hosted on GitHub Pages at
<https://luosyrrrr.github.io>.

Built on the [AcademicPages](https://github.com/academicpages/academicpages.github.io)
Jekyll template (MIT) with light customisations: simplified navigation, a
bilingual (English / Chinese) toggle in the masthead, and content rewritten
for me.

## File map — what to edit where

| File | What it controls |
|---|---|
| `_config.yml` | Site title, URL, sidebar author block, theme skin, nav plumbing |
| `_data/navigation.yml` | Top-nav items (English + Chinese labels) |
| `_pages/about.md` | Home page — the big prose block; bilingual |
| `_portfolio/*.md` | Projects listed at `/portfolio/` |
| `_includes/masthead.html` | Top bar markup + bilingual toggle CSS/JS (inlined) |
| `images/profile.svg` | Sidebar avatar (placeholder "SL" graphic) |
| `resume.pdf` | CV — direct-linked from the nav as "CV" |

## Local preview

Needs Ruby + Bundler:

```bash
bundle install      # first time only
bundle exec jekyll serve
# open http://localhost:4000
```

If you don't want Ruby locally, push to `main` and let GitHub Pages build it —
every push rebuilds the live site within a minute or two.

## Bilingual toggle — how it works

A small script is inlined in `_includes/masthead.html`:

- Adds class `lang-en` or `lang-zh` to `<html>`.
- Elements with `data-en="..." data-zh="..."` have their textContent swapped
  (used for nav items and the brand title).
- Block-level prose uses `<div class="i18n-en" markdown="1">` and `<div class="i18n-zh" markdown="1">` — the inactive one is hidden by CSS.
- Preference is saved in `localStorage` under key `site-lang`.
- Default language is English, unless the browser's primary language is `zh-*`.

To translate a new page, just wrap the content in those two divs.

## Changing the look

**Skin / colour palette.** `_config.yml` → `site_theme`. Options shipped by
AcademicPages: `default`, `air`, `sunrise`, `mint`, `dirt`, `contrast`. We're
on `dirt` — a warm, paper-ish palette.

**Deeper styling.** `_sass/` holds the SCSS for all skins. `_sass/_themes.scss`
is where the skin palettes are defined.

## Optional profile additions

- [ ] Real avatar photo — save as `images/profile.jpg`, set `author.avatar: "profile.jpg"` in `_config.yml`. (400×400+ square recommended.)
- [ ] LinkedIn, Google Scholar, ORCID — fill in the corresponding keys under `author:` in `_config.yml`; the sidebar icons will appear automatically.
- [ ] Public Audio-L3A paper / code links — add them to `_portfolio/2-audio-l3a.md` when they are ready.

The homepage, portfolio highlights, CV page, and `resume.pdf` are currently synced to the August 2026 résumé.

## Attribution

AcademicPages by the [AcademicPages community](https://github.com/academicpages/academicpages.github.io);
originally forked from [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/)
by Michael Rose. Both MIT-licensed. See `LICENSE`.
