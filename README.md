# PM Skill Factory

Claude Code skills for Product Managers. Frameworks, workflows, and domain knowledge that Claude activates automatically when you're working on product tasks.

## Skills Included

### Product Thinking (auto-trigger)
| Skill | Description |
|-------|-------------|
| `lean-delivery` | Story slicing, Hamburger Method, micro-steps |
| `lean-analytics` | SaaS metrics, OMTM, cohorts, churn, MRR |
| `impact-growth` | Impact-Driven Growth, CPVM, outcomes over outputs |
| `user-research` | Research synthesis, pain points, JTBD |
| `business-strategy` | Strategy Kernel (Rumelt), diagnosis, coherent actions |
| `executive-communication` | Executive summaries, stakeholder framing |
| `technical-review` | Feasibility assessment, spec review, effort estimation |
| `lean-product-manager` | Lean Startup, Build-Measure-Learn, team management |

### PM Workflows (auto-trigger)
| Skill | Description |
|-------|-------------|
| `create-prd` | Product Requirements Documents |
| `write-user-stories` | User stories with acceptance criteria |
| `analyze-feedback` | Feedback analysis, themes, pain points |
| `prioritize-features` | RICE, ICE, Value vs Effort, Kano, MoSCoW |
| `competitive-analysis` | Competitor research, SWOT, positioning |
| `roadmap-planning` | Strategic roadmaps with themes and sequencing |
| `feature-discovery` | Idea validation: pursue, hold, or kill |
| `calculate-roi` | ROI, payback period, business cases |

## Quick Start

1. Clone this repo
2. Install skills globally: symlink each skill folder to `~/.claude/skills/`
3. Restart Claude Code
4. Claude will activate skills automatically based on context

## Using Your Skill

This repo includes a `./skills` helper script for global installation.

**Global** (all projects) — use the script to symlink to `~/.claude/skills/`:

```bash
./skills toggle    # interactive picker
./skills status    # check what's installed
```

Edits to `output_skills/` apply immediately since it's a symlink.

**Local** (single project) — copy the skill folder to your project's `.claude/skills/` or create a symlink in your project yourself.

## STARTER_CHARACTER

Each skill defines a `STARTER_CHARACTER = [emoji]` at the top. This is a visual indicator that Claude has loaded the skill and is following its instructions. For example, the nullables skill uses ⭕️ and TDD uses 🔴/🌱/🌀.

To activate this, add the following to your global `~/.claude/CLAUDE.md`:

```
Always start replies with STARTER_CHARACTER + space (default: 🍀). Stack emojis when requested, don't replace.
```

Pick any default emoji you like — it confirms Claude is reading your ground rules. When a skill activates, its emoji stacks on top: `🍀 ⭕️` means both your global rules and the nullables skill are active.

Without this line in your global CLAUDE.md, the `STARTER_CHARACTER` lines in skills might have unpredictable behavior.

## Updating Best Practices

```bash
./update-docs
```

Pulls latest skill patterns from Anthropic.

## Creating New Skills

This repo is also a skill factory. Open this folder in Claude Code, ask it to create a new skill, and it will follow the process in `docs/create_new_skill-process.md`.

## Structure

```
output_skills/
  product-management/  — PM skills (16)
  design/              — Design skills
  practices/           — Delivery practices
  tools/               — Utility skills
docs/                  — Skill creation knowledge and patterns
```
