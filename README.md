<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="images/storix-logo-white.png">
    <img alt="Storix Logo" src="images/storix-logo.png" width="360">
  </picture>
</p>

# Storix Documentation

Mintlify-powered documentation site for the **Storix** enterprise multi-tenant Nextcloud SaaS platform on AWS.

---

## 📂 Structure

```
.
├── docs.json                   # Mintlify configuration (navigation, branding, colors)
├── index.mdx                   # Homepage introduction & quick navigation
├── docs/                       # Core platform documentation (MDX)
│   ├── introduction.mdx        # Platform architecture, tenants & key capabilities
│   ├── architecture-overview.mdx # Full-stack AWS architecture & isolation model
│   ├── quickstart.mdx          # End-to-end setup & initial tenant provisioning
│   ├── deployment/             # Deployment guides, prerequisites & GitHub Actions
│   │   ├── prerequisites.mdx
│   │   ├── github-actions.mdx
│   │   ├── local-cli.mdx
│   │   └── verification.mdx
│   ├── tenants/                # Multi-tenant provisioning & lifecycle operations
│   │   ├── provisioning.mdx
│   │   ├── lifecycle.mdx
│   │   ├── isolation-model.mdx
│   │   └── suspension-resumption.mdx
│   ├── control-plane/          # SuperAdmin Console, Step Functions, Async OCC & Observability
│   │   ├── super-admin-console.mdx
│   │   ├── ssm-runbook.mdx
│   │   ├── dynamodb-registry.mdx
│   │   └── cloudwatch.mdx
│   └── ai/                     # Bedrock AI integration & LiteLLM bridge
│       ├── bedrock-integration.mdx
│       ├── litellm-bridge.mdx
│       └── rag-pipeline.mdx
├── images/                     # Architecture diagrams, screenshots & icons
│   ├── nextcloud_architecture.png
│   ├── console_architecture.png
│   ├── 01_console_login_page.png
│   ├── 02_console_tenants_light.png
│   ├── 03_console_tenants_dark.png
│   ├── 04_console_command_palette.png
│   ├── 05_runtime_storix_theme.png
│   └── 05_runtime_nextcloud_theme.png
└── public/
    └── llms.txt                # AI agent discovery sitemap (llmstxt.org standard)
```

---

## 🚀 Local Development

### 1. Install Mintlify CLI

```bash
npm i -g mintlify
```

### 2. Preview Locally

```bash
mintlify dev
# Opens documentation server at http://localhost:3000
```

### 3. Validate Links & Schema

```bash
mintlify broken-links
```

---

## 🔗 Related Repositories

- [**`FilestoreCloud/infra`**](https://github.com/FilestoreCloud/infra): Modular CloudFormation IaC, Step Functions SAGAs & Lambda Control Plane.
- [**`FilestoreCloud/runtime`**](https://github.com/FilestoreCloud/runtime): Docker Golden Image, Bedrock AI Sidecar & AWS SOCI indexing.
- [**`FilestoreCloud/console`**](https://github.com/FilestoreCloud/console): Super Admin Web Console (React 18 + Refine + Ant Design + WebAuthn).
- [**`FilestoreCloud/reports`**](https://github.com/FilestoreCloud/reports): Sprint reports, threat models & verification evidence.

---

## License

Documentation is licensed under the [MIT License](LICENSE).
