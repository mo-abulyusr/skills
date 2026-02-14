---
name: visual-qa
version: 2.0.0
description: >
  Autonomous visual QA loop for any website or web application. Use when asked to
  "visual QA", "screenshot review", "design review", "visual polish",
  "pixel perfect", "check the design", or "screenshot loop". Captures
  screenshots at desktop/tablet/mobile, analyzes against a 12-category
  checklist, fixes issues, and re-verifies — all autonomously.
---

# Visual QA

Autonomous screenshot-driven visual review for any website or web application.
Captures the live site at three viewports, evaluates against a comprehensive
checklist, fixes issues in code, and re-screenshots to verify — in a tight loop.

## Prerequisites

Before starting, confirm two things:

1. **Dev server is running.** Ask the user for the dev server URL if not obvious. Check that it responds:
   ```bash
   curl -s -o /dev/null -w "%{http_code}" <DEV_SERVER_URL>
   ```
   If not running, look for a `package.json` `dev` script or framework-specific start command and launch the server. Wait a few seconds and re-check the URL.

2. **Playwright is available.** Check common installation paths:
   ```bash
   which playwright || /opt/homebrew/bin/playwright --version || npx playwright --version
   ```

If either prerequisite fails, stop and tell the user.

## Screenshot Commands

Use these exact commands. `--wait-for-timeout 3000` lets fonts load and canvas
animations initialize. `--full-page` captures the entire scrollable page.

| Viewport | Command |
|----------|---------|
| **Desktop (1440 x 900)** | `/opt/homebrew/bin/playwright screenshot --viewport-size "1440,900" --full-page --wait-for-timeout 3000 <url> /tmp/vqa-desktop.png` |
| **Tablet (768 x 1024)** | `/opt/homebrew/bin/playwright screenshot --viewport-size "768,1024" --full-page --wait-for-timeout 3000 <url> /tmp/vqa-tablet.png` |
| **Mobile (iPhone 13)** | `/opt/homebrew/bin/playwright screenshot --device "iPhone 13" --full-page --wait-for-timeout 3000 <url> /tmp/vqa-mobile.png` |

Replace `<url>` with the confirmed dev server URL (usually `http://localhost:3000`).

## Core Loop Protocol

Run four phases in order. Each phase follows the same cycle:
**Screenshot -> Read Image -> Evaluate -> Report -> Fix -> Re-screenshot -> Verify**

### Phase 1: Desktop (1440 x 900)

1. Take a desktop screenshot.
2. Read the image with your vision capability.
3. Evaluate against ALL 12 categories in [references/visual-qa-checklist.md](references/visual-qa-checklist.md).
4. Report findings grouped by severity:
   - **Critical** — Broken layout, unreadable text, missing sections
   - **Major** — Inconsistent spacing, misaligned elements, poor contrast
   - **Minor** — Sub-pixel alignment, polish details
5. Fix **Critical** issues first, then **Major**. Skip Minor for now.
6. Re-screenshot and verify fixes didn't introduce regressions.
7. Repeat up to **3 cycles** max. If issues persist after 3, report them and move on.

### Phase 2: Tablet (768 x 1024)

Same loop as Phase 1, but focus specifically on:
- Responsive layout shifts and breakpoint behavior
- Content reflow and stacking order
- Navigation collapse behavior
- Image scaling and aspect ratios
- Grid layout at this intermediate width

### Phase 3: Mobile (iPhone 13 — 390 x 844)

Same loop as Phase 1, but focus specifically on:
- Touch target sizes (minimum 44 x 44px)
- Text readability (minimum 16px body text)
- Vertical stacking order and spacing
- No horizontal scroll or overflow
- CTA button prominence and reachability
- Content priority and information hierarchy

### Phase 4: Cross-Viewport Comparison

1. Read all three final screenshots side by side (desktop, tablet, mobile).
2. Check for:
   - Consistent brand presentation across viewports
   - Smooth content degradation from wide to narrow
   - No elements that look great on one viewport but broken on another
   - Consistent color, typography, and spacing patterns
3. Report any cross-viewport inconsistencies found.

## Codebase Conventions

Before making fixes, **discover the project's design tokens dynamically**. Inspect these files (check whichever exist):
- `globals.css`, `global.css`, `app.css`, or similar root stylesheet
- `tailwind.config.*` (theme extensions)
- `theme.*`, `tokens.*`, or design-system config files
- CSS custom properties defined on `:root`

### Colors (discover from project)
Look for CSS custom properties or Tailwind theme values. Build a table like:

| Token | Value | Usage |
|-------|-------|-------|
| `--color-bg` | *(from project)* | Page background |
| `--color-text-primary` | *(from project)* | Headings, primary text |
| `--color-text-body` | *(from project)* | Body copy |
| `--color-text-secondary` | *(from project)* | Secondary/muted text |
| `--color-border` | *(from project)* | Borders, dividers |

### Typography (discover from project)
Look for font-family declarations, `@font-face` rules, or Tailwind font config:

| Token | Value | Usage |
|-------|-------|-------|
| `--font-display` | *(from project)* | Headings — note weight and letter-spacing |
| `--font-body` | *(from project)* | Body text — note weight |

### Patterns (discover from project)
Look for recurring values in the stylesheets:
- Transition timing (e.g., `0.3s ease`)
- Hover state conventions (opacity, color shift, underline, etc.)
- Navigation animation patterns
- Layout offsets or sidebar widths

## Reporting Format

After completing all four phases, present a summary:

```
## Visual QA Summary

### Changes Made
- [file:line] Description of what was fixed and why

### Remaining Issues
- [severity] Description (couldn't fix because...)

### Viewport Status
- Desktop: [PASS / n issues remaining]
- Tablet: [PASS / n issues remaining]
- Mobile: [PASS / n issues remaining]
- Cross-viewport: [PASS / n inconsistencies]
```

## Safety Rails

1. **3-cycle cap per viewport.** If an issue isn't fixed after 3 screenshot-fix-verify cycles within a single phase, report it and move to the next phase. Do not loop indefinitely.
2. **Don't change design direction.** Fix implementation bugs (spacing, alignment, overflow, contrast). Do NOT redesign sections, change the color palette, swap fonts, or alter the layout concept. If you believe a design-level change is needed, flag it and ask the user.
3. **Verify before moving on.** Complete each viewport phase fully before starting the next. Don't fix desktop + tablet + mobile all at once then verify — verify after each phase.
4. **Minimize blast radius.** Make the smallest CSS/markup change that fixes the issue. Prefer utility classes over custom CSS. Prefer adjusting existing values over adding new rules.

## Related Skills

- **[page-cro](../../cro/page-cro/SKILL.md)** — Conversion optimization for landing pages
- **[copy-editing](../../content-and-copy/copy-editing/SKILL.md)** — Text quality and readability
- **[seo-audit](../../seo/seo-audit/SKILL.md)** — Technical and on-page SEO
