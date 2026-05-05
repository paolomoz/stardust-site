<!--
_provenance:
  writtenBy: stardust:direct
  writtenAt: 2026-05-04
  resolvedFromPhrase: "redesign digitalinnovation.com to look modern, competent and aligned with thechannelco brand" + clarification ("inherit color + typography only — Lato, #ed1c24, #003049 — build the rest fresh; keep dual-brand TCC + Microsoft Azure lockup")
  readArtifacts:
    - stardust/state.json
    - stardust/current/PRODUCT.md
    - stardust/current/DESIGN.md
    - stardust/current/_brand-extraction.json
    - stardust/brand-source.md
  stardustVersion: 0.3.0
-->

# Direction — digitalinnovation.com

## User phrase (verbatim)

> "redesign digitalinnovation.com to look modern, competent, and
> aligned with thechannelco brand"
>
> Clarification: "The Channel Company is the dominant brand, but we
> don't want to clone thechannelco.com design to the Azure site,
> just keep brand references (let's start with colors and typography).
> Tackle home page first, then 2 other templates."

## Restatement (dimensional vocabulary)

| Dimension | Value | Movement |
|---|---|---|
| register | `brand` | inherited from current site (B2B partner content destination) |
| expressive axis | `committed` | move from `restrained` (Bootstrap defaults) → `committed` (modern, deliberate) |
| tone | `serious` | pinned (B2B, partner-economics, "competent") |
| density | `balanced` | default for brand register; multi-audience hard floor caps `sectionPadding.desktop` at 40–64px |
| distinctiveness | `distinctive` | move from `familiar` (interchangeable Microsoft-partner-portal aesthetic) → `distinctive` (TCC-anchored, modern editorial-content) |
| audience | ISV + SI Azure partners | inherited; both tracks self-route from home |
| constraints | brand-source-aligned (palette + type from `brand-source.md`); IA-faithful | hard pins |

## Movements

- **expressive axis:** restrained → committed — the redesign has a clear point of view (Lato + red + dark blue + editorial composition) versus the current Bootstrap-default fadedness.
- **distinctiveness:** familiar → distinctive — the current site is interchangeable with hundreds of 2014-2020 Microsoft partner portals; the redesign is recognizably a TCC property at a glance.
- **density:** balanced (default; multi-audience hard floor active) — sectionPadding 64/48/32 desktop/tablet/mobile.
- **tone:** serious (pinned) — no playfulness, no decorative emoji, no "We're Excited to Share" intros.

## Mode resolution

Captured signal from `_brand-extraction.json`: **signal-strong**
(5 distinct colors, named family `SegoeUI`, scaleAudit `ad-hoc`).

Default per stardust direct: **Mode A (brand-faithful)**.

Override applied: **brand-source override.** The user explicitly
pinned palette and type to a different surface (`stardust/brand-source.md`,
TheChannelCo) rather than to the captured `_brand-extraction.json`.
This is non-canonical Mode A but preserves its spirit — palette and
type are pinned (not rolled), other axes resolved through standard
direction reasoning. Recorded in `DESIGN.json.extensions.divergence.brand_faithful_inversions[]`.

The redesign is **not** a rebrand:
- Audience preserved (ISV + SI Azure partners)
- IA preserved (categories, audience-routing nav, dual-brand header lockup)
- Content register preserved (B2B content destination)
- Voice register preserved (serious, partner-economics)

What changes is the visual identity inheritance source: from
Microsoft (current) to TCC (target).

## Anchor reference

**TheChannelCo (`thechannelco.com`)** as the visual identity parent.
Implied dimensions:
- **decade** = `2025-now`
- **ground-family** = `stark-white` (white background)
- **register** = `brand` (already pinned)
- **palette + type** = inherited verbatim (Lato; red `#ed1c24` primary, dark blue `#003049` secondary, full TCC palette per brand-source.md)

What is **not** inherited from TCC: layout language, density, voice
rhythm, component shapes, photography treatment, type scale (we
build a more generous scale on the same family).

## Divergence inputs (recorded for audit)

| Dimension | Value | Picked by |
|---|---|---|
| decade | 2025-now | anchor-reference: thechannelco.com |
| register | brand | user-constraint |
| craft | editorial-modern | rolled (consistent with content-publication site) |
| ground-family | stark-white | anchor-reference + brand-faithful: TCC uses #fff |
| font deck | brand-inherited (Lato) | user-constraint (brand-source.md) |
| palette | brand-source.md (TCC palette) | user-constraint |

## Anti-toolbox audit

| Concern | Verdict |
|---|---|
| Generic 2026 SaaS silhouette | guardrail active in components + DESIGN.md |
| Cyan/purple gradient SaaS hero | forbidden — primary accent is TCC red |
| Glassmorphism | forbidden |
| Dark-mode-by-reflex | forbidden — white ground |
| Editorial-register vocabulary on B2B brand | forbidden — voice is partner-economics, not literary |
| Editorial-airy spacing (96px+) | forbidden — multi-audience hard floor caps sectionPadding at 64px |
| Centered hero + dual-CTA template | forbidden — left-anchored editorial composition required |

## IA priorities (preserve in every variant)

1. **Audience routing** — ISV / SI partner CTAs above the fold on
   home; one-click reachable on every page.
2. **Publisher and sponsor provenance** — dual-brand TCC + Microsoft
   Azure header lockup in the first 100px of every page; "Powered by
   The Channel Company. Content sponsored by Microsoft." footer line
   preserved.
3. **Category-led IA** — 6 category routes (AI / Apps / Azure /
   Events / Migration / Partner Offers) reachable from every page.

## Plan (commands, in execution order)

1. ~~stardust:extract https://www.digitalinnovation.com~~ ✓ done — 12 pages crawled
2. ~~stardust:direct~~ ← **this step** (PRODUCT.md, DESIGN.md, DESIGN.json, home-improvements.md, direction.md, state.json updated)
3. **stardust:prototype home** (next) — render before/after, iterate via impeccable craft loop until approved
4. **stardust:prototype `<archetype-1>`** — likely `blog-fy26-investments` (article archetype) or `blog-index` (listing archetype)
5. **stardust:prototype `<archetype-2>`** — the other of the above pair
6. **stardust:migrate** — apply approved templates to remaining pages

## Pages affected

All 12 extracted pages move from `extracted` → `directed` (in scope of this direction).
Pages stale: none (this is the first direction).

## Resolved at

2026-05-04 — Mode A with brand-source override; 5-item home-improvements
list written; tokens authored against brand-source.md.
