# Bulakao Site Spec

## Purpose

Bulakao is becoming a custom workflow software site for teams that need software built around the way their work actually happens.

The first version should be a one-page landing site with an original Bulakao identity: comet, stars, night sky, movement, navigation, and the feeling of turning scattered work into a clear path.

## Brand Direction

### Name

Bulakao.

### Meaning

Bulakao refers to a comet or shooting star. The design should lean into that celestial meaning without becoming decorative fluff.

### Brand Metaphor

Businesses often have scattered tools, messages, spreadsheets, and manual handoffs. Bulakao should feel like a bright moving object in the night sky: focused, directional, and capable of turning scattered points into a constellation.

### Desired Feeling

- Clear, calm, and capable.
- Night-sky atmosphere, not cartoon space.
- Technical but human.
- Premium enough for serious business buyers.
- Early-stage and approachable, not corporate-heavy.

### Visual Motifs

- Deep night background.
- Star fields and subtle constellations.
- One or more comet trails as directional accents.
- Soft glows used sparingly.
- Thin orbital/path lines where they help guide the eye.
- Product UI examples that feel like cockpit panels, maps, dashboards, or mission control without becoming sci-fi.

### Avoid

- Generic SaaS purple gradient look.
- Overly literal rockets/planets/astronauts.
- Emoji-heavy visuals.
- Text that clips offscreen for the sake of drama.

## Design Basis

Bulakao should be designed from its own offer and identity.

What to preserve:

- The action-first direction.
- The focused custom workflow software positioning.
- The plain-language buyer education.
- The sections that reduce risk: what the user sends, what they get, and what happens next.
- The use of a workflow brief as the primary first interaction.

What to keep improving:

- Strengthen Bulakao's comet/night identity without letting visuals overpower the form.
- Add true Bulakao proof or honest early-stage alternatives.
- Improve responsive typography, chip behavior, and form flow.
- Make the visual system feel original.
- Keep copy in Bulakao's own language: short, concrete, and tied to action.

## Site Architecture

This repo is currently a static GitHub Pages site:

- `index.html`: full page HTML, CSS, and JavaScript.
- `CNAME`: custom domain config.
- `.github/workflows/static.yml`: deploys the repo to GitHub Pages.
- `README.md`: short project description.
- `SPEC.md`: product/design/build spec.
- `.env`: local-only form/backend keys. Do not commit.

For the next build, keep the architecture static unless we need more complexity.

Recommended first implementation:

- Single `index.html`.
- Inline CSS and JS are acceptable for v1.
- No framework unless the page grows into reusable components or complex interactivity.
- Keep the page deployable through the existing GitHub Pages workflow.

Possible later architecture:

- Move styles to `styles.css` if the file becomes hard to scan.
- Move animation logic to `script.js` if canvas/scroll effects become complex.
- Add a simple form backend later through Formspree, Tally, Netlify Forms, Basin, or a custom API.
- Current form backend: Web3Forms posting to `https://api.web3forms.com/submit`.

## Page Structure

### 1. Header

Purpose: lightweight orientation and persistent CTA.

Content:

- Brand: `Bulakao`.
- Small definition under brand: `[bu.la.kaw] : a shooting star.`
- Optional short descriptor: `Custom software for operations`.
- CTA: `Start` or `Get started`.

Design:

- Transparent or dark translucent header.
- Subtle star/noise background behind it.
- Small comet dot or mark near the brand.

### 2. Hero

Purpose: communicate the offer in one screen.

Working headline options:

- `Still running operations through spreadsheets and chat?`
- `Custom software for the work your team actually does.`
- `Turn scattered work into software that moves.`

Supporting copy:

- `Send the messy process. Bulakao turns one painful workaround into a custom internal tool your team can actually use.`

CTA:

- Primary: `Send message`
- Secondary: `See what we build`

Design:

- Night sky background.
- Subtle animated star field.
- A comet trail that crosses or frames the hero content.
- Large type, but responsive and never clipped.

### 3. Pain Section

Purpose: show the cost of the current alternatives.

Pattern:

- `Software that almost fits` -> `manual workarounds`
- `Spreadsheets and inboxes` -> `hidden bottlenecks`
- `Traditional custom builds` -> `large upfront risk`

