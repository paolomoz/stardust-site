<!--
_provenance:
  writtenBy: stardust:direct
  writtenAt: 2026-05-03
  stardustVersion: 0.3.0
-->

# Direction — UPS GB home page

## Phrase (verbatim)

> "redesign the home page — analyse and suggest direction, so we can pick the best improvement goals"

Followed by the user's pick after the menu was offered:

> "direction A, density c"

## Restatement (in stardust's dimensional vocabulary)

The user is committing to direction **A — tool-first home** at density tier **c (packed, 48px desktop)**. This is a presales-style refresh of an existing site:

- **Register:** brand (inherited from `current/PRODUCT.md`). The site at large remains a brand surface; the home page deploys a tool-led hero composition within that register.
- **Expressive:** committed (unchanged from captured surface).
- **Tone:** capable / serious (unchanged).
- **Density:** packed (`section-desktop: 48px`, `tablet: 36px`, `mobile: 24px`) — explicitly picked by the user.
- **Distinctiveness:** familiar → distinctive (the redesign earns distinctiveness by inverting a common pattern: the tracker leads, not the marketing). Not singular.
- **Audience:** weighted toward return visitors looking up tracking numbers; SMB shippers second; healthcare addressed via global nav only.
- **Constraints:** `brand-faithful` (Mode A, signal-strong, no `--rebrand` flag), `a11y-first` (the home today fails several baseline rules — empty H1, 60% empty alt, footer columns not in heading tags).

## Mode-detection result

**Mode A — brand-faithful** active by default.

- Captured signal classified as **`signal-strong`** in setup: 9 distinct palette colours after clustering, two named type families (Roboto + IBM Plex Sans), 60-85 declared `:root` custom properties.
- No rebrand triggers fired in the user's phrase. No `--rebrand` flag passed.
- Palette and type are **pinned** to the captured surface.
- Image-reuse contract holds (where reused at all — see Phase 2.5 fixes).

## Movements (axes the phrase moved)

| axis | from (captured) | to (resolved) | trigger |
|---|---|---|---|
| **density** | ad-hoc per-template | packed (48px desktop) | user pick: density `c` |
| **distinctiveness** | familiar (SaaS-template orbit) | distinctive (tool-led hero) | direction A — invert the dominant first-viewport surface |
| **IA priority** | marketing-first hero, tracker mid-page | tool-first hero, marketing below-fold | direction A is exactly this move |
| **CTA vocabulary** | fragmented (Get Started + Start Shipping + Ship & Save) | canonical per task (Track / Get a quote / Start shipping / Log in) | T-cta-vocab tension resolved |
| **radius vocabulary** | 8 distinct values | 3 values (4 / 8 / 50%) | T-radius-vocab tension resolved |
| **type scale** | ad-hoc per template | modular ratio ~1.25 anchored on body 16px | T-scale tension resolved |
| **alt-text floor** | 60% empty above the fold | 0% accidental empty above the fold | T-img-alt-empty + a11y-first |
| **`<h1>` presence** | empty on home (image-baked hero) | display H1 above the tracking strip | a11y / SEO / brand-statement floor |

## Movements (axes the phrase did NOT move — pinned by Mode A)

| axis | value | source |
|---|---|---|
| **palette** | inherited from `_brand-extraction.json` | Mode A pin |
| **type families** | Roboto (heading + body); IBM Plex Sans scoped to `/healthcare/` only | Mode A pin |
| **register** | brand | inherited from current/PRODUCT.md |
| **tone** | capable / serious / Title-Case | inherited from voice samples |
| **logo** | the captured shield + UPS wordmark, unchanged | Mode A pin |

## Gaps (resolved)

The user's phrase was high-confidence. Two gaps the agent surfaced:

1. **Which directional bet leads** — A (tool-first), B (editorial confidence), or C (operational transparency)? Answered: **A**.
2. **Density tier** — (a) airy 96px, (b) balanced 64px, (c) packed 48px. Answered: **(c) packed**.

Density tier `(c)` is consistent with the captured page inventory: the home has commercial-conversion priority (gold CTA verbs Track / Quote / Ship / Log in above the fold), which is the explicit "tighter density (48-56px) is preferred" trigger in `intent-dimensions.md` § 4. No hard-floor conflict to surface.

## Divergence inputs (Mode A, signal-strong)

```
decade           ✓ rolled    → now (2025-)         — current-tier execution
craft            ✓ rolled    → web                  — tool-first home is a web product surface
register         inherited   → brand                — current/PRODUCT.md
ground-family    inherited   → stark-white          — brand-faithful override (captured #fff)
font deck        inherited   → existing site stack  — Roboto
palette          inherited   → existing 9-color set — UPS gold + warm-grey + alert + healthcare-blue
```

