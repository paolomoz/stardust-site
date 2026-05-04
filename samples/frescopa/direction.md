<!-- stardust:provenance
  writtenBy: stardust:direct
  writtenAt: 2026-04-30T11:30:00Z
  readArtifacts:
    - stardust/current/_brand-extraction.json
    - stardust/current/PRODUCT.md
    - stardust/current/DESIGN.md
    - stardust/state.json
  synthesizedInputs:
    - user freeform intent (master skill input)
    - clarifying-question answers (Q1: variant references, Q2: scope=full-site)
    - mode-detection precedence outcome
    - per-variant divergence-toolkit resolutions
  stardustVersion: 0.2.0
-->
---

# Direction — Frescopa redesign (resolved 2026-04-30)

## Phrase

> "Redesign of https://frescopa.coffee/ — white label demo site built by non-designers / non-coffee-marketing experts. Stunning reskin. Pin some colors. Reuse images except banner backgrounds (drop or Gemini-regenerate). Two parallel directions: A=saxbys-led with foxyloxy + myblackbird; B=barninela-led with bluebottle + marinacafe."

## Restatement (dimensional vocabulary)

```
register:        brand                                        (inherited from extracted PRODUCT.md)
expressive:      restrained → committed                       (the references all sit committed-to-drenched)
distinctiveness: familiar → distinctive                       (white-label demo → has a point of view)
tone:            warm-with-conviction (per-variant tonal axis)  
density:         balanced (default for brand register; multi-audience hard floor caps at ≤64px)
audience:        coffee drinkers — B2C primary, B2B secondary, editorial supporting
constraints:
  brand-faithful (partial)         — pin teal #00647D + wine #58181D
  legacy-content-preserved (partial) — reuse images except home banner backgrounds
  no-cream-ground                  — coffee is not paper; cream as ground requires print-paper-category justification (none here)
  no-fabricated-content            — invented stats / customer logos / dates banned across variants
```

## Movement

| Dimension | Direction | Source |
|---|---|---|
| register | brand (unchanged) | inherited from current/PRODUCT.md |
| expressive axis | restrained → committed | "stunning" + reference set |
| distinctiveness | familiar → distinctive | "stunning" + brand-with-a-point-of-view shift |
| tone | per-variant (A: characterful warm; B: refined restrained) | per-variant declared |
| density | balanced (default; multi-audience hard floor) | density tuning question skipped (user said "go with your recommendations"); brand-register multi-audience site (15 pages, B2C+B2B+editorial+subscription tracks) → trigger condition fired → cap at ≤64px desktop, default balanced (64/48/32) |
| distinctiveness — variant A | distinctive | committed-to-distinctive territory |
| distinctiveness — variant B | distinctive (saturated-substrate move pushes toward singular) | the saturated-teal-ground move is the singular gesture |
| audience | resolved tuple (preserved from current PRODUCT.md) | extracted brand surface + user input |

## Gaps and clarifying questions

The master skill asked two clarifying questions before delegating to direct:

**Q1 (asked at master level): Anchor reference per variant, vs blend.**
- A: saxbys as primary, foxyloxy + myblackbird as partners
- B: barninela as primary, bluebottle + marinacafe as partners

**Q2 (asked at master level): Scope.**
- B: full multi-page redesign at page cap ~15

