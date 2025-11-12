---
theme: seriph
background: https://cover.sli.dev
title: Unlocking the Power of Agent-Driven Development with Rules
info: |
  A 45-minute journey into building dependable AI coding workflows with reusable rules, better context, and tooling like backlog.md.
class: text-left
drawings:
  persist: false
transition: slide-left
mdc: true
duration: 45min
---

# Unlocking the Power of Agent-Driven Development with Rules

Guardrails, context, and confidence for your coding agents

<!--
Welcome folks, quick title read, set intent about rules as leverage.
-->

---

## Agenda

- Why rules transform agent-driven development
- Patterns for writing and evolving rules
- Tooling tour: Context7, `.cursor`, `Agents.md`, backlog.md
- Live demo plan and next steps you can try tomorrow

<!--
Reassure 45 min: ~10 intro, ~20 deep dive, ~10 tooling, ~5 demo + Q&A.
-->

---

## 🚨 Breaking News

- The talk has been replaced with **"The History of Artificial Houseplants"**
- We'll compare ficus firmware versions from 1997–1999
- Live terrarium unboxing in 30 minutes

<!--
Deadpan delivery, let them sit in confusion for a beat.
-->

---

## Just Kidding 🤖

- But that feeling of "wait, what?" is what bad agent context creates
- Rules stop surprises before they happen
- Let's get serious about unlocking agent potential

---

## About Me

- Brian Perry · Founding Engineer @ Actual AI
- Chicago suburbs based, Nintendo collector and tinkerer
- Former agent skeptic turned power user

<!--
Invite folks to say hi later, mention Mario Kart setup if relevant.
-->

---

## Actual AI in 20 Seconds

- Building guardrails so AI-enabled teams can ship safely
- Focused on workflows, not just prompts
- Practical patterns like reusable rule libraries and backlog.md

---

## Cursor: Co-Author of This Talk

- Cursor helped draft content, iterate on demos, and tighten language
- `.cursor/rules` keeps Cursor aligned with the story arc
- Today’s deck is proof that rules + agents co-create real work

---

## Agents Are Powerful… and Chaotic

- Speed is intoxicating until the first hallucinated diff ships
- Teams report initial wins, followed by burnout and distrust
- Consistency, not creativity, is where adoption breaks down

---

## We've All Seen This

- Agent refactors working code without asking
- PR descriptions invent files that never existed
- A simple bug fix turns into a three-hour cleanup

---

## Think of Agents Like Junior Developers

- Capable, eager, and fast learners
- Need clarity on expectations, scope, and process
- Without guidance, they'll fill gaps with guesses

---
layout: image-left
image: ./resources/images/junior_dev1.jpeg
class: items-center
---

# Junior Brian, circa 2002

- Graduated college trusting my frosted tips and luck
- Everything felt like guess-and-check
- Production mistakes taught me faster than documentation

<!--
Tell quick story about first prod outage, laughter moment.
-->

---
layout: image-right
image: ./resources/images/junior_dev2.jpeg
---

# What I Needed Back Then

- Patient mentors who codified expectations
- Checklists, style guides, and documented decisions
- A backlog of lessons learned to revisit

<!--
Make the bridge to modern agent workflows.
-->

---

## Agents Need the Same Guardrails

- Rules define the sandbox, defaults, and escalation paths
- Context lets them see the same docs we do
- Tooling keeps the system evolving instead of drifting

---

## Rules 101

- **Rules**: scoped, reusable instructions that shape agent behavior
- Think of them as the team's shared playbook
- Written once, reused across prompts, repos, and teammates

---

## Where Rules Live

- `Agents.md`: human-readable contract for any agent in the repo
- `.cursor/rules`: Cursor-specific directives, syncing with Context7 docs
- `claude.md`: Claude Code instructions, mirrors your repo conventions
- `codex.rules.json`: Codex guardrails, structure and validation baked in

<!--
Call out that duplication is intentional—tool-specific polish matters.
-->

---

## Anatomy of a Rule File

```md
## Important Resources

- /resources/abstract.md — session description
- /resources/outline.md — evolving plan
- /resources/example-slides.md — Slidev patterns

## Creating Slides

- Author in `slides.md`
- Presentation content only; use HTML comments for notes
```

---

## When to Add a Rule

- The moment you correct an agent twice, codify it
- Ask the agent to propose the rule draft, then refine
- Link rules to the scenario that inspired them for future you

---

## Rules About Rules

- Version control rules alongside code for provenance
- Date + owner every non-obvious instruction
- Retire rules that no longer add value—stale guardrails become friction

---

## Context Stops Hallucinations

- Provide docs, configs, and examples as first-class inputs
- Prefer local sources: README, ADRs, git history
- Keep context close to the code, not scattered in chat threads

---

## MCP + Context7 in Practice

```json
{
  "mcpServers": {
    "context7": {
      "url": "https://mcp.context7.com/mcp",
      "headers": {
        "CONTEXT7_API_KEY": "YOUR_API_KEY"
      }
    }
  }
}
```

- Fetch up-to-date Slidev docs, Cursor rule syntax, and more
- Reference the docs inside rules so agents know what to read

---

## Keep Context in the Repo

- `.cursor/context/` for evergreen snippets and API schemas
- `docs/rules/` for team-wide conventions
- Link PRs back to the rules that guided them

---

## Rules-Driven Workflow

1. Start every task by syncing rules + context
2. Prompt the agent with desired outcome and constraints
3. Capture corrections in backlog.md
4. Promote recurring patterns into shared rules

---

## Tooling Spotlight: backlog.md

- Lightweight ledger of learnings, follow-ups, and rule debt
- Lives at the root, versioned with the code
- Sections: `🛠 Corrections`, `📚 New Context`, `✅ Closed`

---

## backlog.md Excerpt

```md
## 🛠 Corrections
- 2025-11-10 · Rule idea: "Validate Slidev layout keys" (Cursor hallucinated layout)

## 📚 New Context
- Link Slidev docs on layout variants via Context7
```

---

## Live Demo Plan

- Show current `Agents.md` + `.cursor/rules`
- Capture a real correction in backlog.md
- Generate an updated rule and re-run the agent
- Compare results before and after the rule

<!--
Remind yourself to open terminal + editor tabs ahead of time.
-->

---

## Common Pitfalls

- Treating rules as static policy instead of living documentation
- Overloading one giant file instead of scoping by tool
- Forgetting to prune conflicting or outdated instructions

---

## Key Takeaways

- Rules turn agent speed into dependable delivery
- Context (especially via MCP + Context7) prevents hallucinations
- Tooling like backlog.md keeps improvements compounding
- Start small: one rule per correction this week

---

## Try This Tomorrow

- Audit one repo for missing or stale rules
- Ask your agent to draft updates based on recent fixes
- Wire up Context7 or your preferred MCP source
- Share your backlog.md learnings with the team

---