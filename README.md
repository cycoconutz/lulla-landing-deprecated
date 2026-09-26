# DEPRECATED — lulla landing page

This repository is retired. It is kept only so the landing page's history stays
readable. **Do not edit anything here — the changes will never ship.**

## Where the landing page lives now

The landing page ships as part of the main app:

- **Source:** [`lulla/public/landing/index.html`](../lulla/public/landing/index.html)
- **Live at:** `/landing` (e.g. `https://lulla.dev/landing`)
- **Deployed by:** Cloudflare Pages, from the `lulla` repo's `main` branch

It is a single self-contained `index.html` with no build step of its own. It sits
in the app's `public/` directory, so `npm run build` copies it verbatim to
`dist/landing/index.html` and Cloudflare Pages serves it at `/landing`. That is
the whole deployment mechanism — there is nothing to configure.

## Making changes

Edit the file in the `lulla` repo, not this one. Because the app is deployed
from `main`, a push to `lulla` is what publishes the update.

The four "Open Lulla free" calls to action were repointed from
`https://cycoconutz.github.io/lulla/` to `/` when the page moved, so the landing
page now hands off to the app on the same origin.

## Note on the contact form

The form still opens a `mailto:` to a personal address. If that should become a
domain address, `lulla.dev` needs Cloudflare Email Routing first — the zone has
no MX records today, so nothing else is in the way.
