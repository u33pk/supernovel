---
name: drafting
description: "Use when chapter outlines are approved and you need to draft chapters — writes chapters in batches of 5, strictly following outlines and batch plans. Updates story-bible.md after each batch."
---

# Drafting (5-Chapter Batches)

Write chapters in batches of 5, strictly following the approved outlines and batch plans. This is the prose-writing phase — all planning is done, now execute.

**Announce at start:** "I'm using the drafting skill to write Batch {N} (Chapters {X}-{Y})."

## When to Use

- After chapter-outlining produces approved batch plans and chapter outlines
- When the user says "start writing", "write chapter N", "begin drafting"

## Pre-Flight

Before writing ANY batch:

1. Read `story-bible.md` — ALL of it: World, Characters, Stats, Inventory, Relationships, Plot, Style
2. Read the batch plan for this batch
3. Read all 5 chapter outlines for this batch
4. If this is NOT the first batch: read ALL previous batch summaries
5. If stats/inventory exist: read current stats and inventory tables

**The Iron Law:**

```
NO PROSE WITHOUT READING THE STORY BIBLE AND BATCH PLAN FIRST.
```

## The Batch Writing Process

### For Each Batch of 5 Chapters:

```
1. READ: story-bible.md + batch plan + 5 chapter outlines + all previous batch summaries
   ↓
2. WRITE: Chapter N (following outline exactly)
   ↓
3. WRITE: Chapter N+1 (following outline exactly)
   ↓
4. WRITE: Chapter N+2 (following outline exactly)
   ↓
5. WRITE: Chapter N+3 (following outline exactly)
   ↓
6. WRITE: Chapter N+4 (following outline exactly)
   ↓
7. UPDATE: story-bible.md (stats, inventory, relationships if needed)
   ↓
8. SAVE: Chapters + batch summary
   ↓
9. INVOKE: supernovel:consistency-check for batch review
```

### Writing Rules

**Follow the outline exactly:**
- Scene order as specified
- Characters as specified (no additions without profiles)
- Conflict as specified
- Emotional arc as specified
- Do NOT "creatively deviate" from the outline
- If the outline feels wrong, STOP and ask the user — do not freelance

**Style adherence (from story-bible.md Style section):**

**Iron Law: The writing style MUST match the style defined in the story bible. If you notice style drift mid-batch, STOP and recalibrate.**

- POV as specified (first/third limited/omniscient)
- Tense as specified
- Description density as specified

**Style consistency rules:**
- **Sentence style:** If "Stark & Restrained" is chosen, don't suddenly produce ornate long sentences with elaborate metaphors; if "Ornate & Lush" is chosen, don't suddenly shift to telegraphic short bursts
- **Vocabulary level:** Colloquial style uses short words and slang; literary style uses longer words and imagery. Don't mix
- **Rhythm:** Sweeping Epic style alternates long and short sentences for impact; Gentle Narrative style maintains uniform sentence length for steady pace. Review the style definition at the start of each batch; self-check for drift at the end
- **Narrative distance:** Stark style keeps distance from characters (less inner monologue); Healing style stays close to character interiority (more feelings). Don't shift between close and distant within the same batch
- **Emotional expression:** Stark style implies emotion through action and environment; Ornate style directly describes emotional imagery. Once chosen, don't randomly switch

**Character voice:**

**Iron Law: Each character's dialogue must be identifiable without dialogue tags. This is not a suggestion — it's a hard requirement.**

- Each character must speak according to their defined speech pattern in their profile
- Reference the example lines from the character profile (covering calm, angry, intimate, crisis states)
- No character should "sound like" another character
- The same character can vary across emotional states, but core traits (word choice habits, sentence length, catchphrases) stay consistent
- If Character A's dialogue could be seamlessly given to Character B → character voice design has failed, STOP and recalibrate
- Dialogue must not include catchphrases or signature expressions not defined in the character profile
- Internal monologue and self-talk must also match the character's speech pattern — don't slip into the author's narration voice

**Prose quality:**
- Show, don't tell (for emotional moments)
- Vary sentence length (no 10 consecutive short sentences, no 10 consecutive long ones)
- Avoid repeated words within the same paragraph
- Each paragraph should have a clear purpose
- Dialogue should advance plot or reveal character — not fill space

### Ending Variety (CRITICAL)

Each chapter ending MUST follow the ending type specified in the chapter outline. If the outline specifies "Cliffhanger", write a cliffhanger. If it specifies "Quiet beat", write a quiet beat.

