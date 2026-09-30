# Retention and Pruning Protocol

**Owner (standard):** Vault Architect (Vault Architect)  
**Operator (day-to-day):** Operations Secretary (GTD secretary)  
**Approver for deletes:** Owner  

Purpose: keep Operational Hub concise and reliable without erasing useful history. Startup should load current instructions and work, not every message ever written.

**Default:** Archive useful history and reduce unnecessary repetition. Do not delete large groups of files without individual review and the Owner's approval.

---

## Core rules

1. **Keep boot context limited.** Boot loads rules, current state, and active work, not full history.
2. **Preserve useful information without loading everything.** Durable facts live on project or resource notes; raw source material remains in its archive.
3. **One week is for review, not destruction.** Use ~7 days to ask “still operational?” not to auto-wipe.
4. **Never delete unchecked open work** without Owner’s explicit OK.
5. **Completed multi-step outcomes** leave `10 Projects` only when Owner sets disposition (`status: close` or `status: delete`). Close **preserves** the project note in `40 Archive/<Area>/`; delete removes the sheet after a safety check. Full rules: [[Project Lifecycle]]. No mandatory synopsis on close.
6. **Operations Secretary performs routine retention reviews.** Vault Architect updates this standard when the system design changes.
7. **A README explains a directory.** Keep it to one page: what the directory is and what it contains. It is not a second walk-in or an SOP. Do not add one merely because a directory exists.

---

## Three Retention Groups

### Group A - Current Instructions And Work

| Material | Examples |
|---|---|
| Rules | Boot Instructions, Access Boundaries, How To Use |
| Orientation | Session Brief, Continuity Notes, Who To Ask, Regulars Roster |
| Live work | Active `10 Projects`, Bring-Back Index, Calendar (events) |
| Open traffic | Unchecked board messages, unprocessed Inbox / Handoff Inbox |

**Retention:** Keep these files while they remain authoritative or active, but keep them concise. Update the current file and move resolved history out of startup-loaded documents.

**Maintain by:** Completing checkboxes, moving resolved messages to history, closing projects, and updating the Session Brief when orientation changes.

### Group B - Retained History

| Material | Examples |
|---|---|
| Daily notes | `Daily/YYYY-MM-DD.md` |
| Journals | `JournalEntries/` |
| AI Work Log | office `Work Log/YYYY-MM.md` (history: `40 Archive/Operational Hub/Offices/AI - Work Log/`) |
| Closed projects | `40 Archive/<Area>/…` (preserved project note; minimal `closed-on` metadata) |
| Retired Control Room | Filed Decision Trail / Map — history only. Locks live in the SOP Binder. |
| Former Town Square decisions | Current decisions belong in the authoritative procedure; historical discussion remains archived. |

**Retention:** Years, not weeks. Personal and operational history has value.

**Prune by:**  
- After a Daily is fully processed: leave the file; optional later collapse of pure Capture already filed elsewhere.  
- Monthly Work Log files stay; do not merge years unless Owner wants a yearly summary.  
- Journals: keep; do not auto-delete.

### Group C - Large Source Collections

| Material | Examples |
|---|---|
| Large AI source collections | Complete packets or conversation exports in `30 Resources/AI Handoff Archive/` |
| Optional exports | Zip or external folder if vault bulk becomes annoying |

**Retention:** Keep the source until its useful facts are recorded in projects or Resources. The complete source may then remain in the archive or move to approved external storage.

**Prune by:**  
- Prefer a one-page index stating what was retained and linking to the official project or Resource files. Keep or externalize the complete source as appropriate.  
- Do not load Group C during startup.  
- Do not treat full chat paste as the system of record.

---

## Material-specific policy

### Message boards (Operations Secretary & Owner, Vault Architect & Owner, Town Square, etc.)

| Action | When |
|---|---|
| Leave open | Unchecked items, active threads |
| Mark read / complete | When handled |
| Move to historical communication | Checked items older than approximately 30 days, or sooner when the active board becomes difficult to scan |
| Delete | Only brief acknowledgments that Owner explicitly allows Operations Secretary to delete, or historical messages that have no lasting value after they are preserved elsewhere as required. |

**Monthly Message Board review (Operations Secretary):** Move old checked lines into `_Retired Communications` or a dated historical file. Record current decisions in the authoritative SOP or the Message Board Decisions section rather than relying on old checkboxes.

### Daily notes

