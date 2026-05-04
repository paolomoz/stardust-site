<!-- stardust:provenance
  writtenBy: stardust:direct
  writtenAt: 2026-05-03T22:00:00Z
  readArtifacts:
    - stardust/state.json
    - stardust/current/_brand-extraction.json
    - stardust/current/PRODUCT.md
    - stardust/current/DESIGN.md
    - stardust/current/DESIGN.json
    - stardust/current/brand-review.html
    - stardust/prototypes/home-improvements.md
  synthesizedInputs: []
  stardustVersion: 0.3.0
-->
---
title: "follow the current NVIDIA design and apply improvements that preserve the current design principles"
resolvedAt: 2026-05-03T22:00:00Z
toolkitVersion: "v1.0 (stardust v0.3)"
schemaVersion: 1
---

# Active direction (2026-05-03T22:00:00Z)

## Phrase

> follow the current NVIDIA design and apply improvements that preserve the current design principles

## Restatement

A brand-faithful refresh of nvidia.com/en-us/. Type and palette are pinned to the captured surface. The brand identity (sharp 0px corners, NVIDIA green as the single CTA accent, two-surface dark/light alternation, sentence-case headings, proper-noun product naming) is preserved. Improvements target structural and system gaps surfaced by the brand-review's tensions: semantic landmarks, modular type scale, CTA verb consolidation, lazy-loaded mega-menu, single visible H1 per page. Density tier sits at packed (close to current execution). The 5-track audience IA, the routing-not-conversion CTA pattern, the news-density home hero, and the geo-locator banner are all preserved as IA priorities.

## Movements

- **brand-faithful** — `pinned` (palette + type both anchored to captured surface)
- **register** — `brand` (inherited from `current/PRODUCT.md`)
- **audience** — `5 tracks preserved` (gamer / enterprise / developer / creator / industry-buyer; constraint surfaced as IA priority)
- **distinctiveness** — `unchanged` (familiar within tech category — current site is recognizable as NVIDIA)
- **tone** — `unchanged` (technical-precise, authoritative, propulsive)
- **expressive** — `unchanged` (committed; carried by green + full-bleed dark sections)
- **density** — `unmoved by phrase` → `packed` (Q1 = b; sectionPadding 48/36/24px desktop/tablet/mobile)
- **decade** — `2025-now` (default)
- **constraints** — `brand-faithful (palette + type pinned)`, `WCAG 2.1 AA target` (newly declared), `8-verb CTA closed list`

## Gaps and questions

1. **Q:** Density tier — (a) balanced 64/48/32px (default), (b) packed 48/36/24px (closer to current execution).
   **A:** (b) packed.

2. **Q:** Mega-menu treatment — (a) preserve eager render (current pattern), (b) lazy-load on hover (perf win, slight SEO/discoverability cost), (c) progressive disclosure with restructured tile counts (deeper IA refactor).
   **A:** (b) lazy-load on hover.

## Anchor references

- (none stated; brand-faithful mode anchors on captured surface itself rather than external references)

## Anti-references

Inherited from `current/PRODUCT.md` and reinforced for the target:

- Friendly / "humanized" tech voice (Mailchimp, Slack marketing, Notion)
- Soft pastel / muted palettes (Linear, Stripe)
- Rounded, bubbly UI (consumer SaaS — agent-default reflex inverted; see `DESIGN.json § extensions.divergence.brand_faithful_inversions[]`)
- Single-product hero / minimalism (Apple)
- Editorial / magazine layout (The Verge, Stripe Press)
- **Generic-2026-SaaS silhouette** (toolkit § 1) — gradient-text headlines, glassmorphism cards, side-stripe accents, "modern" rounded everything. Explicitly guardrailed because "apply improvements" is a common AI-default trigger for the SaaS template silhouette.
- **Editorial-register vocabulary** (toolkit § 1) — `atelier`, `the studio`, `journal`, `mise-en-place`. The brand register is product/commerce/platform; editorial vocabulary applied to NVIDIA reads as misplaced.

## Divergence inputs

