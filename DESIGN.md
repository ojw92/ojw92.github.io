---
name: Ahab
description: A night-sonar field notebook that grades its own predictions honestly.
colors:
  night: "#071522"
  night-2: "#0B2233"
  ink: "#12263A"
  ink-soft: "#3D5266"
  paper: "#F6F4ED"
  water: "#E5ECE8"
  line: "#C9CFC4"
  magenta: "#B02A63"
  phosphor: "#8FD4C1"
typography:
  display:
    fontFamily: "\"Iowan Old Style\", \"Palatino Linotype\", Palatino, Georgia, serif"
    fontSize: "clamp(58px, 10vw, 118px)"
    fontWeight: 600
    lineHeight: 1
    letterSpacing: "0.04em"
  headline:
    fontFamily: "\"Iowan Old Style\", \"Palatino Linotype\", Palatino, Georgia, serif"
    fontSize: "36px"
    fontWeight: 600
    lineHeight: 1.18
    letterSpacing: "-0.005em"
  title:
    fontFamily: "\"Iowan Old Style\", \"Palatino Linotype\", Palatino, Georgia, serif"
    fontSize: "21px"
    fontWeight: 600
    lineHeight: 1.3
  body:
    fontFamily: "\"Iowan Old Style\", \"Palatino Linotype\", Palatino, Georgia, serif"
    fontSize: "17.5px"
    fontWeight: 400
    lineHeight: 1.68
  label:
    fontFamily: "ui-monospace, \"SF Mono\", Menlo, Consolas, monospace"
    fontSize: "13px"
    fontWeight: 400
    letterSpacing: "0.08em"
rounded: {}
spacing:
  xs: "8px"
  sm: "14px"
  md: "22px"
  lg: "28px"
  xl: "48px"
  xxl: "78px"
components:
  nav-link:
    textColor: "{colors.ink}"
    typography: "{typography.body}"
  nav-link-hover:
    textColor: "{colors.magenta}"
  callout-thesis:
    backgroundColor: "{colors.night-2}"
    textColor: "#DCE8E1"
    padding: "28px 32px"
  verdict-row:
    backgroundColor: "{colors.night-2}"
    textColor: "#F0F5F1"
    padding: "14px 18px"
  back-link:
    textColor: "{colors.phosphor}"
    typography: "{typography.label}"
  back-link-hover:
    textColor: "#FFFFFF"
---

# Design System: Ahab

## Overview

**Creative North Star: "The Instrument Log"**

Ahab reads as a field notebook kept by an instrument, not a brochure written by a marketer. A warm paper reading surface carries long-form serif prose; a night-navy instrument register (hero, the "hardest bug" section, footer) breaks in wherever the system is reporting a measurement rather than narrating. Monospace is reserved exclusively for anything that is a literal number, log line, or instrument label — never for body voice. The world is nautical-instrument, not nautical-decorative: the sonar canvas, the mono "bearing" markers (`I / IV`), and the run-manifest log line are the whale-hunt metaphor made functional, not illustrative flourish.

The build carries this world forward from the incumbent site rather than inventing a new one: the sonar canvas script and the three data-figure SVGs are verbatim incumbent assets, and the same five-token color system anchors both. What changed is the container — a single long-form article page instead of a landing page — so a contents nav, numbered sections, dark/light section alternation, and figure/prose rhythm were added on top of the inherited palette and type voice.

Key Characteristics:
- Two registers, not one: warm-paper reading mode (article body) and night-navy instrument mode (hero, challenge section, footer), never blended within a single surface.
- Monospace is a measurement marker, applied only to numbers, log lines, gate labels, and nav/label microcopy — never to headlines or prose.
- Magenta is a rare mark of consequence: first-letter drop caps, the harpoon-line rule under pull quotes, thesis-statement emphasis, "next"-list markers.
- Figures are instrument print-outs: SVG charts with monospace axis labels and callouts, not decorative illustration.

## Colors

The palette is a five-color night/paper system: two dark instrument surfaces, one paper reading surface, one desaturated sage-green neutral, and two accents (magenta for editorial emphasis, phosphor for instrument glow).

