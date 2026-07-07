---
name: revision
description: "Use when consistency check reveals issues, or when you need to revise drafted content for style, pacing, or quality. Systematic, one-problem-at-a-time editing with re-verification."
---

# Systematic Revision

Fix issues found by consistency-check, or improve prose quality. One problem at a time, never bundled. Every fix must be re-verified.

**Announce at start:** "I'm using the revision skill to fix issues in Chapter {N}."

## The Iron Law

```
ONE FIX AT A TIME. VERIFY AFTER EVERY FIX.
```

Do not bundle multiple fixes. Do not "improve" unmarked content while fixing a specific issue.

## When to Use

- After consistency-check reports Critical or Important issues
- When the user requests style/pacing changes
- When the user says "revise this", "rewrite this", "fix the pacing"
- After a meta-review recommends adjustments

## Pre-Flight

1. Read the consistency-check report (issue list with severity)
2. Read the affected chapter(s)
3. Read the relevant section of story-bible.md
4. Prioritize: Critical first, then Important, then Minor

## The Process

### For Each Issue:

```
1. IDENTIFY: What exactly is wrong? (cite chapter:paragraph)
   ↓
2. ROOT CAUSE: Why did this happen?
   - Factual error (contradicts story-bible.md)?
   - Character inconsistency (wrong voice/behavior)?
   - Repetitive pattern (lazy writing)?
   - Pacing issue (too fast/slow)?
   - Style issue (awkward phrasing)?
   ↓
3. PLAN: What is the minimal change to fix this?
   ↓
4. APPLY: Make the change
   ↓
5. VERIFY: Read the result. Does it:
   - Fix the original issue?
   - Not break anything else?
   - Maintain consistency with story-bible.md?
   - Preserve the chapter's emotional arc?
   ↓
6. UPDATE: If the fix changes factual details, update story-bible.md
```

### Revision Types

| Type | What Changes | What Doesn't Change |
|------|-------------|-------------------|
| **Factual correction** | Wrong details → correct details | Everything else |
| **Character voice fix** | Dialogue rewritten to match profile | Plot, events |
| **Repetition fix** | Sentence structure varied | Content, meaning |
| **Pacing fix** | Scene length adjusted | Events, characters |
| **Style polish** | Word choice, flow | Meaning, content |
| **Stats/inventory fix** | Numbers corrected | Narrative |

### Rules

- **Never change unmarked content.** If the consistency-check flagged paragraph 3, do not also "improve" paragraph 5.
- **Preserve the author's voice.** The style section of story-bible.md defines the voice. Don't override it with your preferences.
- **Re-verify after every fix.** Read the changed paragraph in context. Does it still flow?
- **Update story-bible.md.** If a fix changes a factual detail (character name spelling, location name, stat value), update the bible.
- **Re-run consistency check.** After all fixes are applied, re-run the consistency check on the affected chapters.

### After Revision

1. List all changes made
2. Re-run consistency check on affected chapters
3. If all issues resolved → proceed to next batch or next chapter
4. If new issues found → continue revision cycle

## Red Flags

- Fixing multiple issues in one edit
- "Improving" content that wasn't flagged
- Changing the story's voice or tone during revision
- Not re-verifying after fixes
- Skipping story-bible.md updates after factual corrections
- Making the prose "better" when the issue was factual (scope creep)

## Key Principles

- **Minimal changes** — Fix only what's broken
- **One at a time** — Bundled fixes make it hard to identify what helped
- **Verify always** — Every fix must be checked
- **Bible is truth** — If the fix contradicts the story bible, the fix is wrong

## Integration

**Previous skill:** supernovel:consistency-check (finds the issues)
**Next skill:** supernovel:drafting (next batch) or supernovel:finishing (all done)
**Reads:** Consistency-check report, affected chapters, story-bible.md
**Updates:** Affected chapters, story-bible.md (if factual corrections)
