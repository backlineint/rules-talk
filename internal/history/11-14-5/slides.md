---
theme: seriph
background: https://cover.sli.dev
title: Unlocking the Power of Agent-Driven Development with Rules
info: |
  ## Unlocking the Power of Agent-Driven Development with Rules
  The effectiveness of AI coding agents has grown exponentially in the past year. 
  Yet many developers still struggle to see benefits they expect. 
  Rules are the overlooked key to making coding agents truly effective.
class: text-white
drawings:
  persist: false
transition: slide-left
mdc: true
duration: 35min
---

# Unlocking the Power of Agent-Driven Development with Rules

<!-- 
Welcome to today's session on agent-driven development with rules. 
I'm excited to share how rules can transform your AI coding experience.
-->

---
layout: image-right
image: /resources/images/brian-perry.jpg
---

# About Me: Brian Perry

- Founding Engineer at Actual AI
- Live in Chicago suburbs
- Love Nintendo games
- **Bluesky**: https://bsky.app/profile/brianperry.dev
- **GitHub**: https://github.com/backlineint

<!-- 
I'm Brian Perry, a founding engineer at Actual AI. I live in the Chicago suburbs with my family, 
and when I'm not coding, you'll find me playing Nintendo games with my kids.
-->

---
layout: center
background: /resources/images/actual-ai.png
---

<!-- 
This is Actual AI, where we're building the future of intelligent software development.
-->

---
layout: quote
---

## Claude Code: Co-Author of This Talk

- Claude helped draft content, iterate on demos, and tighten language
- `CLAUDE.md` keeps Claude aligned with the story arc  
- Today's deck is proof that rules + agents co-create real work

<!-- 
This presentation was actually co-authored with Claude Code. Claude helped me draft content, 
iterate on demos, and refine the language. The CLAUDE.md file in this project keeps Claude 
aligned with our story arc - which is exactly what we're talking about today.
-->

---
layout: two-cols
---

# The Problem

Everyone has experienced AI making mistakes

::right::

<img src="/resources/images/junior_dev.jpg" class="w-full rounded-lg" />

<!-- 
We've all been there - asking an AI agent to help with code and getting results that miss the mark. 
The common advice is to think of AI as a junior developer, but let me tell you about my experience as an actual junior dev.
-->

---

# I Graduated in 2002

- Thinking of me as a developer 23 years ago is **horrifying**
- What I needed then:
  - **Mentors** to guide me
  - **Guidelines** to follow  
  - **Documentation** to reference
  - **Trial and error** with feedback

**Coding agents need the same thing**

<!-- 
I graduated in 2002, and thinking about me as a developer 23 years ago is honestly horrifying. 
Back then, I needed mentors, clear guidelines, good documentation, and lots of trial and error with feedback. 
Coding agents need exactly the same structure to succeed.
-->

---
layout: section
---

# Rules Basics

---

# What Are Rules?

📝 **Reusable, scoped instructions that control agent behavior**

🎯 **They provide structure and guardrails**  

🔄 **They enable consistent, predictable outcomes**

Rules are defined in your codebase as **markdown files**
*A charmingly low-tech solution*

<!-- 
Rules are reusable, scoped instructions that control how your AI agent behaves. 
They provide the structure and guardrails that enable consistent, predictable outcomes. 
The beautiful thing is they're just markdown files in your codebase - elegantly simple.
-->

---

# Not the Drupal Rules Module

We're talking about **AI agent rules**, not Drupal's Rules module

Different concept, same powerful idea:
- **Drupal Rules**: Event-driven automation for websites
- **Agent Rules**: Behavior-driven guidance for AI coding assistants

<!-- 
Just to clarify - we're not talking about the Drupal Rules module here. 
Though both concepts share the idea of using rules to control behavior, 
we're focused on guiding AI agents, not website automation.
-->

---
layout: section
---

# Understanding Rules Formats

---
layout: two-cols
---

# Cursor Rules

**Multiple format evolution:**

- `.cursorrules` (legacy)
- `.cursor/rules` (current)
- `Agents.md` (also supported)

::right::

```markdown
# Cursor Rules Example

You are an expert TypeScript developer.

## Guidelines
- Use TypeScript strict mode
- Prefer functional components
- Write comprehensive tests
- Follow existing code patterns
```

