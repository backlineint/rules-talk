# Unlocking the Power of Agent-Driven Development with Rules

## Content Structure

### Slide Sections

1. **Title & Introduction**

- A slide about me, Brian Perry. I'm a founding engineer at Actual AI. I live in the Chicago suburbs, and I love Nintendo.
    - Use a an image of me that would be appropriate for a bio slide.
    - Bluesky: https://bsky.app/profile/brianperry.dev
    - Github: https://github.com/backlineint

- A slide about Cursor, who co-authored this talk.

```
## Claude Code: Co-Author of This Talk

- Claude helped draft content, iterate on demos, and tighten language
- `CLAUDE.md` keeps Claude aligned with the story arc
- Today’s deck is proof that rules + agents co-create real work
```

- Actual AI company slide. Just use the Actual AI Image here.

2. **The Problem**

- Everyone has experienced AI making mistakes

- Common advice: "Think of AI as a Junior Developer"

- I graduated in 2002 - thinking of me as a developer 23 years ago is horrifying
- What I needed: mentors, guidelines, documentation, trial and error

- Coding agents need the same thing

3. **Why Rules Matter**

- What are rules?
  📝 **Reusable, scoped instructions that control agent behavior**
  🎯 **They provide structure and guardrails**
  🔄 **They enable consistent, predictable outcomes**

- Rules are defined in your codebase as markdown files. It is a charmingly low tech solution.

- Note: We're not talking about the Drupal Rules module here.

4. **Understanding Rules Formats**

- Overview of different formats

- Cursor rules format

- Claude Code rules format

- Copilot rules format

repository-wide instructions file .github/copilot-instructions.md
path-specific \*.instructions.md

- Agents.md as an emerging standard

Agents.md is also supported by Cursor and Copilot (but not Claude)

- Comparison and use cases

- I really wish everyone could just standarize on Agents.md

5. **Practical Strategies from Building This Talk**

- I started with just a few high level rules

```
# Slide Presentation

Build a presentation ready slide deck, not just an outline.
Don't repeat a previous version of this presentation.
```

With only this much context, the agent will still just make a bunch of stuff up.

- Next, I added rules to lead the agent to the most important context

```
## Important Resources

Impotant resources live in the /resources directory, including:

- abstract.md - a description of the session we will be creating slides for.
- outline.md - an in-progress outline of the session content.
- images directory - images that you should prioritize trying to include in the presentation.
```

- I also used rules to help the agent understand more about the Slide deck framework used in the codebase.

```
- example-slides.md - examples of slides that can be created with Slidev
```

```
## Creating Slides

- When authoring slides, the content belongs in slides.md in the root of this project.
- The slides are a Slidev project. For documentation use context7
```

- use context7 tells the agent to use the context7 MCP. Explain what MCP is and what context7 is.

- Also used context7 to help the agent understand the different rules formats we were convering.

```
### Rules formats

- We'll cover Agents.md, Cursor, Claude Code, and Github Copilot. use context7
```

- When you find yourself correcting an agent, define a rule.

I did this as I found issues in slides during test runs.

```
- The slides should only include content for the presentation, not speaker notes.
- Make sure text doesn't overflow the slide. At most a slide can have 8 lines of text. THIS IS VERY IMPORTANT.
- The slides should have sufficient contrast to be readable. Note that these slides will be presented in dark mode.
- Slides that use lists should not use the class: text-center
- Speaker notes can be included as html comments at the end of a slide.
- Make use of layouts to make the slides more compelling: https://sli.dev/builtin/layouts
- Use headings to make the slides more compelling
```

- Nested rules and scoping

Most tools will allow you to co-locate a rules file in a specific directory to either increase its priority, or scope the rules to that subdirectory.

This is how I helped the agent select key images for the slides. Inside /resources/images

```
# Images for Slides

- junior_dev1.jpg - image of me around the time that I was a junior developer.
- brian-perry.jpg - a good photo of me for the bio slide
- actual-ai.png - an image for the Actual AI Company Slides. This probably won't look right in a two colmn layout.
```

- How to define effective rules
- Best practices for rule writing
- Scoping rules appropriately
- Building a rules library

6. **Tools for Rules-Driven Workflows**

- Backlog.md - A tool for managing project collaboration between humans and AI Agents in a git ecosystem
  Behind the scenes, this is a series of complex rules.
- Backlog.md demo
- Demo of cursor plan mode
- Actual AI ADR Management Demo

7. **Miscellaneous Tips and Tricks**

- Consider keeping additional context in repository.
  If the agent can't see it, it probably doesn't know it (and might make it up)
  I saved all past runs I used for my eval process to the codebase.

- The basics we sometimes ovelook are even more important when working with agents.
  Linting
  Testing
  Documentation

8. **Conclusion & Takeaways**

- Key takeaways recap
- Call to action
- Q&A slide
- "If AI gets it wrong, don't give up - write a rule"

9.

Add anything that is missing from abstract.md
