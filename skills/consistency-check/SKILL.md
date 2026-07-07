---
name: consistency-check
description: "Use after drafting a batch of 5 chapters — verifies consistency against the story bible, detects repetitive patterns, and performs meta-review every 5 batches. Two-level review: batch review + meta-review."
---

# Consistency Check (Two-Level Review)

Verify every batch of 5 chapters against the story bible. Detect repetitive patterns, factual errors, and style monotony. Every 5 batches (25 chapters), perform a meta-review against all batch summaries.

**Announce at start:** "I'm using the consistency-check skill to review Batch {N}."

## When to Use

- After drafting completes a batch of 5 chapters
- After revision makes significant changes
- When the user says "check consistency", "review this batch"

## The Two-Level Review System

```
Level 1: Batch Review (every 5 chapters)
  → Checks this batch against story-bible.md and batch plan
  → Detects within-batch repetition and inconsistencies
  → Updates story-bible.md

Level 2: Meta-Review (every 5 batches = 25 chapters)
  → Reviews all batch summaries together
  → Detects cross-batch patterns and long-term drift
  → Checks overall story arc progress
  → Verifies foreshadowing schedule
```

---

## Level 1: Batch Review

### Pre-Flight

1. Read `story-bible.md` — ALL sections
2. Read the batch plan for this batch
3. Read all 5 chapter outlines for this batch
4. Read the drafted chapters (all 5)
5. If not first batch: read all previous batch summaries

### The Review Checklist

#### 1. Factual Consistency (vs story-bible.md)

Check every chapter against the story bible:

| Check | What to Verify |
|-------|---------------|
| **Characters** | Names spelled consistently, ages correct, appearances match |
| **World** | Place names correct, geography consistent, rules followed |
| **Power System** | Abilities match established rules, no new powers invented |
| **Timeline** | Events in correct order, time references consistent |
| **Stats** | Numbers match current stats table (if applicable) |
| **Inventory** | Characters don't use items they don't have (if applicable) |
| **Relationships** | Attitudes match current relationship status (if applicable) |

#### 2. Repetition Detection (Anti-Laziness)

This is CRITICAL. Check for patterns the model repeats when "lazy":

**Sentence-level repetition:**
- Same sentence structure used across multiple chapters
- Same transition phrases
- Same paragraph patterns (every paragraph starts with character name)

**Ending repetition:**
- Same ending type across consecutive chapters
- Same cliffhanger structure
- Same "character falls asleep" / "looks at sky" endings

**Action repetition:**
- Same body language for the same character across chapters
- Same verbs used repeatedly
- Same reaction patterns (every surprise → eyes widen, every anger → fists clench)

**Character overexposure:**
- Same character appearing in all 5 chapters when the batch plan says otherwise
- Supporting characters completely absent when they should be present
- POV character always alone (no variety in interaction dynamics)

**Pattern detection table:**

| Pattern Type | Ch.1 | Ch.2 | Ch.3 | Ch.4 | Ch.5 | Issue? |
|-------------|------|------|------|------|------|--------|
| Ending type | | | | | | |
| Opening type | | | | | | |
| POV character | | | | | | |
| Dominant emotion | | | | | | |
| Dialogue ratio | | | | | | |

Fill in this table. If any row shows repetition → flag as issue.

#### 3. Batch Plan Adherence

Compare drafted chapters against the batch plan:
- Did the planned events actually happen?
- Did the pacing rhythm match the plan?
- Were the planned foreshadowing operations executed?
- Did character appearances match the plan?

#### 4. Character Consistency

For each character that appears in this batch:
- **Voice:** Does their dialogue match their speech pattern from the profile?
- **Behavior:** Do their actions match their personality traits?
- **Arc:** Is their development progressing as planned?
- **Knowledge:** Do they only know what they should know at this point?
- **Abilities:** Do they only use abilities they actually have?

#### 5. Stats/Inventory Accuracy (if applicable)

- Every stat change event → verify the math is correct
- Every equipment change → verify old item removed, new item added
- Every skill use → verify the character actually has that skill at that level
- Battle outcomes → verify they make sense given the numbers

#### 6. Relationship Consistency (if applicable)

- Character A's attitude toward Character B must match their current relationship status
- If a betrayal hasn't happened yet, characters can't act like it has
- Alliance members should behave consistently with group membership
- Trust levels should match the current state in the relationship network

### Issue Classification

