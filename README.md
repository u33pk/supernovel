# SuperNovel

SuperNovel is an enforced novel-writing methodology for AI coding agents, built on the same plugin architecture as [Superpowers](https://github.com/obra/superpowers). It provides a structured workflow that forces AI agents to follow a disciplined novel creation process — from initial brainstorming through worldbuilding, character design, plot architecture, drafting, consistency checking, and revision.

## How it works

When your coding agent starts a session with SuperNovel installed, it doesn't just jump into writing prose. Instead, it steps back and guides you through a structured creative process:

1. **Brainstorming** — Explores your novel concept, themes, genre, and tone through collaborative dialogue
2. **Worldbuilding** — Constructs the story's world layer by layer (geography, society, history, magic/tech systems)
3. **Character Design** — Creates detailed character profiles with arcs, motivations, and relationships
4. **Plot Architecture** — Designs the story structure (acts, turning points, main plot, subplots)
5. **Chapter Outlining** — Produces detailed chapter-by-chapter outlines with scenes, POV, and foreshadowing
6. **Drafting** — Writes chapters strictly following the outline, maintaining a Story Bible
7. **Consistency Check** — Verifies every chapter against the Story Bible for character, world, and plot consistency
8. **Revision** — Systematic editing for style, pacing, and quality
9. **Finishing** — Final review and delivery options

The skills trigger automatically — you don't need to do anything special. Your coding agent just has SuperNovel.

## The Story Bible

Every SuperNovel project maintains a `story-bible.md` — the single source of truth for all story elements. It tracks world settings, character profiles, plot threads, foreshadowing, timeline, and style guidelines. No detail is "official" until it appears in the Story Bible.

## Installation

### Claude Code

```bash
/plugin install supernovel@supernovel-marketplace
```

### Kimi Code

```text
/plugins
```

Go to `Marketplace` > `SuperNovel` and install it.

Or install directly:

```text
/plugins install https://github.com/supernovel/supernovel
```

## Skills Library

- **using-supernovel** — Bootstrap skill that establishes the "check skills before acting" rule
- **brainstorming** — Creative concept exploration with Socratic dialogue
- **worldbuilding** — Layer-by-layer world construction
- **character-design** — Detailed character profiles, arcs, and relationships
- **plot-architecture** — Story structure, acts, main plot, and subplots
- **chapter-outlining** — Detailed chapter-by-chapter outlines
- **drafting** — Chapter writing with strict outline adherence
- **consistency-check** — Story Bible verification after each chapter
- **revision** — Systematic editing for style, pacing, and quality
- **finishing** — Final review, formatting, and delivery

## Philosophy

- **Structure before prose** — Always plan before writing
- **Consistency is king** — The Story Bible is the single source of truth
- **Evidence over claims** — Verify against the Story Bible before proceeding
- **Incremental validation** — Get approval at each stage before moving on

## License

MIT License - see LICENSE file for details
