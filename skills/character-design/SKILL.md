---
name: character-design
description: "Use when the world is established and you need to design characters — profiles, arcs, motivations, relationships. Also initializes stats, inventory, and relationship tracking when needed."
---

# Character Design

Design all major characters with detailed profiles, then write them into the story bible.

**Announce at start:** "I'm using the character-design skill to design characters."

<HARD-GATE>
Do NOT invoke plot-architecture or any writing skill until all major characters have been designed and approved. Every character that appears in more than one chapter MUST have a profile in story-bible.md.
</HARD-GATE>

## When to Use

- After worldbuilding produces an approved story-bible.md (World section)
- When the user says "design characters", "create characters", "I need characters"
- Before plot-architecture (characters drive plot, not the reverse)

## Pre-Flight

1. Read `story-bible.md` — understand the world, especially power systems
2. Read the concept document — note genre flags: `needs_stats`, `needs_inventory`, `needs_relationship_map`
3. These flags determine which extra modules to initialize

## Checklist

1. **Read story-bible.md and concept** — understand world and flags
2. **Design protagonist** — full profile, confirmed with user
3. **Design antagonist/opposing force** — full profile
4. **Design key supporting characters** — each with clear story function
5. **Map character relationships** — connection web between characters
6. **Initialize stats** — if `needs_stats: true`
7. **Initialize inventory/equipment/skills** — if `needs_inventory: true`
8. **Initialize relationship network** — if `needs_relationship_map: true`
9. **Write to story-bible.md** — compile all character data
10. **User review** — ask user to review before proceeding
11. **Transition to plot-architecture** — invoke `supernovel:plot-architecture`

## Character Design Process

### Step 1: Protagonist (MUST be first)

Design the protagonist in detail. Present each attribute for user confirmation:

- **Name:** (with meaning/etymology if relevant)
- **Appearance:** 2-3 distinctive features, not a head-to-toe inventory. What makes someone recognize them at a glance?
- **Personality:** 3-5 core traits + 1 fatal flaw. The flaw is critical — flawless protagonists are boring.
- **Background:** Key experiences that shaped who they are. Not a biography — just the moments that matter.
- **Core Desire:** What do they want more than anything?
- **Core Fear:** What are they most afraid of? (Often the mirror of their desire)
- **Character Arc:** Story Start State (A) → Story End State (B). What fundamental change do they undergo?
- **Speech Pattern:** A distinctive way of speaking or behaving that lets readers identify them without dialogue tags. Give an example line.
- **Fatal Flaw Consequence:** How does their flaw cause problems in the story?

Use AskUserQuestion for each major attribute. One question at a time.

### Step 2: Antagonist / Opposing Force

Design with the same depth as the protagonist. Key requirements:
- The antagonist must be the protagonist's **mirror or counterpoint**
- They must have their own understandable motivation (not "evil for evil's sake")
- Their strength must directly challenge the protagonist's fatal flaw
- If the opposing force is not a person (nature, society, inner demon), still design it with clear rules and escalation

### Step 3: Key Supporting Characters

For each supporting character, answer ONE core question first:

> "Why does this character exist in this story?"

If the answer is "to make the world feel alive" — cut the character. Supporting characters must serve a story function:

| Function | Description |
|----------|-------------|
| **Mentor** | Guides the protagonist, often flawed themselves |
| **Catalyst** | Triggers change in the protagonist |
| **Mirror** | Shows what the protagonist could become |
| **Contrast** | Highlights the protagonist's qualities by difference |
| **Lever** | Creates pressure that forces the protagonist to act |
| **Witness** | Sees and reflects the protagonist's journey |

For each supporting character, design:
- Name, appearance (brief), personality (2-3 traits)
- Story function (from table above)
- Relationship to protagonist
- Arc: flat characters are fine, but explain WHY they're flat (e.g., "anchor character, doesn't change")

### Step 4: Character Relationship Map

Map all relationships between characters:

```
[Character A] --relationship--> [Character B]
```

