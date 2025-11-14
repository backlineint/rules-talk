---
theme: seriph
background: https://cover.sli.dev
title: Unlocking the Power of Agent-Driven Development with Rules
info: |
  ## Unlocking the Power of Agent-Driven Development with Rules
  
  Learn how to make AI coding agents truly effective through rules - reusable, scoped instructions that provide structure and guardrails for consistent, predictable outcomes.

transition: slide-left
mdc: true
duration: 35min
---

# Unlocking the Power of Agent-Driven Development with Rules

From skeptic to advocate: How rules transform AI agents into effective development partners

<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer" hover:bg="white op-10">
    Let's explore how rules unlock agent potential <carbon:arrow-right class="inline"/>
  </span>
</div>

<!--
Welcome everyone. Today we're talking about something that completely changed my relationship with AI coding agents - rules. If you've struggled to see the benefits from these tools, or found yourself abandoning them, this talk is for you.
-->

---
layout: image-left
image: /resources/images/brian-perry.jpg
---

# About Me

**Brian Perry**  
Founding Engineer at Actual AI

- 🏠 Chicago suburbs
- 🎮 Nintendo enthusiast
- 🐦 @brianperry.dev on Bluesky
- 💻 @backlineint on GitHub

Previously skeptical of AI agents, now they're central to my workflow

<!--
I'm Brian Perry, a founding engineer at Actual AI. I live in the Chicago suburbs and love Nintendo games. You can find me on Bluesky and GitHub. Most importantly for today's talk - I used to be a skeptic of AI coding agents, but now they're absolutely central to my development workflow.
-->

---

# Claude Code: Co-Author of This Talk

- 🤖 Claude helped draft content, iterate on demos, and tighten language
- 📝 `CLAUDE.md` keeps Claude aligned with the story arc
- 🎯 Today's deck is proof that rules + agents co-create real work

*This presentation itself demonstrates agent-driven development in action*

<!--
In fact, Claude Code was my co-author for this presentation. Claude helped draft content, iterate on demos, and tighten the language throughout. I used CLAUDE.md to keep Claude aligned with our story arc, and this deck itself is proof that rules plus agents can co-create real work.
-->

---
layout: image-right
image: /resources/images/actual-ai.png
---

# Actual AI

Building the future of AI-powered development tools

- 🚀 Innovative AI solutions
- 👥 Expert team of engineers
- 🎯 Focused on developer productivity

*Empowering developers through intelligent automation*

<!--
And here's a bit about Actual AI - we're building the future of AI-powered development tools with a focus on empowering developers through intelligent automation.
-->

---

# The Problem: AI Makes Mistakes

<div class="grid grid-cols-2 gap-8">

<div>

## Common Advice
*"Think of AI as a Junior Developer"*

</div>

<div>

## The Reality
- Inconsistent outputs
- Ignores project conventions  
- Repeats the same mistakes
- Generates boilerplate without context

</div>

</div>

*If AI behaves like me in 2002, that's terrifying*

<!--
Everyone has experienced AI making mistakes. The common advice is to think of AI as a junior developer. But I graduated in 2002, and thinking of me as a developer 23 years ago is honestly horrifying. I needed mentors, guidelines, documentation, and lots of trial and error. Coding agents need the same thing.
-->

---
layout: image-left
image: /resources/images/junior_dev.jpg
---

# What Junior Developers Need

- 📖 **Clear documentation**
- 👨‍🏫 **Mentorship and guidance** 
- 📋 **Project conventions**
- 🎯 **Specific instructions**
- 🔄 **Feedback loops**

*Coding agents need the same structure to succeed*

<!--
What I needed as a junior developer - and what coding agents need today - is clear documentation, mentorship and guidance, understanding of project conventions, specific instructions, and good feedback loops. This is where rules come in.
-->

---

# What Are Rules?

<div class="text-2xl space-y-6">

📝 **Reusable, scoped instructions that control agent behavior**

🎯 **They provide structure and guardrails**

🔄 **They enable consistent, predictable outcomes**

</div>

<div class="pt-8">
<div class="text-lg bg-gray-100 dark:bg-gray-800 p-4 rounded">
Rules are defined in your codebase as markdown files.<br>
<em>It's a charmingly low-tech solution.</em>
</div>
</div>

<!--
So what are rules? They're reusable, scoped instructions that control agent behavior. They provide structure and guardrails, and they enable consistent, predictable outcomes. Rules are defined in your codebase as markdown files - it's a charmingly low-tech solution that works incredibly well.
-->

---

# Rules Formats Landscape

<div class="grid grid-cols-2 gap-8">

<div>

## **Cursor**
- `.cursorrules` (legacy)
- `.cursor/rules` (current)
- `Agents.md` support

## **Claude Code**
- `CLAUDE.md`
- Project instructions

</div>

<div>

## **GitHub Copilot**
- `.github/copilot-instructions.md`
- `*.instructions.md` (path-specific)

## **Emerging Standard**
- `Agents.md` (Cursor + Copilot)
- *Not yet supported by Claude*

</div>

</div>

*I really wish everyone could standardize on Agents.md*

<!--
There are several rules formats across different tools. Cursor has evolved from .cursorrules to .cursor/rules and also supports Agents.md. Claude Code uses CLAUDE.md for project instructions. GitHub Copilot uses repository-wide instructions files and path-specific instructions. Agents.md is emerging as a standard supported by Cursor and Copilot, though not yet by Claude. I really wish everyone could just standardize on Agents.md.
-->

---

# Building This Talk: Starting Simple

My initial rules were minimal:

