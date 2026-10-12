# FilestoreCloud Docs

Mintlify-powered documentation for the **FilestoreCloud** enterprise multi-tenant Nextcloud SaaS platform on AWS.

## Structure

```
mint.json          # Mintlify configuration (navigation, colors, tabs)
docs/              # Platform documentation (MDX)
│  introduction.mdx
│  architecture-overview.mdx
│  quickstart.mdx
│  deployment/
│  tenants/
│  control-plane/
│  ai/
reports/           # Sprint reports (MDX) linked to GitHub issues/PRs
│  index.mdx
│  2026-10-05.mdx
│  2026-09-28.mdx
│  2026-09-21.mdx
│  2026-09-14.mdx
│  2026-09-07.mdx
public/
   llms.txt        # AI agent sitemap (llmstxt.org standard)
```

## Local Development

```bash
npm install -g mintlify
mintlify dev
# → http://localhost:3000
```

## Deploy

Pushes to `main` auto-deploy via GitHub Actions → Mintlify cloud hosting.

## Add a New Report

1. Create `reports/YYYY-MM-DD.mdx`
2. Add the page to `mint.json` under `"Sprint Reports"` navigation group
3. Link to GitHub PRs/commits/releases for traceability

## Related Repos

- [aws_nextcloud](https://github.com/FilestoreCloud/aws_nextcloud) — Main platform
- [control-panel](https://github.com/FilestoreCloud/control-panel) — Admin console
