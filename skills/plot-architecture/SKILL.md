---
name: plot-architecture
description: "Use when characters are designed and you need to architect the plot — story structure, main plot, subplots, turning points, and relationship trajectories. Plans the entire story before writing begins."
---

# Plot Architecture

Design the complete story structure — main plot, subplots, turning points, and character arc integration. This is the blueprint for everything that follows.

**Announce at start:** "I'm using the plot-architecture skill to design the plot structure."

<HARD-GATE>
Do NOT invoke chapter-outlining or any writing skill until the plot architecture has been fully designed and approved by the user. Every major turning point must be defined.
</HARD-GATE>

## When to Use

- After character-design produces approved character profiles in story-bible.md
- When the user says "plan the plot", "design the story structure"
- Before chapter-outlining (structure before details)

## Pre-Flight

1. Read `story-bible.md` — especially Characters, World, and power systems
2. Read the concept document — note theme, emotional goal, estimated length
3. Check if `needs_relationship_map: true` — if so, plan relationship trajectories

## Checklist

1. **Read story-bible.md and concept** — understand characters, world, theme, estimated length
2. **Choose planning mode** — one-shot or volume-based based on length
3. **Choose story structure** — recommend and get user choice
4. **Plan main plot** — turning points for current scope, one by one with approval
5. **Plan subplots** — each with theme, connection, and resolution
6. **Plan relationship trajectories** — if `needs_relationship_map: true`
7. **Chapter rough division** — pacing and rhythm plan
8. **Self-review** — check for gaps, dead ends, broken arcs
9. **Write to story-bible.md** — compile into Plot section
10. **User review** — get approval before proceeding
11. **Transition to chapter-outlining** — invoke `supernovel:chapter-outlining`

## Step 0: Choose Planning Mode

Based on estimated length, recommend a planning mode. Use AskUserQuestion.

| Mode | Scope | Approach |
|------|-------|----------|
| **One-shot** | Short (1-30k words) / Novelette (30-100k) / Novel (up to 30 chapters) | Plan all chapter structure and turning points at once |
| **Volume-based** | Serialized (30+ chapters) / Web novels (hundreds of chapters) | Plan macro architecture + first volume only; subsequent volumes planned after previous volume completes |

**Volume mode parameters:**
- **Chapters per volume:** Default 50, user configurable (e.g., 30, 80, 100)
- Use AskUserQuestion to confirm chapters per volume

**Why volumes?**
- Planning every detail of a 500+ chapter novel upfront is unrealistic; later chapters will inevitably deviate
- Volumes allow adjusting direction based on what's already been written
- Foreshadowing can be managed per-volume with independent plant/payoff rhythms
- Character arcs can progress in stages, each volume having its own arc milestone

**Key difference in volume mode:**
- Steps 3-6 (main plot, subplots, relationships, chapter division) detail only the **current volume**
- A **macro architecture** (see below) must define the overall trajectory across all volumes
- After each volume completes, return to plot-architecture to plan the next volume

## Step 1: Choose Story Structure

Based on genre and concept, recommend a structure. Use AskUserQuestion.

| Structure | Best For | Key Feature |
|-----------|----------|-------------|
| **Three-Act** | Most genres, universal | Setup → Confrontation → Resolution |
| **Hero's Journey** | Adventure, growth, fantasy | 12-stage monomyth |
| **Kishotenketsu** | East Asian literary, slice-of-life | Twist-driven, no central conflict required |
| **Save the Cat (15 beats)** | Commercial, screenwriting-influenced | 15 precise story beats |
| **Multi-POV / Braided** | Epic fantasy, political intrigue | Multiple converging storylines |
| **Non-linear** | Mystery, literary, experimental | Time jumps, unreliable narration |

Let the user choose or propose a custom structure. Reference `structure-reference.md` for details on each.

## Step 1.5: Macro Architecture (Volume mode only, skip in one-shot)

**Only needed in volume mode.** One-shot mode proceeds directly to Step 2.

The macro architecture defines the overall trajectory across all volumes, without chapter-level detail:

```markdown
## Macro Architecture

### Full Story Summary
[3-5 paragraphs describing the entire story from beginning to end]

### Volume Plan
| Volume | Est. Chapters | Core Conflict | Protagonist Arc Stage | Key Climax |
|--------|--------------|---------------|----------------------|------------|
| Vol 1 | 50 | [volume conflict] | [A → Intermediate 1] | [volume climax] |
| Vol 2 | 50 | [volume conflict] | [Intermediate 1 → Intermediate 2] | [volume climax] |
| ... | ... | ... | ... | ... |
| Final | 50 | [final conflict] | [Intermediate N → B] | [full story climax] |

### Master Foreshadowing Table
| # | Foreshadowing | Planned Plant Volume | Planned Payoff Volume | Status |
|---|--------------|---------------------|----------------------|--------|
| | | | | |

### Master Subplot Table
| Subplot | Theme Served | Spans Volumes | Joins Main Plot At |
|---------|-------------|---------------|-------------------|
| | | | |
```

The macro architecture only needs user confirmation of the overall direction. Details are fleshed out volume by volume.

## Step 2: Plan Main Plot

**One-shot mode:** Plan all major turning points for the entire story.
**Volume mode:** Plan only the current volume's major turning points. The overall trajectory is defined in the macro architecture.

Walk through each major turning point of the chosen structure. For EACH turning point:

1. **Describe the event** — what happens
2. **Explain the impact** — how it changes the protagonist's situation
3. **Connect to character arc** — how it pushes the protagonist toward their B state
4. **Get user approval** — use AskUserQuestion

Key turning points to define:

- **Opening Hook:** The very first scene. How do you grab the reader in the first paragraph?
- **Inciting Event:** What disrupts the protagonist's ordinary world?
- **Act 1 Turning Point:** What forces the protagonist to commit to the journey?
- **Midpoint:** A revelation or reversal that changes everything. False victory or false defeat.
- **Act 2 Turning Point:** The darkest moment. What's the protagonist's lowest point?
- **Climax:** The final confrontation. How does the protagonist face their ultimate test?
- **Resolution:** The new normal. How has the world and character changed?

For each point, ask: "How does this event advance the protagonist's arc?" If the answer is unclear, the event needs rethinking.

## Step 3: Plan Subplots

For each subplot, answer:

1. **What theme does it serve?** (Subplots explore the main theme from a different angle)
2. **Where does it intersect the main plot?** (Must have at least one intersection point)
3. **Which characters are involved?**
4. **How does it resolve?**
5. **What happens if we cut it?** (If nothing is lost → cut it)

**Rules:**
- A subplot with no intersection with the main plot → cut
- A subplot that doesn't serve the theme → cut
- A subplot with no resolution → either plan a resolution or cut it
- Maximum 3 subplots for a debut novel. Fewer is better.

## Step 4: Plan Relationship Trajectories (if `needs_relationship_map: true`)

For novels with complex interpersonal dynamics, plan how key relationships evolve:

For each major relationship:
1. **Starting state** (from character-design)
2. **Key turning points** — at which chapter/events does the relationship change?
3. **Ending state**
4. **What drives the change?** (Miscommunication, betrayal, shared hardship, growth apart)

For alliance/betrayal arcs:
1. **Alliance formation** — when and why
2. **Strain points** — what creates tension
3. **Breaking point** — what causes the betrayal/split
4. **Aftermath** — how it affects all parties

Write these trajectories as a timeline that can be referenced during chapter-outlining.

## Step 5: Chapter Rough Division

**One-shot mode:** Plan the rhythm for the entire novel.
**Volume mode:** Plan only the current volume's rhythm.

Plan the pacing rhythm:

1. Estimate total chapter count
2. Assign each act/section its chapter range
3. Mark which chapters are **high-intensity** (action, revelation, climax) vs **low-intensity** (breathing room, character development)
4. Ensure the rhythm follows: tension → release → tension → release (never 3+ chapters of the same intensity)
5. Mark **climax chapters** (these need more words and tighter pacing)
6. Mark **transition chapters** (these should be shorter and faster)

Present as a table:

```markdown
| Act | Chapters | Intensity | Focus |
|-----|----------|-----------|-------|
| Act 1 | 1-5 | Medium → High | Setup, inciting event |
| Act 2a | 6-12 | High → Low → High | Rising action, midpoint |
| Act 2b | 13-18 | High → Lowest → High | Descent, darkest moment |
| Act 3 | 19-23 | Highest → Resolution | Climax, denouement |
```

## Step 6: Self-Review

After designing the complete plot:

1. **Arc continuity:** Does every turning point push the protagonist toward their B state?
2. **Subplot convergence:** Do all subplots connect to the main plot?
3. **Dead end check:** Are there any story paths that lead nowhere?
4. **Foreshadowing needs:** What needs to be planted early for later payoff?
5. **Character utilization:** Are all designed characters used in the plot?
6. **Pacing:** Is the rhythm sustainable for the estimated length?
7. **Relationship trajectory coherence:** Do relationship changes have clear triggers?

## Writing to story-bible.md

```markdown
## Plot

### Planning Mode: [One-shot / Volume-based]
### Chapters Per Volume: [if applicable, default 50]
### Structure: [Chosen structure name]

### Macro Architecture (Volume mode)
[Macro architecture content, if applicable]

### Current Volume Main Plot (Volume N)
- **Opening Hook:** [Description]
- **Inciting Event:** [Description]
- **Act 1 Turning Point:** [Description]
- **Midpoint:** [Description]
- **Act 2 Turning Point:** [Description]
- **Climax:** [Description]
- **Resolution:** [Description]

### Subplots
#### [Subplot Name]
- **Theme Served:** [What theme it explores]
- **Main Plot Connection:** [Where it intersects]
- **Characters:** [Who's involved]
- **Resolution:** [How it ends]

### Foreshadowing Plan
| # | What to Plant | Where (Chapter/Volume) | Payoff (Chapter/Volume) | Status |
|---|---------------|----------------------|------------------------|--------|
| | | | | |

### Relationship Trajectories (if applicable)
[Timeline of relationship changes with triggering events]

### Chapter Rough Division
| Act | Chapters | Intensity | Focus |
|-----|----------|-----------|-------|
| | | | |
```

## Red Flags

- Turning points that don't affect the protagonist
- Subplots with no connection to the main plot
- More than 3 subplots (too complex, readers will get lost)
- No clear resolution for each subplot
- Relationship changes without triggering events
- Pacing that's uniformly intense (no breathing room)
- Skipping relationship trajectory planning for complex-relationship novels
- Proceeding to chapter-outlining without user approval

## Key Principles

- **Character drives plot** — Every event should test the protagonist's flaw or push their arc
- **Subplots serve themes** — If it doesn't explore the theme, cut it
- **Less is more** — Fewer subplots, fewer characters, tighter story
- **Plant before payoff** — Foreshadowing must be planned before writing
- **Pacing is rhythm** — Alternate intensity like breathing

## Integration

**Previous skill:** supernovel:character-design (provides character profiles)
**Next skill:** supernovel:chapter-outlining (expands plot into detailed chapter plans)
**Updates:** story-bible.md (Plot section)