Design:

- Light or dark contrast band.
- Minimal table-like comparison.
- Strikethrough or dimmed text can be used carefully.

### 4. Better Path / Offer

Purpose: position Bulakao as the lower-risk custom path.

Working copy:

- `Custom software, built monthly.`
- `Start with one workflow that is costing you time. We map it, build the first useful tool, and improve the system with you.`

Pricing:

- Do not show pricing yet.
- Revisit pricing only after the offer, scope, and pilot structure are clearer.
- If pricing is added later, prefer one simple pilot starting point over a package table.

### 5. What We Build

Purpose: make the offer concrete.

Example chips:

- Operations dashboards
- Approval queues
- Client portals
- Inventory trackers
- Booking systems
- Order boards
- Field reports
- Reporting tools
- Internal admin tools
- AI-assisted workflows

Design:

- Chips should wrap cleanly on mobile and desktop.
- Add small star/dot markers if it fits the identity.

### 6. Value Proposition

Purpose: explain why this model is better.

Cards:

- `Built around your process`
  - `Send the spreadsheet, form, messages, screenshots, or approval flow you use today.`
- `Useful first tool fast`
  - `Start with a focused tool that can remove real friction.`
- `Monthly improvements`
  - `Keep improving the software as your work changes.`
- `Same context`
  - `The team that learns the workflow keeps building with you.`

Design:

- Dark cards with thin borders and subtle comet-glow highlights.
- Avoid heavy nested cards.

### 7. Realistic Workflow Screens

Purpose: show what Bulakao can build even before case studies exist.

Mock product examples:

- Order operations dashboard.
- Approval queue.
- Client portal.
- Booking calendar.
- Inventory tracker.
- Field report review screen.

Design:

- Original UI mockups only.
- Use dense, useful interface examples.
- No placeholder boxes.
- These should look like real internal tools.

### 8. Process

Purpose: make starting feel easy.

Working sequence:

1. `Send`
   - `Send the spreadsheet, screenshots, process doc, or plain-English problem.`
2. `Map`
   - `We map the screens, data, roles, edge cases, and first useful tool.`
3. `Launch`
   - `Your team starts using the tool, then we keep improving it monthly.`

Alternative sequence:

1. `Map the sky`
2. `Build the path`
3. `Keep moving`

Use plain business language first; poetic labels can be secondary.

### 9. Good Fit / Not Fit

Purpose: qualify leads and build trust.

Good fit:

- Teams replacing spreadsheets, inbox approvals, or manual reporting.
- Owners/operators who can explain the daily workflow.
- Businesses that want a working tool before a huge fixed-scope project.

Not fit:

- Website template shopping.
- Staff augmentation only.
- Ideas with no clear workflow owner.
- Buyers who need a long fixed plan before validating the first tool.

### 10. Proof

Purpose: establish credibility honestly.

Use only true facts.

Possible early-stage proof:

- Founder/operator story.
- Existing software projects.
- Open source or shipped product examples.
- Screenshots of realistic sample tools.
- Pilot offer.
- Clear working process.

Do not fabricate:

- Client logos.
- Years in business.
- Number of products shipped.
- Team size.

### 11. Comparison

Purpose: explain how Bulakao differs from alternatives.

Columns:

- Generic tools
- Consultants
- Bulakao

Message:

- Generic tools are fast but force process compromises.
- Consultants can be powerful but often require heavy upfront commitment.
- Bulakao starts with the workflow and improves monthly.

### 12. FAQ / SEO Answers

Purpose: answer buyer questions and make the page indexable.

Questions:

- What should I send?
- What happens after I send it?
- Do I need a polished brief?
- What can Bulakao build?
- Can you work with our current tools?
- How small can we start?

Later candidates:

- How much does a pilot build cost?
- Can Bulakao work with our existing tools?
- How long does the first useful tool take?
- Who is this best for?

Revision plan:

- Make the FAQ a single-column, compact accordion instead of a two-column card grid.
- Reduce the FAQ heading scale so it supports the page rather than dominating it.
- Keep closed FAQ rows short and scan-friendly.
- Add a simple CTA directly under the FAQ.
- Use plain CTA labels: `Start`, `Get started`, or `Send message`.
- Avoid using `workflow map` in buttons or primary FAQ questions. Keep method language internal unless the page has already made the idea clear.

