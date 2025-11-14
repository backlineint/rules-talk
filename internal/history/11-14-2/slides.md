---
theme: seriph
background: https://cover.sli.dev
title: Unlocking the Power of Agent-Driven Development with Rules
info: |
  ## Unlocking the Power of Agent-Driven Development with Rules
  Learn how to make AI coding agents truly effective through rules-driven development
transition: slide-left
mdc: true
duration: 45min
---

# Unlocking the Power of Agent-Driven Development with Rules

Learn how to make AI coding agents truly effective

<!-- Speaker notes: Welcome everyone to the session on unlocking the power of agent-driven development with rules -->

---
layout: image-right
image: /resources/images/brian-perry.jpg
---

# About Me

**Brian Perry**

- Founding Engineer at Actual AI
- Lives in Chicago suburbs
- Nintendo enthusiast
- Bluesky: @brianperry.dev
- GitHub: @backlineint

<!-- Speaker notes: Quick introduction - I'm Brian Perry, founding engineer at Actual AI, based in the Chicago area -->

---

# Claude Code: Co-Author of This Talk

- Cursor helped draft content, iterate on demos, and tighten language
- `CLAUDE.md` keeps Cursor aligned with the story arc  
- Today's deck is proof that rules + agents co-create real work

<!-- Speaker notes: This talk was actually co-created with Claude Code, demonstrating rules-driven development in action -->

---
layout: image
image: /resources/images/actual-ai.png
backgroundSize: contain
---

<!-- Speaker notes: Brief mention of Actual AI, my company -->

---

# The Problem

Everyone has experienced AI making mistakes

- Common advice: "Think of AI as a Junior Developer"
- Personal reflection: "I graduated in 2002 - thinking of me 23 years ago is horrifying" 
- What I needed: mentors, guidelines, documentation, trial and error
- **Coding agents need the same thing**

<!-- Speaker notes: The traditional advice about treating AI like a junior developer is helpful, but we need to think about what junior developers actually need to succeed -->

---
layout: image-right
image: /resources/images/junior_dev.jpg
---

# What Junior Developers Need

- **Clear guidelines and expectations**
- **Documentation and examples** 
- **Mentorship and feedback**
- **Structure and guardrails**
- **Trial and error with guidance**

The same applies to AI agents

<!-- Speaker notes: Just like I needed structure when I was starting out, AI agents need clear guidance to be effective -->

---

# Why Rules Matter

📝 **Reusable, scoped instructions that control agent behavior**

🎯 **They provide structure and guardrails**

🔄 **They enable consistent, predictable outcomes**

Rules are defined in your codebase as markdown files

**"If AI gets it wrong, don't give up - write a rule"**

<!-- Speaker notes: Rules are the key to making AI agents work effectively - they're not just configuration, they're guidance systems -->

---

# Not Talking About Drupal Rules

*This presentation focuses on AI agent rules, not the Drupal Rules module*

We're discussing markdown-based instruction files that guide AI behavior

<!-- Speaker notes: Quick clarification for anyone familiar with Drupal - this is a completely different concept -->

---

# Understanding Rules Formats

Multiple formats serve different tools and use cases:

- **Cursor** - `.cursorrules` files
- **Claude Code** - `CLAUDE.md` files  
- **GitHub Copilot** - `.github/copilot-instructions.md`
- **Agents.md** - Emerging standard format

Each has unique strengths and conventions

<!-- Speaker notes: Different tools use different formats, but the core concept is the same across all of them -->

---
layout: two-cols
---

# Cursor Rules Format

Simple, direct instructions in `.cursorrules` files

```markdown
# Code Style
- Use TypeScript for all new files
- Prefer functional components in React
- Use meaningful variable names
- Add JSDoc comments for functions

# Testing
- Write tests for all new features
- Use Jest and React Testing Library
- Aim for 80%+ code coverage
```

::right::

# Claude Code Format

Structured guidance in `CLAUDE.md`

```markdown
# Project Overview
This is a React application for...

## Important Guidelines
- Follow the existing code structure
- Use the shared component library
- Maintain accessibility standards

## File Locations
- Components: /src/components
- Utils: /src/utils
- Tests: /src/__tests__
```

<!-- Speaker notes: Here's how different tools structure their rules - notice the similarities in approach -->

---

# GitHub Copilot Format

Instructions in `.github/copilot-instructions.md`

```markdown
# Coding Standards
- Follow company style guide
- Use ESLint and Prettier configurations
- Write clear commit messages

# Security Guidelines  
- Never log sensitive information
- Validate all user inputs
- Use environment variables for secrets
```

<!-- Speaker notes: GitHub Copilot uses a centralized approach with instructions in the .github directory -->

---

# Agents.md - Emerging Standard

A proposed universal format for AI agent instructions

```markdown
# Project: My Application

## Role
You are a senior full-stack developer working on this React application

## Guidelines
- Follow existing patterns in the codebase
- Write comprehensive tests
- Maintain documentation

## Context
This application handles user authentication and data management
```

<!-- Speaker notes: Agents.md is gaining traction as a potential universal standard that could work across multiple tools -->

---

# Practical Strategies from Building This Talk

Started with minimal high-level rules:

```markdown
# Slide Presentation

Build a presentation ready slide deck, not just an outline.
Don't repeat a previous version of this presentation.
```

*With only this context, the agent will still make things up*

<!-- Speaker notes: Let me walk you through how I actually built this presentation using rules-driven development -->

---

# Adding Context Rules

Next, I guided the agent to important context:

```markdown
## Important Resources

Important resources live in the /resources directory:

- abstract.md - session description  
- outline.md - session content outline
- images directory - prioritize these images
- example-slides.md - Slidev examples
```

*This helps the agent find and use the right information*

<!-- Speaker notes: The key is progressively adding rules as you discover what the agent needs to know -->

---

# Framework-Specific Rules  

Used rules to help understand the tech stack:

```markdown
## Creating Slides

- Content belongs in slides.md in project root
- This is a Slidev project. For documentation use context7
- Never use the class: text-center
- Max 8 lines of text per slide. THIS IS VERY IMPORTANT.
```

*"use context7" tells the agent to use the context7 MCP*

<!-- Speaker notes: Notice how I included both general guidance and very specific constraints like the text limit -->

---

# MCP: Model Context Protocol

**What is MCP?**
- Protocol for connecting AI models to external data sources
- Enables agents to access real-time information  
- Context7 provides up-to-date library documentation

**Why it matters for rules:**
- Rules can reference external tools and data
- Agents get current, accurate information
- Reduces hallucination and outdated responses

<!-- Speaker notes: MCP is a key technology that makes rules more powerful by connecting agents to live data -->

---

# When You Find Yourself Correcting

**Define a rule!**

During test runs, I discovered issues and added rules:

```markdown
- Slides should only include presentation content, not speaker notes
- Text must not overflow - max 8 lines per slide  
- Sufficient contrast for dark mode presentation
- Speaker notes as HTML comments at slide end
- Use layouts to make slides compelling
- Use headings effectively
- No slide should have more than 4 clicks
```

<!-- Speaker notes: The iterative process of correcting the agent and turning those corrections into rules -->

---

# Nested Rules and Scoping

Most tools allow co-located rules files for:
- **Increased priority** in specific directories
- **Scoped rules** for subdirectories

Example from `/resources/images/CLAUDE.md`:

```markdown
# Images for Slides

- junior_dev.jpg - me as a junior developer
- brian-perry.jpg - good photo for bio slide  
- actual-ai.png - company logo (avoid two-column layout)
```

<!-- Speaker notes: This shows how you can create very specific, scoped rules for particular parts of your project -->

---

# Best Practices for Effective Rules

- **Start simple** - add complexity as needed
- **Be specific** - vague rules lead to unpredictable results  
- **Use examples** - show, don't just tell
- **Iterate based on corrections** - turn fixes into rules
- **Scope appropriately** - general vs. specific contexts
- **Reference external resources** when helpful

<!-- Speaker notes: These practices come from real experience building rules-driven workflows -->

---

# Building a Rules Library

Develop reusable rule sets for common scenarios:

- **Code style and conventions**  
- **Testing requirements**
- **Security guidelines**
- **Documentation standards**
- **Framework-specific patterns**

Share and version control your rules alongside code

<!-- Speaker notes: Think of rules as documentation that actively guides development, not just passive reference material -->

---

# Tools for Rules-Driven Workflows

**Backlog.md** - Project collaboration between humans and AI
- Complex rules behind the scenes
- Manages project state and priorities
- Git-integrated workflow

**Other emerging tools:**
- Cursor plan mode
- ADR (Architecture Decision Records) management
- Automated code review with rules

<!-- Speaker notes: There are tools being built specifically to support rules-driven development workflows -->

---
layout: iframe
url: https://github.com/backlineint/backlog.md
---

<!-- Speaker notes: Live demo of backlog.md showing rules-driven project management -->

---

# Demo: Cursor Plan Mode

*Live demonstration of using Cursor with rules to plan and implement features*

Key points:
- Rules guide the planning process
- Consistent with established patterns  
- Reduces back-and-forth corrections
- Maintains code quality standards

<!-- Speaker notes: Show how rules make the planning mode more effective by providing context and constraints -->

---

# Real-World Results

**Before rules-driven development:**
- Inconsistent code style
- Repeated corrections
- Agent confusion about context
- Wasted time on revisions

**After implementing rules:**
- Predictable, high-quality output
- Faster iteration cycles  
- Consistent patterns across codebase
- Less manual oversight needed

<!-- Speaker notes: The real benefits become clear when you compare before and after implementing a rules-driven approach -->

---

# Key Takeaways

✅ **Rules are critical** to successful agent-driven development

✅ **Start simple** and iterate based on real corrections  

✅ **Different tools** use different formats, but principles are universal

✅ **Scoped rules** provide context-appropriate guidance

✅ **Rules + agents** can co-create real, production-ready work

<!-- Speaker notes: These are the main points I want everyone to remember and apply in their own work -->

---
layout: center
---

# Questions?

**Brian Perry**
- Bluesky: @brianperry.dev  
- GitHub: @backlineint
- Company: Actual AI

*Thank you for attending!*

<!-- Speaker notes: Open for questions and discussion about rules-driven development -->