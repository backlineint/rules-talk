---
theme: default
background: https://source.unsplash.com/1920x1080/?abstract,technology
title: Unlocking the Power of Agent-Driven Development with Rules
info: |
  ## Unlocking the Power of Agent-Driven Development with Rules
  Presentation on using rules to make AI coding agents more effective
class: text-center
highlighter: shiki
drawings:
  persist: false
transition: slide-left
mdc: true
duration: 35min
---

# Unlocking the Power of Agent-Driven Development with Rules

Transform Your AI Assistant from Chaos to Consistency

<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    Press Space for next page <carbon:arrow-right class="inline"/>
  </span>
</div>

<div class="abs-br m-6 flex gap-2">
  <a href="https://github.com/backlineint" target="_blank" alt="GitHub"
    class="text-xl slidev-icon-btn opacity-50 !border-none !hover:text-white">
    <carbon-logo-github />
  </a>
</div>

<!--
Today we're going to explore one of the most overlooked aspects of AI coding assistance - rules. If you've ever felt frustrated with inconsistent AI suggestions or found yourself repeatedly correcting the same mistakes, this talk is for you.
-->

---
layout: image-right
image: ./resources/images/junior_dev2.jpeg
---

# About Me

**Brian Perry**
- Founding Engineer at Actual AI
- Chicago suburbs resident
- Nintendo enthusiast
- Building guardrails for AI-enabled teams

<div class="mt-8">
  <div class="flex items-center gap-2 mb-2">
    <carbon-logo-github class="text-blue-400" />
    <span>github.com/backlineint</span>
  </div>
  <div class="flex items-center gap-2">
    <carbon-logo-twitter class="text-blue-400" />
    <span>bsky.app/profile/brianperry.dev</span>
  </div>
</div>

<!--
I'm Brian Perry, a founding engineer at Actual AI where we're building tools to provide guardrails for AI-enabled software teams. I live in the Chicago suburbs and in my free time, I love Nintendo games. I've been working with AI coding tools since their early days, and I've learned that the secret to success isn't just having powerful AI - it's having well-configured AI.
-->

---
layout: center
class: text-center
---

# Claude Code: Co-Author of This Talk

<div class="grid grid-cols-3 gap-8 items-center mt-8">
  <div class="text-left">
    <h3 class="text-lg font-bold mb-4">Content Creation</h3>
    <p class="text-sm">Helped draft slides, iterate on demos, and tighten language</p>
  </div>
  
  <div class="text-center">
    <div class="w-24 h-24 bg-orange-500 rounded-full mx-auto mb-4 flex items-center justify-center">
      <span class="text-white text-3xl font-bold">AI</span>
    </div>
  </div>
  
  <div class="text-right">
    <h3 class="text-lg font-bold mb-4">CLAUDE.md</h3>
    <p class="text-sm">Keeps Claude aligned with the story arc throughout development</p>
  </div>
</div>

<div class="mt-8 text-center">
  <p class="text-lg">Today's deck is proof that <span class="text-orange-500 font-bold">rules + agents</span> co-create real work</p>
</div>

<!--
Claude Code actually helped me create this presentation. It helped draft content, iterate on demos, and tighten the language. I used a CLAUDE.md file to keep Claude aligned with the story arc throughout our collaboration. This deck itself is proof that rules plus agents can co-create real work.
-->

---
layout: image-right
image: https://source.unsplash.com/800x600/?office,team
---

# Actual AI

<div class="space-y-4">
  <h2 class="text-2xl font-bold text-blue-500">Building Guardrails for AI Teams</h2>
  
  <div class="space-y-3">
    <div class="flex items-start gap-3">
      <carbon-shield-alt class="text-green-500 mt-1 flex-shrink-0" />
      <span>Policy enforcement for AI coding tools</span>
    </div>
    
    <div class="flex items-start gap-3">
      <carbon-analytics class="text-blue-500 mt-1 flex-shrink-0" />
      <span>Usage monitoring and insights</span>
    </div>
    
    <div class="flex items-start gap-3">
      <carbon-user-multiple class="text-purple-500 mt-1 flex-shrink-0" />
      <span>Team collaboration on AI workflows</span>
    </div>
  </div>