### 13. Contact

Purpose: convert interest into a conversation.

Fields:

- Email.
- What needs to work better?
- Optional: company/name.

CTA:

- `Send your workflow`
- `Start mapping`
- `Send my build idea`

Implementation note:

- For v1, the form can use a `mailto:` fallback or static placeholder.
- Add a real submission backend later.

## Interaction And Motion

Motion should feel like a comet crossing a night sky: calm, directional, and purposeful.

Possible v1 motion:

- Canvas star field.
- Slow comet trail in the hero.
- Subtle parallax on stars.
- Scroll-revealed sections.
- Hover glow on chips/cards/buttons.

Accessibility rules:

- Respect `prefers-reduced-motion`.
- Avoid motion that blocks reading.
- Keep text readable over animated backgrounds.
- Do not rely on motion to communicate critical content.

## Design System Draft

### Colors

- Night: `#03050b`
- Deep space: `#080d1a`
- Ink: `#101624`
- Star white: `#f7f3ea`
- Moon gray: `#a9adba`
- Comet gold: `#f5c76b`
- Ion blue: `#70d6ff`
- Aurora green accent: `#9ff3c8`

Use gold/blue/green as accents, not full-page gradients.

### Typography

Current site uses a large serif display style. For this version:

- Display: consider keeping a warm serif or switching to a strong grotesk.
- Body: clean sans-serif for readability.
- Avoid viewport-width-based text sizing.
- Use `clamp()` with sensible min/max sizes.

### Layout

- Full-width bands.
- Constrained inner content.
- Large breathing room.
- Responsive grids.
- No cards inside cards.
- Cards max radius around `8px` unless a stronger system emerges.

## Content Voice

Plainspoken, confident, and specific.

Good:

- `Show us where work gets stuck. We will shape it into software your team can actually use.`
- `Start with one messy workflow and turn it into a clearer system.`
- `Launch a focused first tool, then keep refining it as the work changes.`

Avoid:

- Vague innovation language.
- Generic "digital transformation" phrasing.
- Over-poetic space metaphors that obscure the business value.
- Copy that sounds like a borrowed landing-page template.
- Repeating common service claims without making them specific to Bulakao's offer.

## Copy Differentiation Rules

Bulakao copy should sound like its own offering: direct, useful, and built around the workflow-map offer.

Rules:

- Use Bulakao's core metaphor: scattered work, night navigation, comets, paths, signals, constellations, and momentum.
- Keep the metaphor secondary to clarity. Business buyers should understand the offer before noticing the poetry.
- Prefer verbs like `map`, `shape`, `launch`, `refine`, `untangle`, `connect`, `guide`, and `orbit` only when they fit naturally.
- Create original CTA language.
- Replace generic service claims with specific Bulakao claims once the offer is known.
- Before launch, rewrite anything that feels generic, derivative, or too clever to understand quickly.

Do not use these phrases as primary copy:

- `Your workflow is unique. Your software should be too.`
- `Custom software built around your workflow.`
- `Fast first tool, monthly improvements`
- `No large upfront build fee`
- `Start with the workflow that is costing you time`
- `Tell us what you need built`
- `Software that almost fits`
- `Same team, same context`

Possible Bulakao-native replacements:

- `Turn scattered operations into custom software.`
- `When the work no longer fits the tools, build around the work.`
- `We map the moving parts, launch the first useful tool, and keep improving from there.`
- `Bring the spreadsheet, the inbox trail, the screenshots, or the messy process.`
- `Start with one bottleneck. Leave with a system your team can run on.`
- `Map a workflow`
- `Show us the bottleneck`
- `Build the first tool`

## SEO

Primary themes:

- Custom software studio.
- Custom workflow software.
- Internal tools.
- Client portals.
- Approval workflows.
- Dashboard development.
- Software for small business operations.

Metadata should include:

- Title.
- Description.
- Canonical URL.
- Open Graph tags.
- Twitter card tags.
- Structured data for organization/service.

## Technical Requirements

