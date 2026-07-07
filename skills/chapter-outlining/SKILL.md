---
name: chapter-outlining
description: "Use when plot architecture is approved and you need detailed chapter outlines before drafting. Plans chapters in batches of 5 with batch-level consistency checks."
---

# Chapter Outlining (5-Chapter Batches)

Plan chapters in batches of 5. Each batch gets a batch plan before writing, and a batch review after writing. This prevents the model from "cutting corners" by catching repetitive patterns across chapters.

**Announce at start:** "I'm using the chapter-outlining skill to plan chapter outlines."

<HARD-GATE>
Do NOT invoke the drafting skill until at least the first batch of 5 chapters has been outlined and approved. Every scene must have a purpose.
</HARD-GATE>

## When to Use

- After plot-architecture produces an approved Plot section in story-bible.md
- When the user says "outline chapters", "plan the chapters"
- Before drafting (outlines are the drafting blueprint)

## Pre-Flight

1. Read `story-bible.md` — especially Plot (turning points, chapter rough division), Characters, and World
2. Read the chapter rough division from plot-architecture
3. Calculate total batches: `ceil(total_chapters / 5)`

## The 5-Chapter Batch System

### Why Batches of 5?

Writing and reviewing one chapter at a time causes:
- **Repetitive endings** — model uses the same cliffhanger pattern every chapter
- **Repetitive actions** — same verbs, same body language across chapters
- **Character overexposure** — same character appears in every chapter
- **No cross-chapter pattern detection** — can't spot monotony in single-chapter review

Batching solves this by:
- Planning 5 chapters together (ensures variety)
- Reviewing 5 chapters together (detects repetition)
- Summarizing each batch (creates memory for meta-review)

### Batch Structure

```
For each batch of 5 chapters:
  1. Write Batch Plan (BEFORE writing)
     - Overall arc for this batch
     - Characters appearing in each chapter
     - Pacing rhythm across the 5 chapters
     - Foreshadowing to plant/payoff
  2. Write all 5 chapters (during drafting)
  3. Batch Review (AFTER writing all 5)
     - Check against batch plan
     - Detect repetition patterns
     - Update story-bible.md
     - Write batch summary
```

## The Process

### Step 1: Create Batch Plan

For each batch of 5 chapters, create a batch plan BEFORE outlining individual chapters.

**Batch Plan Template:**

```markdown
# Batch N: Chapters [X]-[Y]

## Batch Arc
[What is the overall trajectory of these 5 chapters? Where does the story
start at Ch.X and where is it at Ch.Y?]

## Characters Appearing
| Chapter | POV | Characters Present | Notes |
|---------|-----|--------------------|-------|
| Ch.X | | | |
| Ch.X+1 | | | |
| Ch.X+2 | | | |
| Ch.X+3 | | | |
| Ch.X+4 | | | |

**Character variety check:** No character should appear in all 5 chapters
unless they are the POV character. If the protagonist appears in every
chapter, at least vary the supporting cast.

## Pacing Rhythm
| Chapter | Intensity | Type | Notes |
|---------|-----------|------|-------|
| Ch.X | | [Action/Dialog/Reflection/Transition/Revelation] | |
| Ch.X+1 | | | |
| Ch.X+2 | | | |
| Ch.X+3 | | | |
| Ch.X+4 | | | |

**Pacing rules:**
- No 3+ consecutive chapters of the same intensity level
- No 2+ consecutive chapters of the same type (e.g., two pure-dialogue chapters)
- At least 1 chapter in each batch should be a "breathing room" chapter

## Foreshadowing Operations
| Chapter | Plant | Payoff | Notes |
|---------|-------|--------|-------|
| | | | |

## Expected Key Events
[List the 3-5 most important things that happen in this batch]
```

### Step 2: Outline Individual Chapters

After the batch plan is approved, expand each chapter into a detailed outline.

**Chapter Outline Template:**

