# nigaan.com

Marketing site for Nigaan AI Consulting & Governance. Static HTML/CSS (Tailwind via CDN) — no build step.

## Local preview

Open `index.html` directly in a browser, or serve it:

```bash
npx serve .
```

## Deploy

This repo deploys to Vercel as a static site with one serverless function — no framework preset or build command needed (leave "Build Command" and "Output Directory" at their defaults for a static site, or explicitly set Output Directory to `.`). Every push to `main` triggers a production deploy once the Vercel project is connected to this GitHub repo.

## Contact form

`index.html` posts to `/api/contact.js`, which emails submissions via Gmail SMTP (nodemailer). It needs these environment variables set in the Vercel project (Settings → Environment Variables):

- `GMAIL_USER` — the sending Gmail address (currently `nigaan.co@gmail.com`)
- `GMAIL_APP_PASSWORD` — a Google [App Password](https://myaccount.google.com/apppasswords) for that account (requires 2-Step Verification enabled)
- `CONTACT_TO` — optional, defaults to `GMAIL_USER` if unset

Redeploy after adding/changing these. The form includes a honeypot field and a minimum-time check for basic spam resistance.
