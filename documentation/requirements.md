# Requirements — baianomauricio.com (personal site)

> **Status:** Draft v0.1 — 2026-09-28. Requirements owner: Elizabeth (UX architect). Implemented by James (full-stack dev). The owner edits this doc directly to request changes.

## §1. Project

- **Purpose:** the owner's personal site — personal life and spare-time interests. One of a three-site collection: mauriciosilva.com = professional life, baianomauricio.com = personal life, baiano.photos = photography. Footer cross-links between the three sites are intentional.
- **Repo:** `baianomauricio/bm`, default branch `master`.
- **Hosting:** Firebase Hosting (Spark plan — free tier, no billing), project `baianomauricio-35586`.
- **URLs:** live at https://baianomauricio-35586.web.app; custom domains `baianomauricio.com` + `www.baianomauricio.com` (DNS propagating at v0.1).
- **Workflow:** same as the portfolio — pushes to `master` auto-deploy via GitHub Actions; `documentation/` is GitHub-only and never deployed (ignored in `firebase.json`).

## §2. Current state — holding page

The holding page is live and the owner likes it — **keep as-is** until the real build:
- H1: "Mauricio Baiano — coming soon"
- Line: "A new personal site is on its way. Stay tuned."
- Footer: "© 2026"

## §3. Analytics

- GA4 via `gtag.js`, measurement ID **G-BRBDZ471ZV** (being added).
- Each site gets its own GA4 property — this ID is for baianomauricio.com only. IDs for mauriciosilva.com and baiano.photos are still to come; do not reuse this one there.

## §4. Standing constraints

- Free tier only: no billing accounts, no paid services; flag anything that might cost.
- `documentation/` never ships to production.

## §5. Future build (parking lot)

- The real personal-site build comes later; scope TBD by the owner.
- Planned: footer cross-links to mauriciosilva.com and baiano.photos (three-site collection).

## §6. Open questions

- **Q1.** GA4 measurement IDs for mauriciosilva.com and baiano.photos — still to come from the owner.
- **Q2.** Confirm custom-domain propagation (`baianomauricio.com`, `www`) once DNS settles.
- **Q3.** Analytics approach differs by site (`gtag.js` here vs GTM planned for the portfolio) — unify later or keep per-site?

## §10. Decision log

- **v0.1 — 2026-09-28:** Initial requirements. Holding page kept as-is per owner; GA4 ID G-BRBDZ471ZV assigned to this site only (per owner's standing rule, relayed by James, Elizabeth owns requirements for all web projects).

*End of requirements v0.1. Owner: mark anything you disagree with — this doc is yours to revise.*
