---
# try also 'default' to start simple
theme: seriph
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://cover.sli.dev
# some information about your slides (markdown enabled)
title: Unlocking the Power of Agent-Driven Development with Rules
info: |
  ## Abstract
  AI coding agents are powerful, but they only shine when guided by intentional rules that encode team context, expectations, and guardrails. This talk shares hard-won lessons on designing reusable rules, demonstrates rule tooling in action, and shows how to build an agent-driven workflow that compounds value over time.

  ### Speaker
  Brian Perry · Founding Engineer, Actual AI · Chicago suburbs · Nintendo enthusiast
# apply UnoCSS classes to the current slide
class: text-center
# https://sli.dev/features/drawing
drawings:
  persist: false
# slide transition: https://sli.dev/guide/animations.html#slide-transitions
transition: slide-left
# enable MDC Syntax: https://sli.dev/features/mdc
mdc: true
# duration of the presentation
duration: 45min
---

---
layout: center
---

# The Definitive Guide to Backyard Mushroom Farming

<Notes>
Quick laugh to reset the room before pivoting.
</Notes>

---
layout: center
---

# Just kidding…

Tonight is all about agent-driven development and the rules that make it work.

<Notes>
Transition line: “If you still want mushroom tips, find me after the session.”
</Notes>

---
class: text-left
---

# Unlocking the Power of Agent-Driven Development with Rules

- Brian Perry · Founding Engineer, Actual AI
- Co-authored with Cursor
- November 2025

<Notes>
Welcome everyone, thank the organizers, and acknowledge Cursor as the co-authoring agent.
</Notes>

---
class: text-left
---

# Run of Show

- Why rules are the backbone of productive agents
- Practical rule patterns you can adopt today
- Tooling tour: backlog.md and live demo
- How to keep rules evergreen and measurable

<Notes>
Set expectations for 45 minutes: ~30 content, 10 demo, 5 Q&A.
</Notes>

---
class: text-left
---

# Who Am I?

- Brian Perry, founding engineer at Actual AI
- Building guardrails for AI-enabled software teams
- Based in the Chicago suburbs
- Lifelong Nintendo fan and tinkerer

<Notes>
Share quick anecdote about juggling Smash Bros. tournaments and production incidents.
</Notes>

---
class: text-left
---

# Meet Cursor

- Coding copilot that co-authored this talk
- Rule-focused workflow with reusable instruction sets
- Demonstrates what “rules in action” looks like

<Notes>
Describe how Cursor assisted with drafting these slides.
</Notes>

---
class: text-left
---

# Actual AI in 30 Seconds

- Building tools that help teams operationalize AI guardrails
- Focus on traceability, audit, and continuous improvement
- Rules are first-class: backlog.md, prompt history, review loops

<Notes>
Connect Actual AI’s mission to the theme of intentional rule systems.
</Notes>

---
class: text-left
---

# If You’ve Used Agents…

- Hallucinations and surprising rewrites
- Ambiguous requirements and context gaps
- Difficulty reproducing past success

<Notes>
Ask for a show of hands—who has had an agent overwrite tests?
</Notes>

---
class: text-left
---

# “Treat It Like a Junior Developer”

- Common advice… but junior devs need structure
- I graduated college in 2002—day-one me was chaos
- Mentors, guidelines, docs, repetition made the difference

<Notes>
Paint vivid picture of early-career mistakes to humanize the analogy.
</Notes>

---
class: text-left
---

# Agents Need the Same Support

- Clear scope and expectations
- Access to tribal knowledge
- Feedback loops that stick

<Notes>
Bridge from analogy to actionable need for rules.
</Notes>

---
class: text-left
---

# What Do We Mean by “Rules”?

- Reusable, scoped instructions that encode team practices
- Live alongside your code, prompts, and processes
- Applied automatically so agents don’t rely on memory

<Notes>
Emphasize that rules are not one-off prompts—they are infrastructure.
</Notes>

---
class: text-left
---

# Rule Surfaces

- Workspace-level guardrails (company policies, tone)
- Project rules (architecture, dependencies, naming)
- Task rules (ticket-specific caveats, success criteria)

<Notes>
Explain how layered rules build context over time.
</Notes>

---
class: text-left
---

# Formats Across Tools

| Tool | Rule Mechanism | Notes |
| --- | --- | --- |
| Cursor | cursor.json + per-project configs | Supports priorities and tags |
| Claude Code | “Workspaces” with scoped instructions | Great for tone and safety guardrails |
| Codex | Embedded prompt templates | Often requires manual injection |

<Notes>
Highlight interoperability challenges and need for translation.
</Notes>

---
class: text-left
---

# Anatomy of a Good Rule

- Clear trigger: when and why it applies
- Concrete expectations: “do” and “do not”
- Native references: link to docs, code owners, examples
- Exit criteria: how you know it was followed

<Notes>
Tie back to junior dev experience—specificity beats vibe.
</Notes>

---
class: text-left
---

# Example: Refactor Safety Net

```yaml
id: refactor-guardrails
appliesTo:
  - repo: monorepo
  - folders: ["services/api"]
rules:
  - Always run `pnpm test services/api` before committing refactors.
  - Never modify generated files under `services/api/generated`.
  - Flag breaking API changes in `backlog.md` with label `api-break`.
```

<Notes>
Walk through each bullet and the operational benefit.
</Notes>

---
class: text-left
---

# Practical Strategies

- Start with your “gotchas” list—codify it
- Pair rules with checklists and code review templates
- Measure adherence: linting, CI checks, retro feedback

<Notes>
Encourage teams to evolve rules weekly, not quarterly.
</Notes>

---
class: text-left
---

# Keep Rules Discoverable

- Store in version control next to source
- Provide short URLs in onboarding docs
- Use backlog.md to capture rule debt and updates

<Notes>
Share how Actual AI customers track rule drift.
</Notes>

---
class: text-left
---

# Demo: Rules-Driven Workflow

- Scenario: shipping a feature with Cursor and backlog.md
- Goal: show rule lookup, application, and feedback loop
- Outcome: agent completes task with minimal rework

<Notes>
Set expectations before switching to demo environment.
</Notes>

---
class: text-left
---

# Demo Flow

1. Pull latest rules from repo
2. Kick off Cursor task with scoped instructions
3. Watch backlog.md capture follow-up items
4. Review diff and compare against rule checklist

<Notes>
Highlight what to watch for: rule invocation, logging, iteration.
</Notes>

---
class: text-left
---

# Demo Contingency Plan

- Pre-recorded clip ready if wifi flakes
- Screenshots staged for key rule interactions
- Summary slide with takeaways if time runs short

<Notes>
Reassure audience that insights land even without live demo.
</Notes>

---
class: text-left
---

# Measuring Success

- Track agent-produced PR rework rate
- Survey developers on trust and velocity
- Audit rule coverage quarterly

<Notes>
Encourage teams to treat rules as product features.
</Notes>

---
class: text-left
---

# Key Takeaways

- Agents are only as effective as the rules around them
- Rules must be layered, discoverable, and evolving
- Tooling like backlog.md turns rules into workflows

<Notes>
Reinforce three memorable points.
</Notes>

---
class: text-left
---

# Resources

- resources/abstract.md for session summary
- resources/outline.md for planning notes
- Actual AI blog: guardrails best practices
- Cursor docs: rule configuration examples

<Notes>
Invite attendees to connect for templates and demos.
</Notes>

---
layout: center
---

# Q&A

What rule will you write first?

<Notes>
Open the floor, remind about contact info after session.
</Notes>