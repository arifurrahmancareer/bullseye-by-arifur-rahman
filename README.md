# 🎯 Bullseye — Interactive Prototypes

**"Aim. Learn. Invest."** — a gamified stock-market learning platform for Indian teenagers.
Product Design Intern Assignment submission.

This bundle is a **static site** (plain HTML/CSS/JS, zero dependencies, no build step). It deploys as-is to any static host.

## Files

| File | Purpose |
|------|---------|
| `index.html` | Landing hub — links to both prototypes. **Entry point.** |
| `flow.html` | Onboarding flow prototype (6 screens: language → hook → first trade → win → lesson → quiz → Bull III rank-up). |
| `dashboard.html` | Live daily-dashboard prototype (BI portfolio chart, rank, quests, watchlist, squad league, achievements). |
| `favicon.svg` | App icon. |
| `vercel.json` / `netlify.toml` | Deploy configs. |
| `package.json` | Metadata + local-preview script. |
| `robots.txt` | Allows indexing. |

## How the two prototypes interlink

- On the flow's final rank-up screen, **🏠 Go to my Dashboard →** plays a short "landing in the app" animation, then navigates to `dashboard.html`.
- In the dashboard sidebar, **↺ Replay onboarding** navigates back to `flow.html`.

All links are relative filenames, so the interlink works locally, in the zip, and on every static host below.

## Run locally

No server needed — just open `index.html` in a browser. Or, for a local server:

```bash
npx serve .
# or
python3 -m http.server 8080
```

## Deploy

### Vercel
```bash
npm i -g vercel
vercel --prod
```
When asked for settings, accept defaults (framework: **Other**, output dir: **./**). `vercel.json` is already included.

### Netlify
```bash
npm i -g netlify-cli
netlify deploy --prod
```
Or drag-and-drop this folder onto <https://app.netlify.com/drop>. `netlify.toml` sets the publish dir to `.`.

### GitHub Pages (automated — recommended)
This repo ships with `.github/workflows/deploy.yml` and a `.nojekyll` file, so deployment is automatic:
1. Push these files to a GitHub repo (files at the **root**).
2. Repo **Settings → Pages → Build and deployment → Source: GitHub Actions**.
3. Every push to `main` builds and publishes automatically. Live at `https://<user>.github.io/<repo>/`.

### GitHub Pages (manual, no Actions)
1. Push these files to a repo (root).
2. **Settings → Pages → Source: Deploy from a branch** → `main` / `/root`.
3. The included `.nojekyll` ensures files are served as-is. Live at `https://<user>.github.io/<repo>/`.

> All internal links are **relative** (`flow.html`, `dashboard.html`, `favicon.svg`), so the site works correctly whether served from a domain root (Vercel/Netlify) or a project subpath (`/<repo>/` on GitHub Pages).

### Cloudflare Pages / Render / any static host
Point the host at this folder with **no build command** and output directory `.` (root).

## Tech

- Self-contained HTML/CSS/vanilla JS.
- macOS-style glassmorphism, JetBrains Mono, heavy micro-animation, BI-style data-viz.
- JetBrains Mono loads from Google Fonts online; a monospace fallback stack is used offline.
- A production-ready **React + Tailwind + Framer Motion** version of the dashboard is in the Notion write-up (Section 5).
