# Docs site deploys to Cloudflare Pages

Supersedes the hosting part of ADR-0025. The VitePress site in `site/` is now built by
`.github/workflows/docs.yml` and deployed with `wrangler pages deploy` to the Cloudflare
Pages project `encore`, on pushes to `develop` that touch `site/**`.

GitHub Pages serves a single custom domain per repository. The site needs several, and
Cloudflare Pages allows any number on one project.

## Consequences

- The workflow needs the repo secrets `CLOUDFLARE_API_TOKEN` (Pages: Edit) and
  `CLOUDFLARE_ACCOUNT_ID`. It creates the project on first run, with `develop` as the
  production branch.
- Custom domains are attached in the Cloudflare dashboard, not in the repo. The site is
  served from `/`, so `DOCS_BASE` stays unset.
