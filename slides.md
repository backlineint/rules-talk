---
theme: seriph
title: Unlocking the Power of Agent-Driven Development with Rules
info: |
  ## Unlocking the Power of Agent-Driven Development with Rules
  
  The effectiveness of AI coding agents has grown exponentially in the past year. Yet many developers and teams still find themselves struggling to see the benefits they expect, or abandoning these tools altogether.

  In this session, we'll explore one of the overlooked keys to making coding agents truly effective: rules.
class: text-center
drawings:
  persist: false
transition: slide-left
mdc: true
duration: 45min
---

# Unlocking the Power of Agent-Driven Development with Rules

A 45-minute journey into making AI agents work for you

<!-- This is the title slide -->

---
layout: image-right
image: /resources/images/brian-perry.jpg
---

# About Me: Brian Perry

🚀 **Founding Engineer at Actual AI**

🏠 **Chicago suburbs resident**

🎮 **Nintendo enthusiast**

🌐 **Find me online:**
- Bluesky: [brianperry.dev](https://bsky.app/profile/brianperry.dev)
- GitHub: [backlineint](https://github.com/backlineint)

<!-- I graduated in 2002, so I've been around the block -->

---
layout: quote
---

## Claude Code: Co-Author of This Talk

🤝 **Claude helped draft content, iterate on demos, and tighten language**

📝 **`CLAUDE.md` keeps Claude aligned with the story arc**

🎯 **Today's deck is proof that rules + agents co-create real work**

<!-- This presentation was built using the very principles we'll discuss -->

---
layout: center
---

![Actual AI](/resources/images/actual-ai.png)

<!-- Actual AI company slide -->

---
layout: two-cols
---

# The Problem We All Face

**Everyone has experienced AI making mistakes**

Common advice: *"Think of AI as a Junior Developer"*

::right::

<div v-click>

![Junior Developer](/resources/images/junior_dev.jpg)

*Me in 2002 - thinking of me as a developer 23 years ago is horrifying*

</div>

<!-- What did I need back then? Mentors, guidelines, documentation, trial and error -->

---

# What Junior Developers Need

🧑‍🏫 **Mentors and guidance**

📚 **Clear documentation**

🛡️ **Guardrails and structure**

🔄 **Trial and error with feedback**

<div v-click class="mt-8">

## Coding agents need the same thing

</div>

---
layout: center
---

# Enter: Rules

📝 **Reusable, scoped instructions that control agent behavior**

🎯 **They provide structure and guardrails**

🔄 **They enable consistent, predictable outcomes**

---

# What Are Rules?

Rules are defined in your codebase as **markdown files**

*It is a charmingly low tech solution*

<div v-click class="mt-8">

**Note:** We're not talking about the Drupal Rules module here

</div>

---
layout: two-cols
---

# How to Define Effective Rules

**Be specific and actionable**

**Provide context and examples**

**Focus on common failure patterns**

**Make them discoverable**

::right::

<div v-click>

**Best Practices:**
- Start simple, iterate
- Use clear, direct language
- Test with real scenarios
- Version control everything

</div>

---

# Understanding Rules Formats

Different tools, different approaches...

<div class="grid grid-cols-2 gap-4 mt-8">

<div v-click>

**Cursor Rules**
- `.cursorrules` (legacy)
- `.cursor/rules` (current)
- Also supports `Agents.md`

</div>

<div v-click>

**Claude Code**
- `CLAUDE.md` format
- Project-specific instructions
- Context-aware rules

</div>

</div>

---

# Rules Formats (continued)

<div class="grid grid-cols-2 gap-4">

<div v-click>

**GitHub Copilot**
- `.github/copilot-instructions.md`
- `*.instructions.md` (path-specific)
- Repository-wide rules

</div>

<div v-click>

**Agents.md Standard**
- Emerging cross-tool standard
- Supported by Cursor and Copilot
- *I really wish everyone could standardize on this*

</div>

</div>

---
layout: quote
---

# Practical Strategies from Building This Talk

*Real examples from creating this presentation*

---

# Starting Simple

I started with just a few high-level rules:

```markdown
# Slide Presentation

Build a presentation ready slide deck, not just an outline.
Don't repeat a previous version of this presentation.
```

<div v-click class="mt-8">

**With only this context, the agent will still make stuff up**

</div>

---

# Adding Important Context

Next, I added rules to lead the agent to key resources:

```markdown
## Important Resources

Important resources live in the /resources directory:

- abstract.md - session description
- outline.md - content outline  
- images directory - prioritize these images
- example-slides.md - Slidev examples
```

<div v-click class="mt-6">

**Guide the agent to the information it needs**

</div>

---

# Framework-Specific Rules

Help the agent understand your tools:

```markdown
## Creating Slides

- When authoring slides, content belongs in slides.md
- The slides are a Slidev project. For documentation use context7
```

<div v-click class="mt-8">

**`use context7` tells the agent to use the context7 MCP**

*MCP = Model Context Protocol - extends agent capabilities*

</div>

---

# Rules Born from Corrections

When you find yourself correcting an agent, **define a rule**

Examples from building these slides:

```markdown
- Make sure text doesn't overflow. At most 8 lines of text
- Slides should have sufficient contrast for dark mode
- Never use the class: text-center on list slides
- Use headings to make slides more compelling
- No slide should have more than 4 clicks
```

<div v-click class="mt-6">

**Each rule solved a recurring problem**

</div>

---
layout: image-right
image: /resources/images/context_in_repository.png
---

# Nested Rules and Scoping

Most tools allow **co-located rules** for:
- Increased priority
- Directory-specific scope

Example: Inside `/resources/images/CLAUDE.md`

```markdown
# Images for Slides

- junior_dev.jpg - me as junior developer
- brian-perry.jpg - bio slide photo
- actual-ai.png - company slide image
```

---

# Miscellaneous Tips and Tricks

**Keep additional context in repository**
- If the agent can't see it, it might make it up
- I saved all past runs for evaluation process

**The basics matter even more with agents:**
- Linting and testing
- Clear documentation
- Consistent patterns

**Use community resources:**
- [Cursor Directory](https://cursor.directory/rules/drupal) for starting points

---

# Demo: Tools for Rules-Driven Workflows

🔧 **Backlog.md**
- Tool for managing human-AI collaboration in git
- Complex rules behind the scenes

🎯 **Cursor Plan Mode**
- Structured approach to complex changes

📋 **Actual AI ADR Management**
- Architecture Decision Records with AI assistance

---
layout: center
---

# Key Takeaways

---

# Remember These Points

✅ **Rules are the key to effective agent-driven development**

✅ **Start simple, iterate based on real problems**

✅ **Different tools have different formats - know your options**

✅ **Co-locate rules for better scoping and priority**

✅ **Treat agents like junior developers who need guidance**

---
layout: quote
---

# "If AI gets it wrong, don't give up - write a rule"

---
layout: center
---

# Questions & Answers

**Thank you!**

🌐 **Bluesky:** [brianperry.dev](https://bsky.app/profile/brianperry.dev)  
💻 **GitHub:** [backlineint](https://github.com/backlineint)

<!-- End of presentation -->