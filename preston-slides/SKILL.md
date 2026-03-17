---
name: preston-slides
description: Create HTML presentation slides for Legacy Investing Show in Preston Seo's brand style. Use when creating slide decks, presentations, pitch decks, or any HTML-based slides for Legacy Investing, Preston Seo, tax optimization content, or wealth-building presentations. Triggers on "create slides", "make a presentation", "Preston slides", "Legacy slides", "pitch deck", or any slide/presentation request for financial education content.
---

# Preston Slides

Create professional HTML presentation slides following the Legacy Investing Show brand guidelines.

## Quick Start

1. Copy the template from `assets/template.html`
2. Select appropriate slide styles for your content
3. Follow the color palette and typography rules
4. Each slide uses class `slide` plus a style-specific class

## Color Palette (6 Colors Only)

| Color | Hex | Usage |
|-------|-----|-------|
| Dark Green | `#0f4c3a` | Primary brand, headers, stat blocks |
| Light Green | `#1a7a5e` | Secondary accents, alternating blocks |
| Gold | `#d4af37` | Accent highlights, CTAs, emphasis |
| Off-White | `#fafafa` | Light backgrounds |
| Near-Black | `#1a1a1a` | Dark text, body backgrounds |
| Red | `#c53030` | Negative/contrast comparisons only |

**Brand contextual colors** (Airbnb pink, Schwab blue) are permitted only when showing those specific brand examples.

## Typography

- **Headlines**: `'Playfair Display', serif` - elegant, high-end feel
- **Body/UI**: `'Inter', sans-serif` - clean, modern, readable
- Import: `https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;500;600;700&family=Inter:wght@300;400;500;600;700;800;900&display=swap`

## Slide Styles

### Style 1: Hero Title (`slide-hero`)

Dark green radial gradient background. Centered content with logo badge.

```html
<div class="slide slide-hero">
    <div class="logo">
        <div class="logo-main">THE LEGACY</div>
        <div class="logo-sub">INVESTING SHOW</div>
    </div>
    <h1>Main Title <span class="gold">Highlighted</span><br>Second Line</h1>
    <p class="subtitle">Subtitle text here</p>
</div>
```

**Use for**: Opening slides, section breaks, major announcements.

### Style 2: Stats Grid (`slide-stats`)

Split layout: left text panel (off-white), right 2x2 colored stat blocks.

```html
<div class="slide slide-stats">
    <div class="stats-left">
        <div class="eyebrow">Label</div>
        <h2>Headline <span class="gold">Gold Text</span></h2>
        <p>Supporting paragraph text.</p>
    </div>
    <div class="stats-right">
        <div class="stat-block"><div class="big">42%</div><div class="label">Label</div></div>
        <div class="stat-block"><div class="big">$87K</div><div class="label">Label</div></div>
        <div class="stat-block"><div class="big">10+</div><div class="label">Label</div></div>
        <div class="stat-block"><div class="big">$0</div><div class="label">Label</div></div>
    </div>
</div>
```

**Use for**: Problem statements, key statistics, data-driven points.

### Style 3: Floating Cards (`slide-section`)

Dark green background. Left text, right staggered floating cards.

```html
<div class="slide slide-section">
    <div class="section-left">
        <div class="eyebrow">Section Label</div>
        <h2>Section Title</h2>
        <p>Description paragraph.</p>
    </div>
    <div class="section-right">
        <div class="card-stack">
            <div class="floating-card"><div class="num">1</div><span class="text">Item text</span></div>
            <div class="floating-card"><div class="num">2</div><span class="text">Item text</span></div>
            <div class="floating-card"><div class="num">3</div><span class="text">Item text</span></div>
            <div class="floating-card"><div class="num">4</div><span class="text">Item text</span></div>
        </div>
    </div>
</div>
```

**Use for**: Process steps, curriculum items, features lists.

### Style 4: Horizontal Cards (`slide-flow`)

Light background with header, 3 horizontal green cards below.

