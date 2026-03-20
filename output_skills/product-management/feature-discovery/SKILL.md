---
name: feature-discovery
description: Systematic validation of a feature idea before committing to build. Use when exploring new feature ideas, validating opportunities, or deciding whether to pursue, hold, or kill an initiative.
argument-hint: "[feature idea]"
---

STARTER_CHARACTER = 💡

# Feature Discovery

Validate a feature idea systematically before committing resources.

## Process

### 1. Understand the idea
- What problem does it solve?
- Who needs this?
- Why now? What triggered this idea?
- What evidence exists? (data, feedback, request frequency)

### 2. Strategic fit
- How does this align with product vision and current goals?
- Does it strengthen or dilute positioning?
- What is the opportunity cost — what won't we do if we do this?
- Is the timing right?

### 3. User need validation
- Is this a real problem for enough users?
- How painful is the current situation? (workaround cost)
- How do users solve this today without the feature?
- What segment of users would benefit most?

### 4. Competitive context
- Do competitors offer this?
- If yes — is it table stakes or differentiation?
- If no — is that because it's not valuable, or an opportunity?
- What can we learn from how others have approached this?

### 5. Technical feasibility
- Can we build this with current architecture?
- Rough effort estimate (t-shirt size)
- Key technical risks or unknowns
- Dependencies on other systems or teams

### 6. Business case
- Expected impact on key metrics
- Rough ROI estimate (even directional)
- Revenue, retention, or efficiency impact
- What assumptions drive the business case?

### 7. Recommendation

**Pursue** — strong signal across dimensions, clear next step
**Hold** — promising but needs more validation or isn't timely
**Kill** — weak signal, poor fit, or better alternatives exist

## Output Structure

1. **Opportunity Summary** — one paragraph
2. **Strategic Fit** — alignment and trade-offs
3. **User Need** — evidence and validation level
4. **Competitive Context** — landscape assessment
5. **Technical Feasibility** — effort, risks, constraints
6. **Business Case** — expected impact and assumptions
7. **Recommendation** — Pursue / Hold / Kill with rationale
8. **Next Steps** — if pursuing, what to do first (experiment, prototype, PRD)

## Anti-patterns to avoid

- Falling in love with the solution before validating the problem
- Skipping competitive check — someone else's failure or success is cheap learning
- "Build it and they will come" — always validate demand signals
- Overinvesting in analysis — this is a lightweight gate, not a full business plan
- Binary thinking — "Hold" is a valid and common outcome

## Credits

Original command from the [Claude Code for Product Managers](https://ccforpms.com) course by Carl Vellotti (@carlvellotti), converted to skill format.
