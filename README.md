# The Age Vanguard — static website

Edition No. 2 · Monday, November 9, 2026 · English-first, with a Spanish version under `/es/`.
Content taken only from the working draft
`~/workspace/diario-longevidad/edicion-2026-11-09-revision-aplicada.md`
and the extension
`~/workspace/diario-longevidad/edicion-2026-11-09-ampliacion.md`
(no invented data, figures or quotes). Every story on the front page opens
its own page in `articulos/` (English) or `es/articulos/` (Spanish).

Home: Montreal, Canada. Owner: Abadeus, Canada.
Publication slot: 06:00 Montreal time (not yet confirmed as final).

## Structure

- `index.html` — English front page: ER-100 lead, second row of 3, The Latest, Goodbye to Old Age, AI & Brain, The Debate, Biohacking, Culture Silver, Reprogramming & Clocks, Brain & Alzheimer's, Body & Money, Finance, Myths vs. Science, Future Counter. 21 stories in total.
- `articulos/` — 21 English article pages, each with full text, evidence label, date, cautions, sources with links, large image, back-to-home link and related stories.
- `es/index.html` — Spanish front page (same 21 stories).
- `es/articulos/` — 21 Spanish article pages.
- Every page has an EN | ES toggle in the top right, linking to the same page in the other language.
- `styles.css` — shared stylesheet (newspaper style, large type, responsive).
- `assets/img/` — 12 editorial illustrations (8 from the first build + 4 new for the extension). Reused where they fit; the Culture Silver image is an illustration, not a photo of Mildred Baker, and the 50 km record image is an illustration, not a photo of the athlete (name not published).
- `.nojekyll` — so GitHub Pages serves the site as-is.

## Local preview

```bash
cd the-age-vanguard-site
python3 -m http.server 8000
```

Open http://localhost:8000 in the browser (English front page; Spanish at http://localhost:8000/es/).

## Publish on GitHub Pages

1. Create a repository on GitHub (for example `the-age-vanguard`).
2. Upload the contents of this folder to the main branch:
   ```bash
   cd the-age-vanguard-site
   git init
   git add .
   git commit -m "The Age Vanguard — Edition No. 2 (9 Nov 2026), English-first"
   git branch -M main
   git remote add origin https://github.com/YOUR-USER/the-age-vanguard.git
   git push -u origin main
   ```
3. In GitHub: Settings → Pages → Source: Deploy from a branch → Branch: `main` / `/ (root)` → Save.
4. The site will be at `https://YOUR-USER.github.io/the-age-vanguard/` (or at `theagevanguard.com` once the custom domain is connected in Pages).

Nothing on this site has been published yet: the steps above are done by John (or whoever he authorizes) from his GitHub account.
