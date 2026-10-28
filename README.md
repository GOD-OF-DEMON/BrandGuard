# BrandGuard — Web (Phase A: interface)

Responsive Next.js (TypeScript, App Router) interface for BrandGuard, based on the “BrandGuard — Evidence Before Publication” Round 1 presentation.

> **Phase A status:** interface, navigation, validation and states only.
> No database, authentication, AI analysis, logo check or approvals are connected yet.
> All data shown is **synthetic demo data** and is labelled as such in the UI.

## Run locally

Requirements: Node.js 20+ (tested on Node 22), npm.

```bash
npm install
npm run dev          # http://localhost:3000
```

Production build and server:

```bash
npm run build
npm run start        # http://localhost:3000
```

## Checks

```bash
npm run typecheck
npm test
```

Browser test (needs Playwright and Chromium, and the app built first):

```bash
pip install playwright && python -m playwright install chromium
python tests/e2e/phase_a_browser_test.py
```

## Pages

| Route | Purpose | Phase A state |
|---|---|---|
| `/` | Landing page | Static content |
| `/login`, `/register`, `/forgot-password` | Auth forms | Client validation; submit shows “not connected” |
| `/dashboard` | Review dashboard | Demo data |
| `/review` | Submit content for review | Client validation; analysis not connected |
| `/review/[id]` | Findings and evidence | Demo example |
| `/guidelines` | Brand rules | Demo data; editing not connected |
| `/evidence` | Evidence sources | Demo data; upload not connected |
| `/approvals` | Decisions and comments | Demo data; actions not connected |
| `/history` | Audit history | Demo data; search works |
| `/settings` | Workspace settings | Demo data; invites not connected |

## Roadmap

- Phase B: authentication, database, sessions and server-side authorization
- Phase C: AI content analysis and OCR
- Phase D: logo similarity, approval workflow and audit events
- Final phase: containerized deployment with API and PostgreSQL

## Security notes

Browser validation improves user experience but is not a security boundary; repeat checks on the server. Security headers are configured in `next.config.mjs`. No secrets are used or stored in this phase; `.env*` files are git-ignored.
