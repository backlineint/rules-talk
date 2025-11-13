---
theme: seriph
background: https://cover.sli.dev
title: Unlocking the Power of Agent-Driven Development with Rules
info: |
  ## Unlocking the Power of Agent-Driven Development with Rules
  
  The effectiveness of AI coding agents has grown exponentially in the past year. Yet many developers struggle to see the benefits they expect. In this session, we'll explore one of the overlooked keys to making coding agents truly effective: rules.

class: text-center
transition: slide-left
mdc: true
duration: 35min
---

# Unlocking the Power of Agent-Driven Development with Rules

**From Frustration to Flow: How Rules Transform AI Coding Assistants**

<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-op-10">
    Press Space for next slide <carbon:arrow-right class="inline"/>
  </span>
</div>

<!--
Welcome everyone. Today we're going to talk about something that's transformed how I work with AI coding assistants - and I think it can do the same for you.
-->

---
layout: image-right
image: ./resources/images/brian-perry.jpg
---

# About Me

## Brian Perry
**Founding Engineer at Actual AI**

- 🏡 Chicago suburbs
- 🎮 Nintendo enthusiast  
- 🔗 Bluesky: [@brianperry.dev](https://bsky.app/profile/brianperry.dev)
- 🐙 GitHub: [@backlineint](https://github.com/backlineint)

Building tools to provide guardrails for AI-enabled software teams

<!--
Quick intro - I'm Brian Perry, founding engineer at Actual AI. We're building tools to help software teams work more effectively with AI. I live in the Chicago suburbs and yes, I'm a big Nintendo fan.
-->

---

# Claude Code: Co-Author of This Talk

- 🤖 Claude Code helped draft content, iterate on demos, and tighten language
- 📝 `CLAUDE.md` keeps Claude Code aligned with the story arc  
- ✨ Today's deck is proof that rules + agents co-create real work

<div class="mt-8 text-center text-sm opacity-75">
This presentation itself demonstrates the power of rules-driven development
</div>

<!--
I want to be transparent - Claude Code co-authored this talk. It helped draft content, iterate on demos, and refine the language. The CLAUDE.md file in our repo keeps Claude aligned with our story arc. This presentation itself is proof that when you combine rules with AI agents, you can create real, valuable work together.
-->

---
layout: image-right
image: ./resources/images/junior_dev2.jpeg
---

# The Problem

Everyone has experienced AI making mistakes

**Common advice:** *"Think of AI as a Junior Developer"*

**Personal reflection:** I graduated in 2002 - thinking of me 23 years ago is horrifying 😱

<!--
We've all been there. You're working with an AI coding assistant, and it makes a mistake. Maybe it uses the wrong framework, ignores your coding standards, or just does something completely unexpected.

The common advice is to think of AI as a junior developer. But here's the thing - I graduated college in 2002. When I think about myself as a junior developer 23 years ago, it's honestly horrifying.
-->

---

# What Junior Developers Need

<div class="grid grid-cols-2 gap-8 mt-8">

<div>

## What I Needed Back Then
- 👥 Mentors and guidance
- 📚 Clear documentation  
- 📋 Guidelines and standards
- 🔄 Trial and error with feedback
- 🎯 Structure and guardrails

</div>

<div v-click>

## What AI Agents Need
- 👥 ~~Mentors and guidance~~ **Rules**
- 📚 ~~Clear documentation~~ **Rules**  
- 📋 ~~Guidelines and standards~~ **Rules**
- 🔄 ~~Trial and error~~ **Rules**
- 🎯 ~~Structure and guardrails~~ **Rules**

</div>

</div>

<div v-click class="mt-8 text-center">

### **Coding agents need the same thing junior developers do**

</div>

<!--
What did I need as a junior developer? Mentors, documentation, guidelines, lots of trial and error, and most importantly - structure and guardrails.

Coding agents need exactly the same things. And the way we provide that structure is through rules.
-->

---

# Why Rules Matter

<div class="grid grid-cols-1 gap-6 mt-8">

<div v-click="1">

## What Are Rules?
📝 **Reusable, scoped instructions that control agent behavior**

</div>

<div v-click="2">

## They Provide Structure
🎯 **Clear guardrails and expectations**

</div>

<div v-click="3">

## They Enable Consistency  
🔄 **Predictable, repeatable outcomes**

</div>

</div>

<div v-click="4" class="mt-12 text-center">

### Rules are defined in your codebase as markdown files

</div>

<div v-click="5" class="mt-6 text-center text-xl font-bold text-blue-600">

**"If AI gets it wrong, don't give up - write a rule"**

</div>

<!--
So what exactly are rules? They're reusable, scoped instructions that control how your AI agent behaves. Think of them as the documentation, guidelines, and mentorship that a junior developer would need, but written in a way that AI can consistently follow.

Rules provide structure and guardrails. They enable consistency and predictable outcomes. And here's the key insight: if AI gets it wrong, don't give up - write a rule.
-->

---

# Rules Formats Across Tools

<div class="grid grid-cols-2 gap-8 mt-4">

<div>

## Cursor
```markdown
# .cursorrules

You are an expert in TypeScript and React.

Follow these rules:
- Use functional components
- Prefer named exports
- Use TypeScript strict mode
```

</div>

<div>

## Claude Code
```markdown
# CLAUDE.md

## Project Guidelines
- Use React with TypeScript
- Follow existing patterns
- Write tests for new features
```

</div>

</div>

<div class="mt-6">

## GitHub Copilot
```markdown
# .github/copilot-instructions.md

Coding standards:
- Use ES6+ features
- Follow company style guide
- Include error handling
```

</div>

<!--
Different AI coding tools use different formats for rules. Cursor uses .cursorrules files, Claude Code looks for CLAUDE.md, and GitHub Copilot can use copilot-instructions.md files. But the concept is the same across all of them - you're providing structured guidance to the AI.
-->

---
layout: two-cols
---

# Rules in Action: Before

```typescript
// AI generates this without rules
function processData(data) {
  const result = [];
  for (let i = 0; i < data.length; i++) {
    if (data[i] != null) {
      result.push(data[i].toUpperCase());
    }
  }
  return result;
}
```

**Problems:**
- No TypeScript types
- Imperative style  
- Loose equality check
- No error handling

::right::

# Rules in Action: After

```typescript
// AI generates this WITH rules
export const processData = (
  data: string[]
): string[] => {
  return data
    .filter((item): item is string => 
      item !== null && item !== undefined
    )
    .map(item => item.toUpperCase());
};
```

**Improvements:**
- ✅ Proper TypeScript types
- ✅ Functional approach
- ✅ Strict equality
- ✅ Type guards

<!--
Here's a concrete example. Without rules, AI might generate imperative JavaScript with loose equality and no types. But with proper rules in place, it generates clean, functional TypeScript that follows your team's conventions.
-->

---

# Building a Rules-Driven Workflow

<div class="grid grid-cols-3 gap-6 mt-8">

<div v-click="1">

## 1. Start Small
- Begin with basic coding standards
- Add language-specific rules
- Document common patterns

</div>

<div v-click="2">

## 2. Iterate Based on Mistakes
- When AI gets it wrong, analyze why
- Write a rule to prevent it
- Test the rule with similar scenarios

</div>

<div v-click="3">

## 3. Share and Scale
- Team-wide rule repositories
- Project-specific guidelines
- Onboarding new developers

</div>

</div>

<div v-click="4" class="mt-12 text-center bg-blue-50 p-6 rounded-lg">

**The goal isn't perfection on day one - it's continuous improvement through rules**

</div>

<!--
Building a rules-driven workflow is iterative. Start small with basic coding standards. When the AI makes mistakes, don't just fix them - write rules to prevent them in the future. Then share those rules across your team so everyone benefits.
-->

---

# Rule Categories

<div class="grid grid-cols-2 gap-8 mt-6">

<div>

## Technical Rules
- **Framework choices:** React vs Vue
- **Language features:** TypeScript strict mode  
- **Architecture patterns:** Clean architecture
- **Testing approaches:** Jest + React Testing Library

</div>

<div>

## Team Rules  
- **Code style:** Prettier + ESLint configs
- **Naming conventions:** camelCase, PascalCase
- **File structure:** Feature-based organization
- **Documentation:** JSDoc requirements

</div>

</div>

<div class="mt-8">

## Business Rules
- **Domain logic:** User permissions, validation
- **Integration patterns:** API client usage  
- **Security requirements:** Authentication flows
- **Performance standards:** Core Web Vitals

</div>

<!--
Rules fall into three main categories. Technical rules cover your technology choices and architectural decisions. Team rules ensure consistency in style and organization. Business rules capture your domain logic and requirements.
-->

---

# Live Demo: Rules in Action

<div class="mt-8 text-center">

## Let's see rules transform AI coding in real-time

</div>

<div class="grid grid-cols-2 gap-8 mt-12">

<div>

### What We'll Demonstrate
- 🚫 AI without rules (chaos)
- ✅ AI with rules (consistency)  
- 🔄 Iterating rules based on feedback
- 📈 Measuring the improvement

</div>

<div>

### Demo Scenario
**Task:** Build a user profile component

**Without Rules:** Generic, inconsistent code

**With Rules:** Follows team patterns, uses correct libraries, proper TypeScript

</div>

</div>

<!--
Now let's see this in action. I'm going to demonstrate how the same AI agent behaves dramatically differently when we provide it with proper rules versus letting it work without guidance.
-->

---

# Measuring Rules Effectiveness

<div class="grid grid-cols-3 gap-6 mt-8">

<div v-click="1">

## Code Quality
- Fewer linting errors
- Better type coverage
- Consistent patterns
- Reduced code review cycles

</div>

<div v-click="2">

## Developer Experience  
- Less manual correction
- Faster onboarding
- Shared understanding
- Reduced context switching

</div>

<div v-click="3">

## Team Productivity
- Consistent codebase
- Faster feature delivery
- Fewer bugs in production
- Knowledge sharing

</div>

</div>

<div v-click="4" class="mt-12 text-center">

### **Rules don't just improve AI - they improve your entire development workflow**

</div>

<!--
The benefits of rules extend far beyond just making AI better. You'll see improvements in code quality, developer experience, and overall team productivity. Rules create a shared language between humans and AI.
-->

---

# Advanced Rules Techniques

<div class="grid grid-cols-2 gap-8 mt-6">

<div>

## Context-Aware Rules
```markdown
# For React components
When creating components:
- Use TypeScript interfaces for props
- Include proper accessibility attributes
- Add error boundaries for complex components

# For API routes  
When creating API endpoints:
- Validate input with Zod schemas
- Include proper error handling
- Add rate limiting
```

</div>

<div>

## Dynamic Rules
```markdown
# Environment-specific
In development:
- Include debug logs
- Use development API endpoints
- Enable hot reloading

In production:
- Remove all console.logs
- Use production API endpoints  
- Optimize for performance
```

</div>

</div>

<!--
As you get more sophisticated, you can create context-aware rules that apply different guidelines based on what you're building, and dynamic rules that change based on your environment or other conditions.
-->

---

# Common Pitfalls to Avoid

<div class="grid grid-cols-2 gap-8 mt-8">

<div>

## ❌ What NOT to Do
- Rules that are too vague
- Conflicting rules  
- Rules that change constantly
- Overly restrictive rules
- Rules without examples

</div>

<div>

## ✅ Best Practices
- Be specific and actionable
- Provide clear examples
- Test rules with edge cases
- Version your rules
- Regular rule reviews

</div>

</div>

<div class="mt-8 bg-yellow-50 p-6 rounded-lg">

**Remember:** Rules should enable creativity, not constrain it

</div>

<!--
There are some common mistakes to avoid. Don't make rules too vague or conflicting. But also don't make them so restrictive that they stifle creativity. The best rules provide clear guidance while still allowing for innovation.
-->

---

# Getting Started Today

<div class="grid grid-cols-1 gap-6 mt-8">

<div v-click="1" class="bg-blue-50 p-6 rounded-lg">

## Step 1: Choose Your Tool
Pick your AI coding assistant and learn its rules format

</div>

<div v-click="2" class="bg-green-50 p-6 rounded-lg">

## Step 2: Start with Basics  
Write 3-5 fundamental rules for your codebase

</div>

<div v-click="3" class="bg-purple-50 p-6 rounded-lg">

## Step 3: Iterate and Improve
When AI makes mistakes, write rules to prevent them

</div>

<div v-click="4" class="bg-orange-50 p-6 rounded-lg">

## Step 4: Share and Scale
Get your team using the same rules

</div>

</div>

<!--
Here's how to get started today. Choose your tool, write a few basic rules, then iterate as you encounter problems. Most importantly, get your whole team involved so everyone benefits.
-->

---

# Tools and Resources

<div class="grid grid-cols-2 gap-8 mt-8">

<div>

## Recommended Tools
- **Cursor:** `.cursorrules` files
- **Claude Code:** `CLAUDE.md` files  
- **GitHub Copilot:** Copilot instructions
- **Actual AI:** Advanced rule management (coming soon!)

</div>

<div>

## Resources
- **Documentation:** Tool-specific rule formats
- **Templates:** Starter rule sets
- **Community:** Share rules with others
- **Examples:** Real-world rule implementations

</div>

</div>

<div class="mt-8 text-center">

### 🔗 **Find example rules and templates at:** [github.com/backlineint/rules-examples](https://github.com/backlineint/rules-examples)

</div>

<!--
Here are the tools I recommend and resources to help you get started. I've put together a GitHub repo with example rules and templates you can use as a starting point.
-->

---
layout: center
class: text-center
---

# Key Takeaways

<div class="grid grid-cols-1 gap-6 mt-12">

<div class="text-xl">
🎯 **Rules are critical to successful agent-driven development**
</div>

<div class="text-xl">
📝 **Start small, iterate based on AI mistakes**  
</div>

<div class="text-xl">
🔄 **Different tools, same concept - provide structure**
</div>

<div class="text-xl">
🚀 **Rules don't just improve AI - they improve your entire workflow**
</div>

</div>

<div class="mt-16 text-2xl font-bold text-blue-600">
**If AI gets it wrong, don't give up - write a rule**
</div>

<!--
Let's wrap up with the key takeaways. Rules are absolutely critical for successful AI-driven development. Start small and iterate. The concept works across all tools. And remember - rules improve your entire workflow, not just the AI.
-->

---
layout: center
class: text-center
---

# Thank You!

## Questions & Discussion

<div class="mt-12 space-y-6">

<div>
🐙 **GitHub:** [@backlineint](https://github.com/backlineint)
</div>

<div>
🔗 **Bluesky:** [@brianperry.dev](https://bsky.app/profile/brianperry.dev)
</div>

<div>
🏢 **Actual AI:** Building guardrails for AI-enabled teams
</div>

</div>

<div class="mt-16 text-lg">
**Let's make AI coding assistants work better for everyone**
</div>

<!--
Thank you! I'd love to hear your questions and discuss your experiences with AI coding assistants. Let's figure out how to make these tools work better for everyone.
-->