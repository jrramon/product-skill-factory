---
name: write-user-stories
description: Write user stories with acceptance criteria from a feature or epic. Use when creating backlog items, writing stories, defining acceptance criteria, or breaking epics into stories.
argument-hint: "[feature or epic name]"
---

STARTER_CHARACTER = ✍️

# Write User Stories

Create detailed, actionable user stories for a feature or epic.

## Process

### 1. Understand context
- Feature/epic name and description
- Target users/personas
- Desired outcome and value delivered
- Any existing research or constraints

### 2. Identify personas involved
- Who interacts with this feature?
- What role does each persona play?
- What value does each get?

### 3. Write stories
Standard format:
> As a **[persona]**, I want to **[action]**, so that **[benefit]**

For each story include:
- **Acceptance criteria** — specific, testable conditions using Given/When/Then or checklist format
- **Edge cases** — what could go wrong or be unusual
- **Priority** — P0 (Must Have), P1 (Should Have), P2 (Nice to Have)
- **Estimate** — t-shirt size (S/M/L/XL)
- **Dependencies** — other stories or systems this depends on
- **Technical notes** — relevant implementation considerations

### 4. Prioritize the backlog
- Order stories by priority and dependencies
- Identify the minimum set for first delivery (P0s)
- Group into logical delivery increments

## Story quality checklist

Every story must be **INVEST**:
- **I**ndependent — can be developed separately
- **N**egotiable — not a contract, open to discussion
- **V**aluable — delivers value to a user or the business
- **E**stimable — small enough to estimate
- **S**mall — completable in one sprint or less
- **T**estable — clear pass/fail criteria

## Anti-patterns to avoid

- Stories without a clear persona — "As a user" is too vague
- Missing acceptance criteria — untestable stories cause scope disputes
- Technical tasks disguised as user stories — "As a developer, I want to refactor..." is not a user story
- Stories too large to estimate — split further
- Benefits that don't connect to real user value

## Credits

Original command from the [Claude Code for Product Managers](https://ccforpms.com) course by Carl Vellotti (@carlvellotti), converted to skill format.