| Action | When |
|---|---|
| Capture freely | Always |
| Process and move to Processed | The same day or during the next Daily review |
| Keep file | Always after process |
| Optional compress | After **~30–90 days**, if Capture is fully reflected on projects, Capture section may be shortened to “Processed — see project links” **only if** Owner wants lighter files. Default: leave intact. |

### Journals (`JournalEntries/`)

- **Keep.** Small and high personal value.  
- Do not casually edit app-managed `DAILYJOURNAL` marker blocks.  
- Record follow-up work in projects or Bring-Back rather than leaving it only in the journal.

### AI Work Log

- One file per month; **keep**.  
- Agents record meaningful completed changes without restating entire conversations.  
- Optional yearly “highlights” note later — not required for v1.

### Projects

| State / status | Location / action |
|---|---|
| `active` | `10 Projects/` |
| `someday` | `50 Someday-Maybe/` |
| `close` (queue) | Owner instruction → Operations Secretary archives per [[Project Lifecycle]] |
| `closed` | `40 Archive/<Area>/…` (original note preserved; not a separate summary) |
| `delete` (queue) | Owner instruction → Operations Secretary safety-check + delete; log in [[40 Archive/Operational Hub/Deletion Log]] |

**Authority:** Owner sets `status` (`active` · `someday` · `close` · `delete`). Operations Secretary reconciles location and runs close/delete workflows. May flag candidates only — does not invent lifecycle state.

Never auto-delete project notes. Never mass-close the portfolio.

**One control:** frontmatter / Projects Base `status`. No parallel `kat-move::` lifecycle commands.

### Areas

Areas are ongoing responsibilities, not finish-line projects.

Default: quiet Areas stay in `20 Area` with:

```markdown
status:: quiet
review-on:: YYYY-MM-DD
```

Only move an Area to `50 Someday-Maybe` when Owner clearly no longer wants it in the active life map.

### Handoff packets & Session Updates

| Stage | Action |
|---|---|
| Unprocessed | `00 Inbox/AI Handoff Inbox` |
| Processed | Archive under `30 Resources/AI Handoff Archive/` or create a short archive note that links to the project |
| Prefer | A concise **Session Update** over a complete conversation export |

When a large packet has been fully processed, keep it in the archive or move it to approved external storage. Ensure that the official projects contain the useful facts.

### Bring-Back Index

- Move handled items to the **Handled** section, or remove a brief administrative acknowledgment when Owner has authorized deletion.  
- Ignored dated items → roll +1 day (or +1 month if `#monthly`) per existing Bring-Back rules.  
- Do not store completed work permanently in Bring-Back.

### Personas / Control Room

- Keep current versions in their active locations.  
- Superseded drafts: mark superseded or archive; don’t leave three “live” truth files.

---

## Cadence

| Cadence | Who | What |
|---|---|---|
| **Each processing review** | Operations Secretary | File Capture, clear processed Handoff packets, and move handled Daily Capture to Processed. |
| **Weekly** | Operations Secretary | Review open Message Board items, due Bring-Back items, and whether Left on the Desk remains current. |
| **Monthly** | Operations Secretary, with Vault Architect when architecture changes | Move resolved Message Board history, process remaining `close` and `delete` statuses, and review large Handoff Archive files. |
| **When the vault becomes difficult to use** | Vault Architect | Review large source collections and propose an index, archive location, or approved external storage. |

---

## What future agents should load

**Minimum boot context:**  
Named **Operations Secretary** or **Vault Architect** reads [[Start Here]], [[Boot Instructions]], [[Access Boundaries]], the named Role, the full Persona, office Lessons, [[Campus Communication Standard]], office [[When I Walk In]], and [[Left on the Desk]] in that order. Left on the Desk identifies current work. Then read the Message Board and the files named there. Open the Mail Box last.

**Do not** require full Handoff Archive, full board history, or all Dailies for a valid boot.

---

## Explicit non-goals (v1)

- Automatic deletion after 7 days of Daily, Journal, or Work Log.  
- Automated retention tools before the manual monthly review has worked successfully.  
- Using full chat history as the GTD system of record.

---

## Related

- [[Signal Preservation Protocol]] - process promptly and preserve useful facts in projects.  
- [[Project Lifecycle]] — one status control; location reconciliation; close / delete  
- [[40 Archive/Operational Hub/Project Closeout and Archive Workflow]]  
- [[70 Strategy & Operations/Offices/Operations Secretary/Operations Secretary - Session Brief]]  
- [[Calendar/Bring-Back Index]]  
- [[30 Resources/AI Handoff Archive]]  
- [[The Control Room]]  
