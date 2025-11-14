---
theme: seriph
background: https://cover.sli.dev
title: Unlocking the Power of Agent-Driven Development with Rules
info: |
  ## Unlocking the Power of Agent-Driven Development with Rules
  A 45-minute exploration of how rules transform AI coding agents from unpredictable tools into reliable development partners.
transition: slide-left
mdc: true
duration: 45min
---

# Unlocking the Power of Agent-Driven Development with Rules

A 45-minute exploration of how rules transform AI coding agents from unpredictable tools into reliable development partners

<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer" hover:bg="white op-10">
    Press Space for next page <carbon:arrow-right class="inline"/>
  </span>
</div>

<div class="abs-br m-6 flex gap-2">
  <a href="https://bsky.app/profile/brianperry.dev" target="_blank" alt="Bluesky"
    class="text-xl slidev-icon-btn opacity-50 !border-none !hover:text-white">
    <carbon-logo-twitter />
  </a>
  <a href="https://github.com/backlineint" target="_blank" alt="GitHub"
    class="text-xl slidev-icon-btn opacity-50 !border-none !hover:text-white">
    <carbon-logo-github />
  </a>
</div>

<!--
Welcome to this talk on unlocking the power of agent-driven development with rules. Today we'll explore how to transform AI coding agents from unpredictable tools into reliable development partners through the strategic use of rules.
-->

---
layout: image-right
image: /resources/images/brian-perry.jpg
---

# About Brian Perry

