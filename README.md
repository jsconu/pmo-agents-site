# pmo-agents marketing site

A single, hand-authored static page (`index.html` + `style.css`) — no build step, no framework,
no JavaScript. Deliberately separate from the `pmo-agents` webapp repo/codebase.

## What still needs to be filled in

- **The signup URL.** Every call-to-action currently points at the literal placeholder
  `https://app.pmo-agents.example/signup` — grep for that exact string in `index.html` and
  replace every occurrence once the real webapp has a public deployment (see the main
  `pmo-agents` repo's README; no hosting has been stood up for it yet as of this site's creation).
- **Real pricing.** The Pricing section (`<!-- PRICING: ... -->` comment in `index.html`)
  intentionally describes the a la carte *model* without hardcoding dollar figures, since real
  Stripe prices haven't been set yet (`scripts/billing_plans.json` in the main repo still has
  placeholder prices). Once real per-agent prices exist, either list them directly in that
  section or link out to a real pricing page on the app itself.

## Local preview

No server needed — just open `index.html` directly in a browser.

## Deploying to GitHub Pages

1. Create a new GitHub repository (e.g. `pmo-agents-site`).
2. Push this directory's contents to that repo's default branch:
   ```
   git remote add origin https://github.com/<your-username>/pmo-agents-site.git
   git add -A
   git commit -m "Initial marketing site"
   git push -u origin master
   ```
3. In the repo's Settings → Pages, set the source to "Deploy from a branch", branch `master`
   (or `main`), folder `/ (root)`.
4. The site will be live at `https://<your-username>.github.io/pmo-agents-site/` within a few
   minutes. A custom domain can be added later from that same Settings page.