### Primary
- **Harpoon Magenta** (#B02A63): the one warm, high-consequence accent. Used on drop-cap first letters, the pull-quote rule, link color, thesis-callout emphasis (`<em>`), figure highlight bars for the number the article wants noticed, and the "what's next" list markers.

### Secondary
- **Phosphor Green** (#8FD4C1): the instrument-glow accent, confined to the two night-navy surfaces (hero, footer). Used for the sonar sweep/blips, the manifest numbers in the hero, footer link color, and the "back to portfolio" nav link.

### Neutral
- **Night** (#071522): the deep instrument-black background for the hero and footer.
- **Night Deep 2** (#0B2233): a slightly lighter navy used for callout/verdict cards sitting on top of Night, giving the dark register two tonal steps instead of flat black-on-black.
- **Paper** (#F6F4ED): the warm off-white reading surface for all article body sections.
- **Water** (#E5ECE8): a pale sage-green, used sparingly as a secondary light surface.
- **Ink** (#12263A): primary body text color on paper, and the "all gates together" bar fill in charts.
- **Ink Soft** (#3D5266): secondary/caption text on paper, chart axis labels, dashed reference lines.
- **Line** (#C9CFC4): hairline dividers between sections, table rows, chart gridlines, dashed pipeline-step borders.

### Named Rules
**The Two-Register Rule.** A surface is either paper (warm, serif, editorial) or night (navy, instrument, monospace-accented). No section blends both backgrounds; the transition between registers is always a hard section boundary, never a gradient.

**The Mono-Is-Measurement Rule.** Monospace type marks only things that are literally measured or logged: numbers, log lines, section bearings (`I / IV`), gate labels, chart axis text, and nav microcopy. It never carries a headline, a sentence of prose, or a decorative label — because in this build the label is not a decorative device, it's how a number earns trust as data rather than claim.

## Typography

**Display Font:** "Iowan Old Style", "Palatino Linotype", Palatino, Georgia, serif
**Body Font:** same serif stack — display and body share one family
**Label/Mono Font:** ui-monospace, "SF Mono", Menlo, Consolas, monospace

**Character:** A single warm literary serif carries every register of prose (hero title through body copy), so voice stays constant across the whole page; monospace is the only second voice, and it speaks exclusively in numbers and instrument labels.

### Hierarchy
- **Display** (600, `clamp(58px, 10vw, 118px)`, line-height 1): the hero `<h1>` ("AHAB") only.
- **Headline** (600, 36px → 29px at ≤760px, line-height 1.18): section `<h2>` titles.
- **Title** (600, 21px): subsection `<h3>` (stack items, learnings, footer heading at 26px).
- **Body** (400, 17.5px → 16.5px at ≤760px, line-height 1.68): all article prose. `.prose` boxes cap measure at 66ch.
- **Label** (400, 12–15.5px, letter-spacing 0.06–0.14em, uppercase where noted): nav labels, bearings, byline, manifest, chart axis text, verdict lens names.

### Named Rules
**The Drop-Cap Opener Rule.** Only the first paragraph of the first section (`.opener`) gets a magenta 64px drop cap. It marks "the article begins here" once; it is not a recurring section device.

## Layout

Single-column long-form article, `max-width: 1020px` centered wrap with 28px side padding; prose blocks additionally cap at 66ch (or 72ch for wider tabular content) for readability regardless of the outer container width. Vertical rhythm is generous and consistent: sections pad 78px top / 30px bottom (56/22 at ≤760px), with a 1px hairline plus 48px margin between sections. A sticky-free contents nav sits directly under the hero as a flat row of anchor links. Two-column grids (challenge section, footer) collapse to one column at the 760px breakpoint; the stack list and pipeline list collapse their grid/flex row structure to full-width stacked blocks at the same breakpoint. The hero uses a bottom-anchored flex column so the masthead always sits at the viewport's lower edge regardless of viewport height (min-height 86vh, 74vh on mobile).

## Elevation & Depth

Flat throughout — there is no box-shadow anywhere in the system. Depth and hierarchy are conveyed entirely through the night/paper register switch and hairline dividers (`1px solid var(--line)`), not through shadow or blur. The one layered surface (verdict cards) separates from its Night-2 backdrop with a 1px rgba(phosphor) border/gap, not a shadow.

### Named Rules
**The No-Shadow Rule.** Structure is drawn with flat color blocks and hairlines. If a component needs to read as "raised," change its background tone (Night → Night-2) rather than adding a shadow.

## Shapes

Rectilinear and unrounded throughout: zero border-radius anywhere in the build. Dividers are 1px hairlines (solid on section/table boundaries, dashed on pipeline-step separators and chart reference lines). The one recurring decorative mark is a short horizontal rule (magenta, 64×3px) used as a "flag" above pull-quotes and as small tick marks (14×2px) before "what's next" list items — a consistent horizontal-dash vocabulary rather than bullets or icons.

## Components

### Navigation
- **Contents nav:** flat row of underlined text links on a paper background, mono uppercase "In this write-up" label, 1px bottom border on the nav bar. Hover: link color and underline shift to magenta.
- **Back-to-portfolio link:** absolute-positioned top-left over the hero, mono uppercase, phosphor color, no underline; hover goes white. It is the only nav element inside the night register.

### Callouts
- **Thesis callout** (`.thesis`): Night-2 background, 21px serif text, max-width 56ch, magenta-underlined `<em>` for the load-bearing phrase. Used once per article to state the core claim.
- **Pull quote** (`.pull`): no background, sits on the night register, marked by a 64×3px magenta rule above it rather than a border or quote glyph.

### Cards / Containers
- **Verdict cards** (`.verdict`): flat Night-2 rectangles in a 1px-gapped rgba(phosphor) grid, no radius, no shadow. Mono lens label + large mono delta number, color-coded red/green/neutral by direction (`.delta.down` / `.delta.up`).
- **Pipeline steps:** unbordered flex items separated by 1px dashed lines, mono timestamp + serif title + caption — a horizontal timeline read left to right, `overflow-x: auto` on narrow viewports.
- **Stack definition list** (`dl.stack`): two-column term/definition grid with 1px hairline row dividers; term in mono/bold, definition in soft ink serif.

### Signature Component: Instrument Charts
Each `figure.chart` is a hand-built inline SVG (carried over verbatim from the incumbent build), styled entirely in the mono/ink-soft/magenta palette: gridlines in `--line`, axis labels in mono `--ink-soft`, the single number the reader should notice highlighted in magenta, secondary bars in ink. Figcaptions run body-serif at 14.5px with inline `<code>` for dataset/column references. These are read as instrument printouts, not marketing infographics — every chart caption names the exact source table and regeneration date.

## Do's and Don'ts

### Do:
- **Do** keep monospace confined to numbers, logs, labels, and axis text (the Mono-Is-Measurement Rule).
- **Do** treat the night/paper split as a hard section boundary (the Two-Register Rule) — never gradient or blend the two.
- **Do** spend magenta rarely: one thesis callout, drop caps, pull-quote rule, and the specific number a chart wants noticed.
- **Do** build charts as SVG with mono axis labels and a named data source in the caption, matching the existing three figures.
- **Do** use flat hairlines and background-tone shifts for hierarchy; never introduce a box-shadow.
- **Do** cap prose measure at 66–72ch regardless of the outer 1020px wrap.

### Don't:
- **Don't** add border-radius; the system is edge-to-edge rectilinear with zero rounded corners anywhere in the build.
- **Don't** add drop shadows or glows outside the sonar canvas's own additive glow effect (which is a canvas-rendered instrument behavior, not a CSS box-shadow token).
- **Don't** use the serif display face for anything except the hero `<h1>` — section headlines are a smaller weight-600 serif, not the display size.
- **Don't** introduce a second accent color; magenta and phosphor are each scoped to one register (paper/mixed vs. night) and should not swap registers.
