# Owner - How To Use This System

This vault is a lightweight digital extension of the Owner's paper GTD system. It should stay simple enough to use offline and clear enough that Operations Secretary or another AI persona can process free-flow notes later.

## Daily use
1. Use today's Daily note (`Daily/YYYY-MM-DD.md`) as your daily overview and Capture page. See [[Templates/Daily Note]] and [[Daily Note Standard]].
2. Capture freely under **Capture** (or in `00 Inbox`). No special syntax required.
3. If something needs action, write it plainly. If you want it returned to your attention later, include a date when you can.
4. Ask Operations Secretary to process the Daily note or Inbox when ready. She moves handled items into **Processed** so you can see they were handled.
5. Morning reflection and the two “must get done” items live in the **Daily Journal**; Operations Secretary copies those two into Daily **Must Do**.

the Operations Secretary's Daily review follows [[Daily Note Standard]]. Journal review follows [[Journal Review Standard]].

## Good capture examples
- Call plumber about sink leak.
- Operations Secretary: turn this into a project if it needs more than one step.
- Waiting on Mark to send the contract.
- Remind me on 2026-08-15 to check whether the insurance paperwork came back.
- tickler:: 2026-09-01 Review fall travel ideas.

## Where things go
- `00 Inbox`: raw capture that has not been processed.
- `Daily`: daily overview and Capture (Must Do, Commitments, Needs My Decision, Capture, and Processed).
- `10 Projects`: active outcomes that need more than one step. Inside each note: **Next Actions** (do now + Context), **Planned Actions** (future path), **Waiting For** — see [[Project Action Layers]]. You mark the Planned line you want with `NEXT` and a Context if you have one. Operations Secretary moves that line. You do not copy it yourself.
- `20 Areas & Contexts`: approved **Areas of Life** (project review labels) and **Contexts** (on Next Action lines only). Not where projects live.
- `30 Resources`: reference material.
- `30 Resources/02 System Lists`: stable routines and reusable checklists after they mature.
- `40 Archive`: closed projects filed under their Area subdirectory. Operational Hub development and Work Log history lives in `40 Archive/Operational Hub/Offices/`.
- `50 Someday-Maybe`: possible future commitments.
- `Calendar/Calendar.md`: real events and appointments only.
- `Calendar/Bring-Back Index.md`: matters you want returned to your attention on a date you chose. It is not a general to-do list. Appointments belong in Calendar.
- `Main Lobby`: **start at `Start Here`**. Floor map: [[Main Lobby/README]]. Contractors: `30 Resources/AI Contractors/`.
- `70 Strategy & Operations`: The Control Room — top-level controls you steer with; `Offices/` desks; `Mail Room/` (Message Board + Mail Boxes + Public Filing Cabinet); `Conference Room/` (Work Table); `Core SOP/` for Core-team procedures.

## How to ask Operations Secretary to process notes
Use simple prompts like:

- "Operations Secretary, process today's Daily note."
- "Process the Inbox and show me proposed changes first."
- "Find anything dated this week and update the calendar tracker."
- "Turn the action items from today's note into projects and next actions."
- `- [ ] @OperationsSecretary: Process this into the right project.`

Operations Secretary should clarify anything ambiguous before making judgment-heavy changes.

## Getting Updates From Other AI Apps
When working in ChatGPT, Grok, Claude, Google AI, or another tool, ask for a packet instead of copying a whole conversation.

### Regulars (Domain Specialist, etc.) — end of a work session
“What we did **this session**,” not the whole history:

```text
Give me a GTD Session Update for Operations Secretary using the AI Session Update Packet Template. Cover ONLY this session / the most recent work in this thread — not the whole chat history. Propose next actions and any project candidates, but do not treat them as final; Operations Secretary is the curator. Keep within field limits.
```

Template: [[30 Resources/AI Persona New Hire Packet/AI Session Update Packet Template]]  
Roster: [[30 Resources/AI Contractors/AI Regulars Roster]]

### Full Handoff - cleanup or first comprehensive transfer from a conversation
```text
Give me a GTD handoff for Operations Secretary using the AI Handoff Packet Template. Keep within the field limits.
```

Template: [[30 Resources/AI Persona New Hire Packet/AI Handoff Packet Template]]  

Paste either type into [[00 Inbox/AI Handoff Inbox]]. Operations Secretary decides final projects and next actions.

