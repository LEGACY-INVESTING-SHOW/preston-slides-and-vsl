---
name: lis-slide-design
description: LIS SLIDE DESIGN creates HTML presentation slides for Legacy Investing Show in Preston Seo's brand style. Use when creating slide decks, presentations, pitch decks, or HTML-based slides for Legacy Investing, Preston Seo, tax optimization content, or wealth-building presentations. In this repo, use `str-vsl/overall.html` as the primary reference and working deck.
---

# LIS SLIDE DESIGN

Create professional HTML presentation slides following the Legacy Investing Show brand guidelines.

In this repository, the main source of truth is [`str-vsl/overall.html`](str-vsl/overall.html). Do not default to the generic template when the request is about this repo's existing slide deck.

## Quick Start

1. Open `str-vsl/overall.html` first.
2. Reuse or duplicate slide sections from that file instead of starting from a blank template.
3. Preserve the existing CSS system, slide class names, presenter mode, and `images/` relative paths unless the user asks for a structural rewrite.
4. Keep new slide work visually consistent with the existing deck.
5. Use `assets/template.html` only as a secondary reference for generic brand styling, not as the default starter in this repo.

## Canonical Files

- `str-vsl/overall.html` - primary working deck with the current slide system, CSS, presenter view, notes, and interaction logic
- `str-vsl/images/` - image assets used by `overall.html`
- `assets/template.html` - older generic slide reference; optional only when the user wants a fresh deck outside the STR/VSL deck structure

## Required Workflow

When working on this repo:

1. Read `str-vsl/overall.html` before making slide changes.
2. Edit that file directly when the task is about the live STR/VSL deck.
3. Prefer modifying existing slide patterns over inventing brand-new structures.
4. Keep image URLs relative to `images/...` so the deck still renders inside `str-vsl/`.
5. Preserve presenter-related JavaScript and `defaultSlideNotes` unless the user explicitly asks to change or remove them.
6. If you add, remove, or reorder slides, update any matching presenter notes and flow so the deck stays coherent.
7. Treat `overall.html` as a pattern library with 30+ reusable slide structures, not just one finished deck.

## Pattern Selection Rule

Before creating a new design:

1. Match the request to the closest existing slide class in `str-vsl/overall.html`.
2. Duplicate and adapt that block first.
3. Reuse inner component classes from the deck whenever possible.
4. Create a brand-new slide class only if no existing pattern fits the content.

If several classes could work, prefer the one that preserves the strongest continuity with the surrounding slides.

## Deck Systems To Preserve

- The standard 16:9 slide canvas and `.slide` container
- The dark green / gold / off-white presentation system
- The existing hover, shadow, rounded-card, and badge treatments
- The presenter mode, teleprompter flow, and `BroadcastChannel` sync
- `defaultSlideNotes`, slide titles, and progression through the deck
- Relative image usage under `str-vsl/images/`

## Visual System

### Color Palette

Use the deck's established palette from `str-vsl/overall.html`:

- Dark green: `#0f4c3a`
- Mid green: `#0a3d2f`
- Deep green: `#072820`
- Light green: `#1a7a5e`
- Gold: `#d4af37`
- Off-white: `#fafafa`
- Near-black: `#1a1a1a`
- Red: `#c53030`

### Typography

- Headlines: `'Playfair Display', serif`
- Body/UI: `'Inter', sans-serif`

### Design Rules

- Favor dense, high-value slides over sparse layouts.
- Use strong green, gold, white, and dark surfaces instead of muted grayscale.
- Keep hierarchy obvious with badges, brows, numbers, cards, and section headers.
- Reuse the deck's existing shadows, borders, and rounded cards for consistency.
- Use contextual screenshots and product visuals when the slide format expects them.

## Full Pattern Catalog

`str-vsl/overall.html` contains a broad pattern library. Use these classes intentionally.

### Inclusion And Recap Slides

- `slide-path-a` for dense "what's included" slides with floating checklist cards and pillar grids
- `slide-path-b-recap` for recap variants that combine checklists with 2-column or 3-column pillar summaries
- `slide-recap` for full three-offer recap and CTA layouts with bottom action banner

### Process And Model Explainers

- `slide-arbitrage-model` for 4-step business models with bottom proof and example numbers
- `slide-process` for ownership/process models with steps plus horizontal "why this works" proof cards
- `slide-decision` for decision-tree or branching-path guidance
- `slide-progression` for A-to-B-to-C tier ladders and offer ascension stories

### Offer And Service Slides

- `slide-dfy-b` for simple centered done-for-you offer slides
- `slide-dfy-c` for high-contrast concierge or flagship offer reveals with scarcity
- `slide-services` for 3-column service breakdowns
- `slide-buying-lane` for 2-column done-for-you process breakdowns with timelines
- `slide-setup` for "we set it up for you" operational grids
- `slide-entity-setup` for premium add-on or partner-service offers with expert tiles

