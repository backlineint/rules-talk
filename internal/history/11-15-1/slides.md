---
theme: seriph
background: https://cover.sli.dev
title: Unlocking the Power of Agent-Driven Development with Rules
info: |
  ## Unlocking the Power of Agent-Driven Development with Rules
  
  The effectiveness of AI coding agents has grown exponentially in the past year. Yet many developers still struggle to see the benefits they expect. This session explores one of the overlooked keys to making coding agents truly effective: rules.

drawings:
  persist: false
transition: slide-left
mdc: true
duration: 45min
colorSchema: dark
---

# Unlocking the Power of Agent-Driven Development with Rules

Building effective AI workflows through structured guidance

<!-- 
Welcome everyone! Today we're going to explore one of the most overlooked aspects of working with AI coding agents - rules. Rules are the key to unlocking the real potential of these tools.
-->

---
layout: image-right
image: /resources/images/brian-perry.jpg
---

# About Me

**Brian Perry**
- Founding Engineer at Actual AI
- Chicago suburbs resident
- Nintendo enthusiast
- Converted AI skeptic → Daily user

**Find me:**
- Bluesky: @brianperry.dev
- GitHub: @backlineint

<!-- 
I'm Brian Perry, and I'll be your guide today. I'm a founding engineer at Actual AI, where we're building tools for developer productivity. I live in the Chicago suburbs and I'm a big Nintendo fan. But most importantly for today's talk - I used to be an AI skeptic who's now completely converted to using these tools daily.
-->

---
layout: center
---

## Claude Code: Co-Author of This Talk

- Claude helped draft content, iterate on demos, and tighten language
- `CLAUDE.md` keeps Claude aligned with the story arc  
- Today's deck is proof that rules + agents co-create real work

<!-- 
Before we dive in, I want to acknowledge my co-author. Claude Code helped me draft this content, iterate on the demos you'll see, and tighten the language throughout. The CLAUDE.md file in my repository keeps Claude aligned with my story arc. This deck itself is proof that rules plus agents can co-create real work.
-->

---
layout: image
image: /resources/images/actual-ai.png
backgroundSize: contain
---

<!-- 
This is Actual AI - the company where I work. We're focused on building tools that help developers be more productive with AI agents.
-->

---
layout: center
---

# The Problem

Everyone has experienced AI making mistakes

<!-- 
Let's start with the problem we're all familiar with. Everyone in this room has experienced AI making mistakes. Whether it's hallucinating APIs that don't exist, suggesting deprecated patterns, or just completely missing the context of what you're trying to build.
-->

---

## Common Advice: "Think of AI as a Junior Developer"

<v-click>

### Thinking of me as a developer 23 years ago is horrifying

</v-click>

<v-click>

What I needed back then:
- 📚 Mentors and guidelines
- 📖 Documentation and context
- 🔄 Trial and error with feedback
- 🎯 Clear expectations and boundaries

</v-click>

<!-- 
The common advice we hear is "think of AI as a junior developer." Well, I graduated in 2002 - thinking of me as a developer 23 years ago is absolutely horrifying! What did I need back then? I needed mentors, guidelines, documentation, trial and error with feedback, and most importantly - clear expectations and boundaries.
-->

---
layout: center
---

# Coding agents need the same thing

Rules provide structure and guardrails for consistent, predictable outcomes

<!-- 
Coding agents need exactly the same thing. Rules provide that structure and those guardrails that enable consistent, predictable outcomes.
-->

---

# What Are Rules?

<v-click>

📝 **Reusable, scoped instructions that control agent behavior**

</v-click>

<v-click>

🎯 **They provide structure and guardrails**

</v-click>

<v-click>

🔄 **They enable consistent, predictable outcomes**

</v-click>

<v-click>

Rules are defined in your codebase as markdown files - a charmingly low-tech solution.

</v-click>

<!-- 
So what exactly are rules? They're reusable, scoped instructions that control how your agent behaves. They provide structure and guardrails. They enable consistent, predictable outcomes. And here's the beautiful part - rules are defined right in your codebase as markdown files. It's a charmingly low-tech solution to a high-tech problem.
-->

---

# Understanding Rules Formats

Different tools, different approaches

<v-click>

## Cursor Rules
- Started with `.cursorrules`  
- Now uses `.cursor/rules`
- Also supports `Agents.md`

</v-click>

<v-click>

## Claude Code Rules  
- `CLAUDE.md` in repository root
- Project-specific instructions

</v-click>

<!-- 
Now let's look at the different formats. Cursor has evolved - it started with .cursorrules files, now uses .cursor/rules, and also supports Agents.md. Claude Code uses CLAUDE.md in your repository root for project-specific instructions.
-->

---

# Understanding Rules Formats (cont.)

<v-click>

## GitHub Copilot Rules
- Repository-wide: `.github/copilot-instructions.md`
- Path-specific: `*.instructions.md`

</v-click>

<v-click>

## Agents.md - Emerging Standard
- Supported by Cursor and Copilot  
- Not yet supported by Claude
- The format I wish everyone would standardize on

</v-click>

<!-- 
GitHub Copilot supports repository-wide instructions in .github/copilot-instructions.md and path-specific instructions in .instructions.md files. Agents.md is emerging as a potential standard - it's supported by Cursor and Copilot, though not yet Claude. It's honestly the format I wish everyone would just standardize on.
-->

