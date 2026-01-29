# ai-chat-ledger
A /ledger slash-command style prompt pattern that turns AI chats into structured execution logs.
This is **not a formal standard** — it’s a practical template you can install into a Custom GPT or any assistant that supports uploaded knowledge + custom instructions.

✅ **Tested with:** ChatGPT **Custom GPTs** and **Project Folders** (within ChatGPT).  
⚠️ Other assistants may behave differently; this repo currently documents the ChatGPT-tested setup.

---

## What you get (output sections)
When installed, typing **`/ledger`** produces:

- Summary & Context
- Actions Taken
- Decisions & Rationale
- Misfires & Fixes
- Artifacts & Files
- Open Items & Next Steps
- Keywords per section + a Hashtag Rollup (for indexing)

----

## Install (the important part)

### 1) Upload the template file
Upload this file into your assistant (Custom GPT → Knowledge / Files):

- `ledger_report.md`

### 2) Add the `/ledger` cue to your assistant instructions

Paste this **exact instruction** into your assistant’s Instructions / Custom Instructions:

> **/ledger behavior:** When the user types `/ledger`, you must generate the ledger report for the current conversation using the uploaded file `ledger_report.md` as the authoritative template. Follow its section headings, ordering, and output rules exactly. Do not add extra sections. If information is missing, mark it as unknown rather than guessing.

**Important:** Uploading the file alone is not enough — this instruction is what binds `/ledger` to the template.


---

## Use
In any chat with the configured assistant, type:

- `/ledger`

Optional (if your assistant supports it):
- `/ledger <topic>`
- `/ledger <date_range>`
- `/ledger <scope>`

---

## Files
- **Template:** `ledger_report.md`

---

## Attribution / Contributing
Created by Al Spaulding.

- GitHub: @alspaulding
- Suggestions welcome via Issues and Pull Requests.
