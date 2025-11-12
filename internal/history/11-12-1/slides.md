---
theme: seriph
background: https://images.unsplash.com/photo-1516116216624-53e697fedbea?q=80&w=2128&auto=format&fit=crop
title: Unlocking the Power of Agent-Driven Development with Rules
info: |
  ## Unlocking the Power of Agent-Driven Development with Rules
  A presentation about making AI coding agents truly effective through rules.
class: text-center
drawings:
  persist: false
transition: slide-left
mdc: true
duration: 45min
---

# Unlocking the Power of Agent-Driven Development with Rules

Making AI Coding Agents Truly Effective

<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer" hover:bg="white op-10">
    Press Space for next page <carbon:arrow-right class="inline"/>
  </span>
</div>

<!--
Welcome to my talk on unlocking the power of agent-driven development with rules. This is about making AI coding agents truly effective in your daily workflow.
-->

---
layout: intro
---

# Brian Perry

<div class="leading-8 opacity-80">
Founding Engineer at Actual AI<br>
Lives in the Chicago suburbs<br>
Nintendo enthusiast<br>
Once a skeptic, now relies on agent-driven development
</div>

<div class="my-10 grid grid-cols-[40px,1fr] w-min gap-y-4">
  <carbon:logo-github class="opacity-50"/>
  <div><a href="https://github.com/brianperry" target="_blank">brianperry</a></div>
  <carbon:logo-x class="opacity-50"/>
  <div><a href="https://twitter.com/brianlperry" target="_blank">brianlperry</a></div>
</div>

<!--
Let me introduce myself. I'm Brian Perry, a founding engineer at Actual AI. I live in the Chicago suburbs and I'm a huge Nintendo fan. 

What's important about my background is that I was once a skeptic of AI coding tools. But now, agent-driven development has become a cornerstone of my daily workflow.
-->

---
layout: center
---

## Cursor: Co-Author of This Talk

<v-click>

- Cursor helped draft content, iterate on demos, and tighten language
- `.cursor/rules` keeps Cursor aligned with the story arc
- Today's deck is proof that rules + agents co-create real work

</v-click>

<!--
Before we dive in, I want to acknowledge that Cursor was actually a co-author of this talk. Cursor helped me draft content, iterate on demos, and tighten the language throughout.

The .cursor/rules file kept Cursor aligned with my story arc and vision. This presentation itself is proof that rules plus agents can co-create real work together.
-->

---
layout: fact
---

# The Problem

Many developers struggle to see benefits from AI coding agents... **or abandon them altogether**

<!--
Here's the core problem we're addressing today. Despite the incredible advances in AI coding agents, many developers still struggle to see the benefits they expect, or they abandon these tools altogether after initial disappointment.
-->

---
layout: quote
---

> "Think of your AI assistant as your **best junior developer** - capable and tireless, but in need of **clear guardrails**."

<!--
Here's how I like to think about it: imagine your AI assistant as your best junior developer. They're incredibly capable and never get tired, but they need clear guardrails to be successful.
-->

---

# Why Agents Fail Without Rules

<v-clicks>

- **Lack of Context**: Agent doesn't understand your project's conventions
- **Inconsistent Output**: Different results for similar requests
- **Scope Creep**: Agent makes changes beyond what was asked
- **Tool Confusion**: Doesn't know which tools or libraries to use
- **Style Mismatch**: Code doesn't fit your team's patterns

</v-clicks>

<!--
Let's talk about why agents fail without rules:

First, lack of context - the agent doesn't understand your project's specific conventions.

Inconsistent output - you get different results for similar requests.

Scope creep - the agent makes changes beyond what you actually asked for.

Tool confusion - it doesn't know which tools or libraries your project uses.

And style mismatch - the code doesn't fit your team's established patterns.
-->

---
layout: center
---

# The Solution: Rules

Rules provide **structure** that allows agents to succeed

<div class="text-center mt-8">
  <span class="text-6xl">📋</span>
</div>

If AI gets it wrong, **don't give up** - write a rule

<!--
The solution is rules. Rules provide the structure that allows agents to succeed.

And here's my key message: if AI gets it wrong, don't give up - write a rule.
-->

---

# What Are Rules?

<v-clicks>

- **Reusable instructions** that control agent behavior
- **Scoped guidance** for specific contexts or projects  
- **Living documentation** that evolves with your project
- **Team knowledge** captured in a shareable format

</v-clicks>

<v-click>

<div class="mt-8 p-4 bg-blue-50 rounded">
<strong>Example:</strong> "Always use TypeScript interfaces instead of types when defining object shapes"
</div>

</v-click>

