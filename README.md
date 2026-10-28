# BrandGuard — Evidence Before Publication

BrandGuard is a prototype for reviewing marketing content against brand guidelines before publication.

## Links

- **Live demo:** https://brandguard-demo-dahiyaharsh630-7779.vercel.app
- **Repository:** https://github.com/GOD-OF-DEMON/BrandGuard
- **Standalone browser demo:** open `index.html` directly or serve it from a static host.

## Prototype status

This repository includes a standalone interactive demo in `index.html`. The demo uses synthetic sample data and browser-only interactions.

**Not production-ready:** authentication, database persistence, real AI analysis, OCR, logo similarity checks, notifications, and server-backed approvals are not connected. Do not use sample compliance scores or decisions for real publication decisions.

## Run the standalone demo

Open `index.html` in a browser. No build step is required for this file.

## Run the Next.js app locally

Requirements: Node.js 20+ and npm.

```bash
npm install
npm run dev
```

Then open http://localhost:3000.

Production build:

```bash
npm run build
npm run start
```

## Checks

```bash
npm run typecheck
npm test
```

## Main workflow areas

- Dashboard and sample review queue
- New content review form
- Brand guidelines
- Evidence library
- Approval decision examples
- Activity history and settings

## Roadmap

1. Add authentication, database, sessions, and server-side authorization.
2. Connect AI content analysis and OCR.
3. Add logo similarity checks, a real approval workflow, and audit events.
4. Add deployment configuration and a production database.

## Security notes

Browser-side validation is for user experience only and is not a security boundary. Repeat validation and authorization on the server. Never commit secrets; keep environment files out of version control.
