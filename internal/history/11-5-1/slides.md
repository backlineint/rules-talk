---
# try also 'default' to start simple
theme: seriph
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://cover.sli.dev
# some information about your slides (markdown enabled)
title: Unlocking the Power of Agent-Driven Development with Rules
info: |
  ## Unlocking the Power of Agent-Driven Development with Rules
  Exploring how rules are critical for effective AI coding agents.

  Learn more at [Sli.dev](https://sli.dev)
# apply UnoCSS classes to the current slide
class: text-center
# https://sli.dev/features/drawing
drawings:
  persist: false
# slide transition: https://sli.dev/guide/animations.html#slide-transitions
transition: slide-left
# enable MDC Syntax: https://sli.dev/features/mdc
mdc: true
# duration of the presentation
duration: 45min
---

# Unlocking the Power of Agent-Driven Development with Rules

Brian Perry

<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    Press Space for next page <carbon:arrow-right class="inline"/>
  </span>
</div>

<!--
Welcome to the talk! Today we're going to explore how rules can unlock the power of agent-driven development.
-->

---

# About Me

**Brian Perry**

- Founding Engineer at Actual AI
- Live in the Chicago suburbs
- Love Nintendo

<!--
Quick intro about myself before we dive into the content.
-->

---

# About Actual AI

We're building a set of tools to provide **guardrails for AI-enabled software teams**.

<!--
Actual AI is working on tooling to help teams succeed with AI development. This sets context for why I'm talking about rules.
-->

---

# The Problem

Anyone who has used AI for development has experienced it making **mistakes**.

<v-click>

- Wrong approach to a problem
- Missing edge cases
- Inconsistent with codebase style
- Not following best practices

</v-click>

<!--
We've all been there - AI makes mistakes, sometimes obvious ones. This is the problem we're trying to solve.
-->

---

# Common Advice

## "Think of AI as a Junior Developer"

<v-click>

This is helpful... but incomplete.

</v-click>

<!--
The junior developer analogy is common, but we need to think about what junior developers actually need to succeed.
-->

---

# Personal Reflection

I graduated college in **2002**.

<v-click>

Thinking of me as a developer 23 years ago is **horrifying**.

</v-click>

<v-click>

I needed:
- Mentors
- Clear guidelines
- Well-documented codebases
- Lots of learning and trial and error

</v-click>

<!--
Personal story about being a junior developer and what I needed to succeed. This connects to what AI agents need.
-->

---

# The Parallel

**Coding agents need the same thing.**

<v-click>

- Structured guidance
- Clear boundaries
- Consistent patterns
- Reusable knowledge

</v-click>

<v-click>

**Rules provide this structure.**

</v-click>

<!--
Transition to rules as the solution. Rules are what provide the structure that junior developers need, and AI agents need too.
-->

---

# Why Rules Matter

Rules control how the agent behaves by providing a set of **reusable, scoped instructions**.

<!--
Introduction to rules and their purpose.
-->

---

# Rules as Guardrails

Think of your AI assistant as your **best junior developer**:

<v-click>

- Capable and tireless ✓
- Needs clear guardrails ✗

</v-click>

<v-click>

**Rules provide the structure that allows agents to succeed.**

</v-click>

<!--
Rules act as guardrails, similar to how we guide junior developers. They provide structure and boundaries.
-->

---

# Rules Enable Success

Rules provide **structure** that allows agents to succeed.

<v-click>

- Consistent behavior
- Predictable outcomes
- Reusable patterns
- Scoped instructions

</v-click>

<!--
How rules enable success through structure and consistency.
-->

---

# The Rule Philosophy

<div class="text-4xl font-bold mt-20">

If AI gets it wrong, **don't give up** - write a rule.

</div>

<!--
Key philosophy: rules are the solution when AI makes mistakes. Don't give up, write a rule.
-->

---

# Rules Are Reusable

Rules are **reusable, scoped instructions**.

<v-click>

- Write once, use everywhere
- Scoped to specific contexts
- Shared across team
- Evolved over time

</v-click>

<!--
Rules are reusable and scoped, making them powerful tools for building consistent AI behavior.
-->

---

# Understanding Rules Formats

Different tools use different rules formats:

- Cursor
- Claude Code
- Codex

Let's explore each one.

<!--
Introduction to the different rules formats we'll be comparing.
-->

---

# Cursor Rules Format

Cursor uses `.cursorrules` files in your project root.

```markdown
# Project Rules

## Code Style
- Use TypeScript for all new code
- Follow ESLint configuration
- Prefer functional components

## Testing
- Write tests for all new features
- Use Jest for unit tests
- Aim for 80% code coverage
```

<!--
Cursor rules format example. Show how it's structured as markdown with sections.
-->

---

# Claude Code Rules Format

Claude Code uses a `rules` directory with markdown files.

```markdown
# .claude/rules/code-style.md

## TypeScript Guidelines
- Always use explicit return types
- Prefer interfaces over types for object shapes
- Use const assertions for immutable data

## Component Patterns
- Use React hooks for state management
- Extract complex logic into custom hooks
```

<!--
Claude Code format example. Show how it organizes rules in a directory structure.
-->

---

# Codex Rules Format

Codex uses a structured rules configuration file.

```json
{
  "rules": [
    {
      "id": "typescript-style",
      "scope": "*.ts,*.tsx",
      "content": "Use TypeScript strict mode. Prefer explicit types."
    },
    {
      "id": "testing-requirements",
      "scope": "**/*.test.ts",
      "content": "Write descriptive test names. Use AAA pattern."
    }
  ]
}
```

<!--
Codex format example. Show JSON-based configuration with scoping.
-->

---

# Format Comparison

<div class="grid grid-cols-3 gap-4">

<div>

**Cursor**
- Single file
- Markdown format
- Project-wide scope

</div>

<div>

**Claude Code**
- Directory structure
- Multiple files
- Organized by topic

</div>

<div>

**Codex**
- JSON config
- Scoped rules
- Structured format

</div>

</div>

<!--
Comparison of the three formats showing their key characteristics.
-->

---

# Format Comparison (cont.)

| Feature | Cursor | Claude Code | Codex |
|---------|--------|-------------|-------|
| **Format** | Markdown | Markdown | JSON |
| **Organization** | Single file | Directory | Config file |
| **Scoping** | Project-wide | File-based | Rule-based |
| **Complexity** | Simple | Moderate | Structured |

<!--
Table comparing the features of each format side by side.
-->

---

# When to Use Which Format

<v-click>

**Cursor** - Simple projects, quick setup

</v-click>

<v-click>

**Claude Code** - Large teams, organized rules

</v-click>

<v-click>

**Codex** - Complex configurations, fine-grained control

</v-click>

<!--
Guidance on when to use each format based on project needs.
-->

---

# Practical Strategies

## How to Define Effective Rules

<!--
Introduction to practical strategies for writing rules.
-->

---

# Strategy 1: Start Specific

<v-click>

**Bad:**
```
Write good code.
```

</v-click>

<v-click>

**Good:**
```
Use TypeScript strict mode. Prefer async/await over promises. 
Include JSDoc comments for all exported functions.
```

</v-click>

<!--
Example of specific vs vague rules. Specificity is key.
-->

---

# Strategy 2: Scope Appropriately

Rules can be:
- Project-wide
- File-specific
- Feature-specific
- Context-specific

<v-click>

**Example:** React component rules only apply to `.tsx` files.

</v-click>

<!--
Discussion of scoping rules appropriately for different contexts.
-->

---

# Strategy 3: Build a Rules Library

<v-click>

- Start with common patterns
- Document your rules
- Share with your team
- Evolve over time

</v-click>

<v-click>

**Pro tip:** Version control your rules like you version control your code.

</v-click>

<!--
Strategy for building and maintaining a rules library over time.
-->

---

# Strategy 4: Iterate and Refine

<v-click>

1. Observe where AI struggles
2. Write a rule to address it
3. Test and refine
4. Repeat

</v-click>

<v-click>

**It's a continuous improvement process.**

</v-click>

<!--
The iterative process of refining rules based on AI behavior and outcomes.
-->

---

# Best Practices

<v-click>

- **Be explicit** - Don't assume the AI knows what you mean
- **Use examples** - Show, don't just tell
- **Keep it focused** - One rule, one purpose
- **Test your rules** - Verify they work as expected

</v-click>

<!--
Best practices for writing effective rules.
-->

---

# Rules-Driven Workflow

Building a workflow around rules

<!--
Introduction to creating a workflow that centers around rules.
-->

---

# The Rules-Driven Development Cycle

<v-click>

1. **Identify** - Where is AI struggling?
2. **Rule** - Write a rule to address it
3. **Test** - Verify the rule works
4. **Refine** - Improve based on results

</v-click>

<v-click>

**Repeat continuously.**

</v-click>

<!--
The cycle of rules-driven development.
-->

---

# Tooling: backlog.md

A simple file to track rules and improvements:

```markdown
# Rules Backlog

## New Rules Needed
- [ ] Add rule for error handling patterns
- [ ] Create rule for API response formatting

## Rules to Refine
- [ ] Improve TypeScript rules (too verbose)
- [ ] Update testing rules with new patterns
```

<!--
Introduction to backlog.md as a tool for managing rules.
-->

---

# Live Demo

<div class="text-center mt-20">

Let's see rules in action!

</div>

<!--
Transition to live demo section.
-->

---

# Key Takeaways

<v-click>

- Rules are critical to successful agent-driven development

</v-click>

<v-click>

- Learn practical strategies to define rules

</v-click>

<v-click>

- Understand the various rules formats (Cursor, Claude Code, Codex)

</v-click>

<v-click>

- Build a "rules-driven" workflow

</v-click>

<v-click>

- Explore tooling like backlog.md

</v-click>

<!--
Recap of key takeaways from the talk.
-->

---

# The Bottom Line

The effectiveness of AI coding agents has grown exponentially.

<v-click>

**Rules unlock their true potential.**

</v-click>

<v-click>

If AI gets it wrong, don't give up - **write a rule**.

</v-click>

<!--
Final message reinforcing the core philosophy.
-->

---

# Questions?

<div class="text-center mt-20">

Thank you!

</div>

<!--
Q&A slide to end the presentation.
-->