<!--
So what are rules exactly?

They're reusable instructions that control how the agent behaves.

They provide scoped guidance for specific contexts or projects.

They act as living documentation that evolves with your project.

And they capture team knowledge in a shareable format.

For example: "Always use TypeScript interfaces instead of types when defining object shapes" - this is a clear, actionable rule that ensures consistency.
-->

---
layout: two-cols
layoutClass: gap-16
---

# Rules Formats Across Tools

Different tools, similar concepts

::right::

<v-clicks>

## Cursor
```
.cursor/rules
```

## Claude Code  
```
CLAUDE.md
```

## GitHub Codex
```
.cursorrules
```

## Agents.md
```
agents.md
```

</v-clicks>

<!--
Different AI coding tools use similar concepts but different file formats for rules.

Cursor uses .cursor/rules files.

Claude Code uses CLAUDE.md.

GitHub Codex uses .cursorrules.

And there's also the Agents.md format for broader agent instructions.

The key is that they all serve the same fundamental purpose - giving your AI assistant clear guidance.
-->

---

# Cursor Rules Example

```markdown
You are an expert frontend developer focused on React and TypeScript.

## Project Context
- This is a Next.js 14 project using the app router
- We use Tailwind CSS for styling
- All components should be functional components with TypeScript

## Code Style
- Use arrow functions for components
- Prefer const assertions for literal types
- Always destructure props at the top of components
- Use meaningful variable names

## File Organization
- Components go in /components with PascalCase naming
- Utilities go in /lib with camelCase naming
- Types go in /types with PascalCase naming

## Testing
- Write unit tests for all utility functions
- Use React Testing Library for component tests
- Test files should be named ComponentName.test.tsx
```

<!--
Here's an example of what Cursor rules look like. You can see we're defining the context - this is a Next.js 14 project. We specify code style preferences like using arrow functions and destructuring props. We explain file organization patterns. And we even include testing requirements.

This gives Cursor a comprehensive understanding of how to work within this specific project.
-->

---

# Claude Code CLAUDE.md Example

```markdown
# Project Guidelines

You are working on a Python data analysis project.

## Dependencies
- Use pandas for data manipulation
- Use matplotlib/seaborn for visualizations  
- Use pytest for testing

## Code Style
- Follow PEP 8 conventions
- Use type hints for all functions
- Include docstrings for public functions
- Prefer list comprehensions over loops when readable

## Data Handling
- Always validate input data before processing
- Use descriptive column names
- Handle missing values explicitly
- Save intermediate results to cache/

## Error Handling
- Use specific exception types
- Include helpful error messages
- Log errors to logs/error.log
```

<!--
Here's an example of a CLAUDE.md file for a Python data analysis project. You can see similar patterns - we specify dependencies, code style, specific domain knowledge like data handling practices, and error handling approaches.

The key is being specific about your project's needs and conventions.
-->

---
layout: two-cols
layoutClass: gap-8
---

# Rule Categories

<v-clicks>

## Technical Rules
- Language/framework preferences
- Library and tool choices
- Architecture patterns
- Code style conventions

## Process Rules  
- Testing requirements
- Documentation standards
- Deployment procedures
- Review processes

</v-clicks>

::right::

<v-clicks>

## Domain Rules
- Business logic constraints
- Data handling requirements
- Security considerations
- Performance guidelines

## Team Rules
- Communication standards
- File organization
- Naming conventions
- Collaboration patterns

</v-clicks>

<!--
Let me break down the different categories of rules you should consider:

Technical rules cover language preferences, library choices, architecture patterns, and code style.

Process rules define testing requirements, documentation standards, and deployment procedures.

Domain rules capture business logic constraints, data handling requirements, and security considerations.

And team rules establish communication standards, file organization, and collaboration patterns.

The goal is to create a comprehensive set of guardrails that guide your AI assistant in every aspect of development.
-->

---

# Writing Effective Rules

<v-clicks>

## Be Specific
❌ "Write good code"  
✅ "Use semantic HTML5 elements and ARIA labels for accessibility"

## Provide Context
❌ "Use TypeScript"  
✅ "Use TypeScript with strict mode enabled. Prefer interfaces for object types."

## Include Examples
❌ "Follow naming conventions"  
✅ "Use PascalCase for components (UserProfile.tsx) and camelCase for utilities (formatDate.ts)"

## Make Rules Actionable
❌ "Consider performance"  
✅ "Lazy load components that are below the fold using React.lazy()"

</v-clicks>

<!--
Here are the key principles for writing effective rules:

Be specific - instead of "write good code", say "use semantic HTML5 elements and ARIA labels for accessibility"

