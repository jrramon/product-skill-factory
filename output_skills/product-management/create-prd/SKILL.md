---
name: create-prd
description: Create a Product Requirements Document from a feature idea. Use when writing PRDs, specifying features, or documenting product requirements.
argument-hint: "[feature idea]"
---

STARTER_CHARACTER = 📝

# Create PRD

Generate a comprehensive Product Requirements Document through structured discovery.

## Process

### 1. Discover the feature
Ask about:
- What problem does this solve?
- Who are the target users?
- What's the desired outcome?
- What evidence exists that this is needed? (feedback, data, research)

### 2. Strategic assessment
- How does this align with product vision and current goals?
- What is the opportunity cost?
- What priority does it warrant and why?

### 3. User perspective
- Which personas are affected?
- What are the relevant user needs and pain points?
- Reference existing feedback or research if available
- Define jobs-to-be-done this addresses

### 4. Requirements
- Functional requirements (what the system must do)
- Non-functional requirements (performance, security, accessibility)
- User stories with acceptance criteria
- Edge cases and error states
- Out of scope — explicitly state what this does NOT include

### 5. Technical considerations
- Affected systems and components
- Technical feasibility assessment
- Known constraints or dependencies
- Rough effort estimate (t-shirt size)
- Technical risks

### 6. Success metrics
- Primary success metric
- Supporting metrics
- Measurement plan — how and when to evaluate
- Success/failure thresholds

## PRD Structure

Output the PRD with these sections:

1. **Overview** — one paragraph: what, why, for whom
2. **Problem Statement** — the problem with evidence
3. **Goals & Success Metrics** — measurable outcomes
4. **User Stories** — standard format with acceptance criteria
5. **Requirements** — functional and non-functional
6. **Technical Considerations** — feasibility, effort, risks
7. **Out of Scope** — explicit boundaries
8. **Open Questions** — unresolved items needing input
9. **Timeline & Milestones** — rough phasing

## Anti-patterns to avoid

- Writing requirements without understanding the problem first
- Skipping success metrics — every PRD needs measurable outcomes
- Solutioning too early — define the problem before the solution
- Scope creep — be explicit about boundaries
- Vague acceptance criteria — must be testable

## Credits

Original command from the [Claude Code for Product Managers](https://ccforpms.com) course by Carl Vellotti (@carlvellotti), converted to skill format.
