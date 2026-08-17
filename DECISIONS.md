# DECISIONS.md

A running log of judgment calls made during this build — the things git diffs can't show on their own: what was tried, what got rejected, and why. Append an entry whenever a real decision happens, not every edit.

**When to log something here (ask "log that" or Claude Code logs proactively):**
- A direction was chosen over a real alternative (not just "I picked an option," but "I built/considered two things and picked one")
- Something was built, then reverted or cut
- A reframe happened — tone, structure, or approach changed mid-stream
- A piece of content moved somewhere else for a reason (not just relocated, but *because* it fit better elsewhere)
- A naming/labeling decision that took more than one attempt to land

**When NOT to log:** routine edits, typo fixes, small copy tweaks, anything git already tells the whole story on by itself.

---

## Entry format

```
### [Short title of the decision]
**Category:** Structural | Content | Tone/Register | Visual | Naming | Cut
**Date/session:**
**What happened:** One or two sentences — what was tried, what was chosen, what was rejected.
**Why:** The actual reasoning. This is the part git can never capture.
```

---

## Log

<!-- Entries go below this line, most recent first -->

> **Note on Session 1:** These entries were reconstructed after the fact from the working chat transcript — Session 1 predates the repo, so there is no git history for it. Only three HTML snapshots survived (v1, v2, v14); most of the decisions below happened in the gaps between them and would be invisible without the transcript. Session 2 onward is captured in git and can be logged live.

