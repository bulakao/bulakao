# Bulakao Layout Audit

## Audit scope

The three-section Bulakao gateway at desktop, tablet, and mobile widths, using `https://agency.symph.co/` as optional comparison context for composition and pacing. The reference informed layout principles only; Bulakao keeps its own typography, color system, copy, and fixed star field.

## User goal and accessibility target

Make Partner and Solutions feel intentionally composed and clearly distinct without turning the homepage into a branching selector. Preserve a logical reading order, visible focus states, useful link labels, 52-pixel targets, and responsive reflow without horizontal scrolling.

## Strengths retained

- The approved copy gives each service a concrete job.
- Bree Serif, coral, gold, blue, and the fixed code-generated stars remain recognizable Bulakao assets.
- Three semantic sections and direct destination links keep the funnel simple.

## UX risks found

1. The earlier Hero used only part of the available desktop width, leaving the composition visually underweighted.
2. Partner placed its headline, description, value list, and CTA on separate offsets, so the asymmetry felt accidental.
3. Solutions repeated that loose arrangement in reverse, which made the two services feel like layout variations rather than two different operating models.
4. Outlined CTA boxes sat apart from their supporting copy instead of completing it.

## Implemented changes

1. **Hero — healthy.** The statement now runs across the wider page grid and anchors the lower half of the viewport, following the reference’s confident large-type pacing without copying its visual style.
2. **Partner — healthy.** A full editorial headline leads into one deliberate lower split: explanatory copy and CTA on the left, operating scope on the right.
3. **Solutions — healthy.** The offset headline and section index lead into a horizontal three-step process band, giving Solutions a system-oriented composition distinct from Partner.
4. **Responsive reflow — healthy.** The desktop structures collapse to one reading column, section indices become quiet background markers, and the process band becomes a vertical list.

## Accessibility risks and evidence limits

- Browser checks confirm no horizontal overflow at 1440, 768, or 390 pixels; links remain 52 pixels high; the fixed background remains singular; and the console is clean.
- Screenshots support visible hierarchy and reflow findings but do not establish full assistive-technology or WCAG conformance. A screen-reader pass and zoom testing beyond the captured widths remain separate verification work.

## Evidence

### Reference

- `reference/01-symph-hero.png`
- `reference/02-symph-contrast.png`
- `reference/03-symph-process.png`

### Before

- `before/01-bulakao-hero.png`
- `before/02-bulakao-partner.png`
- `before/03-bulakao-solutions.png`

### After

- `after/01-bulakao-hero.png`
- `after/02-bulakao-partner.png`
- `after/03-bulakao-solutions.png`
- `after/04-bulakao-mobile-hero.png`
- `after/05-bulakao-mobile-partner.png`
- `after/06-bulakao-mobile-solutions.png`
