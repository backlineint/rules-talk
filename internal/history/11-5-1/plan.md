# Plan: Author Slides for "Unlocking the Power of Agent-Driven Development with Rules"

## Overview

Create a complete slide deck in `slides.md` for a 45-minute presentation. The talk covers how rules are critical for effective AI coding agents, with practical strategies, format comparisons, and workflow demonstrations.

## Content Structure

### Slide Sections (estimated 25-30 slides total)

1. **Title & Introduction** (2-3 slides)

- Title slide with talk name and presenter info
- Speaker introduction (Brian Perry, Actual AI, Chicago suburbs, Nintendo)
- Actual AI company slide

2. **The Problem** (4-5 slides)

- Everyone has experienced AI making mistakes
- Common advice: "Think of AI as a Junior Developer"
- Personal reflection: "I graduated in 2002 - thinking of me 23 years ago is horrifying"
- What I needed: mentors, guidelines, documentation, trial and error
- Coding agents need the same thing

3. **Why Rules Matter** (5-6 slides)

- Rules as guardrails for AI agents
- Rules provide structure for success
- Reusable, scoped instructions
- "If AI gets it wrong, don't give up - write a rule"

4. **Understanding Rules Formats** (6-8 slides)

- Overview of different formats
- Cursor rules format
- Claude Code rules format
- Codex rules format
- Comparison and use cases

5. **Practical Strategies** (4-5 slides)

- How to define effective rules
- Best practices for rule writing
- Scoping rules appropriately
- Building a rules library

(Repurpose - "If AI gets it wrong, don't give up - write a rule")

6. **Rules-Driven Workflow** (3-4 slides)

- Building a workflow around rules
- Tooling overview (mention backlog.md)
- Live demo preparation slides

7. **Conclusion & Takeaways** (2-3 slides)

- Key takeaways recap
- Call to action
- Q&A slide

## Implementation Steps

1. **Update slides.md frontmatter**

- Change title to "Unlocking the Power of Agent-Driven Development with Rules"
- Update duration to 45min
- Keep theme and styling appropriate

2. **Create title and introduction slides**

- Professional title slide
- Speaker bio slide
- Actual AI company slide

3. **Develop problem section**

- Use engaging visuals and examples
- Include the personal narrative about being a junior developer
- Connect to AI agent needs

4. **Build rules explanation section**

- Use code examples and visual diagrams where appropriate
- Explain concepts clearly for the audience
- Include practical examples

5. **Create rules formats comparison section**

- Show actual format examples (using code blocks)
- Use layout: two-cols or similar for comparisons
- Highlight key differences

6. **Add practical strategies section**

- Actionable advice
- Use bullet points and structured content
- Include real-world examples

7. **Develop workflow section**

- Process flow diagrams if helpful
- Tooling overview
- Demo setup slides

8. **Create conclusion slides**

- Summarize key points
- Provide next steps
- Include contact/social info if desired

## Technical Considerations

- Use Slidev features from `example-slides.md`:
- Code blocks for rule format examples
- Layout options (two-cols, image-right, etc.)
- Click animations for progressive disclosure
- Proper slide transitions
- Maintain consistent styling throughout
- Add speaker notes in HTML comments where helpful
- Ensure slides flow logically for 45-minute presentation pace

## Files to Modify

- `/Users/brianperry/repos/rules-talk/slides.md` - Main slide deck file

## Content Sources

- `/Users/brianperry/repos/rules-talk/resources/abstract.md` - Key takeaways and main content
- `/Users/brianperry/repos/rules-talk/resources/outline.md` - Specific slide ideas and structure
- `/Users/brianperry/repos/rules-talk/resources/example-slides.md` - Slidev formatting patterns
