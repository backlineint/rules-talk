---
theme: seriph
background: https://cover.sli.dev
title: Unlocking the Power of Agent-Driven Development with Rules
info: |
  ## Agent-Driven Development with Rules
  Exploring the overlooked key to making coding agents truly effective.
  Learn more about rules, strategies, formats, and workflows.
class: text-center
drawings:
  persist: false
transition: slide-left
mdc: true
duration: 45min
---

# Unlocking the Power of Agent-Driven Development with Rules

Brian Perry

<!--
Welcome the audience and introduce yourself. Set the stage for the talk by acknowledging that AI coding agents have become a huge part of development workflows, but many developers are still struggling to get the results they expect.
-->

---
transition: fade-out
---

# The Problem

Many developers and teams are:
- Struggling to see the benefits they expect
- Abandoning these tools altogether
- Not unlocking the full potential of AI assistants

<!--
Acknowledge the reality that while AI coding agents have grown exponentially in effectiveness, many developers aren't seeing the benefits. This creates frustration and leads to abandonment of tools that could be transformative.
-->

---
transition: slide-up
---

# My Journey

From skeptic to believer

- Once doubted the value of AI coding agents
- Now rely on agent-driven development daily
- **Rules** were the key that unlocked everything

<!--
Share your personal story. You started as a skeptic, which many in the audience can relate to. But something changed - you discovered rules. This is what transformed your experience from struggling to succeeding.
-->

---
transition: slide-up
---

# What Are Rules?

Rules control how the agent behaves

- Reusable, scoped instructions
- Provide structure for agent success
- Think of your AI assistant as your **best junior developer**
- Capable and tireless, but in need of clear **guardrails**

<!--
Introduce the core concept. Rules are instructions that guide the agent's behavior. Use the junior developer analogy here - it's powerful and relatable. A junior developer is capable and willing to work tirelessly, but needs clear direction and boundaries to succeed.
-->

---
transition: slide-up
---

# Why Rules Matter

Rules provide the **structure** that allows agents to succeed

- Without rules: inconsistent, unpredictable behavior
- With rules: reliable, repeatable, aligned with your needs
- If AI gets it wrong, don't give up - **write a rule**

<!--
Emphasize that rules aren't optional - they're essential. Compare the chaos of an unguided agent to the order of a well-ruled one. The key message: when AI fails, the solution isn't to abandon it, but to write better rules.
-->

---
transition: slide-up
level: 2
---

# Practical Strategies: Defining Rules

1. Start with **pain points** - What does the agent get wrong?
2. Be **specific** - Vague rules lead to vague results
3. **Iterate** - Rules improve with refinement
4. **Scope appropriately** - Global vs. context-specific rules
5. **Document examples** - Show what good looks like

<!--
Walk through the practical approach. Start by identifying where the agent fails, then be very specific about what you want. Emphasize that rules are living documents - they get better with iteration. Discuss when to use global rules vs. context-specific ones.
-->

---
transition: slide-up
---

# Rules Formats: Cursor

```markdown
# Cursor Rules Format

When writing code:
- Use TypeScript for type safety
- Prefer functional components
- Include error handling
- Write tests for critical paths
```

<!--
Show the Cursor format. This is typically a .cursorrules file or rules in the project. Keep it simple and show a practical example.
-->

---
transition: slide-up
---

# Rules Formats: Claude Code

```markdown
# Claude Code Rules Format

<rules>
  <rule name="code-style">
    Always use async/await, never callbacks
    Prefer named exports over default exports
  </rule>
  <rule name="testing">
    Write unit tests with Jest
    Aim for 80%+ coverage
  </rule>
</rules>
```

<!--
Show Claude Code format. This uses XML-style tags which is different from Cursor. Show how rules can be organized by category.
-->

---
transition: slide-up
---

# Rules Formats: Codex

```yaml
# Codex Rules Format

rules:
  - name: "Code Style"
    scope: "*.ts"
    instructions:
      - "Use strict TypeScript"
      - "No any types"
      - "ESLint compliant"
```

<!--
Show Codex format which uses YAML. Note the different structure and how it supports scoping rules to specific file types.
-->

---
transition: slide-up
layout: two-cols
layoutClass: gap-16
---

# Comparing Formats

::left::

**Cursor**
- Markdown format
- Simple and readable
- Global or project-specific

**Claude Code**
- XML-style tags
- Organized by categories
- Hierarchical structure

::right::

**Codex**
- YAML format
- File-type scoping
- Structured metadata

**Choose based on:**
- Your tool preference
- Team familiarity
- Project needs