- **mode** — Mode A (brand-faithful)
- **mode reason** — captured signal is `signal-strong` (palette has 8 distinct colors; type families NVIDIA-NALA + Arial fallback are named) AND user phrase contains explicit pin-language ("follow the current NVIDIA design", "preserve the current design principles")
- **seed** — Mode A skips the standard 4-dimension seed roll. Non-locked dimensions resolved as:
  - **decade**: `2025-now` (default)
  - **register**: `brand` (inherited from `current/PRODUCT.md`)
  - **ground-family**: `stark-white` AND `stark-black` (override fired — captured palette has both `#ffffff` and `#000000` as canonical grounds; brand wins per Mode C)
- **font deck** — `brand-inherited` (`NVIDIA-NALA, Arial, Helvetica, sans-serif`); picked_by `user-constraint`
- **palette** — inherited from `_brand-extraction.json`; picked_by `user-constraint`
- **anti-toolbox audit** — 2 hits (Sticky top navigation, Pure black + pure white retention), both justified per brand-faithful direction
- **brand-faithful inversions** — 5 emitted (pure-white retention, pure-black retention, hex format retention, sharp 0px corner retention, saturated color retention). See `DESIGN.json § extensions.divergence.brand_faithful_inversions[]` for the full audit.

## Improvements list (Mode A — load-bearing for variant A)

Wrote `stardust/prototypes/home-improvements.md` (5 home-specific items). Site-wide system improvements (modular scale, CTA taxonomy, semantic landmarks, lazy mega-menu, named rules) live in `DESIGN.md` and apply uniformly to every prototyped page.

Summary of the 5 home-specific items:

1. **[a11y-structural]** Render `<main>` and `<footer>` semantically on home (currently both rendered as `<div>`).
2. **[a11y-headings]** Visible 48px headline becomes the H1; remove the 15px hidden-H1 SEO scaffold.
3. **[ia-hero-overload]** Reduce home hero from 8+ auto-rotating slides to 1 anchor slide + 4-tile rail (no auto-rotate; satisfies WCAG 2.2.2).
4. **[cta-verb-fragmentation]** Map home's 9 distinct CTA verbs to the 8-verb canonical taxonomy.
5. **[chrome-mega-menu-eager]** Lazy-load mega-menu tab content per Q2(b); ship skeleton + tab labels in initial HTML only.

## IA-priority preservation audit

Five `extensions.iaPriorities[]` entries written to `DESIGN.json`. Each is a constraint downstream `prototype` and `migrate` must honor — variants whose page shape briefs omit any preserved priority fail the audit.

| signal | preserveAs | scope |
|---|---|---|
| audience-routing (5-tab nav) | header-prominent | site-wide |
| commercial-conversion (See Buying Options on product pages) | first-viewport | product templates |
| news-announcement-density (carousel hero) | hero (sharpened to 1 anchor + 4 rail) | home |
| developer-routing (For You tab) | header-prominent | site-wide |
| geo-locale-routing (geo-locator banner) | site-wide complementary | site-wide |

## Command sequence (proposed)

1. `$stardust direct` (this command — wrote PRODUCT.md, DESIGN.md, DESIGN.json, direction.md, home-improvements.md)
2. `$stardust prototype home` — render variant A of home (faithful + 5 improvements applied) for review
3. `$stardust prototype <next-slug>` — when home is approved, prototype the next page (likely `data-center` or `geforce-rtx-50` as audience-hub representatives)
4. `$stardust migrate` — apply approved direction across all 40 extracted pages

Variant fork (Phase 2.6) was not triggered — user's phrase did not request multiple variants. Single variant A per page is the default.

## User confirmation

> "Q1 b - Q2 b" (interpreted as: density = packed, mega-menu = lazy-load on hover; full plan implicitly accepted)

## Pages in scope

All 40 pages currently marked `extracted` in `state.json`:

`home, about-nvidia, foundation, sustainability, ai, data-center, geforce, studio, omniverse, geforce-graphics-cards, geforce-rtx-50, geforce-rtx-5090, data-center-dgx-gb300, data-center-gb300-nvl72, networking, shield, geforce-now, products, solutions-ai, solutions-autonomous-vehicles, industries-healthcare, industries, use-cases, use-case-medical-imaging, case-studies, case-study-serve-robotics, software, software-nvidia-app, ngc, glossary, glossary-generative-physical-ai, research, events, training, support, contact, geforce-news, autonomous-machines, edge-computing, high-performance-computing`

All 40 transition `extracted → directed` after this run.