```markdown
# Chapter [N]: [Working Title]

**POV:** [Character Name]
**Type:** [Action / Dialogue / Reflection / Transition / Revelation]
**Estimated Length:** [word count range]

## Scenes

### Scene 1: [Scene Title]
- **Location:** [Where]
- **Characters:** [Who is present]
- **Action:** [What happens]
- **Emotion:** [Emotional tone of this scene]
- **Purpose:** [Why this scene exists — "entertaining" is not enough]

### Scene 2: [Scene Title]
...

## Core Conflict
[What tension drives this chapter? What does the POV character want
vs. what stands in their way?]

## Plot Advancement
[What irreversible change happens in this chapter? If you removed this
chapter, what would be lost?]

## Emotional Arc
[Opening emotion] → [Closing emotion]

## Foreshadowing
- **Plant:** [What is planted in this chapter]
- **Payoff:** [What is paid off from an earlier chapter]

## Chapter Ending
[How does this chapter end? What is the hook that makes the reader
turn the page? NOTE: This must be DIFFERENT from the previous chapter's
ending style. See Ending Variety Rules below.]
```

### Ending Variety Rules

Across a batch of 5 chapters, chapter endings MUST vary. Track the ending type and ensure no repetition:

| Ending Type | Description |
|-------------|-------------|
| **Cliffhanger** | Dangerous situation, unresolved tension |
| **Revelation** | A truth is revealed that changes understanding |
| **Quiet beat** | Reflective moment, emotional processing |
| **Decision** | Character makes a crucial choice |
| **Question** | A new mystery or question is raised |
| **Irony** | Reader knows something character doesn't |
| **Callback** | References an earlier moment with new meaning |

**Rule:** No two consecutive chapters may use the same ending type.
Within a batch of 5, use at least 3 different types.

### Step 3: Self-Review (Per Batch)

After outlining all 5 chapters in a batch, review:

1. **Batch plan adherence:** Does each chapter match the batch plan?
2. **Character variety:** Is any character overexposed (appears in all 5)?
3. **Pacing rhythm:** Are there 3+ consecutive same-intensity chapters?
4. **Ending variety:** Are consecutive endings different types?
5. **Scene purpose:** Does every scene have a clear story purpose?
6. **Continuity:** Does each chapter connect logically to the next?
7. **Foreshadowing:** Are all planned plants/payoffs included?

### Step 4: Save Outlines

Save each chapter outline to:

```
docs/supernovel/outlines/batch-N/chapter-NN-outline.md
```

Save the batch plan to:

```
docs/supernovel/outlines/batch-N/batch-plan.md
```

### Step 5: User Review

After each batch's outlines are complete, ask the user:

> "Batch {N} (Chapters {X}-{Y}) outlines are complete. Please review. After confirmation, we can start the next batch or begin writing."

## Meta-Planning: All Batches Overview

After all batch plans are created (or after the first few batches), create an overview:

```markdown
# All Batches Overview

| Batch | Chapters | Focus | Key Events | Foreshadowing |
|-------|----------|-------|------------|---------------|
| 1 | 1-5 | | | |
| 2 | 6-10 | | | |
| ... | ... | | | |

## Cross-Batch Foreshadowing Tracker
| Plant (Batch/Chapter) | Expected Payoff (Batch/Chapter) | Status |
|----------------------|--------------------------------|--------|
| | | |
```

## Rules

- **Batch plans come first** — Never outline individual chapters without a batch plan
- **No consecutive same-type endings** — Enforced across each batch
- **Character variety** — No character in all 5 chapters unless POV character
- **Pacing alternation** — No 3+ chapters of same intensity
- **Every scene needs purpose** — "Entertaining" is not a purpose
- **Foreshadowing is tracked** — Every plant must have a planned payoff location

## Red Flags

- Writing outlines without a batch plan
- Same ending type for consecutive chapters
- Same 3 characters appearing in all 5 chapters
- All 5 chapters at the same intensity level
- Scenes that exist "to fill space" with no story purpose
- Foreshadowing planted without a planned payoff chapter
- Skipping user review before moving to the next batch

## Integration

**Previous skill:** supernovel:plot-architecture (provides structure and turning points)
**Next skill:** supernovel:drafting (writes chapters based on these outlines)
**Updates:** story-bible.md (adds batch summaries after drafting)
**Output:** docs/supernovel/outlines/batch-N/batch-plan.md + chapter-NN-outline.md