For each relationship:
- Type: lovers / siblings / mentor-student / rivals / allies / superior-subordinate / strangers → confidants / etc.
- Current status
- How it changes over the story (if known)
- Source of tension (if any)

### Step 5: Initialize Stats System (if `needs_stats: true`)

**Only for novels with numerical progression systems** (game novels, cultivation, system novels).

For each character that has stats:

1. Define starting attributes based on the power system in story-bible.md
2. Create the stats table with current values
3. Create an empty change log

Rules:
- Stats MUST be derived from the world's power system rules
- Starting stats must make sense for the character's background
- Leave room for growth (don't start the protagonist at max)

### Step 6: Initialize Inventory/Equipment/Skills (if `needs_inventory: true`)

For each relevant character:

1. List starting equipment (what they have at story start)
2. List starting skills/abilities
3. List any quest items or important possessions
4. Create an empty change log

Rules:
- Starting inventory must match the character's background and resources
- Don't give the protagonist too much at the start (room to grow)
- Equipment stats must follow the power system's grading in story-bible.md

### Step 7: Initialize Relationship Network (if `needs_relationship_map: true`)

For novels with complex interpersonal dynamics (multi-romance, political intrigue, alliance/betrayal):

1. Create the initial relationship matrix
2. Define relationship types with nuance:
   - Not just "friends" — "childhood friends who grew apart"
   - Not just "enemies" — "rivals who respect each other"
3. Define alliance/group structures
4. Plan relationship change trajectory (will be refined in plot-architecture)

The relationship map is a LIVING document — it updates after every chapter batch.

## Writing to story-bible.md

After all characters are approved, write them into story-bible.md:

```markdown
## Characters

### [Character Name]
- **Role:** [Protagonist / Antagonist / Supporting]
- **Appearance:** [2-3 distinctive features]
- **Personality:** [Core traits + fatal flaw]
- **Background:** [Key shaping experiences]
- **Core Desire:** [What they want]
- **Core Fear:** [What they dread]
- **Arc:** [A state] → [B state]
- **Speech Pattern:** [Distinctive way of speaking, example line]
- **Story Function:** [For supporting characters]
- **Key Relationships:** [Who and how]

## Character Stats (if needs_stats)
[Stats tables for each character]

## Inventory & Skills (if needs_inventory)
[Equipment, backpack, skills for each character]

## Relationship Network (if needs_relationship_map)
[Relationship matrix, alliance tracking]
```

## The Iron Law

```
NO CHARACTER INTRODUCED IN DRAFTING WITHOUT A PROFILE IN THE STORY BIBLE.
```

This means:
- Every speaking character needs at least a brief profile
- Every character that appears in more than one scene needs full details
- Background extras (crowd, unnamed servants) are exempt
- If a new character is needed during drafting, STOP and add their profile first

## Self-Review

1. Does the protagonist's arc align with the concept's theme?
2. Does the antagonist directly challenge the protagonist's fatal flaw?
3. Does every supporting character have a clear story function?
4. Are there duplicate characters? (Two characters serving the same function → merge them)
5. Do the stats/inventory match the power system rules?
6. Is the relationship map free of contradictions?

## Red Flags

- Protagonist has no fatal flaw
- Antagonist is "purely evil" with no understandable motivation
- Supporting character exists "just because" with no clear function
- Two characters serving the same purpose
- Stats that don't match the power system's rules
- Starting inventory that's too powerful (nowhere to grow)
- Skipping relationship mapping for complex relationship novels
- Proceeding to plot-architecture without user approval

## Key Principles

- **Characters drive plot** — Design characters before plot structure
- **Flaws create story** — Perfect characters have no story to tell
- **Function over quantity** — Fewer, well-designed characters beat many shallow ones
- **Relationships are story engines** — The best plots come from character relationships
- **Stats are commitments** — Once set, they constrain future writing; set them carefully

## Integration

**Previous skill:** supernovel:worldbuilding (provides world context)
**Next skill:** supernovel:plot-architecture (uses characters to build plot)
**Updates:** story-bible.md (Characters, Stats, Inventory, Relationship Network sections)