The follow-up density-tuning question (asked once when phrase doesn't move density) was deferred — the user replied "go on direct with your recommendations" after extract completed. Default applied: balanced (64px desktop) — within bounds for this multi-audience site.

## Mode detection

Captured brand signal classification: **`signal-strong`**
- Palette has 8 entries (≥3 distinct after clustering, excluding pure black/white)
- `type.headingFamily.name = "Baskerville"` (named)
- `type.bodyFamily.name = "Roboto"` (named)
→ Mode A (brand-faithful) is the default.

Mode-detection precedence outcome: **Mode A active** (no rebrand triggers in phrase, `--rebrand` flag not passed). Mode B (anchor-reference precedence) composes — the user provided per-variant anchor references that imply seed dimensions.

The phrase contains "creatively rethought" (about the non-pinned colors) and "creatively rethought" + a pinned-color carve-out matches the failure-mode-c shape (Hard rule conflict — keep brand and change palette). Resolved as failure-mode-c option (c) — **Mode A with a targeted palette move**: 2 colors pinned (teal + wine), the rest open. Type is also open (the user said "rest can be creatively rethought"; the captured type stack — Baskerville + Roboto — is not pinned).

## Resolved direction per variant

### Variant A — "Frescopa, Refreshed"

**Role:** faithful + improvements (every item from `home-improvements.md` applied; no embellishment).

**Tagline:** Contemporary-collegiate coffee retail with indie-cafe warmth.

**Anchor references → implied seed dimensions:**
- saxbyscoffee.com → decade=2025-now, ground=stark-white, register=retail-confident
- foxyloxycafe.com → craft=handmade-signwriter, register=indie-cafe (signage thread)
- myblackbirdcafe.com → editorial-typography thread (Cormorant Garamond on long-form)

**Resolved seed:**
- decade: `2025-now` (anchor-implied)
- craft: `handmade-signwriter` (anchor-implied: foxyloxy)
- register: `tabloid-cafe` (deterministic — anchor-implied retail-cafe)
- ground-family: `stark-white` (anchor-implied + brand-faithful override per Mode C — Frescopa's body bg is white)

**Font deck:** `serif-luxury` (DM Serif Display + Cormorant Garamond + IBM Plex Sans)
**Off-deck additions (justified):**
- `Caveat` from `handmade-signwriter` deck — for foxyloxy hand-drawn signage thread, ≤2 instances/page, eyebrow position only
- `JetBrains Mono` from `tactile-humanist` deck — for catalog/numeric register

**Palette move:** `Mode A targeted` — 2 anchors pinned (Bay teal #00647D, Roast wine #58181D), coral kept-and-evolved as Cherry, Crema-Pale alt-surface (passes deterministic non-cream test), maroon + amber dropped.

**Type scale:** 1.333 (perfect-fourth) — retail-confident drama.

**Voice:** energetic 2nd-person, ≤1 exclamation per first viewport, mixed-case headings.

### Variant B — "Frescopa, Espresso Bar"

**Role:** one captured trait amplified — the coffee-shop-as-third-place register the captured site under-deploys, rendered as saturated-teal "espresso bar" surfacing.

**Tagline:** Refined modern-geometric specialty coffee.

**Amplified captured trait:** Frescopa's existing brand uses teal across promo-strip + footer + CTA bands (~15-20% of any page surface). The site under-deploys this color — it sits in chrome but never owns the brand's substrate. Variant B inverts the relationship — teal is now the page substrate, content surfaces (Porcelain) sit on top.

**Brand-personality move from PRODUCT.md served:** the *coffee-shop-as-third-place* personality trait — Frescopa as a place with a wall color, not just a catalog. Bluebottle does this with their blue; Stumptown does it with their red; Frescopa-B owns its teal.

**Anchor references → implied seed dimensions:**
- barninela.com → decade=2025-now, craft=technical-illustration, type=geometric-sans
- bluebottlecoffee.com → register=specialty-coffee-restraint, type=editorial-serif counterpoint
- marinacafe.com → register=coastal-elegant, editorial-thread

**Resolved seed:**
- decade: `2025-now` (anchor-implied)
- craft: `technical-illustration` (anchor-implied: barninela + bluebottle)
- register: `museum-didactic / catalogue` (anchor-implied: bluebottle + marina specialty-coffee restraint)
- ground-family: `saturated` — **direction-driven override**

**Ground-family override rationale:** All three anchors (barninela, bluebottle, marina) lean cream/paper-warm in their actual execution. Adopting cream would produce a defensible-but-cliche specialty-coffee result AND would hit the toolkit's most-flagged convergence move. Saturated teal as ground is variant B's defining move — escapes the cream default AND amplifies Frescopa's pinned brand color into substrate role. The toolkit's `ground_family: saturated` option exists for exactly this case ("the brand's saturated color as the page ground").

**Font deck:** `bauhaus-functional` (Space Grotesk + Roboto-Slab-rejected + Martian Mono)
**Deck substitution (justified):**
- Roboto Slab (deck default serif partner) → rejected (overshoots into agricultural-machinery register for specialty-coffee positioning)
- Cormorant Garamond + IBM Plex Sans → substituted for serif-display + body

**Off-deck additions (justified):**
- `Cormorant Garamond` from `serif-luxury` deck — for editorial display on Porcelain pages (bluebottle/marina anchor thread)
- `IBM Plex Sans` from `bureaucratic` deck (sans-cousin) — body type. Same rationale as variant A; reused for cross-variant body unity.

**Palette move:** `Mode A targeted + amplification` — 2 anchors pinned (Bay teal #00647D as substrate, Roast wine #58181D), coral evolved to Tannin (deepened), Gilt new as ≤4% editorial accent, Porcelain alt-surface, cream + maroon + amber + brown-tertiary all dropped.

**Type scale:** 1.25 (major-third) — measured restraint.

**Voice:** declarative 2nd-person, no exclamations in chrome (voice rule 7.2 opted-in), mixed-case headings, Martian Mono catalog register for specs.

## Variant differentiation contract — passes ≥2 substantive changes

| Dimension | A | B | Differs? |
|---|---|---|---|
| Ground family | stark-white | saturated teal | ✓ |
| Display type | DM Serif Display (transitional serif) | Space Grotesk (geometric sans) | ✓ |
| Editorial display | Cormorant Garamond | Cormorant Garamond | shared |
| Type scale | 1.333 perfect-fourth | 1.25 major-third | ✓ |
| Voice rule 7.2 | not opted-in | opted-in | ✓ |
| Banner treatment | full-bleed photography | typographic on saturated ground | ✓ |
| Hand-drawn accent | Caveat (≤2 per page) | none | ✓ |
| Catalog register font | JetBrains Mono | Martian Mono (load-bearing) | ✓ |
| Coral evolution | Cherry (kept hex) | Tannin (deepened) | ✓ |
| Editorial accent | none | Gilt (≤4%) | ✓ |

→ 9 substantive differences. Differentiation contract passes (≥2 required).

## Anti-toolbox audit (per-variant; full trace in DESIGN-{A,B}.json.extensions.divergence)

**Variant A:**
- Hits: 1 (sticky top navigation — justified by e-commerce conversion need)
- Off-toolbox moves: 1 (Caveat signage in eyebrow positions — amplifies captured trait of Frescopa's hand-drawn SVG logotype)

**Variant B:**
- Hits: 1 (sticky top navigation — same justification)
- Off-toolbox moves: 2 (saturated-teal page ground; Cormorant editorial display on Porcelain in a saturated-grounded site)

**Both variants share these guardrails (recorded in PRODUCT.md anti-references):**
- No editorial-register vocabulary on a non-editorial brand
- No fabricated content
- No hero text on photographic background without contrast scrim
- No cream-family ground (variant B explicitly addresses; variant A: stark-white, no risk)
- No generic role names in palette (audited: PASS for both)

## IA-priority preservation audit (Mode A constraint)

Triggers fired on captured surface:
- **Commercial conversion** — pages/home.json shows 5+ product-category cards above the fold
- **Audience routing** — top nav contains 6 product paths + Business + Subscription + Blog (multi-audience)
- **Search-led IA** — pages/locations.json shows search input in hero region

All three triggers preserve identically across A and B. Recorded in `DESIGN-A.json.extensions.iaPriorities[]` and `DESIGN-B.json.extensions.iaPriorities[]`.

## Improvements list (Phase 2.5)

7 specific weaknesses surfaced in `stardust/prototypes/home-improvements.md`:
1. heading-hierarchy (h1 missing on home; h6 reused as nav-label)
2. banner-quality (flat-illustration-on-color reads as white-label-template)
3. type-scale (ad-hoc, no consistent ratio)
4. color-imbalance (3 single-context colors: cream, maroon, amber — drop or expand)
5. image-alt (64% empty alt text)
6. voice-exclamation-load (4 exclamations in first viewport — cap)
7. promo-band-priority (aggressive amber pill competes with nav)

**Variant A applies all 7 exactly.** Variant B honors all 7 as a floor and goes further on items 2 and 6 (banner becomes typographic, not photographic; voice rule 7.2 opted-in).

## Commands run / planned

Plan from master skill (Phase 1 → 5 of overall pipeline):

| Step | Command | Status |
|---|---|---|
| 1 | `$stardust extract https://frescopa.coffee/ --cap 15` | DONE |
| 2 | (user reviews `stardust/current/brand-review.html`) | DONE |
| 3 | `$stardust direct --variants=2 --pin-colors="#00647D,#58181D"` | DONE (this run) |
| 4 | `$stardust prototype home` (renders both variants of home for user pick) | NEXT |
| 5 | (user picks variant A or B) | pending |
| 6 | `$stardust prototype <template-pages>` (representative templates after variant pick) | pending |
| 7 | `$stardust migrate` (apply approved templates across 15-page inventory) | pending |

## Assumptions defaulted in (correct me if wrong)

1. **Density tier:** balanced (64px desktop) — defaulted because the user phrase didn't move density and the multi-audience hard floor caps any push to airy. Both variants share this.
2. **Type stack openness:** the user said "the rest can be creatively rethought" with respect to colors specifically. I extended this to type — Baskerville + Roboto are not pinned. Both variants pick new type stacks. If you want to also pin Baskerville-family for headings, that's an easy direct-edit; reply and I'll re-direct.
3. **Logo preserved verbatim:** the SVG "Frescopa" logotype is treated as pinned in both variants (filter-inverted on Bay ground in variant B). If you want to redesign the logotype, that's a separate scope.
4. **Banner regeneration via Gemini 3 Pro:** the prototypes can be authored without those images (variant A uses extracted MyBarista photo + product photography; variant B uses typographic heroes on saturated ground). If you want to actually regenerate banner images via Gemini 3, you can run that out-of-band between prototype and migrate; the prompts are in the prototype shape brief deliverables.
5. **Improvements list scope:** captured tensions are home-led but apply site-wide. The single `home-improvements.md` file covers the system-level fixes. Per-page deviations (if any) will land in `<slug>-shape.md` briefs at prototype time.
