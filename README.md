# lmnop.app — the site

The landing page and (later) the blog. Deliberately a separate repository from
`lmnop-2609-studio`.

**Why separate:** the app is frozen as the reference implementation for the rebuild.
The site is the one thing that should keep changing. Sharing a repo would mean every
blog post redeploys the app.

- `index.html` — the whole site. No framework, no build step.
- `netlify.toml` — publishes this folder, and holds the commented-out rewrite that
  sends `/studio/*` to the app's deploy once both sites exist.

The app lives at `lmnop.app/studio`, on the same origin on purpose: a path keeps the
browser storage, the saved settings and the installed PWA that a subdomain or a second
domain would throw away.
