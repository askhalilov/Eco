# Deploy to GitHub Pages (Vite + React)

This project uses Vite and outputs production files into the **build/** folder (see `vite.config.ts`).

## Local build
```bash
npm i
npm run build
```

## GitHub Pages deploy (recommended)
A workflow is included at `.github/workflows/deploy.yml`.

1. Push this repo to GitHub.
2. Go to **Settings → Pages** and set **Source** to **GitHub Actions**.
3. Push to `main` (or run the workflow manually). Your site will be deployed.

## Notes
- `vite.config.ts` uses `base: './'` so assets work correctly on GitHub Pages subpaths.
- Routing uses `createHashRouter` so refresh/deep links don't 404 on Pages.