```markdown
# Slide Presentation

Build a presentation ready slide deck, not just an outline.
Don't repeat a previous version of this presentation.
```

**Result:** The agent made stuff up and ignored context

<!--
When building this talk, I started with just a few high-level rules. With only this much context, the agent still made a bunch of stuff up and ignored important context.
-->

---

# Adding Context Direction

Next, I guided the agent to important resources:

```markdown
## Important Resources

Important resources live in the /resources directory, including:

- abstract.md - description of the session content  
- outline.md - in-progress outline of session content
- example-slides.md - examples of slides for Slidev
- images directory - images to prioritize for presentation
```

*Rules should lead agents to the most important context*

<!--
Next, I added rules to lead the agent to the most important context. I pointed it to the resources directory and explained what each file contained. This is crucial - if the agent can't see it, it probably doesn't know it and might make it up.
-->

---

# Framework-Specific Guidance

I used rules to help understand the slideshow framework:

```markdown
## Creating Slides

- When authoring slides, content belongs in slides.md
- The slides are a Slidev project. For documentation use context7
- Make use of layouts to make slides compelling
- Ensure images are contained within their slides
```

*`use context7` tells the agent to use the Context7 MCP for documentation*

<!--
I also used rules to help the agent understand the Slidev framework we were using. The "use context7" instruction tells the agent to use the Context7 MCP - that's Model Context Protocol - which provides up-to-date documentation access. This is a great example of how rules can integrate with modern AI tooling.
-->

---

# Iterative Rule Refinement

When I found issues during test runs, I wrote rules:

```markdown
- Make sure text doesn't overflow slides
- At most 8 lines of text per slide. THIS IS VERY IMPORTANT.
- Ensure sufficient contrast for dark mode presentation
- Never use the class: text-center
- Include speaker notes as HTML comments
```

**Key principle: When you find yourself correcting an agent, define a rule**

<!--
As I found issues during test runs of the presentation, I wrote more specific rules. This is a key principle: when you find yourself correcting an agent, define a rule. Rules capture that knowledge so you don't have to repeat the same corrections.
-->

---

# Nested Rules and Scoping

Most tools allow co-located rules files for specific directories:

```markdown
# Images for Slides (in /resources/images/CLAUDE.md)

- junior_dev.jpg - image of me as a junior developer
- brian-perry.jpg - good photo for the bio slide  
- actual-ai.png - image for company slide
- context_in_repository.png - example of saving context
```

*This helped the agent select the right images for slides*

<!--
Most tools allow you to co-locate rules files in specific directories to either increase their priority or scope the rules to that subdirectory. This is how I helped the agent select key images for the slides by providing context right in the images directory.
-->

---
layout: image-right
image: /resources/images/context_in_repository.png
---

# Keep Context in Repository

- 📁 **If the agent can't see it, it doesn't know it**
- 🗂️ **Save evaluation runs and past iterations**
- 📚 **Document decisions and conventions**
- 🔍 **Make implicit knowledge explicit**

*Context in the repository beats context in your head*

<!--
Here's an important tip: consider keeping additional context in your repository. If the agent can't see it, it probably doesn't know it and might make it up. I saved all my past evaluation runs to the codebase so the agent could learn from previous iterations. This image shows how I organized that context.
-->

---

# The Basics Still Matter

<div class="grid grid-cols-3 gap-8 text-center">

<div>

## 🔍 **Linting**
Automated code quality checks are even more important with agents

</div>

<div>

## ✅ **Testing** 
Agents need clear success/failure signals

</div>

<div>

## 📖 **Documentation**
Self-documenting code helps agents understand context

</div>

</div>

*The fundamentals we sometimes overlook become critical with agents*

<!--
Don't forget that the basics we sometimes overlook are even more important when working with agents. Linting provides automated quality checks, testing gives clear success and failure signals, and good documentation helps agents understand context.
-->

---

# Real-World Example: backlog.md

<div class="grid grid-cols-2 gap-8">

<div>

## The Tool
- Git-based project collaboration
- Humans + AI agents working together  
- Complex rules behind simple interface

## Behind the Scenes
- Sophisticated rule system
- Context management
- Workflow automation

</div>

<div>

## Demo Features
- Task management
- Agent collaboration
- Rule-driven workflows
- Automatic documentation

</div>

</div>

*A series of complex rules creating seamless human-AI collaboration*

<!--
Let me show you a real-world example with backlog.md - a tool for managing project collaboration between humans and AI agents in a git ecosystem. Behind the scenes, this is powered by a series of complex rules that create seamless collaboration.
-->

---

# Key Takeaways

<div class="space-y-6 text-xl">

🎯 **Rules transform unreliable agents into reliable partners**

📝 **Start simple, then iterate based on real problems**

🔄 **When AI gets it wrong, don't give up - write a rule**

🏗️ **Rules + context + tooling = powerful agent workflows**

📚 **Keep context visible and documented in your repository**

</div>

*Think of rules as mentorship for your AI junior developer*

<!--
Here are the key takeaways: Rules transform unreliable agents into reliable partners. Start simple, then iterate based on real problems you encounter. When AI gets it wrong, don't give up - write a rule. The combination of rules, context, and modern tooling creates powerful agent workflows. And always keep your context visible and documented in your repository.
-->

---
layout: center
---

# Questions & Discussion

**If AI gets it wrong, don't give up - write a rule**

<div class="pt-8 opacity-60">
Brian Perry • @brianperry.dev • Actual AI
</div>

<!--
That concludes our exploration of rules-driven development. Remember - if AI gets it wrong, don't give up, write a rule. I'd love to hear your questions and discuss your experiences with AI agents.
-->