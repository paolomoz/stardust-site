<!-- stardust:provenance
  writtenBy: stardust:direct
  writtenAt: 2026-04-30T09:00:00Z
  readArtifacts:
    - stardust/state.json
    - stardust/current/_brand-extraction.json
    - stardust/current/PRODUCT.md
    - stardust/current/DESIGN.md
    - stardust/current/DESIGN.json
    - stardust/current/brand-review.html
    - stardust/current/pages/home.json
    - stardust/current/pages/about-us.json
    - stardust/current/pages/sactionals.json
  synthesizedInputs: []
  stardustVersion: 0.2.0
-->
---
title: "Refresh the existing brand. Fix the chrome clutter and type-scale drift. Amplify the captured modular-system / Designed For Life story."
resolvedAt: 2026-04-30T09:00:00Z
toolkitVersion: "v1.0 (stardust v2)"
schemaVersion: 1
variantMode: multi
variants: [A, B, C, B1, B2]
---

# Active direction (2026-04-30T09:00:00Z)

## Phrase

> Refresh the existing brand. Fix the chrome clutter and type-scale
> drift. Amplify the captured modular-system / Designed For Life
> story — make the kit-of-parts visible. 3 variants.

## Restatement

Mode A brand-faithful refresh of the captured Lovesac surface. The
captured signal is **signal-strong** (8 palette colors with a real
saturated brand teal `#0098a7`, two named type families Miller
Display + Museo Sans, an 85-token CSS-vars system, distinctive
brand vocabulary). The phrase moves *expressive* (committed →
distinctive at variant level), *distinctiveness* (familiar →
distinctive), *tone* (slightly less corporate / more material), and
explicitly pins the IA priority and the "Designed For Life"
narrative. Density resolves to `balanced` (default for brand-
register multi-audience commerce home; hard floor applies — 8-item
audience router, configurator conversion path, 7+ sections on
captured home). Three variants requested → multi-variant fork
applies; variant role contract enforced.

## Movements

- **register** — `brand` (inherited from current PRODUCT.md)
- **expressive axis** — `restrained` (captured) → `committed`
  across all variants; `distinctive` at variant B and C structural
  level
- **tone** — `aspirational` (captured) → `aspirational + material`
  (the kit / heritage substrate the captured copy promises but the
  layout never delivers)
- **density** — `balanced (default)` — phrase did not move the
  axis; brand-register multi-audience hard floor applies (≤ 64px /
  ≥ 40px sectionPadding.desktop; variant B uses 56px, variants A
  and C use 64px; all within bounds)
- **distinctiveness** — `familiar` (captured surface reads as
  premium-furniture-typical) → `distinctive` for variant B (kit-
  bracket motif) and variant C (year-rule motif); variant A stays
  `familiar` by role contract
- **audience** — preserved tuple (first-time furniture buyers /
  existing Sactional owners / lifestyle browsers) per Mode A IA-
  priority preservation
- **constraints** — `brand-faithful` (Mode A active), commercial-
  conversion preservation, audience-routing preservation, trust-
  band preservation
- **multi-variant** — N=3, role-differentiated per Phase 2.6

## Gaps and questions

None — the phrase carried explicit anchors:

- "Refresh the existing brand" → Mode A by default
- "Fix the chrome clutter and type-scale drift" → improvements list
  (items 1, 2, 4, 5)
- "Amplify the captured modular-system / Designed For Life story"
  → variant B (kit-of-parts) + variant C (longevity)
- "Make the kit-of-parts visible" → variant B amplification target
- "3 variants" → multi-variant fork; A is faithful by role contract

Density was defaulted (`balanced`) per the one-shot rule (phrase
did not move the axis; brand register multi-audience triggers
the hard floor). Stamped `density: balanced (default)` here.

## Anchor references

- (none) — phrase carried no external references; amplifications
  are sourced from the captured surface only

## Anti-references

- The Generic-2026-SaaS silhouette (toolkit § 1) — explicitly
  guardrailed because "modernise" is the most common AI-default
  trigger for it, especially on variant A.
- Editorial-register vocabulary applied to a commerce/configurator
  brand. Lovesac is product-commerce + lifestyle, not editorial.
- Hero text on photographic background without contrast scrim
  (toolkit universal hardening).
- "Archival editorial palette" (cream/paper ground + warm-saturated
  accent + muted earth-tone secondary) — guardrail flagged on
  variant C because "longevity / heritage" is the strongest pull
  toward this default.
- Coordinate / lat-long / serial metadata stamps — adjacent to
  variant B's brackets and variant C's year labels; refused on both.
- Stat-callout bar (Stripe-press silhouette) — flagged across all
  variants.

## Divergence inputs

- **mode** — A (brand-faithful) on all three variants. `--rebrand`
  not passed; signal-strong; phrase contains no rebrand triggers.
- **seed** — `Lovesac|2026-04-30` MD5 →
  `2025-now × Tailor's pattern paper × Catalogue × stark-white`
- **picked_by** — deterministic
- **ground_family override** — `brand-faithful` (captured ground
  is `#ffffff` stark-white; seed roll happened to agree, no
  override needed)
