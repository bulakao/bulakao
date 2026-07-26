# Bulakao Gateway Design QA

**Source visual truth:** `audits/source/bulakao-gateway-selected-reference.png`

**Implementation evidence:**

- `audits/implementation/home-desktop-hero.png`
- `audits/implementation/home-desktop-partner.png`
- `audits/implementation/home-desktop-solutions.png`
- `audits/implementation/home-tablet-hero.png`
- `audits/implementation/home-mobile-hero.png`
- `audits/implementation/home-mobile-partner.png`
- `audits/implementation/home-mobile-solutions.png`

**Combined comparison:** `audits/bulakao-gateway-comparison.png`

## Capture normalization

- Source visual: 864 × 1821 pixels, tall desktop concept.
- Desktop implementation: 1440 × 1024 CSS viewport and 1440 × 1024 screenshot pixels.
- Tablet implementation: 768 × 1024 CSS viewport and 768 × 1024 screenshot pixels.
- Mobile implementation: 390 × 844 CSS viewport and 390 × 844 screenshot pixels.
- Device density: 1 CSS pixel per screenshot pixel.
- State: dark theme, star field loaded, reveal transitions settled, no hover or focus lock.
- The selected concept is a compressed full-page mock, while the implementation gives each of the three sections a practical viewport-scale reading experience. Fidelity was judged section by section rather than by total page height.

## Findings

No actionable P0, P1, or P2 issues remain.

### Required fidelity surfaces

- **Fonts and typography:** Bree Serif remains the display face and the system sans-serif stack remains the body face. The implementation preserves the concept’s strong serif hierarchy while adjusting line wrapping for readable desktop, tablet, and mobile compositions. No text clips or truncates.
- **Spacing and layout rhythm:** Hero, Partner, and Solutions remain distinct sections with generous negative space and light dividers. The revised structure uses fewer, stronger alignments: the Hero runs wide; Partner pairs a full editorial headline with a lower copy/list split; Solutions offsets its headline against a large section index and ends in a three-part process band.
- **Colors and visual tokens:** Near-black, off-white, muted gray, coral, gold, and sky blue map directly to the Bulakao family. Accent colors retain sufficient contrast on the fixed night background.
- **Image quality and asset fidelity:** The generated concept is used only as a design reference. Production uses no photographic space image, repeated background image, placeholder art, or rasterized UI. One fixed background contains the deterministic code-generated star field requested by the user.
- **Copy and content:** The hero now leads with the shared customer problem: campaigns and operations accumulating loose ends. Partner makes campaign ownership concrete from matching through reporting; Solutions names a practical entry point—one costly manual workflow—and explains how the work improves from real use. Cosmic metaphors, agency filler, and branching-site language were removed.
- **Icons and controls:** The final design does not require decorative icons. CTA controls use underlined text links and color states consistent with the selected editorial direction.
- **Responsiveness:** No horizontal overflow at 1440, 1280, 768, or 390 pixels. Desktop asymmetry collapses into a clear single-column mobile reading order. CTA targets are at least 52 pixels high.
- **Accessibility:** The page includes semantic headings, exactly three main sections, a skip link, visible focus rules, keyboard-focusable links, reduced-motion handling, and practical tap targets.

## Primary interactions tested

- `See how Partner works` resolves to `https://partner.bulakao.com/`.
- `See what Solutions builds` resolves to `https://solutions.bulakao.com/`.
- Header wordmark resolves to the page top.
- Skip link resolves to `#main`.
- All four anchors have `tabIndex: 0`.
- Fixed background remains `position: fixed` throughout scrolling.
- Browser console contains no errors or warnings.

## Comparison history

1. **Earlier P2 — uniform alignment felt templated.**
   - Evidence: the selected reference aligned Hero, Partner, and Solutions to one common left edge.
   - User impact: the repetition made the page feel mechanically generated and visually predictable.
   - Fix: kept the three-section structure, typography, palette, and one star field, but rebuilt the desktop composition on an asymmetric twelve-column grid.
   - Post-fix evidence: `audits/bulakao-gateway-comparison.png`, plus the three desktop implementation captures.

2. **Post-fix pass.**
   - Partner and Solutions now have different spatial structures without becoming mirrored cards or a branching selector.
   - Mobile preserves a straightforward reading order rather than forcing desktop offsets into a narrow viewport.
   - No additional P0, P1, or P2 findings were identified.

3. **Copy audit implementation.**
   - Earlier issue: the hero described the business category instead of the customer problem, while both service sections relied on broad agency language.
   - Fix: rewrote the hero around fewer operational loose ends; gave Partner specific campaign responsibilities and one accountable owner; gave Solutions a one-workflow starting point, an implementation mechanism, and a real-use feedback loop.
   - CTA labels now preview the destination rather than using generic exploration language.
   - Post-fix evidence: the refreshed desktop and mobile implementation captures listed above.

4. **Layout audit and rebuild.**
   - Earlier issue: the service headline, body, list, and CTA each occupied separate offsets, making the asymmetry feel incidental instead of composed.
   - Reference context: `https://agency.symph.co/` demonstrated the value of wide statements, strong section indices, clear lower information bands, and fewer competing alignment points.
   - Fix: widened the Hero; rebuilt Partner as an editorial split; rebuilt Solutions as an offset proposition followed by a horizontal process band; replaced detached outline buttons with integrated text links.
   - Post-fix evidence: `audits/layout-2026-07-26/after/`, plus the refreshed implementation captures listed above.

## Open Questions

None blocking.

## Implementation Checklist

- [x] Three sections only: Hero, Partner, Solutions.
- [x] One fixed code-generated star background.
- [x] Concrete value-led copy.
- [x] Working destination links.
- [x] Desktop, tablet, and mobile verification.
- [x] Metadata, structured data, social image, robots, sitemap, and CNAME alignment.

## Follow-up Polish

- P3: If the live site later needs stronger cross-site continuity, the wordmark can adopt a shared production logo asset across all three repositories without changing this layout.

final result: passed
