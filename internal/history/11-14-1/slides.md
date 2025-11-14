---
theme: seriph
background: https://cover.sli.dev
title: Unlocking the Power of Agent-Driven Development with Rules
info: |
  ## Unlocking the Power of Agent-Driven Development with Rules
  Learn how rules provide structure and guardrails for AI coding agents

  By Brian Perry - Actual AI
duration: 35min
transition: slide-left
mdc: true
---

# Unlocking the Power of Agent-Driven Development with Rules

### How to make AI coding agents truly effective

Brian Perry · Actual AI

<!-- Speaker notes about the main theme of the talk -->

---
layout: image-right
image: /resources/images/brian-perry.jpg
---

# About Me

## Brian Perry
**Founding Engineer at Actual AI**

- Chicago suburbs resident
- Nintendo enthusiast
- Former skeptic turned agent advocate

**Connect with me:**
- 🦋 Bluesky: @brianperry.dev  
- 🐙 GitHub: @backlineint

<!-- Speaker notes about my background and journey with AI tools -->

---

# Claude Code: Co-Author of This Talk

- Claude Code helped draft content and iterate on demos
- `CLAUDE.md` keeps Claude aligned with the story arc  
- Today's deck is proof that rules + agents co-create real work

**This presentation was built collaboratively with AI**

<!-- Speaker notes about how this talk itself demonstrates the concepts -->

---
layout: image
image: /resources/images/actual-ai.png
backgroundSize: contain
---

<!-- Company slide - Actual AI -->

---

# The Problem

---

# Everyone Has Experienced This

## AI makes mistakes
- Generates incorrect code
- Misunderstands requirements  
- Produces inconsistent results
- Creates frustrating debugging sessions

Common advice: *"Think of AI as a Junior Developer"*

<!-- Speaker notes about universal experience with AI failures -->

---
layout: image-left
image: /resources/images/junior_dev1.jpeg
---

# Personal Reflection

## I graduated in 2002

Thinking of me 23 years ago is **horrifying**

### What I needed back then:
- Mentors and guidance
- Clear documentation  
- Established guidelines
- Trial and error opportunities

**Coding agents need the same thing**

<!-- Speaker notes about the parallel between junior developers and AI -->

---

# Why Rules Matter

---

# What Are Rules?

## 📝 **Reusable, scoped instructions that control agent behavior**

## 🎯 **They provide structure and guardrails**  

## 🔄 **They enable consistent, predictable outcomes**

Rules are defined in your codebase as markdown files

### **"If AI gets it wrong, don't give up - write a rule"**

<!-- Speaker notes about the core concept of rules -->

---

# Understanding Rules Formats

---

# Overview of Rules Formats

## Different tools, different approaches:

- **Cursor** - `.cursorrules` files
- **Claude Code** - `CLAUDE.md` files  
- **GitHub Copilot** - `.github/copilot-instructions.md`
- **Agents.md** - Emerging standard

Each format serves the same goal: **guiding agent behavior**

<!-- Speaker notes about the various formats available -->

---

# Cursor Rules Format

```markdown
# .cursorrules

You are an expert TypeScript developer.

## Code Style
- Use functional components  
- Prefer TypeScript over JavaScript
- Follow ESLint configuration

## File Structure  
- Components in /src/components
- Utilities in /src/utils
```

**Cursor reads `.cursorrules` in your project root**

<!-- Speaker notes about how Cursor implements rules -->

---

# Claude Code Rules Format

```markdown
# CLAUDE.md

# Project Instructions

## Important Guidelines
- Always run tests before committing
- Use existing patterns from the codebase
- Follow security best practices

## File Locations
- Components: /src/components
- Tests: /tests
```

**Claude Code looks for `CLAUDE.md` files throughout your project**

<!-- Speaker notes about Claude Code's approach -->

---

# GitHub Copilot Format

```markdown
# .github/copilot-instructions.md

## Coding Standards
- Follow company style guide
- Use TypeScript for all new code
- Include proper error handling

## Testing Requirements
- Write unit tests for new functions  
- Use Jest testing framework
```

**Copilot reads instructions from `.github/` directory**

<!-- Speaker notes about GitHub's implementation -->

---

# Agents.md: Emerging Standard

```markdown
# AGENTS.md

# Development Guidelines

## Code Quality
- Follow TDD approach
- Maintain 90%+ test coverage
- Use semantic commit messages

## Architecture  
- Clean Architecture principles
- Dependency injection preferred
```