```html
<div class="slide slide-flow">
    <div class="flow-header">
        <div class="eyebrow">Label</div>
        <h2>Title with <span class="green">Green</span> Highlight</h2>
    </div>
    <div class="flow-items">
        <div class="flow-item">
            <div class="num">01</div>
            <h4>Card Title</h4>
            <p>Card description text.</p>
        </div>
        <div class="flow-item">
            <div class="num">02</div>
            <h4>Card Title</h4>
            <p>Card description text.</p>
        </div>
        <div class="flow-item">
            <div class="num">03</div>
            <h4>Card Title</h4>
            <p>Card description text.</p>
        </div>
    </div>
</div>
```

**Use for**: Solutions, pillars, key benefits, 3-point frameworks.

### Style 5: Numbers Strip (`slide-numbers`)

4-column layout: intro text + 3 colored number blocks.

```html
<div class="slide slide-numbers">
    <div class="numbers-intro">
        <div class="eyebrow">Label</div>
        <h2>Section Title</h2>
    </div>
    <div class="num-block"><div class="big">$127K</div><h4>Metric</h4><p>Description</p></div>
    <div class="num-block"><div class="big">3.2x</div><h4>Metric</h4><p>Description</p></div>
    <div class="num-block"><div class="big">89%</div><h4>Metric</h4><p>Description</p></div>
</div>
```

**Use for**: Results, achievements, ROI metrics, social proof numbers.

### Style 6: Comparison (`slide-compare`)

Split 50/50: red "bad" side vs green "good" side.

```html
<div class="slide slide-compare">
    <div class="compare-bad">
        <div class="tag">Without Us</div>
        <h3>The Old Way</h3>
        <ul class="compare-list">
            <li><span class="ico">✕</span> Pain point 1</li>
            <li><span class="ico">✕</span> Pain point 2</li>
        </ul>
    </div>
    <div class="compare-good">
        <div class="tag">With Legacy</div>
        <h3>The New Reality</h3>
        <ul class="compare-list">
            <li><span class="ico">✓</span> Benefit 1</li>
            <li><span class="ico">✓</span> Benefit 2</li>
        </ul>
    </div>
</div>
```

**Use for**: Before/after, us vs competitors, problem vs solution.

### Style 7: Contextual Brand - Airbnb (`slide-context`)

Left text panel, right Airbnb-branded visual with listing card.

```html
<div class="slide slide-context">
    <div class="context-left">
        <div class="eyebrow">Strategy Label</div>
        <h2>Strategy Title</h2>
        <p>Strategy description.</p>
    </div>
    <div class="context-right">
        <div class="airbnb-logo">airbnb</div>
        <div class="airbnb-tag">Tagline</div>
        <div class="listing-card"><!-- card content --></div>
    </div>
</div>
```

**Use for**: Short-term rental strategy slides, Airbnb-specific examples.

### Style 8: Contextual Brand - Brokerage (`slide-brokerage`)

Left text panel, right Schwab-branded visual with account card.

```html
<div class="slide slide-brokerage">
    <div class="brokerage-left">
        <div class="eyebrow">Action Step</div>
        <h2>Account Setup Title</h2>
        <p>Description text.</p>
    </div>
    <div class="brokerage-right">
        <div class="schwab-logo">Charles Schwab</div>
        <div class="schwab-sub">Wealth Management</div>
        <div class="account-card"><!-- card content --></div>
    </div>
</div>
```

**Use for**: Brokerage setup steps, investment account examples.

## Slide Structure

Every slide follows this pattern:

```html
<p class="slide-label">Style Name → Description</p>
<div class="slide [style-class]">
    <!-- content -->
</div>
```

The `slide-label` is optional and used for development/preview purposes.

## Design Principles

1. **No excessive whitespace** - Fill slides with content, use colored blocks
2. **Punchy colors** - Bold, confident color blocks instead of subtle gradients
3. **Visual hierarchy** - Eyebrow labels, headlines, body text in clear order
4. **Interactive feel** - Floating cards, hover states, depth via shadows
5. **Contextual visuals** - Use brand mockups when discussing specific strategies

## Assets

- `assets/template.html` - Full HTML template with all 8 styles and complete CSS
