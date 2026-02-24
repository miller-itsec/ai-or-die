# Academy Team Handoff — AI Training Program Implementation Guide

> **Purpose**: Everything the academy team needs to turn these training materials into an interactive learning platform.
> **Audience**: L&D team, academy developers, instructional designers
> **Last updated**: February 2026

---

## Table of Contents

1. [Program Overview](#1-program-overview)
2. [Content Inventory](#2-content-inventory)
3. [Module Structure](#3-module-structure)
4. [Quiz System Design](#4-quiz-system-design)
5. [Scoring Model](#5-scoring-model)
6. [Recommended Module Flow](#6-recommended-module-flow)
7. [Platform Integration Guide](#7-platform-integration-guide)
8. [Content Maintenance](#8-content-maintenance)
9. [Rollout Plan](#9-rollout-plan)

---

## 1. Program Overview

### What This Is

A complete AI training program covering **9 business functions** — designed to teach every employee how to use AI tools effectively, responsibly, and within company policy.

### Coverage

| Track | Functions | Modules | Quiz Questions |
|-------|-----------|---------|----------------|
| Cross-Functional | Product, Sales, Legal, HR, Marketing, Finance, Customer Support, Operations | 8 | 40 |
| Engineering | Coding tools (Cursor, Copilot) | 6 | 31 |
| **Total** | **9 functions** | **14 modules** | **71 questions** |

### Core Principles (Reinforced Across All Modules)

Every module reinforces these five principles:

1. **AI = draft, not done** — always review AI output before using or sharing it
2. **No sensitive data in prompts** — PII, financials, trade secrets, privileged content stay out of AI tools
3. **Prompt quality = output quality** — specific, contextual prompts beat vague asks
4. **Microsoft Copilot integration** — Copilot for M365 is available across Word, Excel, PowerPoint, Outlook, and Teams
5. **Approved tools only** — ChatGPT, Claude, Gemini, Microsoft Copilot. No shadow AI.

---

## 2. Content Inventory

All content lives in the `ai-training-content/` directory.

### Training Modules

| File | Function | Word Count (approx) | Sections |
|------|----------|---------------------|----------|
| `01-product-management.md` | Product Management | ~4,500 | 4 sections + quiz |
| `02-sales.md` | Sales | ~3,700 | 4 sections + quiz |
| `03-legal.md` | Legal | ~4,500 | 4 sections + quiz |
| `04-hr-people.md` | HR & People | ~5,000 | 4 sections + quiz |
| `05-marketing.md` | Marketing | ~4,400 | 4 sections + quiz |
| `06-finance.md` | Finance | ~4,200 | 4 sections + quiz |
| `07-customer-support.md` | Customer Support | ~4,300 | 4 sections + quiz |
| `08-operations.md` | Operations | ~4,500 | 4 sections + quiz |

### Supporting Files

| File | Purpose |
|------|---------|
| `00-engineering-quiz.md` | Engineering quiz questions (31 questions across 6 modules) |
| `09-quiz-bank-all-functions.md` | All 71 quiz questions in one file, with answer key |
| `10-academy-handoff.md` | This document |

### Content Format

- All files are **standard Markdown** — compatible with Confluence, Notion, GitHub, or any LMS that supports markdown
- No custom syntax, shortcodes, or platform-specific formatting
- Tables use standard pipe syntax
- Code blocks use triple backticks
- Quiz answers are marked with ✓ (Unicode checkmark U+2713)

---

## 3. Module Structure

Every cross-functional module follows an identical 4-section structure:

### Section 1: Why AI Matters for [Function]
- **Purpose**: Motivation and context-setting
- **Content**: Adoption stats, time savings data, what AI can/cannot do
- **Duration**: ~5 minutes reading time
- **Interactivity opportunity**: Poll — "How often do you currently use AI in your role?"

### Section 2: Core AI Tools
- **Purpose**: Tool awareness and selection guidance
- **Content**: ChatGPT vs Claude vs Gemini guidance, Microsoft Copilot for M365 breakdown
- **Duration**: ~5 minutes reading time
- **Interactivity opportunity**: Matching exercise — match tool to use case

### Section 3: Practical Applications (3-5 use cases)
- **Purpose**: Hands-on examples they can immediately apply
- **Content**: Scenario → prompt → AI output → tips pattern
- **Duration**: ~10-15 minutes reading time
- **Interactivity opportunity**: **Prompt Lab** — give learners a scenario and have them write their own prompt, then compare with the example

### Section 4: Responsible AI Use
- **Purpose**: Safety guardrails specific to their function
- **Content**: Data sensitivity rules, review requirements, compliance considerations
- **Duration**: ~5 minutes reading time
- **Interactivity opportunity**: "Is this safe to share?" drag-and-drop exercise

### Quiz (5 questions)
- **Purpose**: Knowledge check / completion gate
- **Format**: Multiple choice, 4 options, 1 correct
- **Duration**: ~3-5 minutes
- **Mix**: ~2 knowledge questions + ~3 scenario-based questions

**Total time per module**: ~25-35 minutes

---

## 4. Quiz System Design

### Question Format

Every question follows this structure:

```
**[FUNCTION-PREFIX]-Q[N]: [Question text]**
- A) [Option]
- B) [Option]
- C) [Option] ✓
- D) [Option]
```

### Question ID Convention

| Prefix | Function |
|--------|----------|
| PM | Product Management |
| SALES | Sales |
| LEGAL | Legal |
| HR | HR & People |
| MKT | Marketing |
| FIN | Finance |
| CS | Customer Support |
| OPS | Operations |
| ENG-[1-6] | Engineering (by module) |

### Question Types

1. **Knowledge questions** (~40% of total)
   - Test understanding of AI capabilities and limitations
   - Example: "Which of the following is something AI CANNOT do in sales?"

2. **Scenario-based questions** (~50% of total)
   - Present a realistic work situation, test judgment
   - Example: "You use AI to generate a prospecting email. Before sending, you notice..."

3. **Tool selection questions** (~10% of total)
   - Test ability to choose the right AI tool for a task
   - Example: "An SDR needs to quickly draft 30 personalized cold emails. Which tool...?"

### Answer Key

The complete answer key is in `09-quiz-bank-all-functions.md` at the bottom, in table format for easy import into quiz platforms.

---

## 5. Scoring Model

### Recommended Pass Threshold

| Setting | Value | Rationale |
|---------|-------|-----------|
| Pass threshold | **80%** (4/5 correct) | Allows 1 mistake per module while ensuring comprehension |
| Retake policy | Unlimited retakes | Learning tool, not gatekeeping |
| Retake cooldown | None (immediate) | Let people learn from mistakes right away |

### Scoring Rules

- Each question is worth **1 point** (no partial credit)
- All questions weighted equally (no bonus questions)
- Score = correct answers / total questions × 100

### Completion Tracking

For each learner, track:

| Field | Type | Description |
|-------|------|-------------|
| `employee_id` | string | Employee identifier |
| `function` | string | Which module they completed |
| `score` | integer | Number correct (0-5) |
| `passed` | boolean | Score >= 80% |
| `completed_at` | timestamp | When they finished |
| `attempt_number` | integer | Which attempt (1, 2, 3...) |

### Certificates / Badges (Optional)

- **Module badge**: Complete any one function module with 80%+
- **Cross-functional badge**: Complete your own function + 2 others
- **AI Champion badge**: Complete all 8 cross-functional modules
- **Full spectrum badge**: Complete all 14 modules (cross-functional + engineering)

---

## 6. Recommended Module Flow

### Assignment Logic

Employees should complete **their own function's module first**, then optionally explore others.

```
Step 1: Complete YOUR function module (mandatory)
         ↓
Step 2: Complete "Responsible AI Use" refresher (shared across all — Section 4 of any module)
         ↓
Step 3: Explore 1-2 adjacent function modules (optional, recommended)
         ↓
Step 4: For engineering staff, continue to engineering-specific modules
```

### Function → Module Mapping

| Role / Department | Primary Module | Suggested Adjacent Modules |
|-------------------|---------------|---------------------------|
| Product Managers | 01 - Product Management | Sales, Engineering |
| Sales / BDR / AE | 02 - Sales | Marketing, Product |
| Legal / Compliance | 03 - Legal | HR, Finance |
| HR / People Ops | 04 - HR & People | Legal, Operations |
| Marketing / Comms | 05 - Marketing | Sales, Product |
| Finance / Accounting | 06 - Finance | Operations, Legal |
| Customer Support | 07 - Customer Support | Sales, Operations |
| Operations / PMO | 08 - Operations | Finance, HR |
| Engineering | Engineering Modules (00) | Product, Operations |

### Prerequisites

- No prerequisites for cross-functional modules — each is self-contained
- Engineering modules have internal prerequisites (defined within the engineering track)
- Recommend (but don't require) completing your primary module before adjacent ones

---

## 7. Platform Integration Guide

### Option A: Confluence (Simplest)

The markdown files are designed to copy-paste directly into Confluence pages.

**Steps:**
1. Create a Confluence space: "AI Training Academy"
2. Create a parent page per function
3. Copy each markdown file into a Confluence page (Confluence handles markdown rendering)
4. For quizzes: use Confluence's native "Poll" or "Forms" macro, or embed a Google Form
5. Manual tracking: use a Confluence table or linked spreadsheet for completion

**Pros**: Zero development effort, everyone already has access
**Cons**: No automated scoring, manual completion tracking

### Option B: LMS Integration (Google Classroom, Moodle, etc.)

**Steps:**
1. Convert markdown to SCORM packages using a tool like `markdown-to-scorm`
2. Import each module as a separate lesson/unit
3. Set up quiz questions in the LMS quiz builder using `09-quiz-bank-all-functions.md`
4. Configure pass threshold at 80%
5. Enable automated completion tracking and reporting

**Pros**: Automated scoring, completion tracking, reporting
**Cons**: Requires LMS setup, content conversion effort

### Option C: Custom Interactive Platform

A Streamlit + Python application can serve these modules interactively. The cross-functional modules can follow a consistent architecture.

**Steps:**
1. Extend the existing `content_en.py` pattern — add module definitions for each function
2. Each module needs: `id`, `title`, `content` (HTML/markdown), `quiz` (questions array)
3. Quiz format matches existing: `{"question": "...", "options": [...], "correct": N}`
4. Add function-based routing (employees see their function's module first)
5. Reuse existing quiz engine, progress tracking, and scoring logic

**Content mapping to code:**
```python
# Each module in content_en.py follows this structure:
{
    "id": "product_management",
    "title": "Product Management: AI-Assisted Product Development",
    "content": "...",  # Sections 1-4 from the markdown
    "quiz": [
        {
            "question": "You need to brainstorm 15 potential solutions...",
            "options": [
                "Microsoft Copilot in Excel",
                "ChatGPT",
                "Claude",
                "Gemini"
            ],
            "correct": 1  # 0-indexed: B = index 1
        },
        # ... 4 more questions
    ]
}
```

**Pros**: Full interactivity, automated scoring and tracking, consistent experience
**Cons**: Development effort required

### Option D: Notion

Similar to Confluence. Markdown files paste directly into Notion pages. Quizzes can be built using Notion's "Toggle" blocks (reveal answer on click) or linked to external quiz tools.

---

## 8. Content Maintenance

### Update Cadence

| Content Type | Review Frequency | Reason |
|--------------|-----------------|--------|
| Tool sections (Section 2) | Quarterly | AI tools update rapidly; new features, pricing, availability |
| Practical applications (Section 3) | Semi-annually | Prompts and examples may need refreshing |
| Responsible AI Use (Section 4) | Quarterly | Policy and regulatory landscape changes |
| Quiz questions | Annually | Questions should remain stable unless content changes significantly |
| Statistics and data points (Section 1) | Annually | Update adoption stats with latest survey data |

### Version Control

- Keep all markdown files in a git repository
- Tag releases: `v1.0`, `v1.1`, etc.
- Track changes in a CHANGELOG.md
- When updating quiz questions, increment all affected question IDs

### Localization

If cross-functional modules need translation into additional languages:

1. Create `content_[lang].py` files following the existing pattern
2. Translate markdown content (use AI for first draft, then human review)
3. Quiz questions need particular care — cultural context in scenarios may need adaptation, not just translation

---

## 9. Rollout Plan

### Phase 1: Pilot (Week 1-2)

- Select 2-3 functions for pilot (recommended: Sales + Marketing + Operations — high AI adoption, enthusiastic teams)
- Deploy as Confluence pages or pilot platform
- Collect feedback via post-module survey (5 questions: clarity, relevance, length, difficulty, actionability)
- Iterate on content based on feedback

### Phase 2: Full Cross-Functional Launch (Week 3-4)

- Deploy all 8 cross-functional modules
- Assign mandatory module per function
- Communication plan: email from L&D + Slack/Teams announcement + manager cascade
- Set completion deadline: 30 days from launch

### Phase 3: Ongoing (Month 2+)

- Track completion rates by function and team
- Identify low-completion teams — follow up via managers
- Collect "AI wins" stories from teams who applied training
- Quarterly content refresh based on tool updates and feedback

### Success Metrics

| Metric | Target | How to Measure |
|--------|--------|----------------|
| Module completion rate | >85% within 30 days | LMS/tracking system |
| Quiz pass rate (first attempt) | >70% | Quiz scores |
| Quiz pass rate (any attempt) | >95% | Quiz scores |
| Learner satisfaction | >4.0/5.0 | Post-module survey |
| AI tool adoption (post-training) | +20% increase | IT usage data or self-reported survey |

---

## Quick Start Checklist

For the academy team — here's your action plan:

- [ ] Choose a platform (Confluence, LMS, custom, or Notion)
- [ ] Import the 8 cross-functional modules (`01-08`)
- [ ] Set up quiz questions from `09-quiz-bank-all-functions.md`
- [ ] Configure pass threshold at 80%
- [ ] Set up completion tracking
- [ ] Map employees to their primary function module
- [ ] Run pilot with 2-3 functions
- [ ] Collect feedback and iterate
- [ ] Full launch with 30-day completion deadline
- [ ] Schedule quarterly content review

---

*For questions about this content, contact the training content team. For platform/technical questions, contact the academy development team.*
