---
name: worldbuilding
description: "Use when you have an approved concept and need to build the story's world — setting, rules, history, culture, geography. Creates or expands the story-bible.md."
---

# Worldbuilding

Build the story's world layer by layer, establishing the foundation that all characters and plot will stand on.

**Announce at start:** "I'm using the worldbuilding skill to build the world."

<HARD-GATE>
Do NOT invoke character-design, plot-architecture, or any writing skill until the world has been presented layer by layer and the user has approved it. Do NOT write story-bible.md until all layers are approved.
</HARD-GATE>

## When to Use

- After brainstorming produces an approved concept document
- When the user says "design the world", "build the setting"
- Starting a new novel project and story-bible.md doesn't exist yet

## Pre-Flight

1. Read the concept document from `docs/supernovel/concepts/`
2. Check if `story-bible.md` already exists
3. Note the flags from the concept: `needs_stats`, `needs_inventory`, `needs_relationship_map`

## Checklist

You MUST create a task for each item and complete them in order:

1. **Read concept document** — understand the world direction
2. **Build Layer 1: Physical World** — geography, climate, key locations
3. **Build Layer 2: Society & Politics** — power structures, social classes
4. **Build Layer 3: History & Timeline** — key events, current era
5. **Build Layer 4: Power Systems** — magic/tech/cultivation/game systems (if applicable)
6. **Build Layer 5: Culture & Daily Life** — customs, economy, language
7. **Write story-bible.md** — compile approved layers into the World section
8. **Flag [TBD] items** — list all unresolved details
9. **User review** — ask user to review before proceeding
10. **Transition to character-design** — invoke `supernovel:character-design`

## Layer-by-Layer Process

### Layer 1: Physical World

Present the physical setting. Scale to the story's needs:
- A single building for a locked-room mystery
- A city for urban fiction
- A continent for epic fantasy
- Multiple planets for space opera

For each major location:
- Physical description (key features, not exhaustive)
- Climate/environment
- Significance to the story
- How it affects the characters who live there

Use AskUserQuestion to confirm each major location before moving to the next.

### Layer 2: Society & Politics

- Political system(s): monarchy, democracy, corporate, tribal, etc.
- Social classes and mobility: rigid or fluid?
- Power holders: who has power, how is it maintained?
- Conflicts: what tensions exist in society?
- Economy: how do people make a living?

Scale to story needs. A corporate thriller needs business structure, not a feudal system.

### Layer 3: History & Timeline

- Key historical events that shaped the current world
- Current era: what's happening now?
- Historical legacies: what problems from the past affect the present?
- Timeline of relevant events (can be expanded later)

Only include history that matters to the story. "Interesting but irrelevant" worldbuilding is a trap.

### Layer 4: Power Systems

**Only if the concept requires it.** Skip for purely realistic fiction.

For each system (magic, cultivation, technology, game mechanics):
- **Rules:** What can it do?
- **Limitations:** What can't it do? (Limits are more important than abilities)
- **Cost:** What does it cost to use?
- **Acquisition:** How do people get it?
- **Social impact:** How does it affect society?
- **Tiers/levels:** If there's a progression system, define the tiers

If `needs_stats: true`, this layer must also define:
- What attributes exist (strength, mana, etc.)
- How they scale
- What the tier/level breakpoints are
- How equipment modifies stats

This is critical for system/game novels — inconsistent power systems break reader trust.

### Layer 5: Culture & Daily Life

- Customs and traditions
- Taboos
- Language/dialect notes (if relevant)
- Daily life for ordinary people
- Economic system (currency, trade)
- Religion/belief systems (if relevant)

## Story Bible Structure

After all layers are approved, write `story-bible.md`:

```markdown
# Story Bible — [Novel Title]

## World

### Geography
[Layer 1 content]

### Society & Politics
[Layer 2 content]

### History / Timeline
[Layer 3 content]

### Power Systems
[Layer 4 content, if applicable]

### Culture & Daily Life
[Layer 5 content]

### [TBD] Items
- [List of unresolved details that need decisions later]
```

## Handling [TBD] Items

Not everything needs to be decided now. Mark uncertain details as `[TBD]`:
- Minor locations not yet visited
- Background characters not yet named
- Details that will be determined by plot needs

**Rules for [TBD]:**
- Each [TBD] must have a context: WHY it's undecided
- [TBD] items MUST be resolved before they appear in drafting
- Flag them in the self-review so they don't get forgotten

## Self-Review

After writing story-bible.md:

1. **Internal consistency:** Do any settings contradict each other?
2. **Concept alignment:** Does the world match the concept document?
3. **Story relevance:** Does every element serve the story? Remove "cool but useless" details.
4. **Limit check:** Are power system limits clearly defined?
5. **[TBD] count:** Are there too many unresolved items?

## Red Flags

- Building elaborate history that doesn't affect the story
- Power system with no clear limits ("can do anything" = no tension)
- Skipping Layer 4 when the concept clearly needs a power system
- Leaving power system limits as [TBD] (these must be decided now)
- Writing worldbuilding prose instead of structured notes
- Proceeding to character-design without user approval

## Key Principles

- **Limits over abilities** — What can't be done matters more than what can
- **Story relevance** — Every detail should serve the story or be cut
- **Internal logic** — The world must be consistent with itself
- **Incremental validation** — Get approval per layer, don't dump everything at once
- **YAGNI** — Don't build what the story doesn't need

## Integration

**Previous skill:** supernovel:brainstorming (produces concept document)
**Next skill:** supernovel:character-design (designs characters within this world)
**Updates:** story-bible.md (World section)
