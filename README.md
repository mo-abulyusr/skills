<div align="center">

# Skills for Claude Code

**42 ready-to-use skills across 10 categories — drop them into `.claude/skills/` and go.**

[![Skills](https://img.shields.io/badge/skills-42-blue)]()
[![Categories](https://img.shields.io/badge/categories-10-green)]()
[![License](https://img.shields.io/badge/license-MIT-yellow)]()

</div>

---

## What Are Claude Skills?

Skills are markdown files that give Claude specialized knowledge and workflows for specific tasks. Drop a skill folder into your project's `.claude/skills/` directory and Claude automatically uses it when relevant — no configuration needed.

This repo contains **26 custom marketing skills** and **16 official Anthropic skills** organized into 10 categories.

## Installation

Copy any skill folder into your project:

```bash
# Copy a single skill
cp -r path/to/skills/marketing/cro/page-cro .claude/skills/

# Or copy an entire category
cp -r path/to/skills/marketing/seo/* .claude/skills/
```

Claude will detect and use the skills automatically based on your prompts.

---

## Table of Contents

**Marketing**
- [CRO (Conversion Rate Optimization)](#cro-conversion-rate-optimization)
- [Content & Copy](#content--copy)
- [SEO](#seo)
- [Analytics & Testing](#analytics--testing)
- [Strategy & Growth](#strategy--growth)
- [Foundation](#foundation)

**Anthropic Official**
- [Documents](#documents)
- [Design](#design)
- [Development](#development)
- [Communication](#communication)

---

## Marketing Skills

### CRO (Conversion Rate Optimization)

#### page-cro

**Use Cases**
- Diagnose why a landing page isn't converting
- Get a prioritized list of CRO fixes for any marketing page
- Optimize homepage, pricing page, or feature page conversions
- Run a conversion audit on blog posts or content pages

Systematic conversion rate optimization for any marketing page — homepage, landing pages, pricing pages, feature pages, or blog posts. Analyzes page structure, copy, CTAs, trust signals, and user flow to deliver prioritized recommendations.

**Related:** signup-flow-cro, form-cro, copywriting, ab-test-setup

---

#### form-cro

**Use Cases**
- Reduce friction in lead capture or contact forms
- Optimize demo request or application forms
- Improve checkout form completion rates
- Audit form field necessity and ordering

Optimizes any non-signup form — lead capture, contact, demo request, application, survey, or checkout forms. Focuses on reducing friction, improving field logic, and increasing completion rates.

**Related:** signup-flow-cro, popup-cro, page-cro, ab-test-setup

---

#### signup-flow-cro

**Use Cases**
- Reduce signup form abandonment
- Optimize free trial registration flows
- Streamline account creation for SaaS products
- Test single-step vs. multi-step signup

Optimizes signup, registration, account creation, and trial activation flows. Covers form design, social login strategy, progressive profiling, and reducing dropoff at each step.

**Related:** onboarding-cro, form-cro, page-cro

---

#### onboarding-cro

**Use Cases**
- Improve user activation rates after signup
- Design effective first-run experiences
- Optimize empty states and onboarding checklists
- Reduce time-to-value for new users

Optimizes post-signup onboarding, user activation, and first-run experience. Focuses on getting users to their "aha moment" faster through smart defaults, progressive disclosure, and activation metrics.

**Related:** signup-flow-cro, email-sequence

---

#### paywall-upgrade-cro

**Use Cases**
- Design effective in-app upgrade screens
- Optimize feature gate messaging
- Improve freemium-to-paid conversion
- Create compelling trial expiration experiences

Creates and optimizes in-app paywalls, upgrade screens, upsell modals, and feature gates. Focuses on in-product upgrade moments where users have already experienced value — distinct from public pricing pages.

**Related:** pricing-strategy, page-cro, popup-cro

---

#### popup-cro

**Use Cases**
- Create high-converting exit-intent popups
- Optimize email capture modals
- Design announcement banners and slide-ins
- Reduce popup annoyance while maintaining conversions

Creates and optimizes popups, modals, overlays, slide-ins, and banners. Covers timing, targeting, copy, design, and A/B testing strategies for conversion-focused overlays.

**Related:** form-cro, page-cro, email-sequence

---

### Content & Copy

#### copywriting

**Use Cases**
- Write homepage or landing page copy from scratch
- Rewrite underperforming page copy
- Craft compelling headlines and CTAs
- Write feature pages, about pages, or product pages

Writes and improves marketing copy for any page type. Uses proven frameworks (PAS, AIDA, storytelling) while avoiding generic AI patterns. Emphasizes clarity, specificity, and conversion-focused writing.

**Related:** copy-editing, page-cro, email-sequence, popup-cro

---

#### copy-editing

**Use Cases**
- Polish and tighten existing marketing copy
- Run a systematic copy review across a site
- Fix tone, clarity, and readability issues
- Ensure consistent voice across pages

Systematic approach to editing marketing copy through multiple focused passes — structure, clarity, persuasion, voice, and polish. Tightens prose, eliminates jargon, and improves readability without losing the original voice.

**Related:** copywriting, page-cro, content-strategy

---

#### content-strategy

**Use Cases**
- Plan a content calendar and topic clusters
- Decide what blog content to create for SEO and growth
- Map content to buyer journey stages
- Prioritize content ideas by impact and effort

Plans content strategy including topic selection, content types, publishing cadence, and distribution. Maps content to business goals and buyer journey stages.

**Related:** copywriting, seo-audit, social-content, programmatic-seo

---

#### social-content

**Use Cases**
- Create platform-specific social media posts
- Build a content calendar across LinkedIn, Twitter/X, Instagram
- Repurpose blog content for social channels
- Optimize posts for engagement and reach

Creates, schedules, and optimizes social media content across platforms. Covers content creation, repurposing strategies, platform-specific best practices, and engagement optimization.

**Related:** content-strategy, copywriting, launch-strategy

---

#### email-sequence

**Use Cases**
- Build onboarding or welcome email sequences
- Create nurture campaigns for leads
- Design re-engagement or win-back flows
- Optimize drip campaign timing and copy

Creates and optimizes email sequences, drip campaigns, and lifecycle email programs. Covers sequence architecture, subject lines, copy frameworks, timing, and segmentation strategies.

**Related:** onboarding-cro, copywriting, ab-test-setup

---

### SEO

#### seo-audit

**Use Cases**
- Run a full technical and on-page SEO audit
- Diagnose why pages aren't ranking
- Review meta tags, headings, and internal linking
- Check Core Web Vitals and crawlability issues

Comprehensive SEO audit covering technical SEO, on-page optimization, content quality, internal linking, and performance. Includes AI/AEO readiness checks and AI-generated content detection patterns.

**Related:** programmatic-seo, schema-markup, page-cro, analytics-tracking

---

#### programmatic-seo

**Use Cases**
- Build directory or location pages at scale
- Create comparison and integration pages programmatically
- Design templates for [keyword] + [city] page patterns
- Generate hundreds of SEO-optimized pages from data

Creates SEO-driven pages at scale using templates and data. Covers page types (directory, location, comparison, integration), template design, data sourcing, and internal linking strategies.

**Related:** seo-audit, schema-markup, content-strategy

---

#### schema-markup

**Use Cases**
- Add JSON-LD structured data to pages
- Implement FAQ, Product, or Review schema
- Fix Google Search Console structured data errors
- Optimize for rich snippets and enhanced SERP features

Adds, fixes, and optimizes schema markup and structured data. Covers JSON-LD implementation for all major schema types — FAQ, Product, Review, Organization, Breadcrumb, and more.

**Related:** seo-audit, programmatic-seo

---

#### competitor-alternatives

**Use Cases**
- Create "[Product] vs [Competitor]" comparison pages
- Build "[Competitor] alternatives" landing pages
- Design competitive comparison content for sales enablement
- Target competitor brand keywords with SEO content

Creates competitor comparison and alternative pages for SEO and sales enablement. Covers four formats: singular alternative, plural alternatives, head-to-head comparison, and third-party comparison. Emphasizes deep research and modular content architecture.

**Related:** seo-audit, copywriting, content-strategy

---

### Analytics & Testing

#### analytics-tracking

**Use Cases**
- Set up GA4 event tracking from scratch
- Implement conversion tracking across platforms
- Design a measurement plan with UTM strategy
- Audit existing analytics for data quality issues

Sets up, improves, and audits analytics tracking and measurement. Covers GA4, GTM, conversion tracking, event taxonomy, UTM parameters, and cross-platform attribution.

**Related:** ab-test-setup, page-cro, seo-audit

---

#### ab-test-setup

**Use Cases**
- Design an A/B test with proper hypothesis and metrics
- Calculate sample size and test duration
- Plan multivariate or sequential tests
- Set up server-side or client-side experiments

Plans, designs, and implements A/B tests and experiments. Covers hypothesis formation, sample size calculation, variant design, statistical significance, and result interpretation.

**Related:** page-cro, analytics-tracking, copywriting

---

### Strategy & Growth

#### pricing-strategy

**Use Cases**
- Design pricing tiers for a SaaS product
- Evaluate freemium vs. free trial models
- Plan a price increase strategy
- Research willingness to pay with Van Westendorp

Guides pricing decisions, packaging, and monetization strategy. Covers pricing research methods (Van Westendorp, conjoint), tier structure design, value metrics, and price communication.

**Related:** paywall-upgrade-cro, page-cro, launch-strategy

---

#### launch-strategy

**Use Cases**
- Plan a Product Hunt launch
- Design a phased rollout with beta and early access
- Create a go-to-market timeline
- Build pre-launch buzz with waitlists and exclusivity

Plans product launches, feature announcements, and release strategies. Covers phased launches, channel strategy, pre-launch community building, and post-launch momentum.

**Related:** marketing-ideas, email-sequence, page-cro, marketing-psychology

---

#### marketing-ideas

**Use Cases**
- Get a comprehensive list of growth tactics for your SaaS
- Find marketing channels you haven't tried yet
- Discover low-effort, high-impact marketing wins
- Brainstorm creative promotion strategies

Provides 139 proven marketing approaches organized by category — from content marketing and SEO to partnerships, community building, and guerrilla tactics. Each idea includes effort level and expected impact.

**Related:** launch-strategy, content-strategy, free-tool-strategy

---

#### marketing-psychology

**Use Cases**
- Apply cognitive biases to landing page design
- Use mental models to improve conversion copy
- Understand why users aren't converting
- Add psychological triggers to pricing pages

Provides 70+ mental models and psychological principles organized for marketing application — anchoring, social proof, loss aversion, commitment/consistency, and more. Includes implementation examples for each.

**Related:** copywriting, page-cro, pricing-strategy, paid-ads

---

#### referral-program

**Use Cases**
- Design a referral program with incentive structure
- Build an affiliate or ambassador program
- Optimize viral loop mechanics
- Choose referral program tools and platforms

Creates and optimizes referral programs, affiliate programs, and word-of-mouth strategies. Covers program design, incentive structure, tracking, and growth optimization.

**Related:** launch-strategy, pricing-strategy, email-sequence

---

#### free-tool-strategy

**Use Cases**
- Evaluate whether a free tool would drive leads
- Plan an "engineering as marketing" project
- Design a calculator, generator, or interactive tool
- Build a free resource for SEO and brand awareness

Plans, evaluates, and builds free tools for marketing purposes — lead generation, SEO value, or brand awareness. Bridges engineering and marketing with frameworks for tool selection, build vs. buy, and distribution.

**Related:** marketing-ideas, content-strategy, seo-audit

---

#### paid-ads

**Use Cases**
- Plan Google Ads or Meta ad campaigns
- Write ad copy and design creative briefs
- Set up retargeting and audience targeting
- Optimize ROAS and reduce CPA

Covers paid advertising across Google Ads, Meta, LinkedIn, Twitter/X, and more. Includes campaign strategy, ad copy creation, audience targeting, budget allocation, and performance optimization.

**Related:** analytics-tracking, page-cro, copywriting

---

### Foundation

#### product-marketing-context

**Use Cases**
- Create a shared marketing context document for all skills
- Define product positioning, audience, and value props once
- Avoid repeating foundational info across marketing tasks
- Set up a new project for marketing skill usage

Creates a `.claude/product-marketing-context.md` file that other marketing skills reference. Defines product positioning, target audience, competitive landscape, and brand voice in one place — used as shared context across all marketing tasks.

**Related:** copywriting, content-strategy, page-cro

---

#### visual-qa

**Use Cases**
- Run automated visual QA across desktop, tablet, and mobile
- Catch spacing, alignment, and typography issues
- Verify responsive behavior at all breakpoints
- Get a prioritized list of visual bugs with fixes

Autonomous screenshot-driven visual QA for any website or web application. Captures at three viewports, evaluates against a 12-category checklist (spacing, typography, color, alignment, responsive, buttons, borders, animation, images, polish, consistency, accessibility), fixes issues, and re-verifies.

**Related:** page-cro, copy-editing, seo-audit

---

## Anthropic Official Skills

> The following skills are from the [Anthropic Skills Repository](https://github.com/anthropics/skills) and included here for convenience.

### Documents

#### docx

**Use Cases**
- Create professional Word documents with formatting
- Extract and reorganize content from .docx files
- Generate reports, memos, and letters
- Work with tracked changes and comments

Creates, reads, edits, and manipulates Word documents (.docx). Handles tables of contents, headings, page numbers, letterheads, images, find-and-replace, and tracked changes.

---

#### pdf

**Use Cases**
- Extract text and tables from PDFs
- Merge, split, or rotate PDF pages
- Add watermarks or encrypt PDFs
- OCR scanned documents

Full PDF toolkit — reading, extracting, combining, splitting, rotating, watermarking, encrypting, form filling, image extraction, and OCR for scanned documents.

---

#### pptx

**Use Cases**
- Create slide decks and presentations from scratch
- Extract content from existing .pptx files
- Edit templates, layouts, and speaker notes
- Build pitch decks with consistent styling

Creates, reads, edits, and manipulates PowerPoint presentations. Handles templates, layouts, speaker notes, comments, and consistent slide styling.

---

#### xlsx

**Use Cases**
- Create spreadsheets with formulas and charts
- Clean and restructure messy data files
- Convert between CSV, TSV, and XLSX formats
- Build formatted reports from raw data

Creates, reads, edits, and manipulates spreadsheet files (.xlsx, .csv, .tsv). Handles formulas, charts, formatting, data cleaning, and format conversion.

---

### Design

#### frontend-design

**Use Cases**
- Build production-grade web components and pages
- Create visually distinctive landing pages
- Design dashboards and React components
- Style and beautify any web UI

Creates distinctive, production-grade frontend interfaces with high design quality. Generates creative, polished code that avoids generic AI aesthetics — for websites, landing pages, dashboards, and components.

---

#### canvas-design

**Use Cases**
- Create visual art as PNG or PDF
- Design posters and static graphics
- Generate original visual compositions
- Build design mockups programmatically

Creates beautiful visual art in PNG and PDF formats using design philosophy. For posters, static art, and original visual compositions — never copies existing artists' work.

---

#### algorithmic-art

**Use Cases**
- Create generative art with p5.js
- Build flow fields and particle systems
- Design seeded-random visual compositions
- Create interactive parameter explorations

Creates algorithmic art using p5.js with seeded randomness and interactive parameter exploration. Covers flow fields, particle systems, and generative compositions.

---

#### brand-guidelines

**Use Cases**
- Apply brand colors and typography to artifacts
- Ensure consistent visual identity across outputs
- Format documents with company design standards
- Create on-brand presentations and reports

Applies brand colors, typography, and design standards to any artifact. Ensures consistent visual identity across all outputs.

---

#### theme-factory

**Use Cases**
- Style slides, docs, or reports with preset themes
- Apply consistent visual themes to any artifact
- Generate custom themes on-the-fly
- Restyle existing content with a new look

Toolkit with 10 preset themes (colors/fonts) for styling any artifact — slides, docs, reports, landing pages. Can also generate new themes dynamically.

---

#### slack-gif-creator

**Use Cases**
- Create animated GIFs optimized for Slack
- Build celebration or reaction animations
- Design team-specific custom GIFs
- Make lightweight animations within Slack constraints

Creates animated GIFs optimized for Slack's constraints. Provides validation tools, animation concepts, and size optimization for smooth Slack display.

---

### Development

#### mcp-builder

**Use Cases**
- Build MCP servers for API integrations
- Create tool interfaces for Claude
- Design well-structured MCP tool schemas
- Integrate external services via Python or TypeScript

Guide for creating high-quality MCP (Model Context Protocol) servers in Python (FastMCP) or TypeScript (MCP SDK). Covers tool design, error handling, and service integration patterns.

---

#### web-artifacts-builder

**Use Cases**
- Build multi-component web artifacts for claude.ai
- Create apps with state management and routing
- Use shadcn/ui components in artifacts
- Build complex interactive web experiences

Suite of tools for creating elaborate, multi-component claude.ai HTML artifacts using React, Tailwind CSS, and shadcn/ui. For complex artifacts requiring state management, routing, or rich component libraries.

---

#### webapp-testing

**Use Cases**
- Test local web applications with Playwright
- Capture browser screenshots for debugging
- Verify frontend functionality and UI behavior
- View and analyze browser console logs

Playwright-based toolkit for interacting with and testing local web applications. Supports screenshot capture, UI verification, browser log analysis, and interactive debugging.

---

#### skill-creator

**Use Cases**
- Create new Claude skills from scratch
- Update and improve existing skills
- Design skill workflows and triggers
- Structure skill reference materials

Guide for creating effective skills that extend Claude's capabilities with specialized knowledge, workflows, or tool integrations. Covers skill structure, triggers, and best practices.

---

### Communication

#### doc-coauthoring

**Use Cases**
- Co-author documentation with Claude
- Write proposals, specs, or decision docs
- Iterate on structured content efficiently
- Create documentation that works for readers

Structured workflow for co-authoring documentation — proposals, technical specs, decision docs, and similar content. Helps transfer context, refine through iteration, and verify reader effectiveness.

---

#### internal-comms

**Use Cases**
- Write status reports and leadership updates
- Draft company newsletters and FAQs
- Create incident reports and postmortems
- Compose project updates in company format

Templates and resources for internal communications — status reports, leadership updates, newsletters, FAQs, incident reports, project updates, and more. Adapts to your company's preferred formats.

---

## Contributing

Want to add a skill? Each skill needs:

1. A folder with a `SKILL.md` file containing YAML frontmatter (`name`, `description`) and the skill content
2. An optional `references/` subfolder for supporting materials
3. Clear trigger phrases in the description so Claude knows when to use it

Place your skill in the appropriate category folder and submit a PR.

## License

Custom marketing skills are licensed under the [MIT License](LICENSE).

Anthropic official skills are sourced from [anthropics/skills](https://github.com/anthropics/skills) under the MIT License. See [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md) for attribution.