</div>

<!--
At Actual AI, we're building a set of tools to provide guardrails for AI-enabled software teams. We help with policy enforcement, usage monitoring, and team collaboration around AI workflows. Everything we've learned about making AI tools work effectively at scale has reinforced how critical rules are to success.
-->

---
layout: center
class: text-center
---

# The Problem

<div class="grid grid-cols-2 gap-12 mt-12">
  <div>
    <h3 class="text-xl font-bold mb-6 text-red-500">Everyone Has Experienced</h3>
    <div class="space-y-4">
      <div class="p-4 bg-red-50 rounded-lg text-red-800">AI suggesting wrong patterns</div>
      <div class="p-4 bg-red-50 rounded-lg text-red-800">Inconsistent code style</div>
      <div class="p-4 bg-red-50 rounded-lg text-red-800">Ignoring project conventions</div>
      <div class="p-4 bg-red-50 rounded-lg text-red-800">Repeating the same mistakes</div>
    </div>
  </div>
  
  <div>
    <h3 class="text-xl font-bold mb-6 text-blue-500">Common Advice</h3>
    <div class="p-6 bg-blue-50 rounded-lg text-blue-800">
      <p class="text-lg italic">"Think of AI as a Junior Developer"</p>
    </div>
  </div>
</div>

<!--
Everyone who's used AI coding tools has experienced this: the AI suggests the wrong patterns, produces inconsistent code style, ignores your project conventions, or keeps repeating the same mistakes. The common advice is to "think of AI as a junior developer."
-->

---
layout: center
class: text-center
---

# Personal Reflection

<div class="text-center space-y-8">
  <div class="text-6xl">🎓</div>
  
  <p class="text-2xl">I graduated in <span class="text-blue-500 font-bold">2002</span></p>
  
  <p class="text-xl text-gray-600">Thinking of me 23 years ago is <span class="text-red-500 font-bold">horrifying</span></p>
  
  <div class="mt-12 p-6 bg-yellow-50 rounded-lg">
    <h3 class="text-lg font-bold mb-4">What I needed back then:</h3>
    <div class="grid grid-cols-2 gap-4">
      <div>✓ Mentors</div>
      <div>✓ Guidelines</div>
      <div>✓ Documentation</div>
      <div>✓ Trial and error</div>
    </div>
  </div>
  
  <p class="text-xl font-bold text-green-600">Coding agents need the same thing</p>
</div>

<!--
I graduated college in 2002. Thinking of myself as a developer 23 years ago is honestly horrifying. What did I need back then? I needed mentors, guidelines, documentation, and lots of trial and error. Coding agents need exactly the same thing - and that's where rules come in.
-->

---
layout: center
class: text-center
---

# Why Rules Matter

<div class="space-y-8">
  <div class="text-center">
    <h2 class="text-3xl font-bold mb-6">What are Rules?</h2>
    
    <div class="grid grid-cols-1 gap-6 max-w-4xl mx-auto">
      <div class="p-6 bg-blue-50 rounded-lg flex items-center gap-4">
        <span class="text-3xl">📝</span>
        <span class="text-lg"><strong>Reusable, scoped instructions</strong> that control agent behavior</span>
      </div>
      
      <div class="p-6 bg-green-50 rounded-lg flex items-center gap-4">
        <span class="text-3xl">🎯</span>
        <span class="text-lg">They provide <strong>structure and guardrails</strong></span>
      </div>
      
      <div class="p-6 bg-purple-50 rounded-lg flex items-center gap-4">
        <span class="text-3xl">🔄</span>
        <span class="text-lg">They enable <strong>consistent, predictable outcomes</strong></span>
      </div>
    </div>
  </div>
</div>

<!--
So what are rules? Rules are reusable, scoped instructions that control agent behavior. They provide structure and guardrails, and they enable consistent, predictable outcomes. Think of them as the documentation and guidelines that turn a chaotic junior developer into a productive team member.
-->

---
layout: two-cols
layoutClass: gap-16
---

# Rules in Practice