- **font deck** — `brand-inherited` (Miller Display + Museo Sans
  preserved verbatim; deck dimension is inert per Mode A)
- **palette** — `inherited from _brand-extraction.json`. No palette-
  picker invocation. Role-renaming applied: `accent-1` → `primary-
  dark` (semantic), `border` (single-context) → `reviews-tint`
  (reserved). The token vocabulary is brand-native by category —
  these aren't generic role names.
- **anti-toolbox audit** — 0 hits across all three variants. Variant
  B and C carry off-toolbox moves with brand-specific
  justifications:
    - B: bracket motif (justified by Sactionals' literal corner-
      bracket physical assembly), exploded-view hero, 12-col grid
      with 6/4/3 splits
    - C: year-rule motif, chronological heritage strip,
      sections sequenced by launch year
- **brand-faithful inversions** — six emitted on each variant:
  pure-white retention, pure-black retention, hex format
  retention, sharp 0px corner retention, saturated color retention,
  reserved-color (`#c4dee0` for reviews/customer-gallery only)

### Variant resolutions

| Slot | Role | Captured trait amplified | Differentiators (vs. previous) |
|---|---|---|---|
| **A** | Faithful + improvements | None — the role is *not* to amplify | baseline |
| **B** | One captured trait amplified | Modular kit-of-parts (spatial grammar) | section sequence: exploded-view hero replaces carousel-leading hero (≠ A); section presence: configuration-grid layout primitive added (≠ A); IA priority: configurator promoted to first affordance (≠ A) → **3 changes** |
| **C** | Different captured trait amplified | Designed-For-Life longevity / heritage timeline (temporal grammar) | section sequence: sections sequenced by product launch year (≠ B's spatial sequencing; ≠ A's captured order); section presence: heritage-strip + year-rule absent in A and B (≠ both); layout strategy: single-frame hero replaces carousel-leading composition (≠ A); IA priority: heritage-narrative trigger added that A and B do not carry (≠ both) → **4 changes vs. A, 3 changes vs. B** |

Differentiation contract (≥ 2 substantive changes per pair):

- **A ↔ B:** ≥ 3 changes (hero strategy, layout primitive, IA
  priority promotion). PASS.
- **A ↔ C:** ≥ 4 changes (hero strategy, section sequence by year,
  heritage-strip presence, IA priority addition). PASS.
- **B ↔ C:** ≥ 3 changes (different motif — bracket vs. year-rule;
  different grammar — spatial vs. temporal; different hero — exploded-
  view kit vs. single-frame photographic; different IA-priority
  addition — modular-kit-affordance vs. heritage-narrative). PASS.

C-cliff audit: variant C amplifies a different trait than B (temporal
not spatial), declares the trait + brand-personality move it serves,
is not "B but more," is not a slider position pushed past B, and is
not editorial-register cosplay (vocabulary explicitly banned, palette
explicitly resists archival-editorial pull). PASS.

## Anti-toolbox audit (resolved direction)

Run on the resolved direction across all three variants:

- **Sticky top navigation** — present in captured site (header-
  wrapper + header--visible classes); preserved per Mode A. Justified
  by inherited site convention.
- **Stat-callout bar** — guardrailed (anti-ref).
- **Generic-2026-SaaS silhouette** — guardrailed (anti-ref).
- **Hero text on photographic background without contrast scrim** —
  guardrailed (a11y rule in PRODUCT.md).
- **Editorial-register vocabulary** — guardrailed (anti-ref).
- **Triplet-cadence pull-quote** — flagged on variant C (longevity
  pull); refused.
- **Coordinate / serial / archival stamps** — flagged on variants B
  and C; refused.

`anti_toolbox_count = 0` (preserved-from-captured items don't count
against the budget under Mode A; the audit lives in
`brand_faithful_inversions[]`).

## Improvements list

Authored at `stardust/prototypes/home-improvements.md` per Phase
2.5 (Mode A only). 7 specific weaknesses meeting the specificity
bar (≥ 3 required, well above floor). Variant A's brief is this
list; variants B and C honor every item as a floor.

## Command sequence (proposed)

This `direct` run wrote PRODUCT.md, DESIGN-{A,B,C}.{md,json}, the
improvements list, and this direction file. Downstream:

1. `$stardust prototype home` — produce `home-shape.md` per variant
   and three rendered before/after viewers (`home-A.html`,
   `home-B.html`, `home-C.html`). Phase 1 of prototype reads each
   DESIGN-{A,B,C} pair and the home-improvements list to compose
   the per-variant page-shape brief.
2. `$stardust prototype sactionals` — variant B's exploded-view
   hero is most legible on this slug; produce comparable variant
   set.
3. `$impeccable critique` — verify the move landed without slop on
   each variant.
4. (User picks) one of the variants to be the canon authority via
   `$stardust prototype --prep`.
5. `$stardust migrate` — apply approved variant to the rest of the
   inventory.

## User confirmation

> "go" (implicit — the operator passed the phrase + multi-variant
> count + per-variant trait targets directly; no clarifying
> questions remained)

## Pages in scope

- `home`, `sactionals`, `sacs`, `about-us`, `inspiration` — all 5
  pages currently in `extracted` status. State transitions to
  `directed` on each.

