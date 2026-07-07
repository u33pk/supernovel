---
name: brainstorming
description: "You MUST use this before any creative work — developing a novel concept, exploring themes, choosing genre, or establishing tone. Explores user intent and requirements through dialogue before writing."
---

# Brainstorming Novel Concepts

Help turn ideas into a fully formed novel concept through natural collaborative dialogue.

Start by understanding what the user wants to write, then ask questions one at a time to refine the idea. Once you understand the concept, present the design and get user approval.

<HARD-GATE>
Do NOT invoke any other skill, write any prose, create any worldbuilding, or take any creative action until you have presented a concept and the user has approved it. This applies to EVERY novel project regardless of perceived simplicity.
</HARD-GATE>

## Anti-Pattern: "This Is Too Simple To Need Planning"

Every novel goes through this process. A short story, a simple romance, a one-shot — all of them. "Simple" stories are where unexamined assumptions cause the most wasted writing. The concept can be short (a few sentences for truly simple stories), but you MUST present it and get approval.

## Checklist

You MUST create a task for each of these items and complete them in order:

1. **Understand creative intent** — genre, audience, length, core inspiration
2. **Explore themes and core conflict** — what the story is really about
3. **Propose 2-3 directions** — with trade-offs and your recommendation
4. **Present concept design** — in sections, get user approval after each section
5. **Write concept document** — save to `docs/supernovel/concepts/YYYY-MM-DD-<topic>-concept.md`
6. **Concept self-review** — check for placeholders, contradictions, scope issues
7. **User reviews concept** — ask user to review the document before proceeding
8. **Transition to worldbuilding** — invoke `supernovel:worldbuilding` skill

## The Process

### Step 1: Understand Creative Intent

Ask questions **one at a time** to understand what the user wants to write. Prefer multiple choice when possible.

Key questions to cover (spread across multiple messages, never dump all at once):

- **Genre:** Sci-fi / Fantasy / Realism / Mystery / Historical / Romance / Light novel / Xianxia / Game-system / Urban / Horror / Other?
- **Target audience:** Young adult / Adult / General / Niche community?
- **Length:** Short (1-30k words) / Novelette (30-100k) / Novel (100k+) / Serialized?
- **Core inspiration:** Any core idea, image, or inspiration? Summarize in one sentence.
- **Numeric elements:** Does it involve numerical systems (levels/attributes/equipment/skill trees)?
- **Combat/action:** Are there combat/action scenes?
- **Complex relationships:** Are interpersonal dynamics complex (multi-romance / faction rivalry / alliance and betrayal)?

The last three questions determine which `story-bible.md` modules will be needed later. Flag the answers for `character-design`.

### Step 2: Explore Themes and Core Conflict

Once you understand the basic intent, dig deeper:

- **Theme:** What is this story really about? (Not plot — theme. e.g., "the cost of power", "finding home", "identity vs duty")
- **Core conflict:** What is the protagonist's biggest challenge?
- **Emotional tone:** Epic / Dark / Warm / Absurd / Healing / Oppressive?
- **Emotional goal:** What should the reader feel when they finish?
- **Unique selling point:** What makes this story different from similar ones?

Ask one question per message. Use AskUserQuestion for structured choices.

### Step 3: Propose 2-3 Directions

Based on the user's answers, propose 2-3 different story directions. For each direction:

- Core premise (1-2 sentences)
- Key selling points
- Potential risks or challenges
- How well it matches the user's stated intent
- Your recommendation and reasoning

Lead with your recommended option. Use AskUserQuestion to let the user choose or modify.

### Step 4: Present Concept Design

Expand the chosen direction into a concept design. Present it **section by section**, getting user approval after each:

1. **Story Synopsis** (3-5 sentences)
2. **Core Selling Points** (what makes readers pick this up)
3. **World Direction** (not details — just the flavor: modern urban / ancient China / space opera / game world / etc.)
4. **Character Direction** (protagonist is who, faces what — no full profiles yet)
5. **Plot Direction** (general trajectory — not structure yet)
6. **Unique Elements** (any special systems, mechanics, or narrative devices)

Ask after each section: "Does this direction look right? Anything to adjust?"

### Step 5: Write Concept Document

Save the validated concept to:

```
docs/supernovel/concepts/YYYY-MM-DD-<topic>-concept.md
```

The document should contain all approved sections from Step 4, plus:
- Genre and audience
- Estimated length
- Flags for which `story-bible.md` modules will be needed:
  - `needs_stats: true/false` (numerical systems)
  - `needs_inventory: true/false` (items/equipment/skills tracking)
  - `needs_relationship_map: true/false` (complex interpersonal dynamics)

### Step 6: Concept Self-Review

After writing the concept document, review it with fresh eyes:

1. **Placeholder scan:** Any "TBD", "TODO", incomplete sections, or vague requirements? Fix them.
2. **Internal consistency:** Do any sections contradict each other?
3. **Scope check:** Is this focused enough for a single novel, or does it need to be a series?
4. **Ambiguity check:** Could any part be interpreted two different ways? Pick one and make it explicit.

Fix any issues inline.

### Step 7: User Reviews Concept

After the self-review, ask the user:

> "Concept document saved to `<path>`. Please review it and let me know if you want to make any changes before we start building the world."

Wait for user response. Only proceed once the user approves.

### Step 8: Transition

After user approval, invoke `supernovel:worldbuilding` to begin building the story's world.

Do NOT invoke any other skill. `worldbuilding` is the next step.

## Key Principles

- **One question at a time** — Don't overwhelm with multiple questions
- **Multiple choice preferred** — Easier to answer when possible
- **No assumptions** — If the user says something ambiguous, ask for clarification
- **Incremental validation** — Present each section, get approval before moving on
- **Be flexible** — Go back and clarify when something doesn't make sense
- **Flag complexity** — If the concept is too large, help decompose into a series

## Red Flags

- Starting to write prose before concept is approved
- Skipping questions because "the answer seems obvious"
- Proposing only one direction (no alternatives)
- Writing a concept document without user approval at each section
- Proceeding to worldbuilding without explicit user sign-off
- Making assumptions about genre, audience, or tone