<!-- 
Cursor has evolved their rules format over time. They started with .cursorrules files, 
moved to .cursor/rules, and now also support the emerging Agents.md standard.
-->

---
layout: two-cols
---

# Claude Code Rules

**CLAUDE.md format:**

- Project-specific instructions
- Context guidance
- Tool preferences

::right::

```markdown
# Project Instructions

## Important Resources
Resources live in /resources including:
- abstract.md - session description
- outline.md - content outline

## Creating Slides
- Content belongs in slides.md
- Use Slidev layouts
- Maximum 8 lines per slide
```

<!-- 
Claude Code uses CLAUDE.md files for project-specific instructions. 
These files can guide the agent to important resources and specify preferences for tools and frameworks.
-->

---
layout: two-cols
---

# GitHub Copilot Rules

**Two main formats:**

- `.github/copilot-instructions.md` (repository-wide)
- `*.instructions.md` (path-specific)

::right::

```markdown
# Copilot Instructions

## Code Style
- Use ESLint configuration
- Follow prettier formatting
- Prefer async/await over Promises

## Testing
- Jest for unit tests
- Use descriptive test names
- Mock external dependencies
```

<!-- 
GitHub Copilot supports repository-wide instructions in .github/copilot-instructions.md 
and path-specific instructions using *.instructions.md files throughout your project.
-->

---

# Agents.md: The Emerging Standard

**Supported by:**
- ✅ Cursor  
- ✅ GitHub Copilot
- ❌ Claude Code (not yet)

**I really wish everyone could standardize on Agents.md**

```markdown
# Development Guidelines

## Framework Preferences
- React with TypeScript
- TailwindCSS for styling
- Vitest for testing

## Code Quality
- Write self-documenting code
- Use meaningful variable names
- Include error handling
```

<!-- 
Agents.md is emerging as a potential standard, supported by both Cursor and GitHub Copilot. 
Unfortunately, Claude Code doesn't support it yet, but I really hope we can all standardize on this format eventually.
-->

---
layout: section
---

# Practical Strategies from Building This Talk

---

# Starting Simple

**My initial rules:**

```markdown
# Slide Presentation

Build a presentation ready slide deck, not just an outline.
Don't repeat a previous version of this presentation.
```

**Problem:** With only this context, the agent will still make stuff up

<!-- 
I started with just these simple, high-level rules for building this presentation. 
But I quickly learned that with only this much context, the agent still tends to make things up rather than working with real information.
-->

---

# Adding Context Guidance

**Next, I guided the agent to important resources:**

```markdown
## Important Resources

Important resources live in the /resources directory, including:

- abstract.md - a description of the session
- outline.md - an in-progress outline of the session content  
- images directory - images to prioritize in the presentation
```

**This tells the agent WHERE to look for information**

<!-- 
The next step was adding rules that guide the agent to the most important context. 
This tells the agent exactly where to look for information rather than inventing it.
-->

---

# Framework-Specific Guidance

**Helping the agent understand the tech stack:**

```markdown
## Creating Slides

- The slides are a Slidev project. For documentation use context7
- When authoring slides, content belongs in slides.md
- example-slides.md shows examples of slides that can be created
```

**The `use context7` directive tells the agent to use the Context7 MCP**

<!-- 
I also added rules to help the agent understand the specific framework we're using. 
The 'use context7' directive tells Claude to use the Context7 MCP server to get up-to-date Slidev documentation.
-->

---

# MCP: Model Context Protocol

**What is MCP?**
- Protocol for connecting AI models to external data sources
- Enables real-time access to APIs, databases, tools

**Context7 MCP:**
- Provides up-to-date library documentation
- Eliminates stale knowledge cutoff issues
- Gives agents current, accurate information

<!-- 
MCP stands for Model Context Protocol - it's a way to connect AI models to external data sources. 
Context7 is an MCP server that provides up-to-date library documentation, 
eliminating issues with stale knowledge from training data cutoffs.
-->

---

# When AI Gets It Wrong, Write a Rule

**I discovered issues during test runs and added rules:**

