---
name: prioritize-features
description: Prioritize backlog features using RICE, ICE, Value vs Effort, Kano, or MoSCoW frameworks. Use when ranking features, deciding what to build next, or creating a prioritized backlog.
argument-hint: "[list of features or epic]"
---

STARTER_CHARACTER = ⚖️

# Prioritize Features

Apply systematic frameworks to rank features objectively.

## Process

### 1. Collect features
- List of features/initiatives to prioritize
- Clarify scope and context for each

### 2. Choose framework
Recommend based on context, or ask PM preference:

**RICE** — best for data-informed teams with measurable reach
- Reach: users impacted in a period
- Impact: level per user (3/2/1/0.5/0.25)
- Confidence: certainty (100%/80%/50%)
- Effort: person-weeks
- Score = (Reach x Impact x Confidence) / Effort

**ICE** — best for quick scoring when data is limited
- Impact (1-10)
- Confidence (1-10)
- Ease (1-10)
- Score = Impact x Confidence x Ease

**Value vs Effort** — best for visual communication with stakeholders
- Plot on 2x2 matrix
- Quick wins (high value, low effort) → do first
- Big bets (high value, high effort) → plan carefully
- Fill-ins (low value, low effort) → do if capacity allows
- Money pits (low value, high effort) → avoid

**Kano Model** — best for understanding user satisfaction drivers
- Must-be (expected, absence causes dissatisfaction)
- One-dimensional (more is better, linear satisfaction)
- Attractive (delighters, absence doesn't cause dissatisfaction)
- Indifferent / Reverse

**MoSCoW** — best for fixed-scope releases
- Must Have / Should Have / Could Have / Won't Have

### 3. Score each feature
For each feature assess:
- Strategic value and alignment with goals
- User impact and reach (which personas, how many)
- Effort estimate (t-shirt size or person-weeks)
- Technical complexity and dependencies
- Available data to inform scoring

### 4. Generate prioritized list

## Output Structure

1. **Framework chosen** and rationale
2. **Scoring table** — each feature with its scores and calculation
3. **Ranked list** — ordered by score
4. **Rationale** — brief justification for each ranking
5. **Strategic overrides** — cases where score doesn't tell the full story
6. **Dependencies** — features that must precede others
7. **Recommended roadmap order** — considering dependencies and strategic context

## Anti-patterns to avoid

- Using frameworks without questioning the inputs — garbage in, garbage out
- Ignoring strategic context — a low-score feature may be critical for a key account
- False precision — don't pretend RICE scores are exact; they're directional
- Prioritizing without considering dependencies and sequencing
- Scoring in isolation — always compare relative to alternatives

## Credits

Original command from the [Claude Code for Product Managers](https://ccforpms.com) course by Carl Vellotti (@carlvellotti), converted to skill format.