## Reviewing Old ChatGPT Conversations
For loose old ChatGPT conversations that do not need a full handoff packet, use a Daily-note header:

```markdown
## Old ChatGPT Conversations
- Chat/project name — one durable thing to capture, decide, or remember.
- Chat/project name — 500-character-or-less summary pasted from the conversation.
```

Operations Secretary treats these as lightweight Capture. She preserves durable information, asks about unclear items, and does not turn old ideas into active projects unless they remain current.

## Calling Attention Inside Notes
Use an unchecked checkbox with the persona name **when you want intentional action**:

- `- [ ] @OperationsSecretary: Turn this into a project if needed.`
- `- [ ] @OperationsSecretary: Route this trading-loop draft to the right trading persona.`

When the item has been reviewed, the recipient should mark it complete:

- `- [x] @OperationsSecretary: Turn this into a project if needed.`

Use `CONTEXT:` before pasted background material that should inform the work but does not need to become an action by itself.

## Requesting A Light Review Without Creating A Task
When you edit a Project or other note and want Operations Secretary to notice it later without turning it into an action:

```markdown
ops-pass:: 2026-07-30
```

Operations Secretary will polish lightly (spelling/grammar/structure), check intent and placement, and look for redundancy — then clear the marker.

## Project lifecycle (active / someday / close / delete)

**You change `status`. Operations Secretary reconciles location.** Full rules: [[Project Lifecycle]].

| You set | Meaning |
|---|---|
| `active` | Live project → `10 Projects` |
| `someday` | Possible future project that is not active now → `50 Someday-Maybe` |
| `close` | No longer active; **keep** the note → Operations Secretary archives to `40 Archive/<Area>/` as `closed` |
| `delete` | Sheet **not** worth keeping → Operations Secretary safety-checks, logs one line, deletes. Not a silent calendar wipe. |

Optional when closing: `close-result: completed` (or `cancelled` / `superseded` / `abandoned`).  
Optional for a Someday-Maybe project: `review-on: YYYY-MM-DD`. Operations Secretary also updates Bring-Back when the date was approved.

Set `status` in Projects Base or the project's frontmatter. During her next Daily review, Operations Secretary moves, closes, or deletes the project accordingly. For example, a project marked `someday` moves from `10 Projects` to `50 Someday-Maybe`. Operations Secretary does not assign `someday`, `close`, or `delete` herself, though she may ask about a project that appears complete.

Areas are different from Projects. If an Area is quiet but still part of life, keep it in the active Areas list. You may give the Area a quiet status and an optional review date.

### Short inserts (Obsidian-native — lives in the vault)
1. **`Cmd+Shift+I`** (Insert template)
2. Type **`kat`**, **`john`**, or **`kp`** → Enter

| Filter | Result |
|---|---|
| `kat` | `- [ ] @OperationsSecretary: ` |
| `kp` | `ops-pass::` + today’s date (custodian eyes — not lifecycle) |

Lifecycle is **not** a snippet — use `status` on the project. Full note: [[Templates/Snippet Shortcuts]].

## Bring-Back Index (resurface system) — v2
Use [[Calendar/Bring-Back Index]] when **you** want something to come back to mind on a **date you choose**. Full rules: [[Bring-Back Index|Core SOP]].

**Belongs:** future re-consider (e.g. look at a subscription in 9 months); recurring habit resurface (`#monthly` backup on the 15th).  
**Does not belong:** undated work, project next actions, “needs my review” with no date — those stay on the project ([[Project Action Layers]]) or Daily. Hard appointments → [[Calendar]].

Good formats:

- `remind:: 2026-08-15 Follow up on insurance paperwork`
- `2027-01-15 - Start planning Camlin visit if still likely. Source: [[Camlin and Aaron Japan Visit 2027]]`

You select the date or confirm a date Operations Secretary proposed. Operations Secretary does not copy project work into Bring-Back automatically. If you do not respond to a due item, Operations Secretary reminds you once and then asks whether it needs a new date, belongs in a project, or should be removed.

## Calendar (events only)
Use [[Calendar/Calendar]] for real appointments, travel, and time-bound events with people/places — not for “remind me later” project follow-ups.

