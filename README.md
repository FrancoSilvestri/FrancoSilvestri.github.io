# Franco Silvestri — Portfolio Site

A single-page, fully self-contained portfolio (one `index.html`, no build step, no dependencies).
Works identically offline, in preview, and on GitHub Pages.

```
portfolio-site/
├── index.html                       # the whole site (HTML + CSS + JS inline)
├── Franco_Silvestri_Resume.pdf      # linked by the "Download résumé" buttons
└── assets/
    ├── poster-thumb.jpg             # research poster preview
    ├── Mercury_Characterization_Poster.pdf
    ├── demo-ar-menu.jpg             # AR human–robot control
    ├── demo-ar-control.jpg          # AR arm teleoperation
    ├── demo-gp.jpg                  # Gaussian-Process contaminant field
    └── demo-explore.jpg             # autonomous exploration / SLAM map
```

## Deploy to GitHub Pages (free, ~3 minutes)

**Option A — personal site at `https://<username>.github.io`:**
1. Create a public repo named exactly `<username>.github.io`.
2. Put the contents of this `portfolio-site/` folder in the repo root (so `index.html` is at the top level).
3. Push. It goes live at `https://<username>.github.io` within a minute.

**Option B — project page at `https://<username>.github.io/portfolio`:**
1. Create a repo (e.g. `portfolio`) and push this folder's contents.
2. Repo → **Settings → Pages** → Source: `Deploy from a branch` → Branch: `main` / `root` → Save.
3. Live at `https://<username>.github.io/portfolio`.

```bash
cd portfolio-site
git init && git add . && git commit -m "Portfolio site"
git branch -M main
git remote add origin https://github.com/<username>/<repo>.git
git push -u origin main
```

## Customize
- **Add your GitHub link:** in `index.html`, search for the `.cta-row` and footer `.links`; add an `<a>` to your GitHub next to the LinkedIn button.
- **Colors:** every color is a CSS variable at the top of `index.html` (`--accent`, `--bg`, etc.). Change `--accent` to re-skin the whole site.
- **Text:** all content is plain HTML in `index.html` — edit directly.
- **Add videos:** upload clips to YouTube (like your workshop playlist) and embed, or replace a gallery `<img>` with a `<video>` tag if you host the file.

## ⚠️ Before making it public
The demo stills and poster come from DOE-funded work (MSIPP / SRNL / Oak Ridge Y-12). The images used here
match content already shown on the **publicly presented conference poster**, but confirm with your ARC / DOE PI
that these specific stills are cleared for public release before publishing the site.