## Creative iterations on variant B (B1, B2)

Appended 2026-04-30T12:50:00Z. B1 and B2 are creative pushes from
variant B — **not replacements**. They explore different axes of
the same captured trait (Lovesac's modular Sactionals kit-of-parts).
Variant B (the original) is preserved unchanged; A and C are also
preserved unchanged.

| Slot | Parent | Captured trait amplified | Axis rotated to | Off-toolbox moves |
|---|---|---|---|---|
| **B1** | B | Same trait — modular kit-of-parts | INTERACTION (verb-led, system-as-operated). The configurator IS the homepage. | live state-driven configurator hero (vanilla JS); bracket-snap micro-animation; footprint-grid canvas (88px cells); click-to-load Rooms Others Built gallery |
| **B2** | B | Same trait — modular kit-of-parts | DOCUMENTATION (noun-with-data, system-as-engineered). Vitra meets Apple. | inline-SVG line-art overlays on captured photos (1px stroke); bill-of-materials pricing typography; dimension-line section dividers; mono caption annotations on every spec |

Both inherit Mode A brand-faithful posture, the same density floor
(B1 at 56px, B2 at 64px sectionPadding.desktop), the same brand-
faithful inversions, and the same anti-toolbox guardrails as B. The
amplification axis is the only thing rotated.

Differentiation contract — same captured trait, distinct
amplifications:

- **B ↔ B1:** ≥ 3 changes (hero is interactive not static; carousel
  removed; gallery wired to load presets into hero state). PASS.
- **B ↔ B2:** ≥ 3 changes (hero is line-art over scrim'd photo;
  pricing is BOM not callout; dimension-line dividers replace
  margins; carousel removed). PASS.
- **B1 ↔ B2:** ≥ 4 changes (interaction vs. documentation register;
  vanilla JS vs. inline SVG; verb-led copy vs. mono spec captions;
  configurator canvas vs. dimensioned photographs). PASS.

C-cliff audit: B1 and B2 amplify the same captured trait as B but
on different axes (interaction / documentation), declare the
trait + axis they serve, are not "B but more," and carry distinct
off-toolbox moves with brand-specific justifications. Both PASS.

### Pages in scope (B1, B2)

- `home` only. Sactionals, Sacs, About-us, Inspiration are not
  prototyped under B1 / B2 in this iteration.

## Variant selection (canonical)

Variant B (kit-of-parts amplified, spatial grammar) approved as canonical on 2026-04-30. A, B1, B2, C archived on disk for reference. Project-root `DESIGN.md` and `DESIGN.json` now mirror `DESIGN-B.{md,json}` and are the authority migrate consumed.


## Corrective re-cascade (2026-04-30 PM)

The prior cascade (direct --prep -> prototype --prep -> migrate) was contaminated: 20 of 25 pages had been synthesized rather than live-crawled. Extract was corrected first (24 pages now have valid Playwright provenance: renderedBy=playwright, waitMs in [3764, 4431], waitMode=medium across all 24). 1 page (`quote-lookup`) is permanently dropped from inventory — `state.json` flags it `failed` with `errorClass: HTTPError` because the URL does not exist on lovesac.com.

Phases re-run today against the real extract:

- **direct --prep** — type catalog auto-confirmed (7 types, 24 pages: landing 1, listing 8, program 6, static 5, unique 2, article 1, form 1). Module-candidate frequencies re-derived from real per-page DOM scans (main-content text + components.{accordions,breadcrumbs,tables}.count). Promoted 9 modules to `confirmed`: `breadcrumb` (15), `financing-band` (10), `customer-gallery-strip` (5), `reviews-band` (5), `faq-accordion` (3), `designed-for-life-band` (2), `comparison-table` (2), `swatch-cta` (1), `help-cta` (1). Color reservations carried forward unchanged (#c4dee0 -> reviews/customer-gallery; #0098a7 -> button-primary/link/focus). Direction re-eval: no change — wider crawl confirms register, IA priorities, anti-references.

- **prototype --prep** — canon files retained where intact (canon.css, header.html, footer.html), with header + footer purged of `quote-lookup` links. Per-type templates collapsed into a single real-data-driven renderer (`stardust/canon/templates/render-pages.mjs`) since the prior `pages.json` archetype objects contained synthesized review quotes ("Marisol, Chicago" etc.). The renderer consumes per-page JSON only.

- **assets prep** — 592 media files copied current -> migrated. `assets/logo.svg` stamped from the captured icon-mark SVG (wordmark-gap retained as dashed-outline placeholder per A/B/C convention). `assets/canon.css` mirrored.

- **migrate** — 24 pages rendered, status table written to state.json. quote-lookup excluded. Internal links: 0 real `/quote-lookup` references in any rendered page (the 24 raw matches are inside `<!-- stardust:provenance -->` comments only). Color-reservation enforcement: 0 violations. Anti-toolbox audit: PASS on all 24 pages (no fabricated quote attributions, no editorial vocabulary, no missing alt on content imagery).

The migrated site is the authority going forward. Per-page provenance comments name the per-page JSON consumed.