```markdown
- Make sure text doesn't overflow the slide
- At most a slide can have 8 lines of text. THIS IS VERY IMPORTANT
- Slides should have sufficient contrast for dark mode
- Never use the class: text-center
- Speaker notes can be included as html comments
- Use headings to make slides more compelling
- Use layouts: https://sli.dev/builtin/layouts
```

<!-- 
As I tested the presentation and found issues, I wrote rules to prevent them from happening again. 
This iterative approach of correcting the agent by defining rules is key to success.
-->

---

# Nested Rules and Scoping

**Most tools allow co-located rules files for:**
- **Increased priority** in specific directories
- **Scoped rules** for subdirectories

**Example: Image selection guidance**
Inside `/resources/images/CLAUDE.md`:

```markdown
# Images for Slides

- junior_dev1.jpg - image of me as a junior developer
- brian-perry.jpg - good photo for the bio slide  
- actual-ai.png - company slide image
```

<!-- 
Most tools support nested rules by placing rule files in specific directories. 
This lets you scope rules to particular areas of your codebase or increase their priority. 
I used this to help the agent select the right images for slides.
-->

---
layout: section
---

# Tips and Tricks

---

# Keep Context in Repository

**If the agent can't see it, it probably doesn't know it**

- Save evaluation runs to the codebase
- Include relevant documentation  
- Store example outputs
- Keep decision records

<img src="/resources/images/context_in_repository.png" class="w-full mt-4 rounded-lg" />

<!-- 
A crucial tip: if the agent can't see information in your repository, it probably doesn't know about it and might make something up. 
I saved all my evaluation runs to the codebase so the agent could learn from previous iterations.
-->

---

# The Basics Matter Even More

**With agents, fundamental practices become crucial:**

- **Linting** - Ensure code quality standards
- **Testing** - Verify agent-generated code works
- **Documentation** - Help agents understand context
- **Code Reviews** - Catch what agents might miss

**Agents amplify both good and bad practices**

<!-- 
When working with agents, the basics of software development become even more important. 
Good practices like linting, testing, and documentation help agents succeed, 
while bad practices get amplified and can cause bigger problems.
-->

---

# Community Resources

**Cursor Directory Drupal Rules:**  
https://cursor.directory/rules/drupal

- Community-contributed rule sets
- Great starting points for specific frameworks
- Learn from others' experiences
- Contribute back to the community

<!-- 
Don't start from scratch! The Cursor Directory has community-contributed rule sets for different frameworks. 
The Drupal rules there could be a great starting point if you're working with Drupal projects.
-->

---
layout: section
---

# Demo: Tools for Rules-Driven Workflows

---
layout: center
---

# Backlog.md Demo

**A tool for managing project collaboration between humans and AI Agents in a git ecosystem**

*Behind the scenes, this is a series of complex rules*

<!-- 
Now let's look at backlog.md - a tool I've been working on for managing project collaboration between humans and AI agents. 
Under the hood, it's essentially a sophisticated rules engine that helps coordinate work between people and AI.
-->

---
layout: center
---

# Cursor Plan Mode Demo

**See rules in action with Cursor's planning feature**

<!-- 
Let's also look at Cursor's plan mode, where you can see rules being applied in real-time as the agent plans out complex tasks.
-->

---
layout: center
---

# Actual AI ADR Management Demo

**Architecture Decision Records managed with agent assistance**

<!-- 
Finally, I'll show how we use agent-driven development with rules to manage Architecture Decision Records at Actual AI.
-->

---
layout: section
---

# Key Takeaways

---

# Remember These Points

📝 **Rules provide structure that allows agents to succeed**

🎯 **Start simple, then add context and framework guidance**  

🔄 **When AI gets it wrong, don't give up - write a rule**

⚡ **Use community resources and contribute back**

🛠️ **The basics of good development practices matter even more**

<!-- 
Let's wrap up with the key takeaways from today's session. 
Rules provide the structure that allows agents to succeed. 
Start simple, add guidance iteratively, and remember that when AI gets something wrong, 
the answer isn't to give up - it's to write a better rule.
-->

---
layout: center
class: text-center
---

# Questions?

**"If AI gets it wrong, don't give up - write a rule"**

Thank you!

<!-- 
That's a wrap! I'll leave you with this thought: when AI gets it wrong, don't give up - write a rule. 
Thank you for your attention, and I'm happy to take any questions you might have.
-->