Provide context - don't just say "use TypeScript", explain "use TypeScript with strict mode enabled and prefer interfaces for object types"

Include examples - show exactly what you mean with concrete file names and patterns

Make rules actionable - instead of "consider performance", give specific guidance like "lazy load components below the fold using React.lazy"
-->

---
layout: center
---

# Building a Rules-Driven Workflow

<div class="grid grid-cols-3 gap-8 mt-8">
  <div class="text-center">
    <div class="text-4xl mb-4">🎯</div>
    <h3>Start Small</h3>
    <p class="text-sm opacity-80">Begin with 3-5 core rules</p>
  </div>
  
  <div class="text-center">
    <div class="text-4xl mb-4">🔄</div>
    <h3>Iterate</h3>
    <p class="text-sm opacity-80">Add rules when patterns emerge</p>
  </div>
  
  <div class="text-center">
    <div class="text-4xl mb-4">🤝</div>
    <h3>Share</h3>
    <p class="text-sm opacity-80">Make rules team knowledge</p>
  </div>
</div>

<!--
Building a rules-driven workflow has three key phases:

Start small - begin with just 3-5 core rules that address your biggest pain points.

Iterate - add new rules when you notice patterns in the agent's mistakes or when new requirements emerge.

Share - make rules team knowledge so everyone benefits from the collective wisdom.
-->

---

# Demo: Rules in Action

<div class="grid grid-cols-2 gap-8">
  <div>
    <h3>Before Rules</h3>
    <div class="bg-red-50 p-4 rounded text-sm">
      <pre><code>// Generic React component
function UserCard(props) {
  return (
    &lt;div style={{padding: "20px"}}&gt;
      &lt;h2&gt;{props.name}&lt;/h2&gt;
      &lt;p&gt;{props.email}&lt;/p&gt;
    &lt;/div&gt;
  );
}</code></pre>
    </div>
  </div>
  
  <div>
    <h3>After Rules</h3>
    <div class="bg-green-50 p-4 rounded text-sm">
      <pre><code>// Following project conventions
interface UserCardProps {
  name: string;
  email: string;
}

export const UserCard: React.FC&lt;UserCardProps&gt; = ({ 
  name, 
  email 
}) =&gt; {
  return (
    &lt;div className="p-5 border rounded-lg"&gt;
      &lt;h2 className="text-xl font-semibold"&gt;{name}&lt;/h2&gt;
      &lt;p className="text-gray-600"&gt;{email}&lt;/p&gt;
    &lt;/div&gt;
  );
};</code></pre>
    </div>
  </div>
</div>

<!--
Here's a concrete example of rules in action. On the left, you see what an AI might generate without rules - generic React with inline styles and loose typing.

On the right, you see the same component after establishing rules - proper TypeScript interfaces, arrow function syntax, Tailwind classes, and consistent destructuring patterns.

The difference is dramatic and this consistency compounds across your entire codebase.
-->

---

# Advanced Rule Strategies

<v-clicks>

## Conditional Rules
```markdown
When working on /api routes:
- Always validate input with Zod schemas
- Return proper HTTP status codes
- Include error handling middleware
```

## Contextual Rules
```markdown
For database migrations:
- Always include rollback scripts
- Test on staging environment first
- Document breaking changes in CHANGELOG.md
```

## Progressive Rules
```markdown
Level 1: Basic TypeScript usage
Level 2: Advanced type patterns  
Level 3: Custom utility types
```

</v-clicks>

<!--
As you get more sophisticated, you can use advanced rule strategies:

Conditional rules that apply only in certain contexts - like specific validation requirements for API routes.

Contextual rules for particular workflows - like database migration procedures that include rollback scripts and staging tests.

Progressive rules that build up complexity over time - starting with basic TypeScript and advancing to custom utility types.
-->

---
layout: quote
---

# "Rules are not constraints - they're **enablers** that unlock agent potential"

<!--
I want to emphasize this key point: rules are not constraints that limit what your AI can do. They're enablers that unlock the full potential of your agents by giving them the context they need to be truly helpful.
-->

---

# Measuring Success

<div class="grid grid-cols-2 gap-8 mt-8">
  
<v-click>
<div>
<h3>Quantitative Metrics</h3>
<ul class="space-y-2">
  <li>📊 Reduced code review iterations</li>
  <li>⚡ Faster feature development</li>
  <li>🐛 Fewer bugs in production</li>
  <li>🔄 Less rework required</li>
</ul>
</div>
</v-click>

