# Skills for Claude Code

42 ready-to-use skills across 10 categories.

Drop a skill folder into `.claude/skills/`, and Claude will use it when the request matches.

## What This Repo Is

This repo is a library of reusable skills for Claude Code.

Each skill is a folder with a `SKILL.md` file and, when needed, supporting scripts, references, examples, or assets. A skill gives Claude a focused workflow for a specific kind of task instead of asking it to figure everything out from scratch every time.

## How Skills Work

1. You copy the skill folder into your project’s `.claude/skills/` directory.
2. Claude notices the skill when your request matches its purpose.
3. Claude reads the skill instructions and any supporting files before answering or taking action.

That means the skill becomes part of the working context, but only when it is relevant.

## Install

### One skill

```bash
cp -R marketing/cro/page-cro /path/to/your-project/.claude/skills/
```

### One category

```bash
cp -R marketing/seo/* /path/to/your-project/.claude/skills/
```

### What happens next

Once the skill is in `.claude/skills/`, you do not need to configure anything else.
Claude can use it automatically when the task fits.

## Browse By Category

| Category | Skills | What it covers |
|---|---:|---|
| CRO | 6 | Landing pages, forms, signup flows, onboarding, paywalls, popups |
| Content & Copy | 5 | Writing, editing, content planning, social content, email sequences |
| SEO | 4 | Audits, programmatic pages, schema, competitor alternatives |
| Analytics & Testing | 2 | Tracking and experimentation |
| Strategy & Growth | 7 | Pricing, launches, ideas, psychology, referrals, ads, free tools |
| Foundation | 2 | Shared marketing context and visual QA |
| Documents | 4 | Word, PDF, PowerPoint, and spreadsheet work |
| Design | 6 | UI, visual art, brand systems, themes, GIFs |
| Development | 4 | Skill creation, MCP servers, web artifacts, web testing |
| Communication | 2 | Internal comms and doc coauthoring |

## Catalog

### Marketing Skills

<details>
<summary><strong>CRO</strong> — 6 skills</summary>

- `page-cro` — Landing page and marketing page conversion optimization.
- `form-cro` — Lead, demo, contact, and checkout form optimization.
- `signup-flow-cro` — Registration and trial signup flow optimization.
- `onboarding-cro` — Post-signup activation and first-run experiences.
- `paywall-upgrade-cro` — In-app paywalls, upgrades, and feature gates.
- `popup-cro` — Popups, modals, overlays, and exit-intent prompts.

</details>

<details>
<summary><strong>Content & Copy</strong> — 5 skills</summary>

- `copywriting` — Marketing page copy and positioning.
- `copy-editing` — Copy review, tightening, and polish.
- `content-strategy` — Content planning, themes, and calendars.
- `social-content` — Social media content and campaign writing.
- `email-sequence` — Drip campaigns and email sequence writing.

</details>

<details>
<summary><strong>SEO</strong> — 4 skills</summary>

- `seo-audit` — Technical and on-page SEO audits.
- `programmatic-seo` — Template-driven pages at scale.
- `schema-markup` — JSON-LD and structured data.
- `competitor-alternatives` — Comparison pages and alternative pages.

</details>

<details>
<summary><strong>Analytics & Testing</strong> — 2 skills</summary>

- `analytics-tracking` — GA4, GTM, and event tracking.
- `ab-test-setup` — Experiment design and analysis.

</details>

<details>
<summary><strong>Strategy & Growth</strong> — 7 skills</summary>

- `pricing-strategy` — Pricing tiers and packaging.
- `launch-strategy` — Product launch planning.
- `marketing-ideas` — Growth tactics and campaign ideas.
- `marketing-psychology` — Mental models and persuasion patterns.
- `referral-program` — Referral and affiliate programs.
- `free-tool-strategy` — Engineering as marketing.
- `paid-ads` — Paid acquisition across major ad platforms.

</details>

<details>
<summary><strong>Foundation</strong> — 2 skills</summary>

- `product-marketing-context` — Shared marketing context for other skills.
- `visual-qa` — Screenshot-driven visual quality checks.

</details>

### Anthropic Official Skills

<details>
<summary><strong>Documents</strong> — 4 skills</summary>

- `docx` — Word document creation and editing.
- `pdf` — PDF creation, extraction, and manipulation.
- `pptx` — PowerPoint presentation creation and editing.
- `xlsx` — Spreadsheet creation and editing.

</details>

<details>
<summary><strong>Design</strong> — 6 skills</summary>

- `frontend-design` — Production-grade web UI design.
- `canvas-design` — Visual art in PNG and PDF formats.
- `algorithmic-art` — Generative art with p5.js.
- `brand-guidelines` — Brand identity application.
- `theme-factory` — Theme toolkit for generated artifacts.
- `slack-gif-creator` — Animated GIFs for Slack.

</details>

<details>
<summary><strong>Development</strong> — 4 skills</summary>

- `mcp-builder` — MCP server creation.
- `web-artifacts-builder` — Multi-component web artifacts.
- `webapp-testing` — Playwright-based web testing.
- `skill-creator` — Skill creation and maintenance.

</details>

<details>
<summary><strong>Communication</strong> — 2 skills</summary>

- `doc-coauthoring` — Document coauthoring workflows.
- `internal-comms` — Internal communication formats and drafts.

</details>

## Repo Map

- `marketing/` — 26 custom skills across 6 categories.
- `design/`, `documents/`, `development/`, `communication/` — 16 official Anthropic skills across 4 categories.
- Each skill lives in its own folder with a `SKILL.md` file and, when needed, supporting files beside it.

## Start Here

If you already know the task, open the matching category, copy the skill folder into your project, and let Claude do the rest.

If you are not sure where to begin, start with the category that matches the work most closely, then narrow down from there.