<div class="space-y-4">
  <h3 class="text-lg font-bold">Rules are defined as markdown files in your codebase</h3>
  
  <div class="space-y-3">
    <div class="p-3 bg-gray-100 rounded font-mono text-sm">
      .cursorrules
    </div>
    <div class="p-3 bg-gray-100 rounded font-mono text-sm">
      CLAUDE.md
    </div>
    <div class="p-3 bg-gray-100 rounded font-mono text-sm">
      .github/copilot-instructions.md
    </div>
    <div class="p-3 bg-gray-100 rounded font-mono text-sm">
      AGENTS.md
    </div>
  </div>
</div>

::right::

<div class="space-y-6">
  <div class="p-4 bg-orange-50 rounded-lg border-l-4 border-orange-500">
    <p class="font-bold text-orange-700">Golden Rule</p>
    <p class="text-orange-800">"If AI gets it wrong, don't give up - write a rule"</p>
  </div>
  
  <div class="space-y-2">
    <p class="font-semibold">Benefits:</p>
    <ul class="space-y-1 text-sm">
      <li>• Persistent memory across sessions</li>
      <li>• Team knowledge sharing</li>
      <li>• Consistent code patterns</li>
      <li>• Reduced repetitive corrections</li>
    </ul>
  </div>
</div>

<!--
Rules are defined as markdown files in your codebase. Different tools use different file names, but they all serve the same purpose. My golden rule is: "If AI gets it wrong, don't give up - write a rule." Rules provide persistent memory across sessions, enable team knowledge sharing, ensure consistent code patterns, and reduce repetitive corrections.
-->

---
layout: center
class: text-center
---

# Understanding Rules Formats

<div class="grid grid-cols-2 gap-8 mt-8">
  <div class="space-y-6">
    <h3 class="text-xl font-bold text-blue-500">Tool-Specific Formats</h3>
    <div class="space-y-3">
      <div class="p-4 bg-blue-50 rounded-lg">
        <p class="font-bold">Cursor</p>
        <p class="text-sm text-gray-600">.cursorrules, .cursor/rules</p>
      </div>
      <div class="p-4 bg-green-50 rounded-lg">
        <p class="font-bold">Claude Code</p>
        <p class="text-sm text-gray-600">CLAUDE.md</p>
      </div>
      <div class="p-4 bg-purple-50 rounded-lg">
        <p class="font-bold">GitHub Copilot</p>
        <p class="text-sm text-gray-600">.github/copilot-instructions.md</p>
      </div>
    </div>
  </div>
  
  <div class="space-y-6">
    <h3 class="text-xl font-bold text-orange-500">Emerging Standard</h3>
    <div class="p-6 bg-orange-50 rounded-lg">
      <p class="text-2xl font-bold">AGENTS.md</p>
      <p class="text-sm text-gray-600 mt-2">Universal format supported by 20,000+ projects</p>
      <p class="text-sm text-gray-600">Backed by OpenAI, Google, Cursor, and others</p>
    </div>
  </div>
</div>

<!--
There are several rules formats to understand. On the left, we have tool-specific formats - Cursor uses .cursorrules files, Claude Code uses CLAUDE.md, and GitHub Copilot uses files in the .github directory. On the right, we have AGENTS.md - an emerging standard that's universal across tools and already used by over 20,000 projects, backed by companies like OpenAI, Google, and Cursor.
-->

---
layout: two-cols
layoutClass: gap-16
---

# Cursor Rules Format

```markdown
---
description: React component guidelines
globs: ["**/*.tsx", "**/*.jsx"]
alwaysApply: false
---

# React Guidelines

- Use functional components with hooks
- Prefer TypeScript for all new files
- Use absolute imports from @/
- Follow the existing component structure

## Naming Conventions
- Components: PascalCase
- Files: kebab-case
- Props: camelCase

## Error Handling
- Always wrap async operations in try-catch
- Use error boundaries for React errors
```

::right::

<div class="space-y-4">
  <h3 class="font-bold text-blue-500">Key Features</h3>
  <ul class="space-y-2 text-sm">
    <li>• <strong>Metadata support:</strong> description, globs, alwaysApply</li>
    <li>• <strong>File scoping:</strong> Apply rules to specific file patterns</li>
    <li>• <strong>Application modes:</strong> Always, intelligent, manual, or file-specific</li>
    <li>• <strong>Hierarchical:</strong> Rules can be nested in subdirectories</li>
  </ul>
  
  <h3 class="font-bold text-blue-500 mt-6">Best Practices</h3>
  <ul class="space-y-2 text-sm">
    <li>• Keep rules under 500 lines</li>
    <li>• Provide concrete examples</li>
    <li>• Split large rules into focused ones</li>
    <li>• Write like clear documentation</li>
  </ul>