<v-click>
<div>
<h3>Qualitative Indicators</h3>
<ul class="space-y-2">
  <li>✨ Code feels more consistent</li>
  <li>🎯 Agent suggestions are more relevant</li>
  <li>😌 Less frustration with AI tools</li>
  <li>🚀 Team adopts AI more readily</li>
</ul>
</div>
</v-click>

</div>

<!--
How do you know if your rules are working?

Quantitatively, you should see reduced code review iterations, faster feature development, fewer production bugs, and less rework.

Qualitatively, the code should feel more consistent, agent suggestions become more relevant, there's less frustration with AI tools, and your team adopts AI more readily.
-->

---

# Common Pitfalls

<v-clicks>

## Too Many Rules at Once
- Start with 3-5 core rules
- Add gradually based on actual pain points

## Rules Too Vague  
- "Write clean code" → "Use descriptive variable names (getUserById, not getUser)"

## Conflicting Rules
- Review rules periodically for contradictions
- Prioritize rules when conflicts arise

## Not Updating Rules
- Rules should evolve with your project
- Remove outdated rules regularly

</v-clicks>

<!--
Let me share some common pitfalls to avoid:

Don't try to create too many rules at once - start with 3-5 core rules and add gradually.

Avoid vague rules - be specific about what you want instead of generic guidance.

Watch for conflicting rules - review them periodically and establish priorities when conflicts arise.

And don't forget to update rules as your project evolves - remove outdated guidance regularly.
-->

---
layout: two-cols
layoutClass: gap-16
---

# Tools and Resources

## Rule Formats
- [Cursor Documentation](https://cursor.com/docs/context/rules)
- [Claude Code CLAUDE.md](https://docs.anthropic.com/en/docs/claude-code)
- [Agents.md Specification](https://github.com/agents-md/agents.md)

## Community
- Share rules on GitHub
- Learn from others' rule sets
- Contribute to open source rule libraries

::right::

## Getting Started
```bash
# Create your first rules file
touch .cursor/rules
# or
touch CLAUDE.md
# or  
touch agents.md

# Start with project basics
echo "You are working on a [framework] project..." >> .cursor/rules
```

## Backlog.md
- Experimental tool for rule-driven backlogs
- Combines project management with AI guidance
- Live demo coming up!

<!--
Here are some tools and resources to help you get started:

Check out the documentation for different rule formats - Cursor, Claude Code, and Agents.md.

Engage with the community by sharing your rules on GitHub and learning from others.

To get started, just create your first rules file and begin with project basics.

I also want to mention backlog.md - an experimental tool that combines project management with AI guidance through rules. We'll see this in action in the demo.
-->

---
layout: center
---

# Live Demo

## Building a Feature with Rules

Let's see agent-driven development in action

<div class="mt-8 text-sm opacity-70">
Demo: Creating a user authentication system with rules-guided development
</div>

<!--
Now let's see this all in action. I'm going to do a live demo where we build a user authentication system using rules-guided development. You'll see how the rules shape the agent's behavior and output in real-time.
-->

---

# Key Takeaways

<v-clicks>

## 1. Rules Transform Agent Effectiveness
From generic output to project-specific, high-quality code

## 2. Start Simple, Iterate Often  
Begin with 3-5 core rules, add based on real pain points

## 3. Be Specific and Actionable
Vague rules lead to inconsistent results

## 4. Rules Enable, Don't Constrain
They unlock agent potential by providing context

## 5. Make Rules Team Knowledge
Share and evolve rules across your organization

</v-clicks>

<!--
Let me leave you with the key takeaways:

Rules transform agent effectiveness from generic output to project-specific, high-quality code.

Start simple and iterate often - begin with just a few core rules.

Be specific and actionable in your rule writing.

Remember that rules enable rather than constrain - they unlock potential.

And make rules team knowledge that everyone can benefit from.
-->

---
layout: center
---

# The Future is Rules-Driven

<div class="mt-8 text-lg opacity-80">
AI agents + Clear rules = Unstoppable development teams
</div>

<div class="mt-12">
  <h3>Questions?</h3>
</div>

<!--
The future of software development is rules-driven. When you combine AI agents with clear rules, you create unstoppable development teams.

Now I'd love to take your questions.
-->

---
layout: center
---

# Thank You

<div class="grid grid-cols-1 gap-4 mt-8 text-center">
  <div>🐦 @brianlperry</div>
  <div>💼 Actual AI</div>
  <div>🚀 Let's build the future together</div>
</div>

<div class="mt-12 text-sm opacity-60">
Slides created with rules-guided development ✨
</div>

<!--
Thank you for your time today. Remember - if AI gets it wrong, don't give up, write a rule.

Let's build the future together.
-->