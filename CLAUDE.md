# Slide Presentation

Build a presentation ready slide deck, not just an outline. Don't repeat a previous version of this presentation.

## Important Resources

Impotant resources live in the /resources directory, including:

- abstract.md - a description of the session we will be creating slides for.
- outline.md - an in-progress outline of the session content.
- example-slides.md - examples of slides that can be created with Slidev

### Rules formats

- We'll cover Agents.md, Cursor, Claude Code, and Codex. use context7
- For cursor reference https://cursor.com/docs/context/rules

## Creating Slides

- The slides are a Slidev project. For documentation use context7
- When authoring slides, the content belongs in slides.md in the root of this project.
- The slides should only include content for the presentation, not speaker notes.
- Speaker notes can be included as html comments at the end of a slide.
- Layouts and images need to be part of a frontmatter block. Here is an example

```
---
layout: image-right
image: ./resources/images/junior_dev2.jpeg
---
```

- Make use of layouts to make the slides more compelling: https://sli.dev/builtin/layouts
- Use headings to make the slides more compelling

## Other Important Guidelines

- Ignore content in the /internal directory
