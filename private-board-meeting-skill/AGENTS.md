---
name: private-board-meeting-skill
platforms: [claude-code, cursor, copilot, cline, roo-code, windsurf, aider, hermes-agent]
---

# Private Board Meeting Skill — AGENTS.md

## Skill Purpose

Simulates a structured private board meeting (私董会) where 7 top business advisors review a user's major business decision. Delivers sharp, personality-consistent feedback with actionable synthesis.

## Activation Triggers

### Direct Commands
- `/private-board-meeting`
- `/私董会`

### Natural Language Detection
Activate when user's message contains:
- 私董会 / 董事会 / 重大决策
- "board meeting" / "advisory board"
- "帮我做个决策" / "这个决定对不对"
- "找人帮我看看这个决策"
- Multi-path business decisions requiring structured evaluation

### Context Clues
- User describes a significant business decision with trade-offs
- User explicitly asks for multiple perspectives
- User mentions needing "顾问意见" or "专家评审"

## Usage Instructions

### For Claude Code / Cursor / Copilot
1. Read `SKILL.md` when triggered
2. Follow the 4-step workflow exactly
3. Reference `references/advisor-profiles.md` for personality consistency
4. Use `references/output-templates.md` for output formatting

### For Hermes Agent
```
skill_view(name='private-board-meeting-skill')
```

### Workflow Summary
1. **Gather** — Decision Anchor Four-Pack (decision subject, content, time window, real constraints)
2. **Pre-review** — Chairman identifies real problem, proposes A/B/C paths with odds×winrate×cost
3. **Deliberate** — 7 advisors speak sequentially with structured output (stance, reasons, questions, quote)
4. **Synthesize** — Chairman delivers vote count, consensus, disagreements, final recommendation + truth line

## Personality Registry

| # | Advisor | Core Lens | Language |
|---|---------|-----------|----------|
| 1 | Steve Jobs | Product zealot, subtraction | EN→ZH |
| 2 | Elon Musk | First principles, 10x | EN→ZH |
| 3 | Warren Buffett | Safety margin, circle of competence | EN→ZH |
| 4 | Jeff Bezos | Customer obsession, long-term | EN→ZH |
| 5 | 任正非 | Crisis consciousness, organization | ZH native |
| 6 | 段永平 | 本分, 平常心, anti-checklist | ZH native |
| 7 | Peter Thiel | Anti-consensus, monopoly, 0→1 | EN→ZH |

## Hard Constraints (Cross-Platform)

All implementations MUST enforce:
1. Four-Pack incomplete → no deliberation
2. Advisors must disagree — no unanimous consensus allowed
3. Chairman takes clear stance — no neutrality
4. One truth-telling line that may offend the user — mandatory, cannot be softened
5. Personality consistency — no AI-style neutralization of advisor voices

## File Map

```
private-board-meeting-skill/
├── SKILL.md                          # Main framework (Chinese)
├── AGENTS.md                         # This file (cross-platform)
├── references/
│   ├── advisor-profiles.md           # Detailed personality specs
│   └── output-templates.md           # Example output structures
└── README.md                         # Installation guide
```
