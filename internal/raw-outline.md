# Unlocking the Power of Agent-Driven Development with Rules

- Add a joke slide that is completely off topic. Then reveal that we're kidding.
- A slide about me, Brian Perry. I'm a founding engineer at Actual AI. I live in the Chicago suburbs, and I love Nintendo.
- A slide about Cursor, who co-authored this talk.

```
## Cursor: Co-Author of This Talk

- Cursor helped draft content, iterate on demos, and tighten language
- `.cursor/rules` keeps Cursor aligned with the story arc
- Today’s deck is proof that rules + agents co-create real work
```

- A slide about Actual AI. We're building a set of tools to provide guardrails for AI endabled software teams.
- Anyone who has used AI for development has experienced it making mistakes.
- Common advice is to think of AI as a Junior Developer.
- I graduated college in 2002. Thinking of me as a developer 23 years ago is horrifying. Use images of me as a junior developer here.
- I needed mentors, clear guidelines, well documented codebases, and lots of learning and trial and error to get to where I am today.
- Coding agents need the same thing.
- Basic introduction to rules files and the various formats.
- I started by adding some basic rules for this talk:

```
## Important Resources

Impotant resources live in the /resources directory, including:

- abstract.md - a description of the session we will be creating slides for.
- outline.md - an in-progress outline of the session content.
- example-slides.md - examples of slides that can be created with Slidev

## Creating Slides

- When authoring slides, the content belongs in slides.md in the root of this project.
- The slides should only include content for the presentation, not speaker notes.
- Speaker notes can be included as html comments at the end of a slide.
```

- A good pattern is to create a rule when you find yourself correcting an agent. In fact, you can as the agent to create a rule for you. You might find yourself creating rules about rules.

- To prevent AI Agents (and Junior developers) from hallucinating, provide context in the form of documentation.
    - Using MCP is a common approach. Context 7 is a great MCP for up to date docs. For this talk, I'm using it to make the agent aware of the docs for Slidev, the presentation framework used for this talk.
    - .cursor/mcp.json

```
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

And then in our rules (or a prompt)

```
## Creating Slides

- The slides are a Slidev project. For documentation use context7
```

- Favor keeping context inside your repository. Git history, local documentation, etc.

Add anything that is missing from abstract.md
