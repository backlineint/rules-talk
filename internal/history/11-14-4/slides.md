---
theme: seriph
background: https://cover.sli.dev
title: Unlocking the Power of Agent-Driven Development with Rules
info: |
  ## Unlocking the Power of Agent-Driven Development with Rules
  A practical guide to making AI coding agents truly effective through proper rules and guardrails.
transition: slide-left
mdc: true
duration: 35min
---

# Unlocking the Power of Agent-Driven Development with Rules

Making AI coding agents truly effective through proper guardrails

<div class="abs-br m-6 opacity-60">
  @brianperry
</div>

---
layout: image-right
image: /resources/images/brian-perry.jpg
---

# About Brian Perry

- Founding Engineer at Actual AI
- Lives in Chicago suburbs  
- Loves Nintendo 🎮
- Building better human-AI collaboration

<br>

**Find me online:**
- Bluesky: [brianperry.dev](https://bsky.app/profile/brianperry.dev)
- GitHub: [backlineint](https://github.com/backlineint)

---

# Claude Code: Co-Author of This Talk

- Claude helped draft content, iterate on demos, and tighten language
- `CLAUDE.md` keeps Claude aligned with the story arc  
- Today's deck is proof that rules + agents co-create real work

---
layout: image
image: /resources/images/actual-ai.png
backgroundSize: contain
---

---
layout: two-cols
---

# The Problem

Everyone has experienced AI making mistakes

Common advice: *"Think of AI as a Junior Developer"*

I graduated in 2002 - thinking of me as a developer 23 years ago is horrifying

::right::

<img src="/resources/images/junior_dev.jpg" class="rounded shadow-lg" alt="Junior developer circa 2002">

<!-- What I needed back then: mentors, guidelines, documentation, trial and error -->

---

# What Junior Developers Need

<v-clicks>

- 👥 **Mentors** - experienced guidance
- 📋 **Guidelines** - clear expectations  
- 📚 **Documentation** - accessible knowledge
- 🔄 **Trial and error** - safe learning space

</v-clicks>

<v-click>

<br>

## Coding agents need the same thing

</v-click>

---

# Rules Basics

<v-clicks>

📝 **Reusable, scoped instructions that control agent behavior**

🎯 **They provide structure and guardrails**

🔄 **They enable consistent, predictable outcomes**

</v-clicks>

<v-click>

<br>

Rules are defined in your codebase as markdown files.  
*It is a charmingly low tech solution.*

</v-click>

---

# Understanding Rules Formats

Different tools, different approaches:

<v-clicks>

- **Cursor**: `.cursorrules` → `.cursor/rules` + `Agents.md`
- **Claude Code**: `CLAUDE.md`  
- **GitHub Copilot**: `.github/copilot-instructions.md` + `*.instructions.md`
- **Agents.md**: Emerging standard (Cursor + Copilot support)

</v-clicks>

<v-click>

<br>

*I really wish everyone could just standardize on Agents.md*

</v-click>

---

# Building This Talk: Rules Evolution

Started with just high-level guidance:

```markdown
# Slide Presentation

Build a presentation ready slide deck, not just an outline.
Don't repeat a previous version of this presentation.
```

<v-click>

**Problem**: Agent will still make stuff up without context

</v-click>

---

# Leading Agents to Key Context

Added rules to guide the agent to important resources:

```markdown
## Important Resources

Important resources live in the /resources directory, including:

- abstract.md - a description of the session
- outline.md - an in-progress outline of the session content  
- images directory - images to prioritize in the presentation
```

<v-click>

**Result**: Agent now knows where to look for truth

</v-click>

---

# Framework-Specific Rules

Helped the agent understand our tooling:

```markdown
## Creating Slides

- When authoring slides, content belongs in slides.md
- The slides are a Slidev project. For documentation use context7
```

<v-click>

**Context7**: MCP (Model Context Protocol) server providing up-to-date library docs

</v-click>

---

# Rules from Corrections

When you find yourself correcting an agent, define a rule:

```markdown
- Make sure text doesn't overflow the slide. 
  At most a slide can have 8 lines of text. THIS IS VERY IMPORTANT.
- The slides should have sufficient contrast for dark mode.
- Never use the class: text-center
- Speaker notes can be included as html comments
```

<v-click>

**Pattern**: Immediate feedback → Permanent rule

</v-click>

---
layout: two-cols
---

# Nested Rules and Scoping

Most tools allow co-located rules files in specific directories

Inside `/resources/images/CLAUDE.md`:

```markdown
# Images for Slides

- junior_dev1.jpg - image of me as a junior developer
- brian-perry.jpg - good photo for the bio slide  
- actual-ai.png - company image
```

::right::

<v-clicks>

**Benefits:**
- Higher priority in that directory
- Scoped to subdirectory context
- Helps agent select the right images

</v-clicks>

---

# Tools for Rules-Driven Workflows

<v-clicks>

- **Backlog.md**: Manages project collaboration between humans and AI
- **Cursor Plan Mode**: Interactive planning with rules context
- **ADR Management**: Architecture Decision Records with AI assistance

</v-clicks>

<v-click>

*Behind the scenes: these are all complex rule systems*

</v-click>

---
layout: image-right
image: /resources/images/context_in_repository.png
---

# Tips and Tricks

**Keep context in repository**
- If the agent can't see it, it might make it up
- Save evaluation runs to codebase
- Document decisions and patterns

**The basics matter more with agents**
- Linting
- Testing  
- Documentation

---

# Getting Started

<v-clicks>

1. **Start with Cursor Directory rules** as a foundation
   - Example: [cursor.directory/rules/drupal](https://cursor.directory/rules/drupal)

2. **Define your basics first**
   - Code style preferences
   - Testing approach
   - Framework choices

3. **Add rules as you find corrections**
   - Don't try to write everything upfront
   - Let real usage guide rule creation

</v-clicks>

---

# Key Takeaways

<v-clicks>

🎯 **Rules are critical** to successful agent-driven development

📝 **Start small** and build rules from real corrections  

🔧 **Use appropriate formats** for your tools (but standardize if possible)

🤖 **Think of AI as a capable junior** who needs clear guidance

</v-clicks>

---

# "If AI gets it wrong, don't give up - write a rule"

---

# Questions?

**Brian Perry**  
@brianperry on Bluesky  
GitHub: backlineint

<br>

*This presentation was co-authored with Claude Code using rules-driven development*