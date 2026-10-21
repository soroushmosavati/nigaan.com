# nigaan.com

Marketing site for Nigaan AI Consulting & Governance. Static HTML/CSS (Tailwind via CDN) — no build step.

## Local preview

Open `index.html` directly in a browser, or serve it:

```bash
npx serve .
```

## Deploy

This repo deploys to Vercel as a static site — no framework preset or build command needed (leave "Build Command" and "Output Directory" at their defaults for a static site, or explicitly set Output Directory to `.`). Every push to `main` triggers a production deploy once the Vercel project is connected to this GitHub repo.