## Direct Conversations With Operations Secretary
Conversations in an application or terminal may be used for brainstorming and clarification. Record important decisions, commitments, and information in the appropriate vault file so another session or model can use them later.

- **AI Work Log** = that agent’s office `Work Log/YYYY-MM.md`. Shared `40 Archive/Operational Hub/Offices/AI - Work Log/` is archived history.
- **Project notes / Daily / Bring-Back / Session Brief** = also update when the talk creates real work or changes orientation.
- Outside collaborators such as Domain Specialist and ChatGPT projects use an **AI Handoff Packet** in [[00 Inbox/AI Handoff Inbox]]. They do not use the Operations Secretary's Work Log as their main reporting location.

## Quick access notes
Keep notes in the folder where they belong, then make them easier to reach only after the workflow has been verified in the Owner's current Obsidian version.

Current quick-access note:
- [[30 Resources/01 Lists-To-Do/Shopping List]]

### Status
Unverified. Do not treat prior Bookmarks guidance as a completed solution.

the Owner's requested end state is: one direct ribbon/sidebar/mobile-equivalent shortcut opens `30 Resources/01 Lists-To-Do/Shopping List.md` while the note stays in `30 Resources`.

Bookmarks may still be useful, but they do not satisfy the direct one-click ribbon-icon outcome unless verified otherwise in the Owner's current app version.

### Research prompt
Take this prompt to a research-capable AI agent before changing durable instructions:

```text
Using the current versions of Obsidian for macOS and iPhone, find the fastest supported method to place a direct shortcut to the existing note `30 Resources/01 Lists-To-Do/Shopping List.md` in the ribbon or mobile equivalent. The note must remain in its current folder. Prefer one maintained community plugin requiring minimal setup. Verify the exact current click path, desktop and mobile support, and any synchronization requirements. Do not recommend Bookmarks unless they provide a one-click direct note shortcut in the ribbon.
```

### Rule
- Do not move a note just to make it easier to click.
- Do not document a current-software workflow as complete until Owner has verified it or the current app path has been researched and confirmed.
- Mark unverified instructions as proposed, not completed.

## Big capture days
When doing a big all-day capture, protect the raw material first.

1. Capture in today's Daily note, a clearly named Inbox note, or a raw handoff archive.
2. Do not let an agent rewrite or compress the raw Capture while you are still recording it.
3. Ask Operations Secretary to process it in stages: file the material first, summarize it when needed, and then create or update projects.
4. Preserve source links from filed notes back to the raw capture.
5. Use [[Signal Preservation Protocol]] when rich detail, emotional nuance, trading context, medical/family details, or major system decisions are involved.

Preserve raw Capture as the original record. A summary should help locate and understand that record without replacing it.

## Solo maintenance
If working without Operations Secretary:

1. Put raw thoughts in today's Daily note or `00 Inbox`.
2. Move multi-step outcomes to `10 Projects`.
3. Put single next actions as checkboxes under the relevant project or Daily note.
4. Put appointments and events in `Calendar/Calendar.md`. Put approved dated reminders in `Calendar/Bring-Back Index.md`.
5. Review Calendar events and due or upcoming Bring-Back items each morning.
6. Keep the system plain and useful. Do not over-file.

## Context markers on next actions (`[WITH]` / `[AT]`)
Use these on next-action lines so you can batch by **who/what** vs **where**:

| Marker | Meaning | Example |
|---|---|---|
| `[WITH] …` | Person, AI, or tool you do the action with | `- [ ] [WITH] Domain Specialist — Roth worst-case review` |
| `[AT] …` | Place or mode where the action happens | `- [ ] [AT] Desk — Empty physical inbox` |
| `- [ ] @OperationsSecretary:` | Intentional Operations Secretary action request (not general context) | `- [ ] @OperationsSecretary: Process today's Daily` |
| `ops-pass:: YYYY-MM-DD` | Custodian eyes only (not lifecycle) | Top of a note you edited |
| project `status` | Lifecycle: `active` · `someday` · `close` · `delete` | Projects Base / frontmatter |

**Areas** and **Contexts**: [[Areas and Contexts]].

## AI access (what agents may touch)
Agents working in this vault — on any platform — default to **vault-only**. They must ask before system-wide or outside-vault actions. Full rules: [[Access Boundaries]].

## General Rule
Capture fast. Clarify later. The system should reduce friction, not become another job.
