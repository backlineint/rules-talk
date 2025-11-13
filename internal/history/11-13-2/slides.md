---
theme: seriph
background: https://cover.sli.dev
title: Unlocking the Power of Agent-Driven Development with Rules
info: |
  ## Unlocking the Power of Agent-Driven Development with Rules
  The effectiveness of AI coding agents has grown exponentially in the past year. Yet many developers still struggle to see the benefits they expect. This session explores rules as the key to making coding agents truly effective.
class: text-center
transition: slide-left
mdc: true
duration: 35min
---

# Unlocking the Power of Agent-Driven Development with Rules

<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    Press Space for next page <carbon:arrow-right class="inline"/>
  </span>
</div>

---
layout: image-right
image: /profile.jpg
class: text-left
---

# About Me

**Brian Perry**
Founding Engineer at Actual AI

- Building AI guardrails for software teams
- Chicago suburbs, Nintendo enthusiast  
- Bluesky: [@brianperry.dev](https://bsky.app/profile/brianperry.dev)
- GitHub: [@backlineint](https://github.com/backlineint)

<!-- Today we're exploring how rules transform AI coding agents from unpredictable tools into reliable development partners -->

---
layout: center
class: text-center
---

# Claude Code: Co-Author of This Talk

- Claude Code helped draft content, iterate on demos, and tighten language
- `CLAUDE.md` keeps Claude aligned with the story arc  
- Today's deck is proof that rules + agents co-create real work

<!-- This presentation itself demonstrates rules-driven development in action -->

---
layout: image-right
image: https://images.unsplash.com/photo-1559136555-9303baea8ebd?w=800&h=600&fit=crop&crop=focalpoint
---

# Actual AI

**Building guardrails for AI-enabled software teams**

- Preventing AI hallucinations in production
- Ensuring code quality and security standards
- Enabling teams to move fast with confidence
- Tools for responsible AI adoption

<!-- We understand the challenges of scaling AI development across teams -->

---
layout: center
class: text-center
---

# The Problem

<div class="text-6xl mb-8">🤖❌</div>

Everyone has experienced AI making mistakes

<!-- Let's start with the reality we all know -->

---

# Common Advice: "Think of AI as a Junior Developer"

<div class="grid grid-cols-2 gap-8 mt-8">
  <div>
    <h3>The Advice</h3>
    <p class="text-lg">"Just treat your AI like a junior developer"</p>
  </div>
  <div>
    <h3>My Reaction</h3>
    <p class="text-lg">"I graduated in 2002 - thinking of me 23 years ago is <em>horrifying</em>"</p>
  </div>
</div>

<!-- Personal reflection: junior developers need guidance, not abandonment -->

---
layout: two-cols
---

# What Junior Me Needed

- 🧑‍🏫 **Mentors** - Someone to guide decisions
- 📖 **Guidelines** - Clear expectations and standards  
- 📚 **Documentation** - Understanding existing patterns
- 🔄 **Trial and Error** - Safe space to experiment
- ⭐ **Examples** - Concrete patterns to follow

::right::

# What Coding Agents Need

- 📝 **Rules** - Structured guidance and constraints
- 🎯 **Context** - Understanding of project patterns  
- 🔄 **Feedback** - Iterative improvement cycles
- 📋 **Standards** - Consistent code quality expectations
- 🛡️ **Guardrails** - Boundaries to prevent mistakes

<!-- The parallels are striking - both need structure to succeed -->

---
layout: center
class: text-center
---

# Why Rules Matter

<div class="text-4xl mb-8">📝 + 🤖 = 🚀</div>

"If AI gets it wrong, don't give up - write a rule"

---

# What Are Rules?

<div class="grid grid-cols-1 gap-6 mt-8">
  <div class="p-6 bg-blue-100 dark:bg-blue-900 rounded-lg">
    📝 <strong>Reusable, scoped instructions that control agent behavior</strong>
  </div>
  <div class="p-6 bg-green-100 dark:bg-green-900 rounded-lg">
    🎯 <strong>They provide structure and guardrails</strong>  
  </div>
  <div class="p-6 bg-purple-100 dark:bg-purple-900 rounded-lg">
    🔄 <strong>They enable consistent, predictable outcomes</strong>
  </div>
</div>

<div class="mt-8 text-center text-lg">
Rules are defined in your codebase as markdown files
</div>

<!-- Rules bridge the gap between AI capability and reliable results -->

---
layout: two-cols
---

# Rules Transform Results

## Without Rules
- Inconsistent code style
- Ignores project conventions
- Repeats the same mistakes
- Requires constant correction
- Unpredictable outputs

::right::

## With Rules  
- Follows established patterns
- Maintains code quality standards
- Learns from previous feedback
- Self-correcting behavior
- Reliable, consistent results

<!-- The difference is night and day -->

---
layout: center
class: text-center
---

# Understanding Rules Formats

<div class="grid grid-cols-4 gap-4 mt-12">
  <div class="p-4 border rounded-lg">
    <carbon:cursor class="text-4xl mx-auto mb-2"/>
    <div class="font-bold">Cursor</div>
    <div class="text-sm">.cursor/rules</div>
  </div>
  <div class="p-4 border rounded-lg">
    <carbon:watson-machine-learning class="text-4xl mx-auto mb-2"/>
    <div class="font-bold">Claude Code</div>
    <div class="text-sm">CLAUDE.md</div>
  </div>
  <div class="p-4 border rounded-lg">
    <carbon:logo-github class="text-4xl mx-auto mb-2"/>
    <div class="font-bold">GitHub Copilot</div>
    <div class="text-sm">.github/copilot-instructions.md</div>
  </div>
  <div class="p-4 border rounded-lg">
    <carbon:collaborate class="text-4xl mx-auto mb-2"/>
    <div class="font-bold">Emerging Standard</div>
    <div class="text-sm">AGENTS.md</div>
  </div>
</div>

<!-- Each tool has its own format, but patterns are emerging -->

---

# Cursor Rules Format

```yaml
---
description: RPC Service boilerplate
globs: ["src/services/**/*.ts"]
alwaysApply: false
---

- Use our internal RPC pattern when defining services
- Always use snake_case for service names
- Include proper error handling and logging

@service-template.ts
```

**Key Features:**
- MDC (Markdown with Context) format
- Metadata header with scoping options
- Support for file globs and conditional application
- Can reference templates and examples

<!-- Cursor pioneered structured rules with powerful scoping -->

---

# Claude Code Rules Format

````markdown
# Project Rules

## Code Style
- Use TypeScript for all new files
- Prefer functional components in React
- Always include JSDoc comments for functions

## Testing
- Write tests for all new features
- Use Jest and React Testing Library
- Aim for 80% code coverage

## Git Workflow  
- Use conventional commits
- Squash feature branch commits
- Include ticket numbers in commit messages

```typescript
// Example: Preferred function structure
/**
 * Calculates user permissions based on role
 */
export const getUserPermissions = (role: UserRole): Permission[] => {
  // implementation
}
```
````

<!-- Claude Code uses simple markdown - accessible and version-controllable -->

---

# GitHub Copilot Rules Format

```markdown
---
excludeAgent: "code-review"
applyTo: "src/**/*.ts"
---

# TypeScript Development Guidelines

## Code Standards
- Use strict TypeScript configuration
- Prefer type assertions over `any`
- Include return types for all functions

## Component Patterns
- Use functional components with hooks
- Implement proper error boundaries
- Follow accessibility guidelines

## Testing Requirements
- Unit tests for all utility functions
- Integration tests for API endpoints
- E2E tests for critical user flows
```

**Features:**
- Path-specific instructions with `applyTo`
- Agent exclusion with `excludeAgent` 
- Multiple instruction files supported

<!-- Copilot offers the most granular control over rule application -->

---

# AGENTS.md - The Emerging Standard

```markdown
# Development Rules

## Architecture
- Follow domain-driven design principles
- Separate business logic from infrastructure
- Use dependency injection for testability

## Code Quality
- No magic numbers or strings
- Comprehensive error handling
- Meaningful variable and function names

## Security
- Validate all user inputs
- Use parameterized queries
- Never log sensitive information

## Performance  
- Lazy load components when possible
- Optimize database queries
- Use caching strategically
```

**Growing adoption across:**
- Cursor (native support)
- GitHub Copilot (supported)
- Claude Code (via import)

<!-- AGENTS.md is becoming the universal format -->

---
layout: comparison
---

# Rules Format Comparison

| Feature | Cursor | Claude Code | GitHub Copilot | AGENTS.md |
|---------|--------|-------------|---------------|-----------|
| **File Location** | `.cursor/rules` | `CLAUDE.md` | `.github/copilot-instructions.md` | `AGENTS.md` |
| **Metadata Support** | ✅ Rich | ❌ None | ✅ Basic | ❌ None |
| **File Scoping** | ✅ Globs | ❌ Manual | ✅ Path patterns | ❌ Manual |  
| **Conditional Rules** | ✅ Yes | ❌ No | ✅ Agent exclusion | ❌ No |
| **Template Support** | ✅ Yes | ✅ Imports | ❌ No | ❌ No |
| **Cross-tool Support** | ❌ No | ❌ No | ❌ No | ✅ Growing |

<!-- Each format has strengths, but AGENTS.md offers the most portability -->

---
layout: center
class: text-center
---

# Building a Rules-Driven Workflow

<div class="text-4xl mb-8">🔄</div>

From reactive fixes to proactive guidance

---

# The Rules-Driven Development Process

<div class="grid grid-cols-1 gap-4 mt-8">
  <div class="flex items-center p-4 bg-blue-100 dark:bg-blue-900 rounded">
    <div class="text-2xl mr-4">1️⃣</div>
    <div><strong>Start with basics:</strong> Code style, conventions, architecture patterns</div>
  </div>
  <div class="flex items-center p-4 bg-green-100 dark:bg-green-900 rounded">
    <div class="text-2xl mr-4">2️⃣</div>
    <div><strong>Observe patterns:</strong> What mistakes happen repeatedly?</div>
  </div>
  <div class="flex items-center p-4 bg-yellow-100 dark:bg-yellow-900 rounded">
    <div class="text-2xl mr-4">3️⃣</div>
    <div><strong>Document solutions:</strong> Turn fixes into reusable rules</div>
  </div>
  <div class="flex items-center p-4 bg-purple-100 dark:bg-purple-900 rounded">
    <div class="text-2xl mr-4">4️⃣</div>
    <div><strong>Iterate and refine:</strong> Update rules based on results</div>
  </div>
  <div class="flex items-center p-4 bg-red-100 dark:bg-red-900 rounded">
    <div class="text-2xl mr-4">5️⃣</div>
    <div><strong>Share and scale:</strong> Version control your rules for team consistency</div>
  </div>
</div>

<!-- Rules evolve with your understanding and needs -->

---

# Practical Rules Examples

<div class="grid grid-cols-2 gap-8 mt-4">
<div>

## Code Quality Rules
```markdown
## Error Handling
- Always use try-catch for async operations
- Return meaningful error messages
- Log errors with context

## Performance
- Use React.memo for expensive components  
- Implement proper loading states
- Avoid unnecessary re-renders
```

</div>
<div>

## Team Workflow Rules
```markdown
## Git Practices
- Use conventional commit format
- Squash commits before merging
- Include issue numbers in commits

## Code Review
- All PRs require 2 approvals
- Include tests with new features
- Update documentation for API changes
```

</div>
</div>

<!-- Start with your team's most common challenges -->

---
layout: center
class: text-center
---

# Demo: Rules in Action

<div class="text-4xl mb-8">🎬</div>

Let's see rules transform AI behavior live

<!-- Time for the live demonstration -->

---

# Key Takeaways

<div class="grid grid-cols-1 gap-6 mt-8">
  <div class="p-6 bg-blue-100 dark:bg-blue-900 rounded-lg">
    <strong>🎯 Rules are critical</strong> - They transform unpredictable AI into reliable development partners
  </div>
  <div class="p-6 bg-green-100 dark:bg-green-900 rounded-lg">
    <strong>📝 Start simple</strong> - Begin with basic style guides and common patterns  
  </div>
  <div class="p-6 bg-purple-100 dark:bg-purple-900 rounded-lg">
    <strong>🔄 Iterate continuously</strong> - Rules evolve as you learn what works
  </div>
  <div class="p-6 bg-yellow-100 dark:bg-yellow-900 rounded-lg">
    <strong>🚀 Scale across tools</strong> - AGENTS.md provides cross-platform compatibility
  </div>
  <div class="p-6 bg-red-100 dark:bg-red-900 rounded-lg">
    <strong>👥 Share with teams</strong> - Version-controlled rules ensure consistency
  </div>
</div>

<!-- Remember: if AI gets it wrong, write a rule -->

---

# The Rules Mindset Shift

<div class="grid grid-cols-2 gap-12 mt-12">
<div>

## Before Rules ❌
- "AI is unpredictable"
- "I have to fix everything"
- "It never learns"
- "Inconsistent results"
- "Can't trust AI output"

</div>
<div>

## After Rules ✅  
- "AI follows my guidelines"
- "It handles edge cases I taught it"
- "Consistent quality every time"
- "Scales across my entire team"
- "AI amplifies my expertise"

</div>
</div>

<div class="text-center mt-8 text-xl">
<strong>Don't give up on AI - give it rules</strong>
</div>

<!-- The transformation is dramatic when you provide structure -->

---
layout: center
class: text-center
---

# Resources & Next Steps

- **Cursor Rules:** [cursor.com/docs/context/rules](https://cursor.com/docs/context/rules)
- **Claude Code:** [docs.anthropic.com/claude-code](https://docs.anthropic.com/claude-code) 
- **GitHub Copilot:** [code.visualstudio.com/docs/copilot/customization](https://code.visualstudio.com/docs/copilot/customization)
- **AGENTS.md Examples:** Community repos and documentation

<div class="mt-8">
<strong>Start building your rules today!</strong>
</div>

---
layout: end
class: text-center
---

# Thank You!

<div class="text-4xl mb-8">🙏</div>

**Questions?**

Brian Perry | @brianperry.dev  
Actual AI | Building AI Guardrails

<div class="mt-8 text-sm opacity-75">
Built with Claude Code + Slidev + Rules
</div>

<!-- This deck itself was created using the principles we discussed -->