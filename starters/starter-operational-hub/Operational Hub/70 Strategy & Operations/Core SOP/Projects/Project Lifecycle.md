# Project Lifecycle

**Owner (standard):** Vault Architect (Vault Architect)  
**Operator:** Operations Secretary (GTD secretary)  
**Approver for lifecycle state:** Owner  

Purpose: define one lifecycle policy controlled by `status`. Owner selects the status, and Operations Secretary moves or closes the project accordingly.

**Stable V1 design principle:**  
**Archive by default when history has value; delete only when Owner explicitly determines the project record does not.**

**Control rule:**  
**Owner changes lifecycle state → Operations Secretary reconciles filesystem location.**

---

## Core authority rule

**Owner decides project lifecycle. Operations Secretary executes it.**

| Who | May do |
|---|---|
| **Owner** | Set frontmatter / Projects Base `status` to `active`, `someday`, `close`, or `delete` |
| **Operations Secretary** | Flag projects that *look* complete, obsolete, duplicated, or inactive; **ask** or leave for review |
| **Operations Secretary** | Reconcile note location to match Owner’s `status` |
| **Operations Secretary** | **Must not** independently assign `someday`, `close`, or `delete` |

There is **no** parallel command language for lifecycle (`kat-move::` is retired). Use `status` only.

Do **not** mass-process the portfolio. Only act on statuses Owner has set (plus cheap location mismatches for those statuses).

---

## Status vocabulary

| `status` | Meaning | Home after Operations Secretary reconciles |
|---|---|---|
| `active` | Live multi-step outcome | `10 Projects/` |
| `someday` | Possible future project that is not active now | `50 Someday-Maybe/` |
| `close` | **Disposition queue:** no longer active; **preserve** the record | Still wherever it is until Operations Secretary runs closeout → `40 Archive/<Area>/` with `status: closed` |
| `delete` | **Disposition queue:** sheet **not** worth preserving | Gone after safety check + log line |
| `closed` | Terminal after successful closeout | `40 Archive/<Area>/` only |

### Canonical form (important — Bases / Obsidian UI)

**Write status as a single scalar string**, not a YAML list:

```yaml
status: someday
```

**Not** this multi-value form (common when Obsidian treats the property as a list/tags):

```yaml
status:
  - someday
```

Both mean the same instruction for **any** lifecycle value (`active`, `someday`, `close`, `delete`, `closed`). Operations Secretary must **recognize either form**, then **normalize to scalar** when she touches the note so Projects Base filters (`status == "someday"`, etc.) keep working.

**Reading-only synonyms (do not invent new ones):**  
Existing notes with `status: archived` or tags like `#status/closed` count as **closed**. Prefer `closed` on new closeouts.

`close` and `delete` are **short-lived queue states**, not permanent classes of project notes.

Optional when closing:

```yaml
close-result: completed   # or cancelled | superseded | abandoned
```

Optional date for reconsidering a Someday-Maybe project:

```yaml
review-on: YYYY-MM-DD
```

If `review-on` is set on a `someday` project, Operations Secretary also maintains [[Calendar/Bring-Back Index]].

---

## How Owner instructs

**Only control:** Projects Base or project frontmatter `status`.

Examples:

```yaml
status: someday
```

```yaml
status: close
close-result: completed
```

```yaml
status: delete
```

```yaml
status: active
```

Operations Secretary completes the corresponding move, archive procedure, or deletion procedure during a normal GTD review.

---

## the Operations Secretary's Routine Reconciliation

Complete this check during every Daily review or other substantive GTD review, not only during the Weekly Review.

Do not search the entire vault during every review. Use the focused checks below.

| Signal | Required? | What Operations Secretary does |
|---|---|---|
| **[[70 Strategy & Operations/Projects.base|Projects Base]] → Lifecycle Queue** | **Yes, every review** | The view filters notes whose scalar `status` is `someday`, `close`, or `delete`. An empty view does not prove the work is complete because list-form status may not appear; use the fallback search. Do not add `closed` to this view because archived projects would overwhelm it. |
| **Fallback search when Base is empty or Owner used the Base interface** | **Yes, every review** | Search `10 Projects` for scalar and list forms of `someday`, `close`, and `delete`. Process every result. |
| **`closed` still in `10 Projects`** | **Yes, every review** | Search that directory for scalar or list-form `status: closed`. Move each misplaced project to `40 Archive/<Area>/`. |
| **Touched / recently modified projects** | When already opening them | If `status` and folder disagree, reconcile immediately; normalize list-form status to scalar |
| **Weekly Review** | Weekly | Spot-check reverse cases (e.g. `active` still in `50 Someday-Maybe`) and any strays Base does not show |
| **Explicit Owner request** | When asked | Full reconcile |

### Why Lifecycle Queue exists

Owner’s control is **`status`**. A note still living in `10 Projects` with `status: someday` (or `close` / `delete` / `closed`) **is work for Operations Secretary**, same class as an open board message — not optional polish.

`status: someday` instructs Operations Secretary to move the note to `50 Someday-Maybe` during the next normal review. Likewise, a project marked `status: closed` does not remain in `10 Projects`.

### Location rules