**Brand-faithful inversions** (inert dimensions where the system *did* change something despite Mode A pinning palette and type):

- Radius vocabulary: 8 captured values → 3 (4 / 8 / 50%). Reason: `T-radius-vocab` tension.
- Type scale: ad-hoc → modular ratio 1.25. Reason: `T-scale` tension; the captured site declared scale tokens but didn't enforce them.
- Shadow vocabulary: 3 → 2 (drop the strong drop on the home; keep card-elevation + subtle hairline).
- Section padding: ad-hoc → 48 / 36 / 24 px. Reason: density `c` pick.
- CTA verbs: `Get Started` + `Start Shipping` + `Ship & Save` → `Track` / `Get a quote` / `Start shipping` / `Log in`. Reason: `T-cta-vocab` tension.

## Anti-toolbox audit

Scanned: `generic-2026-saas`, `editorial-register-vocabulary`, `C-cliff overshoot`, `dual-CTA pattern`, `sliding-pill-as-personality`, `glassmorphism`, `dark-mode-by-reflex`, `cyan/purple gradient`, `gradient-text`, `side-stripes`.

**Hits: 0.** Direction A is a sober tool-first refresh of an established brand. The dual-CTA pattern is forbidden in `componentStyle.dualCTAPattern.allowed: false` to keep the SaaS-template silhouette out as variants progress.

## IA-priority preservation audit

Four signals fired against the captured `pages/home.json`. All are recorded in `DESIGN.json.extensions.iaPriorities[]` and become hard constraints on every variant the prototype phase renders:

1. **Search-led IA** — the `<input name="tracknum">` form lives above the fold; the redesigned hero is built on top of this form, not adjacent to it.
2. **Commercial conversion** — 4 gold CTAs above the fold (Track / Quote / Ship / Log in). Direction A amplifies this — it is the explicit move.
3. **Crisis affordance** — 5 active operational alerts persistent across all 5 captured pages. Preserved as a header-pinned chip + drawer (tightened, not removed).
4. **Audience routing** — Shipping / Tracking / Business Solutions / Support nav. Preserved in the global header above the workhorse.

## Plan shown to user (and confirmed)

```
1. Phase 2.5 — write stardust/prototypes/home-improvements.md
   (5 specific weaknesses, each with one-line fix; the brief variant A renders against)
2. Phase 3   — author target PRODUCT.md at project root
   (register: brand · users: 3 ordered audiences · purpose: fastest path to "where is my package")
3. Phase 4   — author target DESIGN.md + DESIGN.json at project root
   (Stitch frontmatter + 6 sections; sidecar with iaPriorities, divergence trace, voice rules)
4. Phase 5   — write this file + update state.json
   (home: extracted → directed)
5. (Out of scope here) — $stardust prototype to render the home variant
```

User confirmation: implicit (decisive pick of direction A + density c, no questions asked).

## Improvements list (Phase 2.5 — Mode A floor)

Five specific weaknesses written to `stardust/prototypes/home-improvements.md`:

1. **[ia-clutter]** First viewport carries 4 competing surfaces above the tracker. *Fix:* promote tracking band to visual hero; alerts collapse to header chip; IEEPA promo demoted; cookie band slim and non-blocking.
2. **[dated-pattern]** Empty `<h1>`, image-baked hero. *Fix:* display H1 above the tracking strip, verb-led, pivots with active tab.
3. **[cta-vocab]** "Get Started" + "Start Shipping" semantic siblings. *Fix:* canonical verbs Track / Get a quote / Start shipping / Log in.
4. **[a11y-floor]** 60% empty alt; footer columns not `<h*>`. *Fix:* alt audit above the fold; footer column titles become `<h2>` (visually identical).
5. **[radius-vocab]** 8 distinct radii. *Fix:* lock home to 3 (sm 4 / md 8 / circle 50%).

## Output summary

```
Wrote:
  PRODUCT.md                              (target strategy, project root)
  DESIGN.md                               (target visual system, Stitch format)
  DESIGN.json                             (sidecar — iaPriorities, divergence, voice, narrative)
  stardust/prototypes/home-improvements.md (Phase 2.5 brief)
  stardust/direction.md                   (this file)

State:
  home: extracted → directed
  4 other pages remain at status `extracted` (out of scope for this direction)

Next: $stardust prototype  (render the home variant against PRODUCT.md + DESIGN.md + the improvements list)
```
