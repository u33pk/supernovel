# SuperNovel

SuperNovel is an enforced novel-writing methodology for AI coding agents, built on the same plugin architecture as [Superpowers](https://github.com/obra/superpowers). It provides a structured workflow that forces AI agents to follow a disciplined novel creation process — from initial brainstorming through worldbuilding, character design, plot architecture, drafting, consistency checking, and revision.

## How it works

When your coding agent starts a session with SuperNovel installed, it doesn't just jump into writing prose. Instead, it steps back and guides you through a structured creative process:

1. **Brainstorming** — Explores your novel concept, themes, genre, and tone through collaborative dialogue
2. **Worldbuilding** — Constructs the story's world layer by layer (geography, society, history, magic/tech systems)
3. **Character Design** — Creates detailed character profiles with arcs, motivations, and relationships
4. **Plot Architecture** — Designs the story structure (acts, turning points, main plot, subplots)
5. **Chapter Outlining** — Produces detailed chapter-by-chapter outlines in 5-chapter batches
6. **Drafting** — Writes chapters in batches of 5, strictly following outlines with story bible updates
7. **Consistency Check** — Two-level review: batch review (every 5 chapters) + meta-review (every 25 chapters)
8. **Revision** — Systematic one-problem-at-a-time editing with re-verification
9. **Finishing** — Final review and delivery options

## The Story Bible

Every SuperNovel project maintains a `story-bible.md` — the single source of truth for all story elements. It tracks world settings, character profiles, plot threads, foreshadowing, timeline, and style guidelines. No detail is "official" until it appears in the Story Bible.

For novels with numerical systems (game novels, cultivation, system novels), the Story Bible also maintains:
- **Character Stats** — Base attributes, modifiers, and change logs
- **Inventory & Skills** — Equipment, backpack items, acquired abilities with change logs
- **Relationship Network** — Relationship matrix, alliance tracking, and change logs

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
- **worldbuilding** — Layer-by-layer world construction (5 layers)
- **character-design** — Detailed character profiles, arcs, relationships, stats/inventory initialization
- **plot-architecture** — Story structure, acts, main plot, subplots, relationship trajectories
- **chapter-outlining** — 5-chapter batch outlines with ending variety rules
- **drafting** — 5-chapter batch writing with strict outline adherence and story bible updates
- **consistency-check** — Two-level review: batch review (repetition detection, factual consistency) + meta-review (long-term pattern detection, foreshadowing audit)
- **revision** — Systematic one-problem-at-a-time editing
- **finishing** — Final review, formatting, and delivery

## Philosophy

- **Structure before prose** — Always plan before writing
- **Consistency is king** — The Story Bible is the single source of truth
- **Evidence over claims** — Verify against the Story Bible before proceeding
- **Anti-laziness** — 5-chapter batches with repetition detection prevent model shortcuts
- **Incremental validation** — Get approval at each stage before moving on

## License

MIT License - see LICENSE file for details
