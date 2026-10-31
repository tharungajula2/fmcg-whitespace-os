# FMCG Whitespace OS

**An interactive FMCG strategy study, built as a product management portfolio prototype.**

The project explores how a better-for-you product idea might move from consumer occasion to product positioning, channel fit, repeat behavior and unit economics. It packages that reasoning as a five-concept Product Lab and a navigable research workbook.

> **Maturity:** exploratory portfolio work. The concepts and recommendations are hypotheses. The quick-commerce dashboard and its “AI agent” use simulated, hard-coded scenarios; the repository does not establish market demand, product performance, customer traction or validated whitespace.

## Explore the implementation

| Area | What it contains | Source |
|---|---|---|
| Home | Thesis, product-story entry points and portfolio framing | [Home page](app/page.tsx) |
| Product Lab | Five beverage concept profiles with occasion, role, repeat and channel hypotheses | [Page](app/products/page.tsx) · [product registry](app/data/products.ts) |
| How I Can Help | Proposed PM and growth contribution areas | [Page](app/how-i-can-help/page.tsx) |
| Research WIP | Ten selectable chapters covering raw notes, simulated channel intelligence, flavor concepts, supply chain, consumer, economics, positioning and open risks | [Workbook](app/research-wip/ResearchWipClient.tsx) · [chapter data](app/data/research-wip-data.ts) |
| Project Blueprint | Complete source-grounded manual, methods, formulas and caveats | [Read the blueprint](PROJECT_BLUEPRINT.md) |

The workbook allows notes on its editorial chapters and saves them to this browser's `localStorage`. The channel console offers tab, zone, keyword and scenario switches, but its displayed metrics are example values, not live observations.

## What the analysis actually does

The strategic method is a **structured qualitative reading**: define a consumption occasion, propose a product role and message, consider repeat and channel fit, then list economics and risks that would need validation. These are useful product questions, not a computed opportunity score or measured market study.

The unit-economics chapter displays an illustrative P&L waterfall and quick-commerce fee ranges. The numbers are authored table values; there is no calculator, transaction dataset, cohort model or external data pipeline. The [blueprint](PROJECT_BLUEPRINT.md#unit-economics-auditing-the-example) works through the displayed arithmetic and identifies values that need reconciliation.

## Stack and architecture

| Layer | Implementation |
|---|---|
| Web app | Next.js 16 App Router, React 19, TypeScript |
| Styling and motion | Tailwind CSS 4, CSS tokens, GSAP in editorial chapter transitions |
| Content | Typed local modules in `app/data/` and static assets in `public/` |
| State | React component state; browser `localStorage` for workbook notes |
| Services | No application API, database, authentication or live commerce/analytics integration |

## Run locally

```bash
git clone https://github.com/tharungajula2/fmcg-whitespace-os.git
cd fmcg-whitespace-os
npm install
npm run dev
```

Open the localhost URL printed by Next.js. The package also defines `build`, `start` and `lint`; it defines no test script. No application-specific environment variable is required for local use. `NEXT_PUBLIC_SITE_URL` is optional metadata configuration.

## Boundaries

- The five product profiles are concept profiles. Their strategic weights, risk labels and repeat potential are authored judgments, not outputs of a scoring model.
- The workbook includes unverified market, nutrition, competitive price and retention claims. Treat them as prompts for research, not established results.
- The channel console's sample stock, zone and keyword signals are internally fixed; its timed briefing does not call an AI service.
- The displayed economics contain arithmetic gaps. The blueprint shows the exact inputs and discrepancies.
- An unused password form exists in source, but the workbook is open and has no access control.

The older [SOURCE_OF_TRUTH.md](SOURCE_OF_TRUTH.md) is preserved as historical design and research context. This README and the [Project Blueprint](PROJECT_BLUEPRINT.md) describe the current implementation.
