# /ledger Report (Execution Log Template)

**Version:** 1.0.0  
**Status:** Shareable prompt pattern (not a formal standard)

## What this is
When you type **`/ledger`**, the assistant produces a **structured execution log** of the current conversation (or the scoped content the assistant has access to), optimized for:
- decisions you can reference later
- action items you can execute
- issues/misfires you can correct
- artifacts you can locate
- continuity across long threads

## Setup requirement (important)
This works best when the assistant is instructed to **reference an uploaded file** (this document) as the authoritative template.

Add a cue to your Custom Instructions (or your assistant’s system rules) like:
- “When I type `/ledger`, review the uploaded `ledger_report.md` file and respond using its exact section structure and rules.”

## Trigger
- **Command:** `/ledger`

### Optional args (if your assistant supports it)
- **topic:** filter by keyword/topic (example: `/ledger onboarding`)
- **date_range:** filter by dates if the assistant can infer them (example: `/ledger 2026-01-01..2026-01-15`)
- **scope:** `this_chat` (default) or `project_folder` (if the assistant has a project knowledge base)

## Output rules
- Use **Markdown**.
- Use **H2 headings** for sections.
- Use **3–7 bullets per section** (short + scannable).
- Include **section keywords** (3–8 keywords) at the end of each section.
- End with a **Hashtag Rollup** (8–20 tags, kebab-case) for indexing/search.
- Be honest about uncertainty: if something isn’t known, label it clearly (e.g., “unknown,” “not provided,” “needs verification”).

---

## Ledger Output Template

## Summary & Context
- What this conversation/thread is about (in 1–3 bullets).
- The current objective / what “done” looks like.
- Any important constraints, preferences, or boundaries.

**Keywords:** …

## Actions Taken
- Concrete actions completed in the chat (created, edited, decided, drafted, shipped).
- If no actions were taken, say so plainly.

**Keywords:** …

## Decisions & Rationale
- Decisions made (what we chose).
- Why we chose it (short rationale).
- Any tradeoffs or assumptions.

**Keywords:** …

## Misfires & Fixes
- What went wrong (misunderstanding, drift, premature execution, etc.).
- The correction/fix (what changed going forward).
- Any prevention rule (so it doesn’t repeat).

**Keywords:** …

## Artifacts & Files
- Files created/updated (names + locations if known).
- Links to canonical sources (repo path, doc title, etc.).
- If none, say “No artifacts created.”

**Keywords:** …

## Open Items & Next Steps
- What remains open.
- The next 3–7 actions (clear verbs, ordered).
- Any blockers or missing inputs.

**Keywords:** …

## Hashtag Rollup
#ledger-report #execution-log #decision-log #action-items #chat-ops #prompt-pattern #system-of-record #workflow

---

## Author / Contact
Created by Al Spaulding.

- GitHub: @alspaulding
- Questions / improvements: please open an Issue in this repo (preferred).