- **Founding Engineer** at Actual AI
- Lives in Chicago suburbs 
- Nintendo enthusiast
- **Bluesky**: [@brianperry.dev](https://bsky.app/profile/brianperry.dev)
- **GitHub**: [@backlineint](https://github.com/backlineint)

Once a skeptic, now relies on agent-driven development as a cornerstone of daily workflow

<!--
I'm Brian Perry, a founding engineer at Actual AI. I live in the Chicago suburbs and I'm a big Nintendo fan. I was once very skeptical of AI coding assistants, but they've become an essential part of my daily development workflow. You can find me on Bluesky and GitHub at the handles shown here.
-->

---

# Claude Code: Co-Author of This Talk

- **Claude helped** draft content, iterate on demos, and tighten language
- **CLAUDE.md** keeps Claude aligned with the story arc  
- **Today's deck** is proof that rules + agents co-create real work

<!--
Speaking of AI assistants, Claude Code actually co-authored this presentation. Claude helped draft content, iterate on demos, and refine the language throughout. We used a CLAUDE.md file to keep Claude aligned with our story arc, and this very presentation is living proof that rules and agents can co-create meaningful work together.
-->

---
layout: image-right
image: /resources/images/actual-ai.png
---

# Actual AI

Building the future of intelligent software development

**Our Mission**: Empower developers with AI-driven tools that enhance creativity and productivity

<!--
I work at Actual AI, where we're building the future of intelligent software development. Our mission is to empower developers with AI-driven tools that enhance both creativity and productivity.
-->

---
layout: cover
---

# The Problem

Everyone has experienced AI making mistakes

<!--
Let's start with the problem we're all familiar with - everyone who has used AI coding assistants has experienced them making mistakes, producing unexpected results, or simply not understanding what we actually wanted.
-->

---

# Common Advice: "Think of AI as a Junior Developer"

<v-click>

**I graduated in 2002**  
Thinking of me as a developer 23 years ago is **horrifying**

</v-click>

<v-click>

## What I needed back then:
- 👥 **Mentors** to guide my decisions
- 📋 **Guidelines** for consistent code quality  
- 📚 **Documentation** to understand patterns
- 🔄 **Trial and error** with feedback loops

</v-click>

<v-click>

**Coding agents need the same thing**

</v-click>

<!--
The common advice is to "think of AI as a junior developer." I graduated in 2002, and thinking of myself as a developer 23 years ago is honestly horrifying. Back then, I needed mentors to guide my decisions, clear guidelines for maintaining code quality, documentation to understand existing patterns, and lots of trial and error with good feedback loops. Coding agents need exactly the same support structure.
-->

---

# What Are Rules?

<div class="space-y-6">

📝 **Reusable, scoped instructions** that control agent behavior

🎯 **Provide structure and guardrails** for consistent outcomes

🔄 **Enable predictable, reliable results** across projects

</div>

<!--
So what are rules exactly? Rules are reusable, scoped instructions that control how AI agents behave. They provide structure and guardrails that help ensure consistent outcomes, and they enable predictable, reliable results across different projects and contexts.
-->

---

# Rules: A Charmingly Low-Tech Solution

Rules are defined in your codebase as **markdown files**

<v-click>

```markdown
# Project Guidelines

## Code Style
- Use TypeScript for all new files
- Follow existing naming conventions
- Add JSDoc comments to public functions

## Testing
- Write unit tests for all business logic
- Use descriptive test names
- Mock external dependencies
```

</v-click>

<v-click>

*Note: We're not talking about the Drupal Rules module here*

</v-click>

<!--
Rules use a charmingly low-tech solution - they're simply markdown files in your codebase. Here's a simple example of what rules might look like. They're human-readable instructions that agents can understand and follow. And just to be clear, we're definitely not talking about the Drupal Rules module here!
-->

---

# How to Define Effective Rules

<div class="grid grid-cols-2 gap-8">

<div>

## ✅ **Good Rules**
- Specific and actionable
- Include examples
- Explain the "why"
- Scoped to context
- Test-driven

</div>

<div>

## ❌ **Poor Rules**  
- Vague or ambiguous
- No concrete examples
- Missing context
- Overly broad
- Never updated

</div>

</div>

<!--
To write effective rules, focus on being specific and actionable. Include concrete examples and explain the reasoning behind each rule. Scope rules to their appropriate context and treat them like test-driven development. Avoid vague or ambiguous language, always provide examples, don't leave out important context, avoid rules that are too broad, and make sure to keep them updated.
-->

---

# Best Practices for Rule Writing

## 🎯 **Start Small, Iterate Often**
Begin with core patterns, expand based on real issues

## 📁 **Use Scoped Rules**  
Directory-specific rules override global ones

## 🔄 **Update When Correcting**
If you find yourself correcting an agent, write a rule

## 📖 **Document the "Why"**
Include reasoning to help agents understand context

<!--
Here are key best practices: Start small and iterate often - begin with your core patterns and expand based on real issues you encounter. Use scoped rules where directory-specific rules can override global ones. Most importantly, update your rules when you find yourself correcting an agent - that's a perfect signal that you need a new rule. And always document the "why" behind your rules to help agents understand the context and reasoning.
-->

---
layout: section
---

# Understanding Rules Formats

Different tools, different approaches

<!--
Now let's dive into the various rules formats used by different AI coding tools. Each tool has evolved its own approach to handling rules and instructions.
-->

---

# Cursor Rules Evolution

<div class="space-y-4">

## **Historical Formats**
- `.cursorrules` (original format)
- Now: `.cursor/rules` directory structure

## **Current Documentation**
See: [cursor.com/docs/context/rules](https://cursor.com/docs/context/rules)

## **Also Supports**
`Agents.md` format for compatibility

</div>

<!--
Cursor has had quite an evolution in its rules formats. It started with .cursorrules files, then moved to a .cursor/rules directory structure. You can find the current documentation at cursor.com/docs/context/rules. Cursor also supports the Agents.md format for broader compatibility.
-->

---

# Claude Code Rules Format

<div class="space-y-4">

## **Primary File**
`CLAUDE.md` - Project-wide instructions

## **Key Features**
- Markdown-based format
- Supports context references
- Integration with MCP (Model Context Protocol)
- Can reference external documentation via `context7`

</div>

<v-click>

```markdown
# Project Guidelines

## Important Resources
- Use context7 to look up framework documentation
- Reference existing patterns in /examples directory
```

</v-click>

<!--
Claude Code uses CLAUDE.md as its primary rules file for project-wide instructions. It's markdown-based and supports context references. One powerful feature is its integration with MCP - Model Context Protocol - which allows it to reference external documentation through tools like context7. This means rules can direct Claude to look up current documentation for frameworks and libraries.
-->

---

# GitHub Copilot Rules Format

<div class="space-y-4">

## **Repository-wide Instructions**
`.github/copilot-instructions.md`

## **Path-specific Instructions**  
`*.instructions.md` files in relevant directories

## **Scoping**
Instructions can be scoped to specific directories or file types

</div>

<v-click>

```markdown
<!-- .github/copilot-instructions.md -->
# Global Copilot Instructions

Use TypeScript for all new files.
Follow the existing code style patterns.

<!-- src/components/*.instructions.md -->
# Component Guidelines

All React components must include PropTypes.
Use functional components with hooks.
```

</v-click>

<!--
GitHub Copilot uses .github/copilot-instructions.md for repository-wide instructions, and supports path-specific instructions through .instructions.md files in relevant directories. This allows for nice scoping where you can have different rules for different parts of your codebase.
-->

---

# Agents.md: An Emerging Standard

<div class="space-y-4">

## **Broad Support**
- ✅ Cursor  
- ✅ GitHub Copilot
- ❌ Claude Code (not yet supported)

## **Standardization Benefits**
- Single file format across tools
- Community-driven conventions
- Easier tool migration

</div>

<v-click>

**I really wish everyone could just standardize on Agents.md**

</v-click>

<!--
Agents.md is emerging as a potential standard format. It's supported by both Cursor and GitHub Copilot, though not yet by Claude Code. The benefits of standardization are clear - having a single file format across tools, community-driven conventions, and much easier migration between tools. I really do wish everyone would just standardize on Agents.md to make our lives simpler.
-->

---

# Comparison and Use Cases

| Tool | Format | Strengths | Best For |
|------|--------|-----------|----------|
| **Cursor** | `.cursor/rules` | Rich IDE integration | Active development |
| **Claude Code** | `CLAUDE.md` | Context protocol integration | Research & planning |
| **Copilot** | `.instructions.md` | Path-based scoping | Large codebases |
| **Agents.md** | Universal | Cross-tool compatibility | Team standardization |

<!--
Here's a quick comparison of the different formats and their strengths. Cursor's format offers rich IDE integration and is great for active development. Claude Code's CLAUDE.md format excels at context protocol integration, making it ideal for research and planning phases. Copilot's instructions.md format provides excellent path-based scoping for large codebases. And Agents.md offers the promise of cross-tool compatibility, making it ideal for team standardization.
-->

---
layout: section
---

# Practical Strategies from Building This Talk

Real-world rule evolution in action

<!--
Now let me share some practical strategies by walking through how I actually built this presentation using rules. This is a real-world example of rule evolution in action.
-->

---

# Starting with High-Level Rules

## **My First Attempt**

```markdown
# Slide Presentation

Build a presentation ready slide deck, not just an outline.
Don't repeat a previous version of this presentation.
```

<v-click>

**Problem**: With only this context, the agent still just makes stuff up

</v-click>

<!--
I started with just these high-level rules - build a presentation-ready slide deck and don't repeat previous versions. But with only this much context, the agent would still just make things up and create generic content that didn't match what I actually wanted.
-->

---

# Adding Context Direction

## **Next Iteration**

```markdown
## Important Resources

Important resources live in the /resources directory, including:

- abstract.md - a description of the session
- outline.md - an in-progress outline of session content  
- images directory - images to prioritize in the presentation
```

<v-click>

**Result**: Agent now knows where to look for the real context

</v-click>

<!--
So I added rules to direct the agent to the most important context. I pointed it to the resources directory with descriptions of what each file contains - the abstract, outline, and images. This gave the agent a roadmap for finding the actual content rather than making things up.
-->

---

# Framework-Specific Guidance

## **Understanding the Tech Stack**

```markdown
- example-slides.md - examples of slides that can be created with Slidev

## Creating Slides

- When authoring slides, content belongs in slides.md
- The slides are a Slidev project. For documentation use context7
```

<v-click>

**Key Pattern**: Use external documentation tools when available

</v-click>

<!--
I also used rules to help the agent understand the specific technology stack we were using. I pointed it to example slides and explained that this was a Slidev project. The key pattern here is telling the agent to use external documentation tools like context7 when they're available, rather than relying on potentially outdated training data.
-->

---

# Leveraging MCP and Context7

## **What is MCP?**
**Model Context Protocol** - allows Claude to access external tools and data sources

## **Context7 Integration**  
```markdown
### Rules formats

- We'll cover Agents.md, Cursor, Claude Code, and Github Copilot. use context7
```

<v-click>

**Benefit**: Agent gets current, accurate documentation instead of guessing

</v-click>

<!--
Let me explain MCP - Model Context Protocol - which allows Claude to access external tools and data sources. Context7 is one such tool that provides access to up-to-date documentation. By telling the agent to "use context7" for specific topics, it gets current, accurate documentation instead of potentially outdated information from training data.
-->

---

# Corrective Rules: Learning from Mistakes

## **When Things Go Wrong**

<v-click>

During test runs, I noticed issues and created rules:

```markdown
- Make sure text doesn't overflow the slide. 
  At most 8 lines of text. THIS IS VERY IMPORTANT.
- Slides should have sufficient contrast for dark mode.
- Never use the class: text-center
- Speaker notes go in HTML comments at slide end.
- Use layouts to make slides more compelling
```

</v-click>

<v-click>

**Key Principle**: If you find yourself correcting an agent, define a rule

</v-click>

<!--
The most important pattern I discovered was creating corrective rules. When I found problems during test runs - text overflow, poor contrast, wrong CSS classes, missing speaker notes - I turned each correction into a rule. The key principle is: if you find yourself correcting an agent, define a rule to prevent that issue in the future.
-->

---

# Nested Rules and Scoping

## **Directory-Specific Context**

Inside `/resources/images/CLAUDE.md`:

```markdown
# Images for Slides

- junior_dev.jpg - image of me as a junior developer
- brian-perry.jpg - good photo for the bio slide  
- actual-ai.png - company image (won't work in two-column layout)
- context_in_repository.png - example of saved context in git
```

<v-click>

**Pattern**: Co-locate specific rules near the content they describe

</v-click>

<!--
Most tools support nested rules and scoping, where you can place more specific rules in subdirectories. I used this to help the agent select appropriate images by creating an image-specific CLAUDE.md file right in the images directory. The pattern here is to co-locate specific rules near the content they describe, giving the agent detailed context about each resource.
-->

---
layout: section
---

# Tips and Tricks for Rules-Driven Workflows

Beyond the basics

<!--
Now let's cover some additional tips and tricks that can make your rules-driven workflows even more effective.
-->

---

# Keep Context in the Repository

<div class="grid grid-cols-2 gap-8">

<div>

## **If the agent can't see it, it probably doesn't know it**

- Save evaluation runs to codebase
- Include relevant screenshots  
- Document decision history
- Store context for future reference

</div>

<div>

<img src="/resources/images/context_in_repository.png" class="rounded shadow-lg" alt="Example of context stored in repository" />

</div>

</div>

<!--
A crucial tip: if the agent can't see it in the repository, it probably doesn't know about it and might make things up. I saved all my evaluation runs, relevant screenshots, decision history, and other context right in the codebase. This image shows an example of how I stored additional context in the git history for the agent to reference.
-->

---

# Don't Overlook the Basics

## **Fundamentals become even more important with agents**

<div class="grid grid-cols-3 gap-6">

<div>

### 🔍 **Linting**
Automated code quality checks catch issues early

</div>

<div>

### 🧪 **Testing** 
Verify agent-generated code works correctly

</div>

<div>

### 📚 **Documentation**
Clear docs help agents understand context

</div>

</div>

<v-click>

**Good development practices amplify the effectiveness of rules**

</v-click>

<!--
Don't overlook the development fundamentals - they become even more important when working with agents. Linting catches code quality issues in agent-generated code. Testing verifies that what the agent produces actually works correctly. And good documentation helps agents understand the context and patterns in your codebase. These good development practices amplify the effectiveness of your rules.
-->

---

# Community Resources

## **Cursor Directory Rules**
[cursor.directory/rules/drupal](https://cursor.directory/rules/drupal)

<v-click>

- **Pre-built rules** for popular frameworks
- **Community contributions** from experienced developers  
- **Starting points** for your own rule sets
- **Framework-specific** best practices

</v-click>

<v-click>

**Tip**: Use community rules as a foundation, then customize for your specific needs

</v-click>

<!--
Take advantage of community resources like Cursor Directory, which provides pre-built rules for popular frameworks like Drupal. These are community contributions from experienced developers that give you excellent starting points for your own rule sets. They include framework-specific best practices that you might not think of on your own. Use these as a foundation, then customize them for your specific project needs.
-->

---

# Demo: Backlog.md

**A tool for managing project collaboration between humans and AI agents in a git ecosystem**

<v-click>

Behind the scenes: This is a series of complex rules working together

</v-click>

<!--
Let's look at Backlog.md - a tool for managing project collaboration between humans and AI agents within a git ecosystem. What makes this interesting is that behind the scenes, this is actually a sophisticated series of complex rules working together to manage the collaboration workflow.
-->

---

# Demo: Cursor Plan Mode

**Interactive planning with rule-guided constraints**

<v-click>

Shows how rules can guide the planning phase before implementation

</v-click>

<!--
Here we can see Cursor's Plan Mode in action. This demonstrates how rules can guide not just the implementation phase, but also the planning phase of development. The agent uses rules to understand constraints and requirements before writing any code.
-->

---

# Demo: Actual AI ADR Management

**Architecture Decision Records with intelligent assistance**

<v-click>

Rules help maintain consistency across architectural decisions

</v-click>

<!--
Finally, here's how we manage ADRs (Architecture Decision Records) at Actual AI. This shows how rules can help maintain consistency across architectural decisions, ensuring that the format, content, and reasoning patterns stay consistent across your team's documentation.
-->

---

# Key Takeaways

<div class="space-y-6">

<div v-click>

### 📝 **Rules transform unpredictable AI into reliable partners**

</div>

<div v-click>

### 🎯 **Start small, iterate based on real corrections**

</div>

<div v-click>

### 🔧 **Use the right format for your tool and team**

</div>

<div v-click>

### 📚 **Keep context visible in your repository**

</div>

<div v-click>

### 🏗️ **Good development practices amplify rule effectiveness**

</div>

</div>

<!--
Let's recap the key takeaways from today's talk. Rules transform unpredictable AI agents into reliable development partners. Start small with your rules and iterate based on the real corrections you find yourself making. Choose the right format for your specific tool and team needs. Keep important context visible in your repository where agents can access it. And remember that good development practices like testing and linting amplify the effectiveness of your rules.
-->

---
layout: center
---

# "If AI gets it wrong, don't give up - write a rule"

<div class="mt-16 text-xl opacity-75">
Transform frustration into systematic improvement
</div>

<!--
Here's the core principle I want you to remember: If AI gets it wrong, don't give up - write a rule. This simple approach transforms frustration into systematic improvement. Every mistake becomes an opportunity to make your AI assistant more reliable and effective.
-->

---
layout: center
---

# Thank You!

## Questions & Discussion

<div class="mt-12 space-y-4">
  <div>📧 **Email**: brian@actual.ai</div>
  <div>🐦 **Bluesky**: @brianperry.dev</div>
  <div>💻 **GitHub**: @backlineint</div>
</div>

<div class="mt-16 text-sm opacity-50">
Slides created with Slidev and Claude Code
</div>

<!--
Thank you for your attention! I'm excited to hear your questions and discuss how you might implement rules-driven development in your own workflows. You can reach me at the contact information shown here. These slides themselves were created using Slidev and Claude Code - a perfect example of the rules-driven approach we've been discussing.
-->