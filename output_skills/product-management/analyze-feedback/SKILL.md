---
name: analyze-feedback
description: Analyze customer feedback to extract themes, pain points, and actionable insights. Use when processing user feedback, support tickets, survey responses, or NPS comments.
argument-hint: "[feedback source or paste]"
---

STARTER_CHARACTER = 💬

# Analyze Feedback

Turn raw feedback into categorized insights and prioritized recommendations.

## Input

Accept feedback in any format:
- Text paste (quotes, notes)
- CSV or structured data
- File reference
- Summary of feedback sources

Ask for time period and user segment if not specified.

## Analysis Process

### 1. Categorize into themes
- Group feedback by topic/theme
- Count frequency of mentions per theme
- Extract representative quotes for each theme

### 2. Sentiment analysis
- Classify each piece: positive, neutral, negative
- Identify intensity — mild frustration vs critical pain
- Note emotional language and urgency signals

### 3. Pain point identification
- Rank pain points by frequency + severity
- Distinguish between:
  - Usability issues (can't figure out how)
  - Missing functionality (can't do what they need)
  - Bugs/reliability (doesn't work as expected)
  - Performance (too slow, too complex)

### 4. Feature requests
- Extract and group feature requests
- Differentiate between the request and the underlying need
- Count how many users mention similar requests

### 5. Segment analysis
- Which user types/personas are affected?
- Are pain points universal or segment-specific?
- Are there patterns by user maturity, plan, or usage level?

## Output Structure

1. **Executive Summary** — top 3 themes, one sentence each
2. **Themes** — detailed breakdown with quotes and frequency
3. **Priority Pain Points** — ranked by impact (frequency x severity)
4. **Feature Requests** — grouped, counted, underlying need identified
5. **Segment Analysis** — which users are most affected
6. **Recommended Actions** — prioritized, tied to specific themes
7. **Data Gaps** — what we can't conclude from this data alone

## Anti-patterns to avoid

- Taking feature requests at face value without exploring the need
- Letting volume bias override severity — 1 critical issue > 10 minor annoyances
- Ignoring positive feedback — it tells you what to protect
- Generalizing from small samples without flagging confidence level
- Mixing facts with interpretations without labeling them

## Credits

Original command from the [Claude Code for Product Managers](https://ccforpms.com) course by Carl Vellotti (@carlvellotti), converted to skill format.
