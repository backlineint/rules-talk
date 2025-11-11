---
# try also 'default' to start simple
theme: seriph
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://cover.sli.dev
# some information about your slides (markdown enabled)
title: Unlocking the Power of Agent-Driven Development with Rules
info: |
  ## Unlocking the Power of Agent-Driven Development with Rules
  A 45-minute walkthrough of how scoped instructions transform AI coding agents into reliable teammates.
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

# Unlocking the Power of Agent-Driven Development with Rules

Guardrails that turn AI coding agents into reliable teammates.

---

# Agenda

- Why rules matter for agent-driven development
- Rule formats across Cursor, Claude Code, and Codex
- Feeding context with MCP & Context7
- Demo: rules-driven workflow in practice
- Recap and Q&A

<!-- Mention time expectations verbally -->

---

# Quick Detour 🤪

This talk is actually about sourdough starters.

<div v-click class="mt-6 text-secondary">
  Just kidding — let’s talk rules.
</div>

---

# About Brian

- Founding engineer @ Actual AI
- Chicago suburbs based
- Lifelong Nintendo fan
- Former agent skeptic turned daily power user

---

# About Actual AI

- Building guardrails for AI-enabled software teams
- Focused on rules, context delivery, and workflow insights
- Collaboration-first tooling

---

# Co-Author: Cursor

- Partner in building these slides
- Highlights how rules shape agent behavior
- Will appear in the demo segment

---

# AI Always Makes Mistakes First

- Everyone has seen hallucinations or wrong edits
- Default reaction: "Just fix it by hand"
- Opportunity: teach the agent instead

---

# Think Junior Developer

- Common advice: treat AI like a junior dev
- Junior devs improve with structure, mentorship, feedback
- Agents respond similarly to clear rules and context

---

# Brian, 2002

- Fresh grad without guardrails
- Needed mentors, docs, and patience
- Agents are at that stage today

---

# Rules Are Reusable Guardrails

- Scoped instructions that steer behavior
- Reapply successful patterns across tasks
- Combine with contextual docs for reliability

---

# Rule Strategy Patterns

- Capture corrections as new rules
- Organize rules by domain, tool, or workflow stage
- Revisit rules during retrospectives

---

# Cursor Rule Format

- Structured YAML with globals, tools, directives
- Strong integration with repository context
- Supports MCP fetches and task-specific overrides

---

# Claude Code Rules

- Conversation-level instructions
- Emphasis on tone, completeness, and safety
- Works well for exploratory coding sessions

---

# Codex Rules

- Persistent guidelines in `codex.rules`
- Use for formatting, test coverage, review etiquette
- Encourage short, auditable diffs

---

# backlog.md Pattern

- Living log of decisions, todos, and clarifications
- Source material for future rules
- Keeps humans and agents aligned

---

# Context Delivery with MCP

- Let agents read docs on demand
- Configure Context7 via `.cursor/mcp.json`
- Ensure API keys and scopes are documented

---

# Context7 Highlights

- Fresh docs for tools like Slidev
- Semantic retrieval keeps prompts focused
- Great for live coding or documentation questions

---

# Actual AI Guardrails

- Vision: centralized rule management
- Metrics on rule usage & agent adherence
- Early adopter stories (teaser)

---

# Demo Setup

- Scenario: agent refactors feature with new rule set
- Tools: Cursor + Context7 docs + backlog.md
- Goal: show iteration loop and rule capture

---

# Demo Flow

1. Run into an agent misstep
2. Draft or refine a rule
3. Re-run agent with added context
4. Log learnings in backlog.md

---

# Wrap-Up

- Rules amplify agent reliability
- Tooling choices matter (Cursor, Claude Code, Codex)
- Context pipelines (MCP, Context7) close the loop
- Start small, iterate, and capture every correction

---

# Resources & Next Steps

- `resources/abstract.md`, `resources/outline.md`
- Cursor + Context7 configuration examples
- Actual AI waitlist link
- Follow Brian for updates

---

# Q&A

What rules will you write first?

<!-- Encourage audience participation -->