<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="logo/storix-logo-white.png">
    <img alt="Storix Logo" src="logo/storix-logo.png" width="360">
  </picture>
</p>

# Storix Documentation

Mintlify-powered documentation for the **Storix** enterprise multi-tenant Nextcloud SaaS platform on AWS.

## Structure

```
docs.json          # Mintlify configuration (navigation, colors, tabs)
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

### 1. Install the CLI

```bash
npm i -g mint
```

> ⚠️ The CLI package is `mint`, not `mintlify`. Do not install the legacy `mintlify` package.

### 2. Verify install

```bash
mint --version
```

### 3. Preview locally

```bash
mint dev
# → http://localhost:3000
```

### 4. Validate before pushing

```bash
mint validate
mint broken-links
```

## Deploy

Pushes to `main` auto-deploy via GitHub Actions → Mintlify cloud hosting.

Add `MINTLIFY_API_KEY` to GitHub repo secrets (get from [app.mintlify.com](https://app.mintlify.com/settings/organization/api-keys)).

## Add a New Report

1. Create `reports/YYYY-MM-DD.mdx`
2. Add the page to `docs.json` under the `"Sprint Reports"` navigation group
3. Link to GitHub PRs/commits/releases for traceability

## Related Repos

- [aws_nextcloud](https://github.com/Storix/aws_nextcloud) — Main platform
- [control-panel](https://github.com/Storix/control-panel) — Admin console
