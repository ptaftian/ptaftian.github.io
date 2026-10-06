# Pooriya Taftiyan — portfolio

Personal portfolio site. Static: one HTML file, four images, no build step and no dependencies to install.

**Live:** https://REPLACE-ME/

## Publishing it on GitHub Pages

1. Create a new **public** repository named exactly `<your-github-username>.github.io`.
   That name is what gives you the root URL `https://<your-github-username>.github.io/`
   instead of a `/repo-name/` subpath. A private repo will not serve Pages on a free account.
2. Upload the contents of this folder to the repository root — `index.html`, `og-image.png`,
   `.nojekyll` and the `img/` folder. Do not nest them inside another folder.
3. Go to **Settings → Pages**. Under *Build and deployment*, set **Source** to
   *Deploy from a branch*, branch `main`, folder `/ (root)`. Save.
4. Wait 1–2 minutes, then open `https://<your-github-username>.github.io/`.

Or from a terminal:

```bash
git init
git add .
git commit -m "Portfolio site"
git branch -M main
git remote add origin https://github.com/<your-github-username>/<your-github-username>.github.io.git
git push -u origin main
```

## One edit to make before you share the link

`index.html` has three `REPLACE-ME` placeholders in the `<head>`, in the `og:` and
`twitter:` meta tags and the canonical link. Replace each with your real address, e.g.
`https://pooriya.github.io`. Those tags control the preview card that appears when the
link is pasted into LinkedIn, Telegram or WhatsApp. Until they are set, the preview
shows no image.

## Files

| Path | What it is |
|---|---|
| `index.html` | The whole site — markup, styles, scripts, and the insole mesh data |
| `img/*.webp` | Project and website screenshots |
| `og-image.png` | 1200×630 social preview card |
| `.nojekyll` | Stops GitHub from running Jekyll over the files |

## Notes

- **Language toggle** — EN/FA in the top right. All copy is in `data-en` / `data-fa`
  attributes on each element, so translations are edited in place in the markup.
- **The insole viewer** renders `Right-Insole-Test.STL`, resampled to a 58×156 height
  grid and embedded in `index.html` as base64 in `window.INSOLE`. It draws with
  three.js r128 from cdnjs. If WebGL is unavailable the inline SVG `#insole-mesh`
  shows instead.
- **Fonts** are Archivo, Lexend, IBM Plex Mono and Vazirmatn, loaded from Google Fonts.
  The site needs a network connection to look right; without one it falls back to
  system sans-serif.
- **Custom domain:** add a file named `CNAME` containing just your domain, then point
  an `ALIAS`/`ANAME` or four `A` records at GitHub's Pages IPs at your registrar.
