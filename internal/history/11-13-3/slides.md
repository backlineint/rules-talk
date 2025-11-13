---
theme: seriph
background: https://cover.sli.dev
title: Unlocking the Power of Agent-Driven Development with Rules
info: |
  ## Unlocking the Power of Agent-Driven Development with Rules
  
  The effectiveness of AI coding agents has grown exponentially in the past year. 
  Yet many developers still struggle to see the benefits they expect. 
  This session explores how rules can make coding agents truly effective.

class: text-center
highlighter: shiki
drawings:
  persist: false
transition: slide-left
mdc: true
duration: 35min
---

# Unlocking the Power of Agent-Driven Development with Rules

The key to making AI coding agents truly effective

<div class="abs-br m-6 text-xl">
  @brianperry
</div>

<!-- Welcome! Today we're going to explore how rules can transform your experience with AI coding agents from frustrating to fantastic. -->

---
layout: image-right
image: /resources/images/brian-perry.jpg
---

# About Me

**Brian Perry**

- 🚀 Founding Engineer at Actual AI
- 🏠 Chicago suburbs
- 🎮 Nintendo enthusiast
- 💻 Former Drupal developer turned AI tools advocate

**Find me online:**
- 🦋 Bluesky: [@brianperry.dev](https://bsky.app/profile/brianperry.dev)
- 🐙 GitHub: [@backlineint](https://github.com/backlineint)

<!-- I'm Brian Perry, a founding engineer at Actual AI where we're building guardrails for AI-enabled software teams. I've been coding for over 20 years, and I've witnessed firsthand the transformation that AI agents can bring to development workflows. -->

---
layout: center
class: text-center
---

# Claude Code: Co-Author of This Talk

- 🤝 Claude Code helped draft content, iterate on demos, and tighten language
- 📋 `CLAUDE.md` keeps Claude aligned with the story arc
- 🎯 Today's deck is proof that rules + agents co-create real work

<!-- This presentation itself is a demonstration of what's possible when you use rules effectively. Claude Code didn't just help me write slides - it collaborated as a true partner because we established clear rules and expectations. -->

---
layout: image-right
image: /resources/images/AGENTS.md
---

# Actual AI

**Building Guardrails for AI-Enabled Software Teams**

We're creating a set of tools to help teams:
- 🛡️ Implement safety controls for AI development
- 📏 Establish consistent coding standards
- 🔍 Monitor and audit AI-generated code
- ⚡ Accelerate development while maintaining quality

<!-- At Actual AI, we're solving the exact problem we're talking about today - how do you scale AI-assisted development while maintaining quality, security, and consistency? -->

---
layout: center
class: text-center
---

# The Problem

<v-click>

## Everyone has experienced AI making mistakes

</v-click>

<v-click>

## Common advice: *"Think of AI as a Junior Developer"*

</v-click>

<v-click>

## Personal reflection: *"I graduated in 2002 - thinking of me 23 years ago is horrifying"*

</v-click>

<!-- Let's be honest - we've all had those moments where an AI agent produces code that makes us wonder if it's ever actually programmed before. The common advice is to treat AI like a junior developer, but when I think about myself as a junior developer 23 years ago... yikes. -->

---
layout: image-right
image: /resources/images/junior_dev1.jpeg
---

# What Junior Developers Need

<v-click>

**What I needed 23 years ago:**
- 👥 **Mentors** - guidance and feedback
- 📖 **Guidelines** - clear expectations
- 📚 **Documentation** - context and standards
- 🔄 **Trial and error** - safe space to learn

</v-click>

<v-click>

## Coding agents need the same thing

</v-click>

<!-- Just like junior developers, AI agents need structure, guidance, and clear expectations. They need to understand not just what to do, but how you want it done, what your conventions are, and what good looks like in your specific context. -->

---
layout: center
class: text-center
---

# Why Rules Matter

<v-click>

## What are rules?

</v-click>

<v-click>

📝 **Reusable, scoped instructions that control agent behavior**

</v-click>

<v-click>

🎯 **They provide structure and guardrails**

</v-click>

<v-click>

🔄 **They enable consistent, predictable outcomes**

</v-click>

<!-- Rules are your way of codifying your expectations and preferences. They're like having a conversation with your future self about how you want code to be written, what patterns to follow, and what to avoid. -->

---
layout: center
---

# The Rules Philosophy

<div class="grid grid-cols-2 gap-8">
<div>

## ❌ Without Rules
- Inconsistent output
- Repeated corrections
- Frustrating interactions
- Generic solutions
- Context switching overhead

</div>
<div v-click>

## ✅ With Rules
- Predictable behavior
- Aligned with your style
- Efficient workflows
- Project-specific solutions
- Continuous improvement

</div>
</div>

<v-click>

<div class="mt-8 text-center text-2xl font-bold">
"If AI gets it wrong, don't give up - write a rule"
</div>

</v-click>

<!-- This is the core philosophy: instead of getting frustrated when AI doesn't behave the way you want, capture that expectation in a rule. Over time, you build up a library of preferences that make every interaction better. -->

---
layout: center
class: text-center
---

# Understanding Rules Formats

Different tools, different approaches

<v-click>

**We'll explore:**
- 🎯 **Cursor** - `.cursor/rules` files
- 🤖 **Claude Code** - `CLAUDE.md` files  
- 🐙 **GitHub Copilot** - `.github/copilot-instructions.md`
- 📋 **Agents.md** - emerging cross-platform standard

</v-click>

<!-- Each major AI coding tool has developed its own approach to rules and instructions. Let's explore how each one works and when you might use each format. -->

---
layout: two-cols
layoutClass: gap-16
---

# Cursor Rules

**Location:** `.cursor/rules`

**Format:** MDC (Markdown with metadata)

```yaml
---
description: RPC Service boilerplate
globs: ["**/*.rpc.ts"]
alwaysApply: false
---

- Use internal RPC pattern when defining services
- Always use snake_case for service names
- Include error handling for all RPC calls
```

::right::

**Key Features:**
- 📁 Directory-based organization
- 🎯 File pattern matching with globs
- ⚙️ Application modes (Always, Intelligent, Manual)
- 👥 Team-wide rule sharing
- 🔄 Composable rule inheritance

<!-- Cursor's approach is very structured. You can organize rules by directory, target specific file patterns, and control exactly when rules apply. This is great for large codebases with different conventions in different areas. -->

---
layout: two-cols
layoutClass: gap-16
---

# Claude Code Rules

**Location:** `CLAUDE.md` (project root)

**Format:** Plain Markdown

```markdown
# Project Rules

## Code Style
- Use TypeScript for all new files
- Prefer functional components in React
- Include JSDoc comments for public APIs

## Testing
- Write tests alongside implementation
- Use Jest for unit tests
- Aim for 80%+ coverage

@docs/api-guidelines.md
```

::right::

**Key Features:**
- 📝 Natural language format
- 📁 File import with `@path` syntax
- 🔄 Works across all Claude interfaces
- 🎯 Project-specific context
- 💡 Memory and learning integration

<!-- Claude Code takes a more conversational approach. You write rules in natural language, and Claude remembers them across sessions. The import syntax lets you reference other documentation files. -->

---
layout: two-cols
layoutClass: gap-16
---

# GitHub Copilot Rules

**Location:** `.github/copilot-instructions.md`

**Format:** Plain Markdown

```markdown
# Repository Instructions

When working with this codebase:

- Follow the established React patterns
- Use TypeScript for type safety
- Write comprehensive tests for new features
- Adhere to the ESLint configuration
- Document public APIs with JSDoc
```

::right::

**Alternative:** `AGENTS.md` files

```markdown
# Agent Instructions

## Code Review Agent
- Focus on security vulnerabilities
- Check coding standards adherence
- Provide constructive feedback

## Documentation Agent  
- Generate clear JSDoc comments
- Update README files
- Maintain API documentation
```

<!-- GitHub Copilot supports both repository-wide instructions and agent-specific configurations. The repository instructions apply to all Copilot interactions, while AGENTS.md files can define behavior for specific AI agents. -->

---
layout: center
---

# Agents.md: The Emerging Standard

<div class="grid grid-cols-2 gap-8">
<div>

**Growing adoption across tools:**
- ✅ GitHub Copilot Chat
- ✅ Claude Code (as alternative)
- ✅ Cursor (planned support)
- ✅ VS Code extensions

</div>
<div>

**Benefits:**
- 🔄 Cross-platform compatibility
- 🎯 Agent-specific instructions
- 📁 Directory-scoped rules
- 🏢 Enterprise-friendly

</div>
</div>

<v-click>

```markdown
# AGENTS.md

## Default Behavior
- Prioritize code readability and maintainability
- Follow established project conventions
- Include appropriate error handling

## Security Focus
- Validate all user inputs
- Use parameterized queries for database access
- Implement proper authentication checks
```

</v-click>

<!-- Agents.md is becoming a de facto standard because it works across multiple tools. As AI agents become more sophisticated and specialized, having a common format for instructions becomes increasingly valuable. -->

---
layout: center
class: text-center
---

# Rules-Driven Development Workflow

## The Process

<v-click>

**1. Start with basics** - coding style, patterns, preferences

</v-click>

<v-click>

**2. Observe and iterate** - add rules when AI misses the mark

</v-click>

<v-click>

**3. Share and standardize** - team-wide rules for consistency

</v-click>

<v-click>

**4. Specialize by context** - different rules for different areas

</v-click>

<v-click>

**5. Continuously improve** - refine rules based on experience

</v-click>

<!-- This isn't a one-time setup. Rules-driven development is an iterative process where you continuously refine your expectations and preferences, building up institutional knowledge that makes every interaction better. -->

---
layout: center
---

# Practical Rules Examples

<div class="grid grid-cols-2 gap-8">
<div>

## Code Quality
```markdown
- Use meaningful variable names
- Prefer pure functions when possible  
- Include error handling for external calls
- Write self-documenting code
- Follow the single responsibility principle
```

## Security
```markdown
- Validate all user inputs
- Use parameterized queries
- Implement proper authentication
- Log security events
- Never commit secrets
```

</div>
<div>

## Testing
```markdown
- Write tests before implementation (TDD)
- Use descriptive test names
- Test edge cases and error conditions
- Mock external dependencies
- Maintain test independence
```

## Documentation  
```markdown
- Include JSDoc for public APIs
- Update README for new features
- Document breaking changes
- Provide usage examples
- Keep documentation in sync with code
```

</div>
</div>

<!-- These are real-world examples of rules that teams use to maintain consistency and quality. The key is to be specific enough to be actionable, but general enough to apply broadly. -->

---
layout: center
class: text-center
---

# Building Your Rules Strategy

## Start Simple

<v-click>

**Begin with:**
- 📝 Coding style preferences
- 🏗️ Architecture patterns you use
- 🧪 Testing approaches
- 📚 Documentation standards

</v-click>

<v-click>

**Then expand:**
- 🔒 Security requirements
- ⚡ Performance considerations
- 🎨 UI/UX guidelines
- 🔄 Git workflow preferences

</v-click>

<v-click>

**Finally optimize:**
- 👥 Team-specific conventions
- 🎯 Project-specific requirements
- 🏢 Organizational policies
- 🔧 Tool-specific configurations

</v-click>

<!-- Don't try to write every rule at once. Start with the basics that affect every piece of code you write, then gradually add more specific guidance as you encounter situations where the AI doesn't behave the way you'd like. -->

---
layout: center
---

# Live Demo Time! 🚀

## We'll demonstrate:

<v-click>

**1. Setting up rules** - from scratch to sophisticated

</v-click>

<v-click>

**2. Agent behavior** - before and after rules

</v-click>

<v-click>

**3. Iterative improvement** - refining rules based on output

</v-click>

<v-click>

**4. Cross-tool compatibility** - same rules, different agents

</v-click>

<!-- Now let's see this in action. I'll show you how to set up rules from scratch, how dramatically they can change agent behavior, and how to continuously improve your setup. -->

---
layout: center
class: text-center
---

# Key Takeaways

<v-click>

## 🎯 Rules transform AI agents from generic tools to specialized partners

</v-click>

<v-click>

## 📈 Start simple, iterate continuously, and capture learnings

</v-click>

<v-click>

## 🤝 Different tools have different approaches - choose what fits your workflow

</v-click>

<v-click>

## 🔄 "If AI gets it wrong, don't give up - write a rule"

</v-click>

<v-click>

## 🚀 Rules-driven development scales human expertise through AI

</v-click>

<!-- These are the core principles to remember. Rules aren't just configuration - they're a way to scale your expertise and preferences across every interaction with AI. -->

---
layout: center
---

# Getting Started Today

<div class="grid grid-cols-2 gap-8">
<div>

## Quick Wins
- ✅ Create your first rules file
- ✅ Document 3 coding preferences
- ✅ Test with your current project
- ✅ Observe the difference

</div>
<div>

## Next Steps
- 🔄 Share rules with your team
- 📋 Try Agents.md format
- 🎯 Add project-specific rules
- 📈 Measure productivity impact

</div>
</div>

<v-click>

<div class="mt-8 text-center">

**Resources:**
- 📖 Examples: github.com/backlineint/rules-examples
- 🤖 Claude Code docs: docs.claude.com/claude-code
- 🎯 Cursor rules guide: cursor.com/docs/context/rules

</div>

</v-click>

<!-- Don't wait - you can start implementing rules today. Pick one tool, write down three preferences, and see how it changes your next AI interaction. The compound benefits build over time. -->

---
layout: center
class: text-center
---

# Questions & Discussion

## Let's talk about your experiences with AI coding agents

<div class="mt-12">

**Connect with me:**
- 🦋 **Bluesky:** @brianperry.dev
- 🐙 **GitHub:** @backlineint
- 💼 **Learn more:** actual.ai

</div>

<div class="mt-8">
<small>This presentation was co-created with Claude Code using rules-driven development</small>
</div>

<!-- Thank you! I'd love to hear about your experiences with AI coding agents, what's worked well, what hasn't, and what questions you have about implementing rules in your workflow. -->