</div>

<!--
Here's what Cursor rules look like. They support metadata like descriptions and file glob patterns. You can scope rules to specific files, set different application modes, and organize them hierarchically. Best practices include keeping rules under 500 lines, providing concrete examples, and writing them like clear documentation.
-->

---
layout: two-cols
layoutClass: gap-16
---

# GitHub Copilot Format

```markdown
# .github/copilot-instructions.md

You are a senior developer working on a Node.js 
Express API. Follow these guidelines:

## Code Style
- Use ES modules (import/export)
- Prefer async/await over promises
- Use TypeScript for type safety

## API Conventions
- All endpoints return JSON
- Use proper HTTP status codes
- Include error handling middleware

## Testing
- Write unit tests with Jest
- Integration tests for API endpoints
- Aim for 80%+ code coverage

## Dependencies
- Prefer built-in Node.js modules
- Use lodash sparingly
- Always validate input with joi
```

::right::

<div class="space-y-4">
  <h3 class="font-bold text-green-500">Configuration Options</h3>
  
  <div class="text-xs bg-gray-100 p-3 rounded font-mono">
settings.json
  </div>
  
  ```json
  {
    "github.copilot.chat.codeGeneration.instructions": [
      { "file": ".vscode/rules/style.md" }
    ],
    "github.copilot.chat.testGeneration.instructions": [
      { "file": ".vscode/rules/testing.md" }
    ]
  }
  ```
  
  <h3 class="font-bold text-green-500 mt-4">Features</h3>
  <ul class="space-y-2 text-sm">
    <li>• Repository-wide instructions</li>
    <li>• Path-specific rules</li>
    <li>• Task-specific guidance</li>
    <li>• VS Code integration</li>
  </ul>
</div>

<!--
GitHub Copilot uses a simpler format - just natural language Markdown in the .github/copilot-instructions.md file. You can also configure it through VS Code settings to use different instruction files for different tasks like code generation and testing. It supports repository-wide instructions, path-specific rules, and task-specific guidance.
-->

---
layout: two-cols
layoutClass: gap-16
---

# AGENTS.md - The Emerging Standard

```markdown
# AGENTS.md

## Project Overview
This is a React TypeScript project using Vite
and TailwindCSS.

## Development
- Run `npm run dev` to start development server
- Use `npm run build` to create production build
- Run `npm test` to execute test suite

## Code Conventions
- Components in PascalCase
- Use functional components with hooks
- Prefer composition over inheritance

## Testing
- Write unit tests for all components
- Integration tests for user flows
- Use React Testing Library

## File Structure
- Components: `/src/components/`
- Pages: `/src/pages/`
- Utils: `/src/utils/`
```

::right::

<div class="space-y-4">
  <h3 class="font-bold text-orange-500">Why AGENTS.md?</h3>
  <ul class="space-y-3 text-sm">
    <li>
      <div class="font-semibold">🌐 Universal</div>
      <div class="text-gray-600">Works with any AI coding tool</div>
    </li>
    <li>
      <div class="font-semibold">🏢 Industry Backed</div>
      <div class="text-gray-600">OpenAI, Google, Cursor, Factory</div>
    </li>
    <li>
      <div class="font-semibold">📈 Adoption</div>
      <div class="text-gray-600">20,000+ open source projects</div>
    </li>
    <li>
      <div class="font-semibold">📁 Simple</div>
      <div class="text-gray-600">Just standard Markdown</div>
    </li>
  </ul>
  
  <div class="mt-6 p-3 bg-orange-50 rounded-lg">
    <p class="text-sm font-semibold">Pro Tip:</p>
    <p class="text-xs">Large repos benefit from hierarchical AGENTS.md files in subdirectories</p>
  </div>
</div>

