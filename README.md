# bm

Personal website of **Mauricio Silva** — personal life and spare-time interests. A plain HTML/CSS/JS holding page for now.

- **Production:** https://www.baianomauricio.com
- **Dev/staging:** https://baianomauricio-35586.web.app
- **Hosting:** Firebase Hosting, project `baianomauricio-35586` (Spark/free tier — no billing, no backend)

This site is the personal member of a three-site collection: [mauriciosilva.com](https://www.mauriciosilva.com) (professional life), this site (personal life), [baiano.photos](https://www.baiano.photos) (photography). The sites cross-link intentionally.

## Pages

| Route | Content |
|---|---|
| `/` | Holding page — intentionally minimal until the real site is scoped |

## Sitemap

- https://www.baianomauricio.com/ (holding page — the sitemap will grow when the real site is scoped)

## Repo layout

- `public/` — site source and deploy directory (currently a single `index.html` holding page)
- `firebase.json` — Hosting config (`public/` web root)
- `.github/workflows/` — CI: pushes to `master` auto-deploy to production

## Workflow

1. Requirements live in the portfolio repo: `documentation/bm/requirements.md` (versioned, owned by Elizabeth).
2. Edit `public/index.html`, commit, push to `master` — GitHub Actions deploys to production automatically.

## Constraints

- **Cost:** everything stays on free tiers — Firebase Spark, GitHub Actions.
- **Secrets:** never committed. Production deploys use the `FIREBASE_SERVICE_ACCOUNT` GitHub secret.
