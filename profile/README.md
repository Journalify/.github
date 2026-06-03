<div align="center">

# Journalify

### **Editorial OS for modern newsrooms.**

*Multi-tenant · Arabic-first · AI-native · Built in Berlin.*

[![Website](https://img.shields.io/badge/website-journalify.io-7912D5?style=for-the-badge)](https://journalify.io)

</div>

---

## What we're building

Journalify is a **multi-tenant SaaS editorial platform** that helps newsrooms publish faster — from assignment to byline to public reader, in one workflow. We give editors, journalists, and newsroom admins the tools they actually need in 2026: AI-assisted writing, multilingual + RTL-first publishing, real-time collaboration, integrated analytics, and a clean publish-anywhere workflow.

**The problem.** Most newsroom CMSes were built English-first and bolted Arabic / RTL / multilingual on top a decade later. Editors fight their CMS to publish a clean Arabic story. Multi-language workflows are duct-tape. AI is either absent or grafted on as a useless sidecar.

**Our take.** Build it Arabic-first from day zero. Give editors AI that *challenges* their work, not replaces it. Make multilingual + multi-tenant the default architecture, not the special case. Ship on Azure-native infra with strong DSGVO posture for European publishers, with MENA-first attention to RTL details, calendars, and editorial culture.

---

## Public surfaces

| Surface | URL | Role |
|---|---|---|
| **Marketing site** | [journalify.io](https://journalify.io) | Product story, pricing, contact |
| **Editorial app (newsroom)** | [cloud.journalify.app](https://cloud.journalify.app) | Where journalists & editors live |
| **Atlas admin (workspace)** | [atlas.journalify.app](https://atlas.journalify.app) | Tenant onboarding + ops |
| **Reader (public)** | [halo-Journalify-reader](https://github.com/journalify/halo-Journalify-reader) *(repo)* | Public-facing story reader |

## Open repos here

We're pre-MVP. Most platform repos are private during the build window — public surfaces ship as they harden:

- **`halo-Journalify-reader`** — the public reader SPA (React 19 / Vite / MUI 6). The audience-facing front door for any newsroom publishing via Journalify.
- *(more public repos coming as the platform stabilizes — currently in active development across ~12 private repos covering editorial, atlas, sage AI, infra, marketing)*

## Tech approach (in a paragraph)

FastAPI + PostgreSQL + Row-Level Security for the editorial backend. React 19 + Vite + MUI 6 + TypeScript strict on every SPA. Azure App Service + PgBouncer + APIM for the platform; Cloudflare for the edge. NewRelic for observability across the stack. Stripe for billing. Azure OpenAI (GPT-4o) for the AI assistant — token-quota controlled per tenant, never auto-publish. Terraform for infra-as-code. Multi-tenant via shared Postgres + RLS (not DB-per-tenant — locked architectural decision after benchmark).

## Where we're based

**Sherif Mohamed Investments UG (haftungsbeschränkt)**
Französische Straße 20, 10117 Berlin, Germany
HRB 268211 B · Amtsgericht Charlottenburg

Founder: Sherif Sayed Zaki Mohamed — building Journalify after a decade across newsroom tech.

## Get in touch

- **Product / sales:** [hello@journalify.io](mailto:hello@journalify.io)
- **Security disclosures:** [security@journalify.io](mailto:security@journalify.io)
- **Business:** [sherif.mohamed@journalify.io](mailto:sherif.mohamed@journalify.io)
- **Website:** [journalify.io](https://journalify.io)

## Status

Pre-revenue, pre-MVP launch (LG-01 target Q2-Q4 2026). Bootstrapped from Berlin with support from Microsoft for Startups Founders Hub. Actively shipping daily.

---

<div align="center">

*If you're an editor, a developer, or a newsroom CTO who cares about what publishing tooling should feel like in 2026 — say hello.*

</div>