<!--
AGENTS.md is emerging as the universal standard. It's just standard Markdown, but it works with any AI coding tool. It has industry backing from OpenAI, Google, Cursor, and Factory, and it's already adopted by over 20,000 open source projects. The format is simple - just put the guidance your AI needs in a file called AGENTS.md in your project root. For large repos, you can have multiple AGENTS.md files in subdirectories.
-->

---
layout: center
class: text-center
---

# Building a Rules-Driven Workflow

<div class="grid grid-cols-3 gap-8 mt-12">
  <div class="space-y-4">
    <div class="w-16 h-16 bg-blue-500 rounded-full mx-auto flex items-center justify-center">
      <span class="text-white text-2xl">1</span>
    </div>
    <h3 class="font-bold text-blue-500">Start Small</h3>
    <p class="text-sm">Begin with basic coding standards and conventions</p>
  </div>
  
  <div class="space-y-4">
    <div class="w-16 h-16 bg-green-500 rounded-full mx-auto flex items-center justify-center">
      <span class="text-white text-2xl">2</span>
    </div>
    <h3 class="font-bold text-green-500">Iterate</h3>
    <p class="text-sm">Add rules when AI makes the same mistake twice</p>
  </div>
  
  <div class="space-y-4">
    <div class="w-16 h-16 bg-purple-500 rounded-full mx-auto flex items-center justify-center">
      <span class="text-white text-2xl">3</span>
    </div>
    <h3 class="font-bold text-purple-500">Scale</h3>
    <p class="text-sm">Share rules across teams and projects</p>
  </div>
</div>

<div class="mt-12 p-6 bg-gray-50 rounded-lg max-w-2xl mx-auto">
  <p class="font-semibold mb-2">Remember:</p>
  <p class="text-sm">Rules are living documents - update them as your project evolves</p>
</div>

<!--
Building a rules-driven workflow is straightforward. Start small with basic coding standards and conventions. Then iterate - every time AI makes the same mistake twice, add a rule to prevent it. Finally, scale by sharing rules across teams and projects. Remember that rules are living documents that should evolve with your project.
-->

---
layout: image-right
image: https://source.unsplash.com/800x600/?checklist,productivity
---

# Tooling: backlog.md

<div class="space-y-4">
  <p class="text-lg">Track AI-suggested improvements systematically</p>
  
  <div class="space-y-3">
    <div class="p-3 bg-blue-50 rounded-lg">
      <p class="font-bold text-blue-700">Capture Ideas</p>
      <p class="text-sm">Log AI suggestions for later review</p>
    </div>
    
    <div class="p-3 bg-green-50 rounded-lg">
      <p class="font-bold text-green-700">Prioritize</p>
      <p class="text-sm">Rank improvements by impact and effort</p>
    </div>
    
    <div class="p-3 bg-purple-50 rounded-lg">
      <p class="font-bold text-purple-700">Implement</p>
      <p class="text-sm">Turn validated suggestions into rules</p>
    </div>
  </div>
  
  <div class="mt-6 p-4 bg-yellow-50 rounded-lg border-l-4 border-yellow-500">
    <p class="text-sm font-semibold">Pro Tip:</p>
    <p class="text-sm">Use backlog.md to bridge the gap between AI suggestions and formalized rules</p>
  </div>
</div>

<!--
I want to introduce you to a simple but powerful concept: backlog.md. This is a file where you track AI-suggested improvements systematically. You capture ideas by logging AI suggestions for later review, prioritize them by impact and effort, and then implement the validated suggestions as formal rules. Think of backlog.md as the bridge between AI suggestions and formalized rules.
-->

---
layout: center
class: text-center
---

# Live Demo

<div class="space-y-8">
  <div class="text-6xl">🚀</div>
  
  <h2 class="text-3xl font-bold">Rules in Action</h2>
  
  <p class="text-lg text-gray-600">Let's see how rules transform AI behavior in real-time</p>
  
  <div class="grid grid-cols-3 gap-6 mt-8">
    <div class="p-4 bg-red-50 rounded-lg">
      <h3 class="font-bold text-red-700">Before</h3>
      <p class="text-sm">Inconsistent suggestions</p>
    </div>
    <div class="p-4 bg-blue-50 rounded-lg">
      <h3 class="font-bold text-blue-700">Add Rules</h3>
      <p class="text-sm">Define clear guidelines</p>
    </div>
    <div class="p-4 bg-green-50 rounded-lg">
      <h3 class="font-bold text-green-700">After</h3>
      <p class="text-sm">Predictable, quality output</p>
    </div>
  </div>