---
layout: center
---

# Practical Strategies from Building This Talk

Let me show you my actual rules evolution

<!-- 
Now let me show you some practical strategies by walking through how I actually built this talk using rules.
-->

---

## Started Simple

```markdown
# Slide Presentation

Build a presentation ready slide deck, not just an outline.
Don't repeat a previous version of this presentation.
```

<v-click>

**Result:** The agent still makes stuff up with only this context

</v-click>

<!-- 
I started simple with just these basic rules. But with only this much context, the agent will still just make a bunch of stuff up.
-->

---

## Added Context Guidance

```markdown
## Important Resources

Important resources live in the /resources directory, including:

- abstract.md - description of the session content
- outline.md - in-progress outline of session content  
- images directory - images to prioritize including
```

<v-click>

**Result:** Now the agent knows where to find the important context

</v-click>

<!-- 
So I added rules to lead the agent to the most important context. Now the agent knows exactly where to find the information it needs.
-->

---

## Framework-Specific Rules

```markdown
## Creating Slides

- When authoring slides, content belongs in slides.md
- The slides are a Slidev project. For documentation use context7
- example-slides.md - examples of slides that can be created
```

<v-click>

**What is context7?** An MCP (Model Context Protocol) server that provides up-to-date documentation for libraries and frameworks

</v-click>

<!-- 
I also used rules to help the agent understand the slide framework. The "use context7" instruction tells the agent to use the context7 MCP server - that's Model Context Protocol - which provides up-to-date documentation for libraries and frameworks.
-->

---

## Iterative Rule Development

```markdown
- Make sure text doesn't overflow. At most 8 lines per slide
- Ensure sufficient contrast for dark mode presentation
- Never use the class: text-center  
- Speaker notes as HTML comments at slide end
- Use layouts to make slides more compelling
- No slide should have more than 4 clicks
```

<v-click>

**Key insight:** When you find yourself correcting an agent, define a rule

</v-click>

<!-- 
As I tested the slides, I found issues and turned those corrections into rules. Here's the key insight: when you find yourself correcting an agent repeatedly, define a rule for it.
-->

---
layout: image-right
image: /resources/images/context_in_repository.png
---

## Nested Rules and Scoping

Most tools allow co-located rules files for:
- Increased priority
- Directory-specific scope

Example in `/resources/images/CLAUDE.md`:

```markdown
# Images for Slides

- junior_dev.jpg - image of me as junior dev
- brian-perry.jpg - good photo for bio slide  
- actual-ai.png - company slide image
```

<!-- 
Tools also support nested rules and scoping. Most allow you to place rules files in specific directories to either increase their priority or scope them to that subdirectory. This is how I helped the agent select the right images for slides.
-->

---

# Miscellaneous Tips and Tricks

<v-click>

## Keep Context in Repository
- If the agent can't see it, it might make it up
- I saved all past runs to the codebase for evaluation

</v-click>

<v-click>

## The Basics Matter Even More  
- Linting becomes crucial
- Testing provides safety nets
- Documentation guides behavior

</v-click>

<v-click>

## Cursor Directory Rules
- Community-curated rules: cursor.directory/rules
- Great starting points for frameworks like Drupal

</v-click>

<!-- 
Here are some additional tips. Keep context in your repository - if the agent can't see it, it might make it up. The basics we sometimes overlook become even more important - linting, testing, and documentation. And check out Cursor Directory for community-curated rules that can be great starting points.
-->

---
layout: center
---

# Demo Time

Let's see rules-driven workflows in action

<!-- 
Now let's see some of this in action with a few demos.
-->

---
layout: center
---

## Demo: Cursor Plan Mode

Planning complex implementations with AI assistance

<!-- 
First, let me show you Cursor's plan mode, which helps you plan complex implementations with AI assistance.
-->

---
layout: center  
---

## Demo: Backlog.md

A tool for managing project collaboration between humans and AI agents

**Behind the scenes:** This is a series of complex rules working together

<!-- 
Next, I'll demo backlog.md - a tool for managing project collaboration between humans and AI agents. What you'll see is actually a series of complex rules working together behind the scenes.
-->

---
layout: center
---

## Demo: Actual AI ADR Management

Architecture Decision Record management with AI assistance

<!-- 
Finally, I'll show you our ADR management demo at Actual AI, where we use AI to help manage Architecture Decision Records.
-->

---
layout: image-left
image: /resources/images/junior_dev.jpg
---

# Key Takeaways

<v-click>

## Rules transform agents from unpredictable to reliable

</v-click>

<v-click>

## Start simple, iterate based on corrections

</v-click>

<v-click>

## Keep important context in your repository

</v-click>

<v-click>

## **"If AI gets it wrong, don't give up - write a rule"**

</v-click>

<!-- 
Here are the key takeaways. Rules transform agents from unpredictable tools to reliable partners. Start simple and iterate based on the corrections you find yourself making. Keep important context in your repository. And remember: if AI gets it wrong, don't give up - write a rule.
-->

---
layout: center
---

# Questions?

**Thank you!**

Bluesky: @brianperry.dev  
GitHub: @backlineint

<!-- 
That's all I have for you today. I'd love to take any questions you might have. Thank you so much for your attention!
-->