### Handoff to Claude Code
**Category:** Structural
**Date/session:** Session 1 (pre-git) · captured as snapshot v14
**What happened:** Produced a full master prompt (design system, page structure, bento logic, all eight phases' state, open items) and moved the build from the chat into Claude Code.
**Why:** The concept had stabilized enough that faster, file-based iteration would beat continuing in conversation. v14 is the exact file that became repo commit #1.

### Warm/cream palette replaced with the unified teal system
**Category:** Visual
**Date/session:** Session 1 (pre-git) · between v2 and v14
**What happened:** Retired the tan/cream palette on the summary and tile blocks in favor of one teal system (shell #12363a and its tints); page background settled at #FCFCFC, body type at Merriweather.
**Why:** Cohesion. The warm blocks read as a different project from the teal tracker; one system makes the page look designed rather than assembled.

### "Work Tie-Ins" block removed
**Category:** Cut
**Date/session:** Session 1 (pre-git) · between v2 and v14
**What happened:** A per-phase "Work Tie-Ins" block, present since the first hub draft, was cut entirely. The underlying data was left in place, unrendered.
**Why:** Once the bento pass landed, it was redundant with the other blocks — it repeated content rather than adding a distinct read.

### "From My Own Story" renamed "Entering This Phase:"
**Category:** Naming
**Date/session:** Session 1 (pre-git) · captured in v14
**What happened:** The per-phase opening block was retitled, with the name explicitly flagged as still unresolved.
**Why:** "From My Own Story" over-committed to memoir; "Entering This Phase" reads as a frame anyone can use. Kept as a placeholder pending a firmer concept.

### "Observations & Experience" merged, then split internally
**Category:** Structural
**Date/session:** Session 1 (pre-git) · captured in v14
**What happened:** Two separate tiles — "What This Phase Comprised" and "What I Observed" — were merged into one "Observations & Experience" tile, which was then split internally into "What Happened" and "Takeaways" columns.
**Why:** One tile with two columns reads as a single unit (what happened vs. what it taught) instead of two loosely related lists.

### Summary panel added above the tracker
**Category:** Structural
**Date/session:** Session 1 (pre-git) · between v2 and v14
**What happened:** Added a summary panel above the tracker — teal gradient, dark stroke, a miniature tracker, and a directional slide animation on phase change.
**Why:** The tracker is pure navigation; the summary panel gives the active phase a stable, legible home without cluttering the bar.

### Accordion (Option B) rejected for navigator + separate card (Option A)
**Category:** Cut
**Date/session:** Session 1 (pre-git) · between v2 and v14 (prototype never snapshotted)
**What happened:** Two segmented-bar treatments were mocked: (A) the bar as a navigator with a separate detail card, and (B) an accordion that expands a segment in place. A was chosen; B was built enough to compare, then discarded.
**Why:** The accordion crushed seven of eight segments to unreadable slivers to make room for the active one, undercutting the "eight phases, one journey" read the bar exists to create.

### Puzzle-piece grid prototype rejected
**Category:** Cut
**Date/session:** Session 1 (pre-git) · between v2 and v14 (prototype never snapshotted)
**What happened:** A 4×2 puzzle-piece grid navigator was fully built and interactive, then rejected in favor of the sequential tracker.
**Why:** A puzzle implies peer, non-sequential pieces forming one picture. The project's argument is exponential *progression* — each phase compounding on the last — which a sequential tracker argues structurally and a puzzle does not.

### Detail layout rebuilt as a bento grid; "Things I Built" → "Relevant Builds"
**Category:** Structural
**Date/session:** Session 1 (pre-git) · bento visible by v2, rename by v14
**What happened:** The flat stack of equal-width blocks was rebuilt as a mixed masonry (bento) grid; the "Things I Built" block was renamed "Relevant Builds."
**Why:** Bento matches tile shape to content and reads as designed. "Relevant Builds" frames the entries as evidence for the point, not a personal portfolio list.

### Full reframe: memoir → case study
**Category:** Tone/Register
**Date/session:** Session 1 (pre-git) · between v2 and v14
**What happened:** Every phase's copy was rewritten to lead with a generalized, transferable lesson, with personal specifics demoted to a supporting role.
**Why:** The story is the evidence, not the point. The page has to answer "what does this teach any average person approaching AI?" first, or it reads as biography.

### Thesis given a two-part lineage (Phase 02 → Phase 07)
**Category:** Content
**Date/session:** Session 1 (pre-git)
**What happened:** Rather than stating the thesis once, it was split: first *felt* in Phase 02 (the geopolitics what-if scenarios → "this is like writing my own little story"), then *proven* in Phase 07.
**Why:** A thesis that's felt before it's named lands harder than one announced up front — the reader arrives at it instead of being told it.

### Front-End Breakthrough demoted from a phase to a component
**Category:** Content
**Date/session:** Session 1 (pre-git) · componentized by v2
**What happened:** Originally scoped as its own Phase 03, the breakthrough was corrected to something smaller and earlier — realizing HTML could generate in-chat at all — and moved into Phase 02 as a callout. Phase 03 was left an explicit open slot; the "I wonder" mechanism was planted in Phase 04.
**Why:** The real breakthrough was a stumble-into-realization, not building an app. Overstating it as its own phase misdescribed what actually happened.

### The eight phase titles adopted
**Category:** Naming
**Date/session:** Session 1 (pre-git)
**What happened:** The stubbed phase set was replaced with a supplied slate: Curiosity/Skepticism/Fear, Initial Applications, Front-End Breakthrough, Unlocking of Ideas, UMD Completion, Professional Community, AI Fluency Push, Now — Looking Ahead. (Front-End Breakthrough was demoted shortly after; see above.)
**Why:** Real titles gave the arc its inward-to-outward shape — the 06/07 split (community vs. push) in particular.

### Pivot: static one-pager → interactive "Progression" hub
**Category:** Structural
**Date/session:** Session 1 (pre-git) · the v1 → v2 leap
**What happened:** The Honcho one-pager (a static, cream, single-column timeline) was set aside for an interactive, clickable phase tracker — a "Domino's-tracker" navigator with a detail panel — built for a colleague returning from leave first, then Honcho. Started at eight phases ("start big and dwindle").
**Why:** The timeline was more versatile as a shared storytelling vehicle than a Honcho-only leave-behind. It also argues the core point — an exponential progression, not a one-off course — structurally.

### First artifact: the Honcho one-pager
**Category:** Structural
**Date/session:** Session 1 (pre-git) · snapshot v1
**What happened:** Built a static, editorial/newspaper-style one-pager ("AI Fluency & Organizational Readiness") with a personal bio timeline and a "more sections to come" placeholder.
**Why:** The starting brief was a leave-behind for a single 1:1. Everything after this is the concept outgrowing that container.