<!--
Compare the three formats side-by-side. Help the audience understand when each might be appropriate. Emphasize that the format matters less than actually writing and maintaining rules.
-->

---
transition: slide-up
---

# Building Rules-Driven Workflows

Step 1: **Identify** recurring issues

Step 2: **Document** rules incrementally

Step 3: **Test** and refine

Step 4: **Share** with your team

Step 5: **Maintain** as codebase evolves

<!--
Walk through the workflow step-by-step. This is about building a sustainable process, not just writing rules once. Emphasize the iterative nature and the importance of team collaboration.
-->

---
transition: slide-up
---

# Building Rules-Driven Workflows (cont.)

## Example Workflow

1. Agent generates code without error handling
2. You write a rule: "Always include try/catch for async operations"
3. Agent now includes error handling automatically
4. Team adopts the rule
5. Codebase quality improves consistently

<!--
Give a concrete example of how the workflow plays out in practice. Show the before/after and the ripple effects of good rules.
-->

---
transition: slide-up
---

# Tooling: backlog.md

A powerful pattern for agent-driven development

- Maintain a backlog of tasks
- Agent can read and work from it
- Rules guide how the agent interprets items
- Creates a sustainable workflow

<!--
Introduce backlog.md as a tooling example. This is a practical pattern that many teams are adopting. Explain how it integrates with rules to create a complete workflow.
-->

---
transition: slide-up
layout: two-cols
layoutClass: gap-16
---

# backlog.md Example

::left::

```markdown
# backlog.md

## High Priority
- [ ] Add error handling to API routes
- [ ] Implement user authentication
- [ ] Write unit tests for core modules

## Medium Priority
- [ ] Refactor legacy components
- [ ] Update documentation
```

::right::

**How rules help:**

- Rule: "Always check backlog.md first"
- Rule: "Prioritize items marked High Priority"
- Rule: "Update backlog.md when tasks complete"
- Agent becomes self-directed

<!--
Show a concrete example of backlog.md and explain how rules interact with it. This demonstrates the power of combining rules with tooling.
-->

---
transition: slide-up
class: text-center
---

# Live Demo

Let's see it in action!

<!--
This is a placeholder for the live demo section. You'll demonstrate:
- Writing a rule
- Seeing the agent respond to it
- Working with backlog.md
- Showing the iterative improvement process
-->

---
transition: slide-up
layout: center
class: text-center
---

# Live Demo: Setup

<!--
Set up the demo environment. Show your rules file, backlog.md, and prepare to demonstrate the workflow.
-->

---
transition: slide-up
layout: center
class: text-center
---

# Live Demo: Writing a Rule

<!--
Demonstrate writing a rule in real-time. Show how you identify a pain point, write a specific rule, and then show the agent responding to it.
-->

---
transition: slide-up
layout: center
class: text-center
---

# Live Demo: Rules in Action

<!--
Show the agent using the rules you just wrote. Demonstrate how behavior changes immediately when rules are applied.
-->

---
transition: slide-up
layout: center
class: text-center
---

# Live Demo: backlog.md Workflow

<!--
Demonstrate working with backlog.md. Show how the agent reads tasks, prioritizes them based on rules, and updates the backlog.
-->

---
transition: slide-up
---

# Key Takeaways

1. **Rules are critical** to successful agent-driven development
2. **Practical strategies** exist for defining effective rules
3. **Different formats** (Cursor, Claude Code, Codex) - choose what works
4. **Rules-driven workflows** create sustainable processes
5. **Tooling like backlog.md** amplifies the power of rules

<!--
Summarize the main points. Make sure each key takeaway is clear and actionable. This is what you want the audience to remember.
-->

---
transition: slide-up
---

# Key Takeaways (cont.)

## The Golden Rule

**If AI gets it wrong, don't give up - write a rule.**

Rules are the guardrails that turn chaos into consistency.

<!--
Reinforce the core message. This is the takeaway you want everyone to remember. Rules transform frustration into success.
-->

---
transition: fade-out
layout: center
class: text-center
---

# Thank You!

Questions?

<!--
Open the floor for questions. Be prepared to answer questions about:
- Specific rule examples
- Integrating rules into existing workflows
- Team adoption strategies
- Troubleshooting common issues
-->

---
layout: center
class: text-center
---

# Resources & Next Steps

- Start with one rule addressing your biggest pain point
- Iterate and refine
- Share rules with your team
- Build a rules-driven workflow that scales

**Remember: Your AI assistant is your best junior developer - give them the guardrails they need to succeed.**

<!--
Provide actionable next steps. Make it easy for people to get started. Encourage them to begin small and build from there.
-->
