# Bragg Family Website

The family website, live at **[braggfam.com](https://braggfam.com)**.

A simple static site — one HTML file with all CSS inline. No framework, no
build step, no dependencies.

## How it's hosted

| Piece | Where | Notes |
|-------|-------|-------|
| Files | This repo (`Tomicle/braggfam`), `main` branch | Public repo |
| Hosting | GitHub Pages | Free; deploys from `main`, root folder |
| Domain | braggfam.com via Namecheap | DNS: 4 A records to GitHub Pages IPs + `www` CNAME to `tomicle.github.io` |
| HTTPS | Automatic (Let's Encrypt via GitHub Pages) | Auto-renews; "Enforce HTTPS" is on in repo Pages settings |

The `CNAME` file in the repo root tells GitHub Pages to serve the site at
braggfam.com. Don't delete or rename it.

## Repo structure

```
index.html    The entire website (HTML + CSS in one file)
CNAME         Custom domain config for GitHub Pages
README.md     This file
.cursor/      Rules that teach AI agents how this project works
.gitignore    Keeps local-only reference files out of the public repo
```

Some files exist only locally and are intentionally not committed (see
`.gitignore`): the original browser-saved HTML backup, and the Cloudflare
migration plan.

## Making changes

1. Edit `index.html`.
2. Preview locally: `open index.html` (or use a local server).
3. Publish:

   ```bash
   git add index.html
   git commit -m "Describe the change"
   git push
   ```

GitHub Pages redeploys automatically — changes are live at braggfam.com in
about a minute. Check deploy status at the repo's **Actions** tab if needed.

## Important: this repo is public

GitHub Pages on the free plan requires a public repo, so **anything committed
here is visible to the whole internet** (both on GitHub and at braggfam.com).
Never commit home addresses, phone numbers, personal emails, or travel dates.

If the family later wants password-protected content, the plan is to move to
Cloudflare Pages with an email allowlist — see the local
`CLOUDFLARE-MIGRATION-PLAN.md` for the full gameplan.

## Design quick-reference

- **Fonts** (Google Fonts): Passion One (headings), Nunito (body), Caveat
  (script accents)
- **Palette** (CSS variables in `:root`): canyon `#C1440E`, rust `#8A3324`,
  sand `#EFD4A6`, sage `#6E7F5C`, teal `#2E6E6A`, paper `#FBF1DE`,
  ink `#3A2A1E`, gold `#E0A83E`
