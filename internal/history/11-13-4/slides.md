---
theme: seriph
background: '#2b2b2b'
title: 'Unlocking the Power of Agent-Driven Development with Rules'
info: |
  ## Unlocking the Power of Agent-Driven Development with Rules
  
  Presentation on how rules transform AI coding agents from unreliable assistants 
  into powerful development partners.
class: text-center
drawings:
  persist: false
transition: slide-left
mdc: true
duration: 35min
---

# Unlocking the Power of Agent-Driven Development with Rules

*Transform your AI coding agents from unreliable assistants into powerful development partners*

---
layout: image-right
image: /resources/images/brian-perry.jpg
---

# About Me

**Brian Perry**
- Founding Engineer at Actual AI
- Building guardrails for AI-enabled teams
- Chicago suburbs resident
- Nintendo enthusiast

📘 [bsky.app/profile/brianperry.dev](https://bsky.app/profile/brianperry.dev)  
🐙 [github.com/backlineint](https://github.com/backlineint)

<!-- Speaker notes: Brief intro, set the stage for credibility -->

---
layout: center
---

# Co-Author of This Talk

## Claude Code helped draft content, iterate on demos, and tighten language

- `CLAUDE.md` keeps Claude aligned with the story arc
- Today's deck is proof that rules + agents co-create real work
- Rules enabled this collaboration

<!-- This slide demonstrates the power of rules in action -->

---
layout: image-right
image: /resources/images/actual-ai.png
---

# Actual AI

Building tools to provide **guardrails** for AI-enabled software teams

- Rules management and governance
- Agent behavior consistency
- Team workflow alignment
- Enterprise AI safety

*Making AI agents reliable partners, not unpredictable assistants*

---
layout: center
class: text-center
---

# The Problem

## We've all experienced AI making mistakes

---

# Common Advice

> "Think of AI as a Junior Developer"

## Personal reflection: 
*I graduated in 2002 - thinking of me 23 years ago is horrifying*

<!-- What I needed back then: mentors, guidelines, documentation, trial and error -->

---
layout: image-right
image: /resources/images/junior_dev1.jpeg
---

# What Junior Developers Need

- **Mentors** to guide them
- **Guidelines** to follow  
- **Documentation** to reference
- **Trial and error** to learn

## Coding agents need the same thing

*Rules provide structure and guardrails*

---
layout: center
---

# What Are Rules?

## 📝 Reusable, scoped instructions that control agent behavior
## 🎯 They provide structure and guardrails  
## 🔄 They enable consistent, predictable outcomes

---

# Rules in Practice

Rules are defined in your codebase as **markdown files**

They tell agents:
- How to write code in your style
- What patterns to follow
- What to avoid
- Project-specific context

## *"If AI gets it wrong, don't give up - write a rule"*

---
layout: two-cols
layoutClass: gap-16
---

# Rules vs Prompts

**Rules:**
- Persistent and reusable
- Version controlled
- Team shareable
- Hierarchical application
- System-level authority

::right::

**Prompts:**
- One-time instructions
- Session specific
- Individual usage
- Single context
- User-level requests

---

# Understanding Rules Formats

Different tools, different approaches:

- **Cursor** - `.cursor/rules` files
- **Claude Code** - `CLAUDE.md` files  
- **GitHub Copilot** - `.github/copilot-instructions.md`
- **Agents.md** - Emerging standard

---
layout: two-cols
layoutClass: gap-16
---

# Cursor Rules

```markdown
---
description: React component patterns
globs: "**/*.tsx"
alwaysApply: false
---

- Use functional components with hooks
- Implement proper TypeScript types
- Follow component composition patterns
```

::right::

**Key Features:**
- MDC format with metadata
- Glob pattern targeting
- Intelligent vs always apply
- Nested rule directories
- Team/enterprise rules

---
layout: two-cols
layoutClass: gap-16
---

# Claude Code (CLAUDE.md)

```markdown
# Project Architecture

This is a React TypeScript project using:
- Vite for bundling
- Tailwind for styling
- Zustand for state management

## Coding Standards
- Use functional components
- Prefer composition over inheritance
- Always include TypeScript types
```

::right::

**Key Features:**
- Markdown format
- Project and user scopes
- Strict instruction hierarchy
- Memory integration
- XML for complex rules

---
layout: two-cols
layoutClass: gap-16
---

# GitHub Copilot

```markdown
# Repository Instructions

Use double quotes for JavaScript strings.
Prefer tabs over spaces for indentation.
Always include JSDoc comments for functions.

## Security
- Validate all inputs
- Use environment variables for secrets
```

::right::

**Key Features:**
- `.github/copilot-instructions.md`
- Repository-wide scope
- Path-specific instructions
- Agent-specific files (AGENTS.md)
- Natural language format

---

# Agents.md Standard

Emerging cross-tool standard:

```markdown
# AI Agent Instructions

## Code Style
- Use TypeScript for all new code
- Follow existing patterns in the codebase
- Add tests for new functionality

## Architecture
- Keep components small and focused
- Use custom hooks for shared logic
```

**Benefits:** Tool-agnostic, widely supported, simple format

---
layout: center
---

# Building a Rules-Driven Workflow

## Start small → Iterate → Scale

---

# Step 1: Identify Pain Points

Common scenarios where rules help:

- **Inconsistent code style** → Style rules
- **Wrong patterns used** → Architecture rules  
- **Missing tests** → Testing rules
- **Security issues** → Security rules
- **Framework misuse** → Framework rules

---

# Step 2: Write Your First Rule

```markdown
# Testing Requirements

## Unit Tests
- Every new function needs a unit test
- Use Jest with @testing-library for React components
- Aim for 80%+ code coverage

## Test Structure
- Arrange, Act, Assert pattern
- Descriptive test names
- One assertion per test when possible
```

**Key:** Be specific, provide examples, explain the "why"

---

# Step 3: Iterate and Improve

Rules evolve with your codebase:

- **Monitor** agent behavior
- **Identify** new patterns
- **Refine** existing rules
- **Share** with team
- **Version control** everything

## Rules are living documentation

---
layout: center
---

# Demo: Rules in Action

*Live demonstration of rule-driven development*

<!-- Show actual coding session with rules -->

---

# Best Practices

## Keep rules under 500 lines
## Split large rules into composable pieces
## Provide concrete examples
## Avoid vague guidance
## Write rules like clear documentation

---

# Tools and Ecosystem

**Rule Management:**
- Version control rules with code
- Use rule templates for new projects
- Create rule libraries for common patterns

**Integration:**
- CI/CD validation
- Team rule sharing
- Rule conflict detection

---

# The Future of Rules

**Emerging trends:**
- Cross-tool compatibility (Agents.md)
- AI-generated rules from codebases
- Dynamic rule application
- Rule effectiveness metrics
- Team rule governance

---
layout: center
---

# Key Takeaways

## 🎯 Rules transform agents from assistants to partners
## 📚 Different tools have different formats - choose what fits
## 🔄 Start with pain points, iterate based on results  
## 👥 Rules enable team-wide consistency
## 🚀 Rules-driven development is the future of AI coding

---
layout: center
class: text-center
---

# Questions?

**Brian Perry**  
📘 [bsky.app/profile/brianperry.dev](https://bsky.app/profile/brianperry.dev)  
🐙 [github.com/backlineint](https://github.com/backlineint)

*Thank you for attending!*

<!-- 
Presentation notes:
- Total slides: ~25, appropriate for 35min duration
- Good mix of content, code examples, and visuals
- Clear narrative arc from problem to solution
- Includes concrete examples and actionable advice
- Ends with forward-looking perspective
-->