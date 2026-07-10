# Bulakao UI/UX Audit

Date: 2026-07-09
Surface: `http://127.0.0.1:4173/`
Mode: Combined UI/UX and accessibility-risk audit

## Captured Steps

1. `01-desktop-entry.png`
   - Health: strong.
   - Shows the main offer, quick-pick buttons, and workflow-map form in the first desktop viewport.

2. `02-desktop-chip-filled.png`
   - Health: mixed.
   - The Inventory chip fills the textarea correctly, but focus moves to the textarea and scrolls the page so the top of the hero is clipped.

3. `03-desktop-output.png`
   - Health: solid.
   - Shows the output/value section with three deliverables.

4. `04-mobile-entry.png`
   - Health: solid with one concern.
   - The hero and chips fit without horizontal overflow, but the form begins below the first mobile viewport.

## Strengths

- The page now has a clear job: get the visitor to submit one rough workflow.
- The headline is concrete enough to understand quickly: one manual workflow becomes software.
- The first desktop viewport shows both the promise and the form, which reduces CTA friction.
- Quick-pick buttons are useful because they help a visitor start without writing from scratch.
- The form labels are explicit and the textarea placeholder gives a realistic example.
- The visual identity is cohesive: Bree Serif, night background, comet, gold CTA.
- The output section explains what the user gets before committing to a build.
- Mobile has no horizontal overflow in the captured state.
- Console had no relevant errors or warnings during capture.

## UX Risks

- The hero headline is visually heavy. It creates drama, but it pushes the page toward spectacle and can compete with the form.
- The quick-pick click behavior causes an abrupt scroll/focus jump on desktop. This makes the page feel less controlled and partially hides the main headline.
- The form asks for email before the workflow. For this kind of action-first page, the workflow field may be the more natural first input.
- The `Start` nav label is vague. It jumps to the form, but the outcome is more specifically a workflow map.
- The quick-pick chips fill the textarea, but there is no visible selected state. Users may not realize a chip was applied if the scroll position changes.
- The output section is clear, but it is spatially distant from the form. The strongest proof substitute, "You get a workflow map and first-build plan," may deserve more prominence above the fold.
- The page still relies on trust by assertion. There is no example of a workflow map, sample build plan, or before/after sketch.

## Accessibility Risks

- Focus behavior after chip click needs review. Moving focus to the textarea is defensible, but the resulting scroll jump can be disorienting.
- Quick-pick buttons should expose selected/pressed state if selection becomes persistent. Consider `aria-pressed` and visible selected styling.
- The gold CTA likely has acceptable contrast against dark text, but contrast should be checked with computed colors before launch.
- Placeholder text should not be the only instruction. The page has a label, which is good, but the example may be too low-contrast for some users.
- Screenshot review cannot confirm keyboard order, screen-reader announcement quality, or full WCAG compliance.

## Recommended Fixes

1. Keep the action-first layout.
   - This is the right strategic direction. Do not go back to a long service brochure.

2. Change the chip behavior.
   - Fill the textarea without forcing focus, or scroll the form into a stable position intentionally.
   - Add selected styling to the chosen chip.
   - Status: addressed. Chips now use a visible selected state with `aria-pressed`, fill the workflow textarea, and keep the hero position stable.

3. Put the workflow field before email.
   - Let the user start with the problem first, then ask for email after they are invested.
   - Status: addressed. The workflow textarea now appears before the email field.

4. Make the nav CTA more specific.
   - Replace `Start` with `Get the map` or `Workflow map`.

5. Add one concrete sample.
   - A small "Example map" or "From messy input to first-build plan" block would increase trust without adding much page weight.

6. Slightly reduce hero type scale.
   - Keep the strong Bree Serif look, but give the form more breathing room and reduce the sense of visual shouting.

7. Move proof closer to the form.
   - The "You send / You get / Then build" block is good. Keep it near the CTA and make it scan faster.

## Evidence Limits

- This audit used screenshots and light DOM checks from the local rendered page.
- It did not test screen readers, real email-client behavior from `mailto:`, form submission analytics, or performance metrics.
- It did not compare against user behavior data because none is available yet.