| Severity | Definition | Action |
|----------|-----------|--------|
| **Critical** | Direct contradiction with story-bible.md (dead character alive, destroyed city intact, wrong stats) | MUST fix before proceeding |
| **Important** | Character personality inconsistency, timeline confusion, repetitive pattern | SHOULD fix before proceeding |
| **Minor** | Word repetition, slight pacing issue, minor style inconsistency | Note in summary, fix if time permits |

### After Batch Review

1. **Fix Critical issues** — invoke `supernovel:revision` or fix inline
2. **Fix Important issues** — same
3. **Record Minor issues** — note in batch summary for later
4. **Update story-bible.md** — if the review found new details that should be tracked
5. **Write/update batch summary** — including review findings

---

## Level 2: Meta-Review (Every 5 Batches / 25 Chapters)

### When to Trigger

After every 5th batch summary is written. The meta-review compares all 5 batch summaries to detect long-term patterns.

### Meta-Review Checklist

#### 1. Story Arc Progression

Read all 5 batch summaries. Check:
- Is the protagonist's arc progressing toward the B state?
- Is the pacing (from the chapter rough division) being followed?
- Are we on track for the planned turning points?
- Has the story deviated from the plot architecture?

#### 2. Long-Term Repetition Patterns

Across 25 chapters, check:
- **Character dominance:** Has one character appeared in 80%+ of chapters?
- **Setting monotony:** Have most scenes been in the same location?
- **Conflict type:** Has every chapter had the same type of conflict?
- **Emotional range:** Has the emotional palette been too narrow?
- **Sentence style drift:** Has the writing style degraded or become monotone?

#### 3. Foreshadowing Audit

Check the foreshadowing tracker:
- Are planned payoffs on schedule?
- Have any planted foreshadowing elements been forgotten?
- Are there payoffs that have no corresponding plant?
- Should any foreshadowing be moved to earlier/later chapters?

#### 4. Character Arc Audit

For each major character:
- How much has their arc progressed in these 25 chapters?
- Is the progress too fast, too slow, or on track?
- Have they had enough screen time relative to their importance?
- Have their relationships evolved as planned?

#### 5. Stats/Inventory Integrity (if applicable)

Across 25 chapters of stat changes:
- Are the numbers still internally consistent?
- Has the power scaling been reasonable (no sudden jumps)?
- Is the protagonist's growth pace appropriate for the story's timeline?
- Are there any mathematical errors accumulated?

#### 6. Relationship Network Health (if applicable)

Across 25 chapters:
- Have all planned relationship changes occurred on schedule?
- Are there relationship threads that have been forgotten?
- Is the relationship complexity manageable?
- Do character attitudes match the latest relationship matrix?

### Meta-Review Output

Save to: `docs/supernovel/meta-reviews/meta-review-N.md`

```markdown
# Meta-Review [N]: Chapters [1]-[25]

## Story Arc Status
[Is the overall story on track?]

## Repetition Patterns Detected
[Any long-term patterns found]

## Foreshadowing Audit
[Status of all planned plants/payoffs]

## Character Arc Progress
| Character | Arc Progress | On Track? | Notes |
|-----------|-------------|-----------|-------|
| | | | |

## Relationship Network Status (if applicable)
[Summary of relationship evolution]

## Stats Integrity (if applicable)
[Power scaling assessment]

## Recommendations
[What adjustments are needed for the next 25 chapters?]
```

---

## Red Flags

- Skipping the repetition detection table
- Accepting "should work" without verifying numbers
- Marking Critical issues as Important to avoid fixing them
- Not checking against ALL previous batch summaries
- Skipping meta-review because "the story seems fine"
- Not updating story-bible.md after finding new details
- Trusting the drafting skill's self-assessment without independent verification

## Key Principles

- **Evidence before claims** — Run the checks, then state the verdict
- **Repetition is the enemy** — The #1 sign of model laziness
- **Numbers don't lie** — Stats/inventory must be mathematically consistent
- **Relationships must evolve** — Static relationships in a dynamic story = bug
- **Meta-review catches drift** — Single-batch review can't see long-term patterns

## Integration

**Previous skill:** supernovel:drafting (produces the chapters and batch summary)
**Next skill:** supernovel:revision (fixes issues found), or supernovel:drafting (next batch)
**Reads:** story-bible.md, batch plans, chapter outlines, all previous batch summaries
**Updates:** story-bible.md, batch summaries
**Output:** Issue reports, meta-review documents
