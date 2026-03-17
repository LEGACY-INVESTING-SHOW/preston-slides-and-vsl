# LIS SLIDE DESIGN

Single-skill GitHub repo for designing Legacy Investing Show HTML slides from raw topics, scripts, outlines, or offer copy.

The installable skill is the root [`SKILL.md`](SKILL.md). The bundled reference deck is [`str-vsl/overall.html`](str-vsl/overall.html).

## Install

Install directly from the GitHub repo:

```bash
npx skills add LEGACY-INVESTING-SHOW/lis-slide-design
```

You can also install from the full GitHub URL:

```bash
npx skills add https://github.com/LEGACY-INVESTING-SHOW/lis-slide-design
```

If your agent does not pick up the new skill immediately, restart it.

## What This Skill Does

- Turns raw content into slide-ready visual structures instead of dumping text onto slides
- Chooses the best existing layout from the bundled reference deck
- Reuses the patterns, classes, and visual system from `str-vsl/overall.html`
- Preserves presenter notes, deck flow, and bundled image assets when editing the reference deck

## Why This Skill Is Better

- It chooses a design direction before choosing a layout
- It includes slide-specific anti-patterns so the output does not drift into generic AI deck design
- It pushes for stronger hierarchy, rhythm, and visual intent instead of repetitive card grids
- It treats the reference deck as a real pattern library, not just a template dump

## Best Use Cases

- Convert a VSL script into slides
- Turn a topic or outline into a visual deck
- Rebuild or extend the existing Legacy Investing Show slide deck
- Choose the best layout for numbers, comparisons, frameworks, offers, or support slides

## Example Prompts

- `Turn this VSL section into 3 slides using the existing LIS deck patterns.`
- `Take this topic and choose the best slide design from the repo before writing the slide.`
- `Use the current ROI layout to visualize these numbers.`
- `Make a Path C support slide from this speaker script without inventing a new design system.`

## Repo Layout

- [`SKILL.md`](SKILL.md): installable skill definition
- [`assets/template.html`](assets/template.html): secondary generic template reference
- [`str-vsl/overall.html`](str-vsl/overall.html): canonical reference deck and pattern library
- [`str-vsl/images/`](str-vsl/images): image assets used by the reference deck
- [`str-vsl/home-office-deduction-slide.html`](str-vsl/home-office-deduction-slide.html): companion slide file in the same visual family

## How Installation Works

The `skills` CLI looks for skills in a repository. For a single-skill repo, the cleanest path is a root `SKILL.md`, which is how this repo is structured.

That means the repo URL is enough. A user does not need to point at a nested subdirectory or guess the skill path.

## Notes

- This repo is intentionally packaged as a single-skill repository.
- `str-vsl/overall.html` is the main reference artifact the skill uses to choose layouts.
- `assets/template.html` is kept only as a secondary helper for generic deck starts.
- The public skill title is `LIS SLIDE DESIGN`.
- The install identifier stays `lis-slide-design` for compatibility with the skills ecosystem and `skills` CLI naming rules.
