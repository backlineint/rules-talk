---
theme: seriph
title: Unlocking the Power of Agent-Driven Development with Rules
info: |
  ## Unlocking the Power of Agent-Driven Development with Rules
  
  Learn how to make coding agents truly effective through strategic use of rules - providing structure and guardrails for consistent, predictable outcomes.
background: /background-dark.png
class: text-center
drawings:
  persist: false
transition: slide-left
mdc: true
duration: 35min
---

# Unlocking the Power of Agent-Driven Development with Rules

If AI gets it wrong, don't give up - write a rule.

<div class="abs-br m-6 opacity-60">
  Brian Perry • Actual AI
</div>

<!-- The effectiveness of AI coding agents has grown exponentially, but many developers struggle to see the benefits they expect. This talk explores rules as the overlooked key to making coding agents truly effective. -->

---
layout: image-right
image: /resources/images/brian-perry.jpg
---

# About Me: Brian Perry

- Founding Engineer at Actual AI
- Live in the Chicago suburbs
- Love Nintendo (obviously)
- Building guardrails for AI-enabled teams

**Find me:**
- Bluesky: [brianperry.dev](https://bsky.app/profile/brianperry.dev)
- Github: [backlineint](https://github.com/backlineint)

<!-- I'm Brian Perry, a founding engineer at Actual AI where we're building tools to provide guardrails for AI-enabled software teams. I live in the Chicago suburbs with my family and am a huge Nintendo fan. -->

---
layout: center
class: text-center
---

# Claude Code: Co-Author of This Talk

- Claude Code helped draft content, iterate on demos, and tighten language
- `CLAUDE.md` keeps Claude Code aligned with the story arc
- Today's deck is proof that rules + agents co-create real work

<!-- This presentation itself demonstrates the power of agent-driven development. Claude Code helped draft content, iterate on demonstrations, and refine the language throughout. The CLAUDE.md file in this project keeps the agent aligned with our story arc and goals. -->

---
layout: center
---

# Actual AI

## Building guardrails for AI-enabled software teams

<img src="/resources/images/actual-ai.png" class="h-40 mx-auto" />

We're building tools that help teams harness AI effectively while maintaining quality and security standards.

<!-- At Actual AI, we're focused on solving the challenges that come with AI adoption in software teams. We're building tools that provide the necessary guardrails and structure to help teams leverage AI effectively. -->

---
layout: center
class: text-center
---

# The Problem

## Everyone has experienced AI making mistakes

<!-- Let's start with a universal truth - we've all experienced AI making mistakes. Whether it's generating incorrect code, misunderstanding requirements, or producing inconsistent results. -->

---

# The Standard Advice

## "Think of AI as a Junior Developer"

<v-click>

### Personal reflection: I graduated in 2002

Thinking of me 23 years ago is **horrifying**

</v-click>

<v-click>

### What I needed then:
- **Mentors** to guide me
- **Guidelines** to follow
- **Documentation** to reference
- **Trial and error** to learn

</v-click>

<!-- The common advice is to think of AI as a junior developer. But when I reflect on myself as a junior developer - I graduated in 2002 - that thought is honestly horrifying. I needed so much structure and guidance. -->

---
layout: center
class: text-center
---

# Coding agents need the same thing

**Structure, guidance, and clear expectations**

<!-- Just like junior developers, coding agents need structure, guidance, and clear expectations to be effective. That's where rules come in. -->

---

# What Are Rules?

<v-click>

## 📝 **Reusable, scoped instructions that control agent behavior**

</v-click>

<v-click>

## 🎯 **They provide structure and guardrails**

</v-click>

<v-click>

## 🔄 **They enable consistent, predictable outcomes**

</v-click>

<v-click>

### Rules are defined in your codebase as markdown files

### "If AI gets it wrong, don't give up - write a rule"

</v-click>

<!-- Rules are reusable, scoped instructions that control how agents behave. They provide the structure and guardrails that enable consistent, predictable outcomes. They're defined as markdown files in your codebase and follow a simple principle: if AI gets it wrong, don't give up - write a rule. -->

---
layout: two-cols
---

# Understanding Rules Formats

Different tools, different formats:

## Cursor
- `.cursorrules` file
- Project-level configuration
- Natural language instructions

## Claude Code  
- `CLAUDE.md` file
- Memory and instructions
- Import external rule sets

::right::

## GitHub Copilot
- `.copilotignore` file
- Workspace instructions
- Editor-specific settings

## Agents.md
- Emerging standard
- Cross-platform compatibility
- Community-driven format

<!-- Different AI coding tools use different formats for rules. Cursor uses .cursorrules files, Claude Code uses CLAUDE.md, GitHub Copilot has workspace instructions, and there's an emerging standard called Agents.md that aims for cross-platform compatibility. -->

---

# Practical Strategies: Building This Talk

## Starting Simple

```markdown
# Slide Presentation

Build a presentation ready slide deck, not just an outline.
Don't repeat a previous version of this presentation.
```

<v-click>

**Problem:** With only this context, the agent makes things up

</v-click>

<!-- When I started building this talk, I began with just a few high-level rules. But with only this basic context, the agent would still make up content rather than using the actual project materials. -->

---

# Adding Context Navigation

```markdown
## Important Resources

Important resources live in the /resources directory, including:

- abstract.md - description of the session we're creating slides for
- outline.md - in-progress outline of the session content  
- images directory - images to prioritize in the presentation
```

<v-click>

**Result:** Agent now knows where to find the right information

</v-click>

<!-- So I added rules that guide the agent to the most important context - telling it exactly where to find the session description, content outline, and relevant images. -->

---

# Framework-Specific Rules

```markdown
## Creating Slides

- When authoring slides, content belongs in slides.md
- The slides are a Slidev project. For documentation use context7
- example-slides.md - examples of slides that can be created with Slidev
```

<v-click>

**Key insight:** `use context7` tells the agent to use the context7 MCP

**MCP = Model Context Protocol** - allows agents to access external tools and data

</v-click>

<!-- I also added framework-specific rules to help the agent understand the Slidev environment. The key insight here is that 'use context7' tells the agent to use the context7 Model Context Protocol server, which gives it access to up-to-date documentation. -->

---

# Iterative Rule Refinement

## When you find yourself correcting an agent, define a rule

```markdown
- The slides should only include content for presentation, not speaker notes
- Make sure text doesn't overflow. At most 8 lines of text per slide
- Slides should have sufficient contrast for dark mode presentation  
- Slides using lists should not use class: text-center
- Speaker notes can be included as html comments at slide end
- Use headings to make slides more compelling
```

<!-- As I tested the slides during development, I found issues and turned each correction into a rule. This iterative refinement process ensures the agent learns from mistakes and doesn't repeat them. -->

---

# Nested Rules and Scoping

Most tools allow co-locating rules files to increase priority or scope rules to specific directories.

## Example: Image Selection Rules

Inside `/resources/images/CLAUDE.md`:

```markdown
# Images for Slides

- junior_dev1.jpg - image of me as a junior developer
- brian-perry.jpg - good photo for the bio slide  
- actual-ai.png - Actual AI company logo
```

<v-click>

**Result:** Agent prioritizes these specific images for the presentation

</v-click>

<!-- Most tools support nested rules that apply to specific directories. For example, I created a CLAUDE.md file inside the images directory that helps the agent select the right images for specific slides. -->

---
layout: two-cols
---

# Cursor Rules Format

**File:** `.cursorrules`

```markdown
# React TypeScript Project Rules

You are an expert React and TypeScript developer.

## Code Style
- Use functional components with hooks
- Prefer const assertions for better type inference
- Use meaningful variable names
- Implement proper error boundaries

## Testing
- Write tests for all new components
- Use React Testing Library
- Test user interactions, not implementation
```

::right::

# Claude Code Format  

**File:** `CLAUDE.md`

```markdown
# Project Memory

## Code Preferences
- Use TypeScript strict mode
- Prefer composition over inheritance
- Follow SOLID principles

## Important Commands
- Build: `npm run build`
- Test: `npm test`
- Lint: `npm run lint`

## External Rules
@./rules/react-best-practices
@./rules/testing-standards
```

<!-- Here are examples of the different rule formats. Cursor uses .cursorrules files with natural language instructions, while Claude Code uses CLAUDE.md files that can import external rule sets using the @ syntax. -->

---
layout: two-cols
---

# GitHub Copilot Format

**File:** Multiple approaches

```markdown
# In workspace settings.json
{
  "github.copilot.enable": {
    "*": true,
    "yaml": false
  },
  "github.copilot.advanced": {
    "length": 500,
    "temperature": 0.1
  }
}
```

```markdown
# Workspace instructions
Use TypeScript for all new files.
Follow the existing code style.
Add JSDoc comments for public APIs.
Prefer async/await over Promises.
```

::right::

# Agents.md Format

**File:** `AGENTS.md`

```markdown
# AGENTS.md

## Setup commands
- Install deps: `pnpm install`
- Start dev: `pnpm dev`  
- Run tests: `pnpm test`

## Code style
- TypeScript strict mode
- Single quotes, no semicolons
- Functional patterns preferred

## Testing instructions
- All tests must pass before commit
- Update tests for changed functionality
```

<!-- GitHub Copilot can be configured through workspace settings and instructions, while Agents.md provides an emerging standard that aims to work across multiple tools with a simple markdown format. -->

---

# Best Practices for Rule Writing

<v-click>

## **Be Specific**
"Use consistent naming" → "Use camelCase for variables, PascalCase for components"

</v-click>

<v-click>

## **Provide Context**
Don't just say what, explain why when it matters

</v-click>

<v-click>

## **Start Simple, Iterate**
Begin with high-level rules, refine based on experience  

</v-click>

<v-click>

## **Scope Appropriately**
Global rules for team standards, local rules for project specifics

</v-click>

<v-click>

## **Make Rules Discoverable**
Document where rules live and how to update them

</v-click>

<!-- Here are the key best practices for writing effective rules. Be specific rather than vague, provide context when needed, start simple and iterate based on experience, scope rules appropriately, and make sure your team knows where rules live and how to update them. -->

---
layout: center
---

# Building a Rules-Driven Workflow

## 1. **Start with team standards** - coding style, testing requirements
## 2. **Add project specifics** - build commands, deployment steps  
## 3. **Capture learnings** - turn corrections into rules
## 4. **Share and evolve** - make rules part of your team culture

<!-- Building a rules-driven workflow involves starting with team standards, adding project specifics, capturing learnings from agent interactions, and making rules part of your team culture. -->

---
layout: image-left
image: /resources/images/junior_dev1.jpeg
---

# The Junior Developer Analogy

## That junior developer from 2002?

With the right mentorship, guidelines, and structure, they became pretty capable.

## The same is true for AI agents

Rules provide the mentorship and structure that transform unreliable agents into dependable team members.

<!-- Looking back at that junior developer from 2002 - with the right mentorship, guidelines, and structure, they eventually became pretty capable. The same transformation happens with AI agents when you provide them with proper rules and structure. -->

---
layout: center
class: text-center
---

# Key Takeaways

## **Rules control agent behavior through reusable instructions**

## **Different tools use different formats, but principles are universal**

## **Start simple, iterate based on experience**  

## **If AI gets it wrong, don't give up - write a rule**

<!-- The key takeaways are that rules control agent behavior through reusable instructions, different tools use different formats but the principles are universal, you should start simple and iterate, and most importantly - if AI gets it wrong, don't give up, write a rule. -->

---
layout: center
class: text-center
---

# Thank You

## Questions?

**Brian Perry** • Actual AI  
Bluesky: [brianperry.dev](https://bsky.app/profile/brianperry.dev)  
Github: [backlineint](https://github.com/backlineint)

### This presentation and demo code:
**github.com/backlineint/rules-talk**

<!-- Thank you for your time today. I'm happy to take any questions about rules-driven development, specific implementation details, or anything else we covered. You can find me on Bluesky and GitHub, and all the code and slides from this presentation are available on GitHub. -->