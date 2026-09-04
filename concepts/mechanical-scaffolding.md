# Mechanical Scaffolding

**Core insight**: Separate what is REPEATABLE (structure, format, fields) from what is VARIABLE (context, content, specifics).

## The Problem

Every time you ask an LLM to format a Jira ticket, you spend tokens explaining:
- What fields exist
- What format each should use
- What tone to strike
- What sections to include

This re-explanation happens every single time, even though the structure never changes.

## The Solution

Build the mechanical scaffold ONCE as a script, template, or skill. The LLM's job becomes:
1. Understand the context you provide
2. Fill the scaffold with appropriate content

You pay for structure definition ONCE. Every subsequent use pays only for content.

## Example: Jira Ticket Generator

### Without Scaffolding (every time)

```
Create a Jira ticket for this bug. Include:
- Summary (under 80 chars)
- Description with context
- Acceptance criteria as checkboxes
- Priority suggestion
- Labels

The bug is: users can't log in after password reset...
```

Token cost: ~150 tokens for structure + variable content tokens

### With Scaffolding (one-time setup)

**scaffold.py** (runs locally, zero tokens):
```python
def format_ticket(summary, description, criteria, priority, labels):
    return {
        "fields": {
            "summary": summary[:80],
            "description": format_adf(description),
            "customfield_acceptance": criteria,
            ...
        }
    }
```

**LLM prompt** (each use):
```
Given this bug report, extract:
- one-line summary
- technical description
- acceptance criteria (list)
- suggested priority

Bug: users can't log in after password reset...
```

Token cost: ~50 tokens for extraction + variable content tokens

**Savings**: 60%+ on structure tokens, compounding across every ticket.

## When to Use

| Signal | Action |
|--------|--------|
| You explain the same format repeatedly | Build a scaffold |
| Output format is predictable | Encode it in code |
| Validation rules exist | Move them to the scaffold |
| You copy-paste between prompts | Extract the common parts |

## When NOT to Use

- One-off tasks (no repetition to amortize)
- Exploratory work where format is unknown
- Tasks where the LLM should invent the structure

## Implementation Approaches

1. **Scripts**: Python/JS that calls the LLM API, handles formatting
2. **Skills**: Claude Code skills with embedded templates
3. **Workflows**: Multi-step orchestration with fixed stages
4. **Hooks**: Pre/post processing around LLM calls

## Relationship to SHRINE Patterns

- **Structured Output**: scaffolding is the mechanism, structured output is the pattern
- **Pipeline Orchestration**: scaffolds often form pipeline stages
- **Discovery Propagation**: scaffold improvements propagate to all uses

## Exercise

Identify a task you do weekly that involves:
1. Explaining format to an LLM
2. Producing a predictable output shape
3. Applying consistent validation

Design the scaffold. What stays in code? What does the LLM provide?
