# trustflux-landing

Company site for Trustflux Ltd at [trustflux.co.uk](https://trustflux.co.uk). Static HTML, no build step, deployed via GitHub Pages (CNAME in repo root).

## SEO keyword strategy (researched Aug 2026)

The page targets four keyword clusters, chosen from SERP research because they are (a) rising, (b) match real credentials, and (c) winnable by an individual practitioner. Bare stack terms ("React contractor") were deliberately demoted to body copy: those SERPs are owned by job boards and demand is flat or declining, while Azure contract demand grew ~74% YoY.

### Primary clusters (one section each on the page)

1. **Technology / AI due diligence** - "AI due diligence" has split intent (assessing AI companies vs using AI for DD); the assessment side is underserved. The "is the AI real or a wrapper" question is voiced by VCs but no UK practitioner owns the commercial answer. Long-tails: "AI due diligence checklist for investors", "technical due diligence of AI products", "agentic AI risk assessment for investors", "sell-side technology due diligence".
2. **Fractional CTO (fintech, London, outside IR35)** - fractional demand rising 40-68% YoY while advertised CTO contracts collapse (the market moved from job boards to search). Individuals demonstrably rank (fractionalcto.london, fracto.london). Gaps owned by nobody: "outside IR35 fractional CTO", "fractional CTO fintech UK", pricing-transparency pages.
3. **Agentic AI for regulated businesses** - strongest tailwind: EU AI Act high-risk obligations enforceable from 2 Aug 2026, FCA AI Live Testing running, OWASP Agentic Top 10 (Dec 2025). Every ranker is a tool vendor, GRC firm, or content farm; none can claim shipped-in-production regulated experience. Long-tails: "AI agent audit trail", "how to audit AI agents", "AI agent observability regulated industries", "agentic AI governance framework", "AI agent security review", "Claude Code consultant" (early land-grab).
4. **Azure architecture and cost review** - Azure is the fastest-rising UK contract skill; "Azure cost optimization consultant" SERP has zero independents (only enterprise partners charging $25k-60k per assessment). The open-source azure-costs-analyzer is the linkable asset none of them have. Long-tails: "Azure cost optimization consultant UK", "Azure FinOps consultant", "Azure event-driven architecture consultant".

### Stack keywords (secondary, in body copy only)

React, Next.js, Node.js, NestJS, TypeScript, GraphQL, FIX protocol - woven into the delivery section with fintech/trading qualifiers ("fintech React and Node.js contractor London", "trading platform React developer" are the winnable combinations). Never as headlines.

### Roadmap (highest-ROI next steps, in order)

1. **Publish real pricing.** Every ranking UK fractional-CTO page leads with concrete rates (£800-£2,000/day, £3k-£7k/month benchmarks). A dedicated pricing/engagement page with actual numbers is the single highest-conversion addition.
2. **Split into service pages** once content exists to support them: `/technology-due-diligence`, `/fractional-cto-london`, `/azure-cost-review`, `/agentic-ai`. Separate URLs rank better for their clusters than anchors on one page.
3. **Checklist lead magnets.** Every DD SERP is dominated by checklist pages with downloads: "AI due diligence checklist" is the obvious first one.
4. **Blog stays on nakrosis.com; cross-link both ways.** Articles targeting the informational long-tails (how to audit AI agents, EU AI Act logging for fintech, FCA AI Live Testing, is-the-AI-real) should link to the relevant trustflux.co.uk service section, and vice versa.
5. **Year-stamp and refresh annually.** Ranking pages in these niches all carry "(2026)"-style freshness in titles and update yearly.
6. **Google Search Console + Bing Webmaster Tools**: verify the domain, submit sitemap.xml, monitor which queries actually land.

## Selected work section

Screenshots live in `img/` (captured Aug 2026 from the live sites, except intick.jpg and halved.jpg which are product screenshots supplied by Mindaugas).

Note: Expana was delivered through Trustflux by a different contract engineer (not Mindaugas) - keep its blurb worded accordingly.

## Editing notes

- Single-file page: all CSS inline in `index.html`, no external dependencies.
- British English, no em dashes (use "-"), no emojis, no hype language.
- Keep title/meta description in sync with positioning changes; JSON-LD (ProfessionalService + founder Person) at top of `index.html`.
- `sitemap.xml` lastmod should be bumped when content changes.
