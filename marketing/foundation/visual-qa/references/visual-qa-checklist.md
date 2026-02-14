# Visual QA Checklist

Comprehensive 12-category checklist for visual inspection. Work through every
category on each screenshot. Mark items as PASS, FAIL (with details), or N/A.

---

## 1. Spacing & Layout

- [ ] Consistent vertical rhythm between sections (equal or intentionally varied)
- [ ] Section padding follows a predictable scale (not arbitrary values)
- [ ] No content touching container edges without padding
- [ ] Adequate breathing room around text blocks
- [ ] No unexpected overflow causing horizontal scroll
- [ ] Margins collapse predictably (no double-spacing or missing gaps)
- [ ] Spacing between heading and its content is tighter than spacing between sections
- [ ] Footer has sufficient top margin separating it from content
- [ ] Hero section has appropriate vertical space for visual weight

## 2. Typography

- [ ] Clear size hierarchy: H1 > H2 > H3 > body > small/caption
- [ ] Line-height appropriate for each text size (1.4-1.6 for body, 1.1-1.3 for headings)
- [ ] Line length does not exceed ~75 characters for body text
- [ ] Fonts loaded correctly (no FOUT/FOIT visible in screenshot)
- [ ] No orphaned words (single word on last line of a paragraph)
- [ ] No widows (single line of a paragraph at top of next column/page)
- [ ] Letter-spacing matches project design tokens
- [ ] Font weights match project's defined font weights
- [ ] Text color uses project's defined text color tokens
- [ ] No text truncation or ellipsis where full text should show

## 3. Color & Contrast

- [ ] Body text on background meets WCAG AA (4.5:1 minimum contrast ratio)
- [ ] Large text (18px+ or 14px+ bold) meets 3:1 minimum contrast
- [ ] Secondary/muted text (secondary text on background) still readable
- [ ] All colors come from the defined palette (no rogue hex values)
- [ ] Links are visually distinguishable from surrounding text
- [ ] No adjacent sections with indistinguishable background colors
- [ ] Accent color usage is intentional and consistent
- [ ] Border color (uses project's defined border color) provides subtle but visible separation

## 4. Alignment & Grid

- [ ] Content aligns to a consistent grid or max-width container
- [ ] Horizontal alignment is consistent within sections (all left, all center, etc.)
- [ ] Centered text is truly centered (not offset by padding/margin)
- [ ] Multi-column layouts have equal column widths or intentional asymmetry
- [ ] Card grids handle orphans gracefully (last row with fewer items)
- [ ] Left edges of text blocks align vertically across sections
- [ ] No elements visually "floating" outside the implied grid
- [ ] Project-specific layout offsets are consistently applied

## 5. Responsive Behavior

- [ ] No horizontal scrollbar at any tested viewport width
- [ ] Breakpoints transition cleanly (no awkward in-between states)
- [ ] Images scale proportionally (no squishing or stretching)
- [ ] Text doesn't overlap or get cut off at narrower widths
- [ ] Stack order makes sense on mobile (most important content first)
- [ ] Touch targets are at least 44 x 44px on mobile
- [ ] Font sizes scale appropriately (not too large on mobile, not too small)
- [ ] Navigation is usable at every viewport
- [ ] Multi-column layouts collapse to single column at mobile
- [ ] No elements that are too wide for their container

## 6. Buttons & Interactive Elements

- [ ] All buttons have consistent padding and border-radius
- [ ] Primary CTA is visually prominent (highest contrast, largest size)
- [ ] Secondary actions are visually subordinate to primary CTA
- [ ] Button text has adequate padding on all sides
- [ ] Click/tap target area is large enough (minimum 44 x 44px on touch)
- [ ] Hover states exist and follow project's hover conventions
- [ ] Focus states are visible for keyboard navigation
- [ ] Interactive elements have appropriate cursor styles (pointer for clickable)
- [ ] No buttons that look disabled but are actually active (or vice versa)

## 7. Borders & Shadows

- [ ] Border color is consistent (uses project's border color token)
- [ ] Border weight is consistent across similar elements
- [ ] No doubled borders where elements touch (adjacent cards, stacked sections)
- [ ] Box shadows (if any) are consistent in offset, blur, and color
- [ ] Dividers and separators match the overall visual language
- [ ] No borders that are too heavy for the project's visual aesthetic

## 8. Animation & Motion

- [ ] No layout shift during or after animations (CLS)
- [ ] Animation timing is consistent (follows project's timing conventions)
- [ ] Animations use GPU-accelerated properties (transform, opacity)
- [ ] No janky or stuttering animations visible
- [ ] Reduced-motion media query is respected
- [ ] Canvas or background animations don't interfere with content readability
- [ ] Navigation animations work smoothly

## 9. Icons & Images

- [ ] No broken images (no alt text placeholders visible)
- [ ] Images maintain correct aspect ratio (not squished or stretched)
- [ ] Alt text is present on meaningful images (check markup if visual suggests issues)
- [ ] Icons are vertically aligned with adjacent text
- [ ] Icon sizes are proportional to surrounding text
- [ ] SVG icons are crisp at all resolutions (not blurry)
- [ ] Image placeholder background uses project's image placeholder background token
- [ ] No images causing layout shift as they load

## 10. Visual Polish

- [ ] No content clipping or being cut off by overflow:hidden
- [ ] No rogue scrollbars on elements that shouldn't scroll
- [ ] Cursor styles are correct (pointer on clickable, text on selectable, default elsewhere)
- [ ] Long text or dynamic content doesn't break layouts
- [ ] No visible rendering artifacts (hairline gaps, sub-pixel bleed)
- [ ] Background colors extend to full container edges (no white gaps)
- [ ] Transitions between sections are smooth (no jarring jumps)
- [ ] No z-index issues (elements overlapping incorrectly)

## 11. Consistency

- [ ] Repeated patterns are identical (all cards match, all section headers match)
- [ ] Spacing units are from a consistent scale (not arbitrary pixel values)
- [ ] Typography patterns are uniform (same style for same content type everywhere)
- [ ] Button styles are consistent throughout the page
- [ ] Icon style is consistent (all outline, all solid, or intentional mix)
- [ ] Color usage is consistent (same token for same purpose everywhere)
- [ ] Border/divider treatment is consistent across sections
- [ ] Heading levels correspond to visual hierarchy (H1 biggest, H2 next, etc.)

## 12. Accessibility

- [ ] Focus indicators are visible on interactive elements
- [ ] Heading hierarchy is logical (H1 → H2 → H3, no skipped levels)
- [ ] Semantic HTML elements are used (nav, main, section, article, footer)
- [ ] Form inputs have visible labels
- [ ] Tap targets have at least 8px spacing between them (WCAG 2.5.8)
- [ ] Text is resizable without breaking layout
- [ ] No information conveyed solely through color
- [ ] Skip-to-content or equivalent navigation aid exists
- [ ] ARIA labels present where visual meaning isn't conveyed by text
- [ ] Sufficient contrast on all interactive element states (default, hover, focus, active)
