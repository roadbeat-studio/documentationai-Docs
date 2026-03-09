# roadbeat Studio — Documentation

Public documentation for [roadbeat Studio](https://studio.roadbeat.dev), the self-hosted headless CMS for structured content publishing.

**Live site:** Published automatically via [Documentation.AI](https://documentation.ai) on push to `main`.

## Structure

```
studio-docs/
├── documentation.json          # Site config, branding, navigation
├── openapi.yaml                # OpenAPI 3.0 spec (auto-generates API Reference)
├── introduction.mdx            # Landing page
├── quickstart.mdx              # Getting started guide
├── concepts.mdx                # Core concepts
├── architecture.mdx            # Technical architecture
├── guides/                     # In-depth guides
│   ├── content-types.mdx
│   ├── content-management.mdx
│   ├── content-relations.mdx
│   ├── content-layouts.mdx
│   ├── assets.mdx
│   ├── publishing.mdx
│   ├── localization.mdx
│   ├── users-and-roles.mdx
│   ├── webhooks.mdx
│   ├── search.mdx
│   ├── backup-and-export.mdx
│   ├── cdn.mdx
│   └── consumer-features.mdx
├── editors/                    # Editor-focused documentation
│   ├── guide.mdx
│   ├── content-editor.mdx
│   ├── rich-text.mdx
│   └── working-with-assets.mdx
├── api-reference/              # API overview pages (endpoints from openapi.yaml)
│   ├── overview.mdx
│   ├── authentication.mdx
│   └── delivery-api.mdx
├── plugins/                    # Plugin system & CE vs Pro
│   ├── overview.mdx
│   ├── developing-plugins.mdx
│   └── ce-vs-pro.mdx
├── deployment/                 # Self-hosting & configuration
│   ├── self-hosting.mdx
│   └── configuration.mdx
├── help-center.mdx             # Help center landing
├── help-center/                # FAQ, troubleshooting, step-by-step guides
│   ├── faq/
│   ├── troubleshooting/
│   └── guides/
└── changelog.mdx               # Release notes
```

## Editing

All pages are `.mdx` files (Markdown + JSX components). Available components:

- `<Callout>` — info, tip, alert, danger, success
- `<Card>` / `<Columns>` — navigation cards in grid layouts
- `<Steps>` / `<Step>` — sequential procedures
- `<Tabs>` / `<Tab>` — tabbed content
- `<CodeGroup>` — multi-language code blocks
- `<Expandable>` — collapsible sections (FAQ)
- `<ParamField>` / `<ResponseField>` — API parameter docs
- Mermaid diagrams via fenced code blocks

Navigation is defined in `documentation.json`. Every new page must be added there.

## Workflow

1. Edit `.mdx` files locally or via the Documentation.AI web editor
2. Commit and push to `main`
3. Documentation.AI auto-builds and deploys

## Related

- [Studio source code](https://github.com/roadbeat/studio) (CE, AGPL 3.0)
- [Schema Registry docs](../schema-registry-docs/)
- [Context Directory docs](../context-directory-docs/)
