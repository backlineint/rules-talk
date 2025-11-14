---
theme: seriph
background: https://cover.sli.dev
title: Unlocking the Power of Agent-Driven Development with Rules
info: |
  ## Unlocking the Power of Agent-Driven Development with Rules
  
  The effectiveness of AI coding agents has grown exponentially in the past year. Yet many developers and teams still find themselves struggling to see the benefits they expect, or abandoning these tools altogether.
  
  In this session, we'll explore one of the overlooked keys to making coding agents truly effective: rules.
drawings:
  persist: false
transition: slide-left
mdc: true
duration: 35min
---

# Unlocking the Power of Agent-Driven Development with Rules

Brian Perry • Actual AI

---
layout: two-cols
---

# About Brian Perry

- Founding Engineer at Actual AI
- Lives in Chicago suburbs
- Loves Nintendo
- Former Drupal developer turned AI enthusiast

### Connect
- GitHub: github.com/backlineint
- Bluesky: bsky.app/profile/brianperry.dev

::right::

<img src="/resources/images/brian-perry.jpg" alt="Brian Perry" class="rounded-lg shadow-lg w-64 mx-auto" />

<!-- Speaker notes: Brief intro about myself and my background -->

---
layout: center
---

# Claude Code: Co-Author of This Talk

- Claude helped draft content, iterate on demos, and tighten language
- `CLAUDE.md` keeps Claude aligned with the story arc  
- Today's deck is proof that rules + agents co-create real work

<!-- This demonstrates the power of rules-driven collaboration -->

---
layout: image
image: /resources/images/actual-ai.png
---

<!-- Company slide showcasing Actual AI -->

---
layout: center
class: text-center
---

# The Problem

## Everyone has experienced AI making mistakes

---
layout: quote
---

# "Think of AI as a Junior Developer"
## Common advice, but incomplete

---
layout: two-cols
---

# I graduated in 2002...

Thinking of me as a developer 23 years ago is horrifying

## What I needed:
- Mentors
- Guidelines  
- Documentation
- Trial and error

::right::

<img src="/resources/images/junior_dev.jpg" alt="Junior developer Brian" class="rounded-lg shadow-lg w-64 mx-auto" />

<!-- Coding agents need the same structure and guidance -->

---
layout: center
---

# Coding agents need the same thing

---
layout: section
---

# Why Rules Matter

---

# What are rules?

📝 **Reusable, scoped instructions that control agent behavior**

🎯 **They provide structure and guardrails**

🔄 **They enable consistent, predictable outcomes**

Rules are defined in your codebase as markdown files.

*It is a charmingly low tech solution.*

---

# Note: We're not talking about the Drupal Rules module here

*(Though that was pretty cool too)*

---
layout: section
---

# Understanding Rules Formats

---

# Rules Formats Overview

Different tools, different approaches:

- **Cursor**: `.cursorrules` and `.cursor/rules`
- **Claude Code**: `CLAUDE.md` 
- **GitHub Copilot**: `.github/copilot-instructions.md`
- **Agents.md**: Emerging standard

---

# Cursor Rules Format

## `.cursorrules` file in project root
```markdown
# Project Rules

Use TypeScript for all new code
Follow existing code patterns
Prefer functional programming approaches
```

## `.cursor/rules` directory for scoped rules
Supports project-specific rules and Agents.md format

---

# Claude Code Rules Format

## `CLAUDE.md` in project root
```markdown
# Project Instructions

Build a presentation ready slide deck, not just an outline.
Don't repeat a previous version of this presentation.

## Important Resources
Important resources live in the /resources directory
```

---

# GitHub Copilot Rules Format

## Repository-wide instructions
`.github/copilot-instructions.md`

## Path-specific instructions  
`*.instructions.md` files throughout codebase

---

# Agents.md: The Emerging Standard

## Supported by Cursor and Copilot
*(but not Claude Code yet)*

```markdown
# Agent Instructions

This codebase follows these conventions...
Use these libraries and patterns...
```

**I really wish everyone could just standardize on Agents.md**

---
layout: section
---

# Practical Strategies from Building This Talk

---

# Started with High-Level Rules

```markdown
# Slide Presentation

Build a presentation ready slide deck, not just an outline.
Don't repeat a previous version of this presentation.
```

**Problem**: With only this context, the agent will still make stuff up

---

# Added Rules to Guide Context Discovery

```markdown
## Important Resources

Important resources live in the /resources directory, including:

- abstract.md - description of the session
- outline.md - in-progress outline of session content  
- images directory - images to prioritize in presentation
```

*Lead the agent to the most important context*

---

# Framework-Specific Rules

```markdown
- example-slides.md - examples of slides created with Slidev

## Creating Slides
- When authoring slides, content belongs in slides.md
- The slides are a Slidev project. For documentation use context7
```

*Help the agent understand the tools and frameworks*

---

# Using MCP for External Knowledge

```markdown
### Rules formats
- We'll cover Agents.md, Cursor, Claude Code, and Github Copilot. use context7
```

**context7** tells the agent to use the Context7 MCP server

**MCP** = Model Context Protocol - allows agents to access external tools and data sources

---

# Rules from Iteration and Correction

When you find yourself correcting an agent, define a rule:

```markdown
- Make sure text doesn't overflow. Max 8 lines per slide
- Slides should have sufficient contrast for dark mode
- Never use the class: text-center
- Include speaker notes as HTML comments
```

*If AI gets it wrong, don't give up - write a rule*

---

# Nested Rules and Scoping

Most tools allow co-located rules files for increased priority or scoped application

## Example: `/resources/images/CLAUDE.md`
```markdown
# Images for Slides

- junior_dev.jpg - image of me as a junior developer
- brian-perry.jpg - good photo for bio slide  
- actual-ai.png - company slide image
```

*Context-specific rules help with precise selections*

---
layout: section
---

# Tools for Rules-Driven Workflows

---

# Backlog.md

A tool for managing project collaboration between humans and AI Agents in a git ecosystem

**Behind the scenes**: Complex rules that enable structured collaboration

*Demo time!*

---

# Cursor Plan Mode

Interactive planning with rules-driven suggestions

*Let's see it in action*

---
layout: image
image: /resources/images/context_in_repository.png
---

<!-- Example of keeping context in repository for AI agents -->

---
layout: section
---

# Miscellaneous Tips and Tricks

---

# Keep Additional Context in Repository

**If the agent can't see it, it probably doesn't know it**
*(and might make it up)*

- Save evaluation runs to codebase
- Include relevant documentation
- Store examples and templates

---

# The Basics Matter Even More

When working with agents, fundamental practices become critical:

- **Linting** - Consistent code style
- **Testing** - Verify agent output  
- **Documentation** - Help agents understand context

---
layout: section
---

# Conclusion & Takeaways

---

# Key Takeaways

🎯 **Rules are critical** to successful agent-driven development

📝 **Start simple**, then iterate based on agent corrections

🔧 **Choose the right format** for your tools and team

🚀 **Build a rules library** for consistent outcomes

---

# Call to Action

1. **Try rules** with your current AI coding tools
2. **Start a rules library** for your team
3. **Iterate and improve** based on agent behavior
4. **Share your patterns** with the community

---
layout: center
class: text-center
---

# "If AI gets it wrong, don't give up - write a rule"

---
layout: center
---

# Questions?

**Brian Perry**  
GitHub: github.com/backlineint  
Bluesky: bsky.app/profile/brianperry.dev

**Actual AI**  
Building the future of AI-powered development