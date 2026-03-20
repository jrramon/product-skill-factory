---
name: lean-analytics
description: SaaS metrics analysis using Lean Analytics framework. Use when evaluating metrics, analyzing churn, retention, MRR, cohorts, or deciding what to measure at each business stage.
---

STARTER_CHARACTER = 📊

# Lean Analytics for SaaS

Reason about SaaS metrics using Lean Analytics principles. A SaaS is a relationship-based, recurring-revenue business — metrics must reflect recurring use, value delivered, and stability over time.

## Core Principles

- Focus on learning over reporting
- Prefer actionable metrics over vanity metrics
- Always reason in terms of cohorts, behavior, and value delivered
- Optimize retention before growth, and efficiency before scale
- Sign-ups are weak signals — prioritize activation and repeat usage
- Averages hide problems — use cohort-based insights
- Distinguish between free users, activated users, and paying customers

## Business Stages and Their Metrics

### 1. Empathy — validate the problem
Does the product solve a real, relevant problem?
- Activations (users completing first meaningful use)
- Usage of core features (not total users)
- Time to first value
- Early retention (day 1, week 1)

Signing up is not adopting. The real signal is consistent return and use.

### 2. Stickiness — build the habit
Do users come back because the product is necessary?
- **Retention** (weekly or monthly cohorts)
- **Churn** (cancellations, abandonment)
- Frequency of use (daily, weekly, monthly — depends on product type)
- Core feature engagement
- Active/registered ratio

Evaluate retention against expected usage pattern: financial SaaS → monthly, collaborative → daily, reporting → weekly.

### 3. Virality — organic growth
Does natural use expose new users?
- Explicit: invitations, referrals, shared links
- Implicit: shared documents, dashboards, collaboration
- Invitations per user, invitation conversion
- Organic vs paid growth
- CAC relative to value generated

Forcing virality in B2B SaaS is usually counterproductive. Slow growth with good retention beats fast growth without a base.

### 4. Revenue — sustainable monetization
Design a sustainable recurring revenue system.
- **MRR** (Monthly Recurring Revenue)
- ARPU / ARPA
- Free to paid conversion
- Paying customer churn
- LTV (Lifetime Value)

Not all users must pay. Freemium works if: free users generate indirect value, there's a clear path to payment, and cost of serving free users is controlled.

### 5. Scale — efficient growth
Can we grow without costs outpacing revenue?
- **LTV / CAC ratio**
- Gross margin
- Support cost per customer
- Infrastructure cost per user
- Account expansion (upsell, cross-sell)

Reducing churn is usually more profitable than acquiring new customers, even at advanced stages.

## One Metric That Matters (OMTM)

Choose one focus metric per stage:
- Empathy → activation or initial use
- Stickiness → retention
- Virality → organic growth
- Revenue → MRR or paid conversion
- Scale → economic efficiency

The OMTM must: reflect real customer value, connect directly to product decisions, and be understandable and shared by the whole team.

## Operating Logic

When analyzing a SaaS situation:
1. Identify the current stage
2. Select the OMTM for that stage
3. Evaluate whether current metrics reflect real user value and enable concrete decisions
4. Highlight risks, blind spots, and false positives in the data
5. Propose clear next actions or experiments

## Credits

Based on **"Lean Analytics: Use Data to Build a Better Startup Faster"** by **Alistair Croll & Benjamin Yoskovitz**.

Original agent by @jrramon, converted to skill format.