**Never:**
- Use the same ending type as the previous chapter
- End every chapter with a character "falling asleep" or "looking at the sky"
- End with "and then everything changed" type vague statements

### After Writing Each Chapter

Save to: `docs/supernovel/drafts/chapter-NN.md`

Do NOT pause between chapters in a batch. Write all 5 chapters, then do the batch review.

## After the Batch (5 Chapters Written)

### Step 1: Update story-bible.md

After all 5 chapters are written, update the story bible:

**Stats (if needs_stats):**
- Apply any stat changes that occurred in these 5 chapters
- Update the current stats table
- Append to the stat change log

**Inventory (if needs_inventory):**
- Add acquired items, remove used/lost items
- Update equipment changes
- Append to the change log

**Relationships (if needs_relationship_map):**
- Update any relationship changes with triggering events
- Update alliance/group status
- Append to the relationship change log

**Chapter Summaries:**
Write a summary for each chapter in story-bible.md:

```markdown
### Chapter [N]: [Title]
- **POV:** [Character]
- **Key Events:** [2-3 bullet points]
- **Character Arc Progress:** [How the protagonist changed]
- **New World Details Added:** [Any new details added to the world]
- **Stats/Inventory Changes:** [If applicable]
- **Relationship Changes:** [If applicable]
```

### Step 2: Write Batch Summary

Create a batch summary document:

```markdown
# Batch [N] Summary: Chapters [X]-[Y]

## What Happened
[2-3 paragraph narrative summary of these 5 chapters]

## Key Events
- [Event 1]
- [Event 2]
- ...

## Character Status
| Character | Status at End of Batch | Arc Progress |
|-----------|----------------------|--------------|
| | | |

## Stats/Inventory Changes (if applicable)
[Summary of all numerical changes]

## Relationship Changes (if applicable)
[Summary of all relationship shifts]

## Foreshadowing Status
| Planted | Expected Payoff | Status |
|---------|----------------|--------|
| | | |

## Writing Pattern Notes
[Self-check: Did I repeat any patterns? Did I vary endings?
Did I give any character too much/too little screen time?
**Style check:** Is the writing style consistent with the story bible's Style section? Any drift toward "model default style"?
**Voice check:** Is each character's dialogue distinctive? Could Character A's lines be seamlessly given to Character B?]
```

Save to: `docs/supernovel/batch-summaries/batch-N-summary.md`

### Step 3: Invoke Consistency Check

After completing the batch, invoke `supernovel:consistency-check` to review the batch.

## The TBD Resolution Rule

Chapter outlines may contain `[TBD]` items. These MUST be resolved during drafting:

- When you encounter a `[TBD]` in an outline, STOP
- Present the context and options to the user
- Get user decision
- Update the outline and story-bible.md
- Continue writing

Never fill in a `[TBD]` without asking the user.

## Red Flags

- Writing prose without reading story-bible.md first
- Deviating from the approved outline
- Same ending type for consecutive chapters
- Character acting out of profile (saying/doing something inconsistent)
- Introducing a character not in story-bible.md
- Not updating stats/inventory after a batch
- Skipping batch summary writing
- Filling in [TBD] items without asking the user
- "Creatively" adding scenes not in the outline
- Every chapter having the same paragraph structure
- Writing style drifting to "model default" (suddenly ornate / suddenly colloquial)
- Character dialogue that could be swapped between characters (A's lines work for B too)
- Same character's speech varying too much across scenes (losing identifiability)

## Key Principles

- **Outline is law** — Follow it exactly; if it's wrong, ask the user
- **Style is consistent** — Adhere to the Style section of story-bible.md
- **Characters are consistent** — Voice, behavior, abilities must match profiles
- **Numbers are accurate** — Stats and inventory must reflect actual events
- **Relationships evolve** — Update after each batch, not just at the end
- **Batch memory** — Write batch summaries for future meta-review

## Integration

**Previous skill:** supernovel:chapter-outlining (provides batch plans and outlines)
**Next skill:** supernovel:consistency-check (reviews each batch)
**Reads:** story-bible.md (everything), batch plans, chapter outlines, previous batch summaries
**Updates:** story-bible.md (Stats, Inventory, Relationships, Chapter Summaries)
**Output:** docs/supernovel/drafts/chapter-NN.md, docs/supernovel/batch-summaries/batch-N-summary.md