**Cross-tool format gaining adoption across the ecosystem**

<!-- Speaker notes about the standardization effort -->

---

# Practical Strategies from Building This Talk

---

# Starting Simple

## I began with just high-level guidance:

```markdown
# Slide Presentation

Build a presentation ready slide deck, not just an outline.
Don't repeat a previous version of this presentation.
```

### Result: The agent made up content

**With minimal context, agents will fill gaps with assumptions**

<!-- Speaker notes about the importance of providing sufficient context -->

---

# Adding Context Pointers

## Next, I guided the agent to key resources:

```markdown
## Important Resources

Important resources live in the /resources directory:

- abstract.md - session description  
- outline.md - session content structure
- images directory - prioritized images
```

**Rules should lead agents to the most important context**

<!-- Speaker notes about directing attention to key information -->

---

# Framework-Specific Guidance

```markdown
## Creating Slides

- Content belongs in slides.md in project root
- This is a Slidev project. For documentation use context7
- example-slides.md - examples of Slidev capabilities
```

### The `use context7` instruction

Tells the agent to use the Context7 MCP server for up-to-date documentation

<!-- Speaker notes about MCP and context7 -->

---

# MCP: Model Context Protocol

## **Extends agent capabilities with real-time data**

- Context7 provides current library documentation
- Eliminates outdated information in training data  
- Enables agents to access fresh API references

```markdown
- We'll cover Agents.md, Cursor, Claude Code, 
  and Github Copilot. use context7
```

**This instruction fetched current documentation for each tool**

<!-- Speaker notes about what MCP is and why it's valuable -->

---

# Corrective Rules

## When you find yourself correcting an agent, define a rule

### Issues I discovered during test runs:

```markdown
- Make sure text doesn't overflow slides  
- At most 8 lines of text per slide. THIS IS VERY IMPORTANT
- Ensure sufficient contrast for dark mode
- Never use the class: text-center
- Include speaker notes as HTML comments
```

**Transform repeated corrections into reusable rules**

<!-- Speaker notes about the iterative improvement process -->

---

# Nested Rules and Scoping

## Most tools allow co-located rules files

### Inside `/resources/images/CLAUDE.md`:

```markdown
# Images for Slides

- junior_dev1.jpg - me as a junior developer
- brian-perry.jpg - good photo for bio slide  
- actual-ai.png - company image
```

**Scoped rules provide targeted guidance for specific contexts**

<!-- Speaker notes about how scoping increases rule effectiveness -->

---

# Best Practices for Rule Writing

## **Be Specific and Actionable**
- "Use semantic commit messages" vs "Write good commits"

## **Provide Context, Not Just Commands**  
- Explain the "why" behind rules

## **Start Small, Iterate**
- Begin with high-level guidance
- Add specificity as you discover edge cases

## **Scope Appropriately**
- Global rules for project-wide standards
- Local rules for specific functionality

<!-- Speaker notes about effective rule authoring -->

---

# Building a Rules Library

## **Document Patterns You Want Repeated**

### Code Quality Rules
- Testing requirements
- Security practices  
- Performance guidelines

### Project Structure Rules
- File organization
- Naming conventions
- Import patterns

### Team Workflow Rules  
- Git commit standards
- PR requirements
- Documentation expectations

<!-- Speaker notes about systematically building rule collections -->

---

# Key Takeaways

---

# Rules Transform Agent Effectiveness

## ✅ **Rules provide the structure agents need to succeed**

## ✅ **Different tools offer various rule formats - choose what fits**

## ✅ **Start simple, then iterate based on real corrections**  

## ✅ **Scope rules appropriately for maximum impact**

## ✅ **Build a rules library that captures your team's knowledge**

<!-- Speaker notes about the main points to remember -->

---

# Don't Give Up - Write a Rule

### When AI gets it wrong, that's not a failure
### It's an opportunity to teach it better

**Rules are how we scale human expertise through agents**

<!-- Final motivational message -->

---

# Questions?

**Brian Perry**
🦋 @brianperry.dev
🐙 @backlineint  

**Actual AI - Building the future of AI-powered development**

<!-- Contact slide for Q&A -->

---

# Thank You

### Let's unlock the power of agent-driven development together

<!-- Closing slide -->