</div>

<!--
Now let's see rules in action with a live demo. I'll show you the transformation from inconsistent AI suggestions to predictable, quality output by adding clear guidelines through rules files.
-->

---
layout: center
class: text-center
---

# Key Takeaways

<div class="space-y-8 max-w-4xl mx-auto">
  <div class="grid grid-cols-2 gap-8">
    <div class="p-6 bg-blue-50 rounded-lg">
      <h3 class="font-bold text-blue-700 mb-3">🎯 Rules Are Critical</h3>
      <p class="text-sm">They transform chaotic AI into productive teammates</p>
    </div>
    
    <div class="p-6 bg-green-50 rounded-lg">
      <h3 class="font-bold text-green-700 mb-3">📝 Practical Strategies</h3>
      <p class="text-sm">Start small, iterate often, provide concrete examples</p>
    </div>
  </div>
  
  <div class="grid grid-cols-2 gap-8">
    <div class="p-6 bg-purple-50 rounded-lg">
      <h3 class="font-bold text-purple-700 mb-3">🔧 Multiple Formats</h3>
      <p class="text-sm">Choose the right format for your tools and team</p>
    </div>
    
    <div class="p-6 bg-orange-50 rounded-lg">
      <h3 class="font-bold text-orange-700 mb-3">🚀 Rules-Driven Workflow</h3>
      <p class="text-sm">Build systematic approaches to AI-assisted development</p>
    </div>
  </div>
  
  <div class="mt-8 p-6 bg-yellow-50 rounded-lg border-l-4 border-yellow-500">
    <p class="text-xl font-bold text-yellow-800">Remember: If AI gets it wrong, don't give up - write a rule!</p>
  </div>
</div>

<!--
Let's wrap up with our key takeaways. Rules are critical - they transform chaotic AI into productive teammates. Use practical strategies: start small, iterate often, and provide concrete examples. There are multiple formats available, so choose the right one for your tools and team. Build a rules-driven workflow with systematic approaches to AI-assisted development. And remember our golden rule: If AI gets it wrong, don't give up - write a rule!
-->

---
layout: center
class: text-center
---

# Questions?

<div class="space-y-8">
  <div class="text-6xl">❓</div>
  
  <div class="space-y-4">
    <p class="text-xl">Let's discuss rules, AI workflows, and agent-driven development</p>
    
    <div class="flex justify-center gap-8 mt-8">
      <div class="flex items-center gap-2">
        <carbon-logo-github class="text-blue-400" />
        <span>github.com/backlineint</span>
      </div>
      <div class="flex items-center gap-2">
        <carbon-logo-twitter class="text-blue-400" />
        <span>bsky.app/profile/brianperry.dev</span>
      </div>
    </div>
  </div>
  
  <div class="mt-12 p-4 bg-gray-50 rounded-lg">
    <p class="text-sm text-gray-600">Slides and resources available at: github.com/backlineint/rules-talk</p>
  </div>
</div>

<!--
I'd love to hear your questions about rules, AI workflows, and agent-driven development. Feel free to reach out to me on GitHub or Bluesky, and you can find all the slides and resources from this talk in the GitHub repository.
-->

---
layout: center
class: text-center
---

# Thank You!

<div class="space-y-6">
  <div class="text-6xl">🎉</div>
  
  <h2 class="text-3xl font-bold">Start Your Rules Journey Today</h2>
  
  <p class="text-lg text-gray-600">Transform your AI assistant from chaos to consistency</p>
  
  <div class="mt-8 p-6 bg-gradient-to-r from-blue-500 to-purple-600 rounded-lg text-white">
    <p class="text-xl font-bold">Your AI is only as good as the rules you give it</p>
  </div>
</div>

<!--
Thank you for your attention! I hope you're inspired to start your own rules journey today. Remember, your AI is only as good as the rules you give it. Transform your AI assistant from chaos to consistency, and unlock the true power of agent-driven development.
-->