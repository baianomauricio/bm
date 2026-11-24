# bm

Personal website of **Mauricio Silva** — personal life and spare-time interests. A plain HTML/CSS/JS holding page for now.

- **Production:** https://www.baianomauricio.com
- **Dev/staging:** https://baianomauricio-35586.web.app
- **Hosting:** Firebase Hosting, project `baianomauricio-35586` (Spark/free tier — no billing, no backend)

This site is the personal member of a three-site collection: [mauriciosilva.com](https://www.mauriciosilva.com) (professional life), this site (personal life), [baiano.photos](https://www.baiano.photos) (photography). The sites cross-link intentionally.

## Pages

| Route | Content |
|---|---|
| `/` | Holding page — minimal, with Hobby → Finance and Retirement → Planning expandable launchers linking the finance and retirement pages |
| `/finance/stocks/chart_pattern.html` | Bearish Candlestick Patterns reference - 16 pattern cards with example charts, plus a MACD Indicator section (signal line crossover, divergence, centerline crossover — bullish and bearish) |
| `/finance/stocks/market_recovery.html` | Market Shocks & Recovery - S&P 500 returns 1 and 12 months after 28 major world events, 1940–2026, with sparklines and a near-a-recession column (source: LPL Financial; three rows computed from index closes) |
| `/retirement/planning/family_trust_structure.html` | Family Trust Structure - ownership, management, succession and separate business risks; grantor, family trust, holding company and separate LLCs diagram (source: The Marathon Group) |
| `/ai/` | AI hobby index |
| `/ai/claude-secret-codes.html` | Five Claude prompt shortcuts from Outskill, with attribution and unverified-claims notes |

## Site-wide behavior

- **Breadcrumb bar:** a fixed 25px bar at the top of every page, showing the trail from Home (e.g. Home / Finance / Stocks / Chart Patterns). Finance and Stocks are plain text until index pages exist for those segments. The bar scrolls horizontally on narrow screens.
- **Curtains wipe transition:** plain left-clicks on same-origin links wipe three dark panels across the screen before navigating; the new page loads covered and lifts the curtain. The panels' leading edge is slanted 12°. Vanilla JS + CSS only — no framework, no CDN, no new requests. Reduced motion disables it; with JS off, navigation is plain.

## Sitemap

- https://www.baianomauricio.com/ (holding page — the sitemap will grow when the real site is scoped)
- https://www.baianomauricio.com/finance/stocks/chart_pattern.html (Bearish Candlestick Patterns reference)
- https://www.baianomauricio.com/finance/stocks/market_recovery.html (Market Shocks & Recovery reference)
- https://www.baianomauricio.com/retirement/planning/family_trust_structure.html (Family Trust Structure reference)

- https://www.baianomauricio.com/ai/ (AI hobby)
- https://www.baianomauricio.com/ai/claude-secret-codes.html (Claude prompting reference)

## Repo layout

- `public/` — site source and deploy directory: the `index.html` holding page plus standalone pages in `finance/stocks/` and `retirement/planning/`, and the AI hobby pages in `ai/`
- `firebase.json` — Hosting config (`public/` web root)
- `.github/workflows/` — CI: pushes to `master` auto-deploy to production

## Workflow

1. Requirements live in the portfolio repo: `documentation/bm/requirements.md` (versioned, owned by Elizabeth).
2. Edit files under `public/`, commit, push to `master` — GitHub Actions deploys to production automatically.

## Constraints

- **Cost:** everything stays on free tiers — Firebase Spark, GitHub Actions.
- **Secrets:** never committed. Production deploys use the `FIREBASE_SERVICE_ACCOUNT` GitHub secret.