### Toolkit, Feature, And Asset Grids

- `slide-features` for large image-backed feature cards across a wide grid
- `slide-tools-c` for condensed tool or software bundles with license/value tags
- `slide-pillars-summary` for compact path-by-path pillar summaries

### Qualification, Education, And Support Slides

- `slide-built-for` for qualification and ideal-client slides with highlighted checklist cards
- `slide-tax-optimized` for two-column strategy/partner education slides
- `slide-referrals` for partner network or vetted referral slides
- `slide-wealth-guide` for concierge/contact/support slides with feature cards and portrait area
- `slide-wealth-circle` for community slides with social-post mockups
- `slide-ai-advisor` for product reveal slides centered around app/chat mockups

### Numbers, Proof, And Comparison Slides

- `slide-math-v2` for value-stack math, ROI math, and year-one economics
- `slide-path-combined` for "why this wins" comparison stories with a featured option
- `slide-comparison-table` for side-by-side offer comparisons with factor rows
- `slide-comparison-matrix` for larger feature matrix tables across all paths
- `slide-roi` for bold end-of-deck ROI slides with proof bullets and image band

### Narrative Bridge Slides

- `slide-transition` for simple emotional transition statements between major sections
- `slide-snapshot` for visual/document "before vs after" or strategy snapshot storytelling

## Reusable Inner Components

The deck also contains reusable sub-patterns. Reuse these inside slides before inventing new markup:

- `checklist-floating`, `floating-item`, `check-badge` for benefit checklists
- `pillars-grid`, `pillars-grid-2`, `pillars-grid-3`, `pillar-card` for curriculum or service pillars
- `steps-flow`, `step-card` for 4-step sequences
- `why-stack`, `why-card`, `why-cards-row`, `why-card-horizontal` for explanatory proof blocks
- `feature-card-large`, `tool-card-large`, `card-image`, `overlay-title` for screenshot-backed cards
- `service-card`, `card-bullets`, `timeline-tag` for structured service descriptions
- `math-v2-card`, `math-v2-row`, `math-v2-total` for calculation storytelling
- `featured-card`, `standard-card` for qualification criteria
- `tax-card-white`, `referral-card-white`, `guide-feature-card`, `expert-card` for support and partner content
- `community-mockup`, `community-post` for social proof / private group visuals
- `snapshot-document`, `scenario-box` for visual artifact or plan previews
- `comparison-table`, `comparison-check`, `comparison-section-label` for tabular comparisons
- `progression-card`, `progression-arrow` for offer ladders
- `chat-interface`, `chat-message`, `chat-input` for AI or messaging product demos

## How To Choose A Design

Use this mapping when translating requests into deck structures:

- "What's included", "deliverables", "bonus stack", "curriculum" -> `slide-path-a` or `slide-path-b-recap`
- "how it works", "process", "framework", "model" -> `slide-arbitrage-model` or `slide-process`
- "done for you", "service breakdown", "what we handle" -> `slide-dfy-b`, `slide-dfy-c`, `slide-services`, or `slide-buying-lane`
- "toolkit", "software", "assets", "what you get" -> `slide-features` or `slide-tools-c`
- "numbers", "ROI", "economics", "comparison" -> `slide-math-v2`, `slide-path-combined`, `slide-comparison-table`, `slide-comparison-matrix`, or `slide-roi`
- "who it's for", "ideal fit", "qualification" -> `slide-built-for`
- "partners", "team", "support", "community", "advisor" -> `slide-referrals`, `slide-wealth-guide`, `slide-wealth-circle`, or `slide-ai-advisor`
- "transition", "belief shift", "section break" -> `slide-transition`
- "snapshot", "plan preview", "document preview" -> `slide-snapshot`
- "choose your option", "pick a path", "offer ladder" -> `slide-decision`, `slide-recap`, or `slide-progression`

## Input-To-Slide Workflow

This skill should accept raw input in many forms:

- a topic
- a rough idea
- a transcript excerpt
- a VSL script
- a speaker script
- a bullet list
- an outline
- a block of notes
- offer copy
- educational content

The job is not to dump that text onto slides. The job is to interpret the content, choose the best existing visual structure from `overall.html`, and then turn the content into slides that fit that structure.

### Step 1: Normalize The Input

Figure out what kind of source the user gave you:

- single concept needing one slide
- several points that should become multiple slides
- a long-form script that should be broken into beats
- an existing slide that just needs better structure

If the input is long, break it into logical beats before designing.

### Step 2: Extract The Core Payload

For each beat or section, identify:

- the main point
- supporting proof
- any numbers or comparisons
- whether the goal is explanation, persuasion, qualification, proof, transition, or CTA
- whether there are assets or screenshots that should be shown

Each slide should usually have one dominant communication job.

### Step 3: Classify The Content Type

Classify each beat into one of these buckets:

- promise / headline
- process / framework
- offer / deliverables
- proof / results
- qualification / who this is for
- comparison / alternatives
- support / team / community
- product / software / toolkit
- transition / belief shift
- CTA / decision

### Step 4: Choose The Best Existing Slide Pattern

Map the classified content to the strongest pattern from `overall.html`:

- promise / reveal -> `slide-dfy-c`, `slide-transition`, or `slide-path-combined`
- process / framework -> `slide-arbitrage-model` or `slide-process`
- offer / deliverables -> `slide-path-a`, `slide-path-b-recap`, `slide-services`, `slide-buying-lane`, or `slide-recap`
- proof / numbers -> `slide-math-v2`, `slide-roi`, `slide-comparison-table`, or `slide-comparison-matrix`
- qualification -> `slide-built-for`
- support / team / white-glove help -> `slide-wealth-guide`, `slide-referrals`, or `slide-entity-setup`
- community / social proof -> `slide-wealth-circle`
- toolkit / software / assets -> `slide-features`, `slide-tools-c`, or `slide-ai-advisor`
- transition / belief shift -> `slide-transition` or `slide-snapshot`
- CTA / path selection -> `slide-decision`, `slide-recap`, or `slide-progression`

Choose the design that helps the content read visually, not just semantically.

### Step 5: Fit The Content To The Structure

Once you choose the slide class:

- compress the copy to fit the visual slots that structure supports
- rewrite long paragraphs into cards, bullets, stats, steps, labels, or comparison rows
- preserve the strongest proof and remove filler
- turn abstract ideas into visible hierarchy

Do not force a dense script paragraph into a visual pattern that only supports a short headline and one sentence.

### Step 6: Build The Slide

When implementing:

- duplicate the closest existing slide block
- replace the content while keeping the structure intact
- reuse existing subcomponents
- add or swap images only when they strengthen the slide
- update presenter notes if the new slide changes the speaking flow

## Selection Heuristics

Use these heuristics when deciding the best display structure:

- If the content is step-by-step, use a step flow, not a comparison table.
- If the content is mostly numbers, use a math or comparison layout, not a generic bullet slide.
- If the content is a list of included items, use checklist and pillar layouts.
- If the content is about support, access, team, or guidance, use support-style cards or partner grids.
- If the content is a belief-shift moment, use a transition slide or a visual snapshot slide.
- If the content compares options, use one of the comparison layouts.
- If the content is about software, tools, or assets, use image-backed feature grids.
- If the content is emotional or punchy, prefer bold single-message slides over overloaded grids.

## Default Behavior

If the user gives raw content and does not specify a layout:

1. infer the content type
2. choose the best-fit existing slide pattern from `overall.html`
3. adapt the copy to that structure
4. produce the slide in the style of the existing deck

The skill should behave like a slide designer, not a text formatter.

## Editing Guidance

### If the user wants to update the existing VSL deck

- Work in `str-vsl/overall.html`.
- Preserve the current slide order unless the request includes re-sequencing.
- Match nearby slide structure, spacing, and headline tone.
- Keep presenter notes aligned with the visible slide content.
- Reuse all relevant existing classes from the pattern catalog before introducing anything new.

### If the user wants a new slide in the same style

- Duplicate the closest existing slide block in `str-vsl/overall.html`.
- Rename classes only when a new visual pattern is genuinely needed.
- Add matching notes if the slide should participate in presenter mode.
- When possible, borrow inner components from multiple existing slides instead of building new primitives.

### If the user wants a brand-new generic deck

- You may use `assets/template.html` as a helper reference.
- Still carry over the same brand palette and typography.
- Make it clear when you are not working from `str-vsl/overall.html`.

## Guardrails

- Do not treat `assets/template.html` as the default file for this repo.
- Do not break `images/...` asset paths.
- Do not remove presenter view features accidentally.
- Do not rewrite the whole deck when a local edit will do.
- Do not introduce off-brand colors or generic presentation aesthetics.
- Do not ignore existing slide classes that already solve the requested layout.

## Output Expectation

For repo-specific slide work, the deliverable should normally be an update to `str-vsl/overall.html` and any supporting assets under `str-vsl/images/`.

## Examples

- "Turn this VSL segment into 3 slides using the existing deck patterns."
- "Use the existing ROI structure to visualize these numbers."
- "Choose the best existing slide design for this topic and build the slide."
- "Adapt this script beat into a Path C style slide without inventing a new layout."