| If `status` is… | And note is… | Operations Secretary does… |
|---|---|---|
| `active` | Outside `10 Projects` (and is a project note) | Move to `10 Projects/` |
| `someday` | Still in `10 Projects` or otherwise outside `50 Someday-Maybe` | Move it to `50 Someday-Maybe/` during this review. |
| `close` | Anywhere (usually `10 Projects`) | Run **close** workflow below |
| `delete` | Anywhere | Run **delete** workflow below |
| `closed` | Outside `40 Archive/<Area>/` | Move into that Area subdirectory, or ask Owner when the Area is unclear. |

### Simple `someday` / `active` move steps

1. Confirm Owner set `status` (do not invent it).
2. Preserve the full note body — no compress/rewrite for the move.
3. Move the file to the correct folder.
4. Leave `status` as Owner set it (`someday` or `active`).
5. When moving a project to **active**, add Next Actions, Planned Actions, and Waiting For headings. Do not select an action or invent Contexts. See [[Project Action Layers]].
6. If `review-on` is set on a `someday` project, update [[Calendar/Bring-Back Index]] when useful.
7. Confirm `area`, `status`, `priority`, and `review-on` on the note so [[70 Strategy & Operations/Projects.base|Projects Base]] stays current. See [[Active Projects Map]].
8. Optional one-line Notes/Decisions: moved by Operations Secretary because `status: someday` (or active).

If half a note is active and half is someday, split only when the divide is obvious; otherwise ask Owner once.

---

## `close` — Operations Secretary handling

**Meaning:** Owner decided the project is no longer active; the note has durable value and should be preserved.

1. **Open-loop check** — Unchecked Next Actions, open Planned Actions that still matter, Waiting For, dated Bring-Back/Calendar items, follow-on work that should stay live elsewhere. (Action layers: [[Project Action Layers]].)
2. Resolve remaining current work, move it to the correct active record, or explain it to Owner when his decision is required. Leave completed checkboxes in the project history.
3. **Preserve the project note** substantially intact — it is the historical record.  
   **No** mandatory synopsis or retrospective. Richer write-up only if Owner asks or the project clearly warrants it.
4. **Minimal closeout metadata:**

```yaml
status: closed
closed-on: YYYY-MM-DD
close-result: completed   # optional
```

5. **Move** to archive destination (below).
6. **Navigation hygiene** — Active Projects Map and other manual links.
7. Log briefly in Work Log when useful.

### Archive destination

Closed projects belong under their primary Area. Archive subdirectories match [[20 Areas & Contexts/Areas of Life]]. Operations Secretary files the project. Vault Architect creates a new Area subdirectory only when Owner adds that Area to the approved list.

| Rule | Destination |
|---|---|
| **Default** | `40 Archive/<Area>/<same filename>.md` |
| **Travel / dated trip** | `40 Archive/Travel/<Place-or-theme> YYYY/` when that pattern already exists or is an obvious one-off trip |
| **Office / Core history** | `40 Archive/Operational Hub/Offices/` - Work Log history and AI-system notes. The related deletion record is [[40 Archive/Operational Hub/Deletion Log]]. Keep these files inside the Operational Hub Area rather than in a separate top-level directory. |
| **Owner specifies** | Use his path |

If the Area is blank or unclear, ask Owner once. Do not leave a closed project in `10 Projects` or move it to `30 Resources`.

### Archive review (not auto-delete)

When a closed note reaches its `review-on` date, Operations Secretary asks Owner to review it. The date does not authorize deletion. Owner may set `status: delete` or choose a new `review-on` date. A closed note without `review-on` has no automatic review date.

---

## `delete` — Operations Secretary handling

**Meaning:** Owner decided the project **sheet itself** is not worth preserving.

1. **Quick safety check** — backlinks, unique reference, open loops, info that should move first.
2. Explain any material risk to Owner before deleting when his decision is needed.
3. Add one line to [[40 Archive/Operational Hub/Deletion Log]] with the name, date, and optional reason.
4. **Delete** the note — do **not** archive; do **not** invent a replacement summary.
5. Clean manual nav / Bring-Back lines that only pointed at the deleted project.
6. Log briefly when useful.

---

## Areas (not projects)

Areas are ongoing responsibilities, not finish-line projects.

- Do not move an Area to Someday-Maybe merely because it is quiet.
- Quiet but still part of life: keep it in the life map with optional `status:: quiet` and `review-on:: YYYY-MM-DD` on the Area vocabulary/map side.
- Move an Area out of the active life map only when Owner clearly wants it gone from that map.

---

## What is deliberately *not* required (V1)

- Second control path (`kat-move::` or other markers) for lifecycle  
- Mandatory project retrospective on every close  
- Auto-delete of archived notes from a calendar or a stale `review-on`  
- Mass closeout of projects that only “look done”  
- Operations Secretary inventing `someday` / `close` / `delete` without Owner  
- Expensive full-vault lifecycle scan every boot  

---

## Related

- [[Retention and Pruning Protocol]] - current instructions, retained history, large source collections, and the default preference for archiving useful records.  
- [[Templates/Project Template]]  
- [[70 Strategy & Operations/Projects.base|Projects Base]] - inventory and **Lifecycle Queue** for `someday`, `close`, or `delete` projects still in `10 Projects`.  
- [[40 Archive/Operational Hub/Deletion Log]]  
- [[Active Projects Map]] — how Operations Secretary keeps Projects Base current. The Project Dashboard file was deleted.
- [[40 Archive/Operational Hub/Project Closeout and Archive Workflow]] - design history; the current procedure is this file.  