- Static GitHub Pages compatible.
- Works without a build step.
- Responsive from mobile to desktop.
- Good Lighthouse basics:
  - readable contrast,
  - semantic headings,
  - form labels,
  - image alt text if images are added,
  - reduced-motion support.
- Keep external dependencies minimal.
- Avoid large assets unless they materially improve the page.

## First Build Plan

1. Replace the current splash page with the landing page skeleton.
2. Preserve the current celestial identity through a better night-sky/comet visual system.
3. Build the full one-page layout with placeholder-but-polished copy.
4. Add responsive styles.
5. Add lightweight star/comet animation.
6. Add realistic workflow UI mockups in HTML/CSS.
7. Add contact form shell.
8. Test desktop and mobile.
9. Iterate copy and business offer.

## Open Questions

- What exact offer should Bulakao sell first?
- Will pricing be public?
- Which market should the first copy target: Philippines, US, global, or local Cebu/Philippines businesses?
- Should Bulakao sell one-off projects, monthly retainers, or both?
- What proof can be used honestly on launch?
- What contact destination should the form use?

## Todo

### Now

- [ ] Confirm first-page copy direction.
- [ ] Decide whether to keep pure static HTML or split CSS/JS.
- [ ] Draft first version of landing page.
- [ ] Revisit pricing only after the offer is clearer.
- [ ] Create original workflow UI mockups.
- [ ] Add responsive comet/star animation.
- [ ] Add accessible contact form markup.

### Later

- [ ] Add real form handling.
- [ ] Add case studies or pilot project pages.
- [ ] Add real client/project proof.
- [ ] Add analytics.
- [ ] Add performance pass.
- [ ] Add social preview image.
- [ ] Consider a reusable component structure if the site grows.

## Build Principle

The site should not just say Bulakao builds custom software. It should feel like Bulakao can take scattered business work and draw a clear constellation from it.

## Current Design Direction

The active direction is action-first restraint, not brochure-page density.

Principles:

- One clear idea per section.
- The first viewport should let the visitor do the thing, not just read about it.
- The first build should read as the entry point into an ongoing software relationship, not the ceiling of the offer.
- One primary CTA path: send one rough project note.
- Large, calm hero typography using the existing `Bree Serif` Bulakao font.
- Short copy that sounds like action, not explanation.
- A useful intake form is more important than a fake product mockup.
- Stars, night, and comet imagery as quiet atmosphere.
- Motion should stay quiet: uneven scattered stars, denser star clusters, varied twinkle speeds, multiple occasional comets in different sizes, parallax depth, and small CTA/selection feedback. Avoid obvious diagonal constellation lines.
- The final Start small section can reuse the star field behind the section content, but not inside the form card.
- The final form should stay compact: starter chips, message, reply email, submit. Avoid adding a process explainer under the form.
- Middle sections should use subtle dark-band contrast, soft separators, and small star/dot accents so the page has rhythm without switching to a light theme.
- No dense feature grids, long proof sections, long FAQ stacks, or heavy comparison tables in v1.

Current page shape:

1. Header with Bulakao and `Start`.
2. Hero question: `Still running operations through spreadsheets and chat?`
3. Hero copy stays focused on the problem.
4. Example build section showing one painful workaround becoming a usable internal tool.
5. Growth path section showing one workflow becoming a first tool, then an improving system.
6. Minimal build list.
7. Compact FAQ for pre-contact questions.
8. Quick-pick project chips live inside the final form as starter shortcuts and fill the message.
9. Project message form at the end of the page as the final conversion point. The form posts to Web3Forms and shows inline success/error status.
10. Footer repeats the Bulakao brand lockup with comet mark and `[bu.la.kaw] : a shooting star.`

Current copy direction:

- `Still running operations through spreadsheets and chat?`
- `Send the messy process. Bulakao turns one painful workaround into a useful internal tool, then keeps improving the system as the work grows.`
- Primary CTA: `Send message`, `Get started`, or `Start`.
- Avoid CTA labels that require understanding Bulakao's internal method, such as `Get my workflow map`.
- `You send: a rough note. You get: a clear next step and first-build plan.`
- `Start with one workflow. Grow into the system.`
- `The first build is the starting point, not the ceiling.`
