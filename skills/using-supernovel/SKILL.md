---
name: using-supernovel
description: Use when starting any conversation about writing a novel - establishes how to find and use skills, requiring skill invocation before ANY response including clarifying questions
---

<SUBAGENT-STOP>
If you were dispatched as a subagent to execute a specific task, ignore this skill.
</SUBAGENT-STOP>

<EXTREMELY-IMPORTANT>
If you think there is even a 1% chance a skill might apply to what you are doing, you ABSOLUTELY MUST invoke the skill.

IF A SKILL APPLIES TO YOUR TASK, YOU DO NOT HAVE A CHOICE. YOU MUST USE IT.

This is not negotiable. You cannot rationalize your way out of this.
</EXTREMELY-IMPORTANT>

## The Rule

**Invoke relevant or requested skills BEFORE any response or action** — including clarifying questions, exploring files, or checking the project. If it turns out wrong for the situation, you don't have to use it.

Then announce "Using [skill] to [purpose]" and follow the skill exactly. If it has a checklist, create a todo per item.

## Skill Priority

When multiple skills apply, process skills come first — they set the approach, then writing skills carry it out.

- "I want to write a novel" / "Let's write a story" → supernovel:brainstorming first
- "Let's design the world" / "I need a setting" → supernovel:worldbuilding
- "I need characters" / "Design the protagonist" → supernovel:character-design
- "Plan the plot" / "Structure the story" → supernovel:plot-architecture
- "Outline chapters" / "Break it into chapters" → supernovel:chapter-outlining
- "Write chapter N" / "Draft the next chapter" → supernovel:drafting
- "Check consistency" / "Review this chapter" → supernovel:consistency-check
- "Revise this" / "Edit the draft" / "Fix the pacing" → supernovel:revision
- "Finalize" / "Wrap up" / "Deliver the novel" → supernovel:finishing

## Red Flags

These thoughts mean STOP — you're rationalizing:

| Thought | Reality |
|---------|---------|
| "I'll just start writing" | You need an approved outline first. Check for skills. |
| "The idea is clear enough" | Skills tell you HOW to clarify. Check first. |
| "This is a simple story" | Simple stories need structure too. Use the skills. |
| "I know the character already" | Write a profile first. Memory fades. Skills prevent this. |
| "Let me just draft one chapter" | Drafting without outline = guaranteed rework. |
| "I'll fix consistency later" | Inconsistencies compound. Check now, not later. |
| "The user wants to see progress" | Progress without structure is chaos. Skills prevent this. |
| "I don't need a world bible" | You WILL contradict yourself by chapter 5. |
| "This doesn't need a formal skill" | If a skill exists, use it. |
| "I remember this skill" | Skills evolve. Read current version. |
| "The skill is overkill" | Simple things become complex. Use it. |
| "I'll just do this one thing first" | Check BEFORE doing anything. |

## The Story Bible

Every novel project MUST maintain a `story-bible.md` in the project root. This is the single source of truth for all story elements: world settings, character profiles, plot threads, foreshadowing, timeline, and style guidelines.

**No detail is "official" until it appears in the Story Bible.**

When starting a new project, if `story-bible.md` does not exist, the worldbuilding skill will create it. Every subsequent skill reads from and updates the Story Bible.

## Platform Adaptation

- Claude Code: uses hook-based injection (hooks/hooks.json)
- Kimi Code: uses sessionStart.skill injection (native)

## User Instructions

User instructions (direct requests) take precedence over skills, which in turn override default behavior. Only skip skill workflows or instructions when your human partner has explicitly told you to.
