---
name: calculate-roi
description: Calculate ROI and build a data-driven business case for a feature investment. Use when justifying a feature, building business cases, estimating payback period, or comparing investment alternatives.
argument-hint: "[feature name]"
---

STARTER_CHARACTER = 💰

# Calculate ROI

Build a data-driven business case for a feature investment.

## Process

### 1. Understand the feature
- Feature description and scope
- Purpose and expected impact
- Target users and segment

### 2. Estimate investment (costs)

**Development cost:**
- Effort estimate (person-weeks)
- Team cost rate (ask or use reasonable default)
- Development cost = effort x rate

**Ongoing costs:**
- Maintenance effort (% of dev time per month, typically 15-20%)
- Infrastructure costs if applicable
- Third-party service costs

### 3. Estimate returns (value)

**Revenue impact:**
- New revenue (new customers, upsell, new pricing tier)
- Retention improvement (reduced churn x LTV)
- Conversion improvement (trial→paid, free→premium)

**Efficiency gains:**
- Time saved per user/team (hours x frequency x cost)
- Support ticket reduction
- Manual process automation

**Strategic value (qualitative):**
- Competitive positioning
- Platform capability enablement
- Market expansion potential

### 4. Calculate metrics

- **ROI** = (Net Benefit - Cost) / Cost x 100%
- **Payback Period** = Total Investment / Monthly Net Benefit
- **3-Year NPV** = sum of discounted future cash flows - investment
- Use discount rate of 10% unless specified otherwise

### 5. Sensitivity analysis

Run three scenarios:
- **Optimistic** — assumptions go well
- **Likely** — base case
- **Pessimistic** — things take longer, adoption is slower

Identify which assumptions have the biggest impact on the outcome.

## Output Structure

1. **Feature Summary** — what we're evaluating
2. **Investment Required** — one-time + ongoing costs, broken down
3. **Expected Returns** — revenue, retention, efficiency, with assumptions stated
4. **ROI Calculation** — with formula shown
5. **Payback Period** — months to break even
6. **3-Year NPV** — discounted value
7. **Sensitivity Analysis** — optimistic / likely / pessimistic table
8. **Key Assumptions** — listed explicitly, flagged by confidence level
9. **Strategic Considerations** — qualitative value not captured in numbers
10. **Recommendation** — Go / No-go with rationale

## Anti-patterns to avoid

- False precision — don't present estimates as exact; show ranges
- Ignoring ongoing costs — maintenance, infra, and support add up
- Only counting revenue — retention and efficiency gains are often larger
- Ignoring opportunity cost — what else could this investment fund?
- Hiding assumptions — state them explicitly so they can be challenged

## Credits

Original command from the [Claude Code for Product Managers](https://ccforpms.com) course by Carl Vellotti (@carlvellotti), converted to skill format.
