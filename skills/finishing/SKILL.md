---
name: finishing
description: "Use when all chapters are drafted and consistency checks pass — final review across the entire novel, formatting, and delivery options."
---

# Finishing

Final review and delivery of the completed novel. Cross-chapter verification, formatting, and presentation of delivery options.

**Announce at start:** "I'm using the finishing skill for final review."

## When to Use

- All chapters are drafted and batch reviews are complete
- All meta-reviews show no Critical issues
- The user says "finalize", "wrap up", "deliver the novel"

## Pre-Flight

1. Read `story-bible.md` — ALL sections
2. Read ALL batch summaries
3. Read ALL meta-reviews
4. Count total chapters drafted

## The Process

### Step 1: Final Consistency Sweep

A quick but comprehensive cross-chapter check:

- **Character names:** Are all names spelled consistently across ALL chapters?
- **Location names:** Same check
- **Timeline:** Is the overall timeline consistent?
- **Stats integrity (if applicable):** Final math verification across all chapters
- **Inventory final state (if applicable):** Does the final inventory make sense?
- **Relationship final state (if applicable):** Does it match the planned ending?

### Step 2: Pacing Review

Read chapter summaries in sequence:

- Are there sections where 3+ chapters have the same intensity?
- Are there chapters that feel too long or too short relative to their importance?
- Is the climax adequately paced (not rushed, not dragged)?
- Does the resolution feel earned?

### Step 3: Foreshadowing Final Audit

Check every planted foreshadowing element:

- Was every plant paid off?
- Was every payoff properly planted?
- Are there orphaned plants (planted but never paid off)?
- Are there unmotivated payoffs (paid off but never planted)?

### Step 4: Present Delivery Options

Use AskUserQuestion to present exactly these options:

```
All chapters complete, consistency checks passed. What would you like to do?

1. Merge into complete manuscript
   — Combine all chapters into a single file

2. Keep chapters separate
   — Maintain the current chapter file structure

3. Export story bible
   — Save story-bible.md as a standalone reference document

4. Clean up drafts and outlines
   — Keep final manuscript, delete intermediate drafts and outlines

5. Keep everything
   — Don't delete any files
```

### Step 5: Execute Choice

**Option 1: Merge into complete manuscript**
- Concatenate all chapter files in order
- Add title page with novel title
- Add table of contents
- Save to `docs/supernovel/final/[title]-complete.md`

**Option 2: Keep chapters separate**
- Report: "Chapter files remain in `docs/supernovel/drafts/`"

**Option 3: Export story bible**
- Copy story-bible.md to `docs/supernovel/final/story-bible-final.md`
- Remove [TBD] markers (all should be resolved)
- Clean up change logs (keep only final state)

**Option 4: Clean up drafts**
- Keep `docs/supernovel/final/` and `story-bible.md`
- Remove `docs/supernovel/drafts/`
- Remove `docs/supernovel/outlines/`
- Remove `docs/supernovel/batch-summaries/`
- Keep `docs/supernovel/meta-reviews/` (useful for series continuations)

**Option 5: Keep everything**
- Report: "All files remain unchanged"

## Red Flags

- Skipping the final consistency sweep
- Not checking foreshadowing completion
- Deleting files without user confirmation
- Not offering all delivery options
- Merging chapters without fixing known issues first

## Key Principles

- **Final verification** — One last check before declaring done
- **User choice** — Let the user decide what to keep
- **Clean delivery** — The final product should be polished and ready

## Integration

**Previous skill:** supernovel:consistency-check (final batch review passed)
**Reads:** story-bible.md, all batch summaries, all meta-reviews
**Output:** Final manuscript, cleaned story bible, or preserved file structure
