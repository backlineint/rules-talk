---
theme: seriph
title: Unlocking the Power of Agent-Driven Development with Rules
info: |
  How clear, reusable rules unlock reliable AI coding agents.
class: text-left
transition: slide-left
mdc: true
duration: 45min
---

---
layout: cover
background: linear-gradient(135deg, #020024 0%, #1f3a93 35%, #0b8793 100%)
---
# Unlocking the Power of Agent-Driven Development with Rules
## Building trustworthy AI teammates with great guardrails
Brian Perry · Founding Engineer, Actual AI

---
layout: statement
---
# Agenda
- Why rules matter for agents
- Rule formats across Cursor, Claude Code, and Codex
- Building rules that grow with your workflow
- Demo: rules in action inside Cursor
- Takeaways you can apply today

---
layout: statement
---
# BREAKING NEWS: Let’s review the 1993 Chicago Bulls playbook

---
layout: statement
class: text-primary
---
# Just kidding.  
## We’re here for agent-driven development—and how rules make it real.

---
layout: two-cols
---
### Hi, I'm Brian Perry
- Founding Engineer, Actual AI
- Chicago suburbs based
- Nintendo superfan

::right::
```
Actual AI · Guardrails for AI-enabled software teams
```

---
layout: image-right
image: ./resources/images/junior_dev1.jpeg
---
# Junior Developer Brian (2002)
- Bright-eyed, slightly overwhelmed
- Needed mentors, clear guidelines, and repetition
- Made every mistake twice—sometimes three times

---
layout: statement
---
# Agents feel the same way I did back then

---
layout: image-right
image: ./resources/images/junior_dev2.jpeg
---
# What junior Brian needed
- Documented expectations
- Repeatable checklists
- Reliable feedback loops

<!-- Agents need the same guardrails to succeed -->

---
layout: two-cols
---
### Actual AI
- Building rails for reliable AI teammates
- Opinionated workflows, not generic chatbots
- Rules-first approach guides every feature

::right::
### Cursor: Co-Author of This Talk
- Drafted content, iterated on demos, tightened language
- `.cursor/rules` keeps Cursor aligned with the story arc
- This deck is proof: rules + agents = high-leverage output

---
layout: statement
---
# Agents without rules are unpredictable collaborators

---
layout: fact
---
## My journey
- 2023: skeptical observer  
- 2024: experimenting with coding agents  
- 2025: rules-driven development is default

---
layout: statement
---
# Rules give agents reusable, scoped intent

---
layout: two-cols
---
::left::
### What are rules?
- Persistent instructions scoped to repos, teams, or flows
- Guardrails that outlive a single conversation
- Documentation that agents actually read

::right::
### Why they matter
- Reduce re-prompting and frustration
- Encode best practices as you discover them
- Align agents to product, process, and tone

---
layout: two-cols
---
::left::
### Rule Formats Landscape
- `AGENTS.md` for human + agent collaborators
- Cursor `.cursor/rules` folders
- Claude Code `.claude/rules` workspaces
- Codex project rulesets

::right::
### Keep them consistent
- Shared vocabulary and examples
- Explain the "why," not just the "what"
- Version alongside the codebase

---
layout: two-cols
---
::left::
### `AGENTS.md`
- Home base for mixed human/agent collaboration
- Surfaces essential context, constraints, and resources
- Lives in the repo so agents can cite it

::right::
```
# Slide Presentation
Build the actual deck, not just an outline.
Resources live in /resources.
Use Slidev layouts and images.
```

---
layout: two-cols
---
::left::
### Cursor Rules
- `.cursor/rules` directory scopes instructions
- Supports contextual docs via Context7 MCP
- Keeps agents aligned with story arcs and demos

::right::
```
## Creating Slides
- Slides live in slides.md
- Use Context7 for Slidev docs
- Favor repo-local context
```

---
layout: two-cols
---
::left::
### Claude Code Rules
- `.claude/rules` mirrors repo structure
- Great for pairing multiple Claude agents
- Explicitly define style, tone, and safety rails

::right::
- Treat Claude like a teammate on rotation
- Keep rules short, link out to deeper docs
- Capture "do this, not that" examples

---
layout: two-cols
---
### Codex Rules
- Codex rulesets bundle instructions + tools
- Encourage scoped playbooks per workflow
- Automations reference shared rule libraries

::right::
- Document trigger conditions
- Provide testable acceptance criteria
- Pair rules with backlog-driven work

---
layout: statement
---
# When you correct an agent, capture it as a rule

---
layout: default
---
### Rules about Rules
- Ask the agent to draft the rule it needed
- Refine, commit, and reuse
- Let git history show how rules evolved

```
- If AI gets it wrong, don’t give up—write a rule.
- Favor context inside the repo over external links.
```

---
layout: two-cols
---
::left::
### Stop Hallucinations with Context
- Provide docs, not vibes
- Co-locate examples, APIs, and constraints
- Automate context delivery with MCP servers

::right::
```
{
  "mcpServers": {
    "context7": {
      "url": "https://mcp.context7.com/mcp",
      "headers": {
        "CONTEXT7_API_KEY": "YOUR_API_KEY"
      }
    }
  }
}
```

---
layout: two-cols
---
::left::
### Slide Rules in Practice
- Slides belong in `slides.md`
- Use Slidev layouts for narrative impact
- Include speaker notes as HTML comments only

::right::
```
---
layout: image-right
image: ./resources/images/junior_dev2.jpeg
---
```

---
layout: statement
---
# Workflow Pattern: Backlog + Rules + Agents

---
layout: two-cols
---
::left::
### Workflow Building Blocks
- `backlog.md` captures scoped tasks
- Rules encode expectations
- Agents execute, humans review

::right::
### Feedback Loop
1. Spot friction → capture rule  
2. Update backlog item  
3. Re-run agent with new context  
4. Celebrate consistency

---
layout: statement
---
# Demo Plan: Cursor + Rules + Context7
- Show `.cursor/rules` in action
- Pull docs from Context7
- Iterate live on a backlog item

---
layout: fact
---
## Key Takeaways
- Rules turn agents into reliable collaborators
- Keep formats in sync across tools
- Capture every correction as a reusable guardrail
- Context delivery (MCP, docs) prevents hallucinations

---
layout: statement
---
# Ready to unlock agent-driven development?
## Start by writing one new rule today.