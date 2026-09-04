# Full-Day Workshop (8 hours)

**Audience**: Teams building AI-assisted workflows or integrating LLMs into products.

**Prep**: Review [SHRINE patterns](https://stablekernel.github.io/SHRINE/patterns/overview/) and [proposals](https://github.com/stablekernel/SHRINE/discussions/categories/proposals) before delivering.

## Agenda

### Morning Session

#### Block 1: Foundations (90 min)

| Time | Topic | SHRINE Link |
|------|-------|-------------|
| 0:00 | Welcome, objectives, participant intros | |
| 0:15 | The context window: mechanics and mental model | |
| 0:35 | [TTV: Tokens to Value](https://github.com/stablekernel/SHRINE/discussions/2): measuring what matters | Proposal #2 |
| 0:55 | [Task Routing](https://stablekernel.github.io/SHRINE/patterns/task-routing/): when to use what | Pattern |
| 1:15 | Live demo: task routing across models | |
| 1:30 | Q&A | |

#### Break (15 min)

#### Block 2: Prompting Patterns (75 min)

| Time | Topic | SHRINE Link |
|------|-------|-------------|
| 1:45 | [Chain of Thought](https://stablekernel.github.io/SHRINE/patterns/chain-of-thought/): forcing explicit reasoning | Pattern |
| 2:00 | [Few-Shot Examples](https://stablekernel.github.io/SHRINE/patterns/few-shot-examples/): teaching by showing | Pattern |
| 2:15 | [Structured Output](https://stablekernel.github.io/SHRINE/patterns/structured-output/): schemas, JSON mode | Pattern |
| 2:35 | Lab: convert a prose prompt to structured | |
| 3:00 | Q&A | |

#### Lunch (60 min)

### Afternoon Session

#### Block 3: Scaffolding and Consistency (90 min)

| Time | Topic | SHRINE Link |
|------|-------|-------------|
| 4:00 | [Mechanical Scaffolding](https://stablekernel.github.io/SHRINE/patterns/mechanical-scaffolding/): separate structure from content | Pattern |
| 4:15 | [Consistency as Leverage](https://github.com/stablekernel/SHRINE/discussions/6): codebase predictability | Proposal #6 |
| 4:35 | Case study: Jira tickets, PR bodies, status reports | |
| 4:55 | Lab: design a scaffold for your team's workflow | |
| 5:30 | Share-outs | |

#### Break (15 min)

#### Block 4: Verification and Trust (60 min)

| Time | Topic | SHRINE Link |
|------|-------|-------------|
| 5:45 | [Fail Fast, Recover Smart](https://github.com/stablekernel/SHRINE/discussions/7): designing for failure | Proposal #7 |
| 6:00 | [Self-Critique](https://stablekernel.github.io/SHRINE/patterns/self-critique/): model checks itself | Pattern |
| 6:15 | [Adversarial Review](https://stablekernel.github.io/SHRINE/patterns/adversarial-review/): external skeptic | Pattern |
| 6:30 | [Human in the Loop](https://github.com/stablekernel/SHRINE/discussions/8): where automation stops | Proposal #8 |
| 6:45 | Q&A | |

#### Break (15 min)

#### Block 5: Orchestration (60 min)

| Time | Topic | SHRINE Link |
|------|-------|-------------|
| 7:00 | When single prompts are not enough | |
| 7:10 | [Pipeline Orchestration](https://stablekernel.github.io/SHRINE/patterns/pipeline-orchestration/): chaining stages | Pattern |
| 7:25 | [Subagent Fanout](https://stablekernel.github.io/SHRINE/patterns/subagent-fanout/): parallel work | Pattern |
| 7:40 | Live demo: code review workflow | |
| 8:00 | Q&A | |

#### Block 6: Synthesis (30 min)

| Time | Topic |
|------|-------|
| 8:00 | Recap: TTV, scaffolding, verification, orchestration |
| 8:10 | Action planning: what will you try Monday? |
| 8:20 | Resources: [SHRINE](https://stablekernel.github.io/SHRINE/), [staying current](https://github.com/stablekernel/SHRINE/discussions/3) |
| 8:30 | Close |

## Materials Needed

- Laptops with Claude Code, Cursor, or similar [harness](https://stablekernel.github.io/SHRINE/stack/harness/)
- Real domain data from attendees
- [SHRINE docs](https://stablekernel.github.io/SHRINE/) bookmarked
- Whiteboard for diagramming

## Outcomes

Attendees leave with:
- Deep understanding of TTV and model selection
- Multiple working scaffolds for real tasks
- Verification strategy for their use case
- Action plan for team adoption
