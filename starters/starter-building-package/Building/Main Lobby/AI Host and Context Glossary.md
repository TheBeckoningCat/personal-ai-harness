# AI Host and Context Glossary

**Version:** 2026-08-24.1  
**Canonical source (optional campus):** `{{TOWN_HALL_PATH}}/Main Lobby/AI Host and Context Glossary.md` — solo Buildings may keep this local copy only.

Published Campus and host vocabulary. Propose additions or retirements through a Town Hall Conference Room topic. Do not conduct the discussion on this reference file.

Shared vocabulary for {{OWNER}} and AI personas working across ChatGPT, Codex, Grok, Claude, local models, and future tools.

## Campus rooms

Standard rooms every Building presents:

- **Main Lobby** — front door, boot, Role, and Persona.
- **Offices** — desks. A Building with one occupant still uses this room name.
- **Conference Room** — Work Table and The Docket.
- **Mail Room** — Message Board, Mail Boxes, Public Filing Cabinet, and Mail Clerk.

Procedures and Templates are supporting infrastructure, not rooms. Departments, Resources, Cases, programs, and other local spaces appear only when the Building's work needs them.

In some campus layouts the Mail Room may live under a Strategy & Operations tree. Open 1:1 mail lives in `Mail Room/Mail Boxes/<name>/` or this Building's `Mail Room/Mailboxes/<name>/`. Spelling of the campus folder is often **Mail Boxes**, two words.

## Furniture, Equipment, Instrument

- **Furniture** — structure that makes a Building usable: directories, desks, Mail Boxes, instructions, and standard Markdown files.
- **Equipment** — something used to perform or produce work: an app, program, engine, script, workbook, or other working tool.
- **Instrument** — a Building's domain-specific equipment used to measure, reconcile, analyze, or show state.

## Work and action verbs

- **dump** — {{OWNER}}'s unstructured Daily / Inbox capture only.
- **mail** — a Town Hall packet. Not dump.
- **pull** — take a Town Hall transit copy into the local Mail Box.
- **clear** — delete the Town Hall copy after the local copy is complete.
- **process** — your campus operations secretary (optional) files the official home in {{OWNER}}'s action system. Do not say stamp.
- **File** / **Delete** — {{OWNER}}'s footer marks after Finished.
- **hatch** — stand up a Building.
- **capture** — {{OWNER}} putting something into the personal action system so it can be filed.
- **NEXT** — {{OWNER}}'s mark on a Planned line; the campus ops seat (if any) or {{OWNER}} moves it.

## Retired Campus terms

- **persona tray** → name the Mail Box or the path.
- **Trays** (drawer name) → **Mail Boxes**.
- **Mail** (room name) → **Mail Room**. mail as the packet type stays.
- **stamp** → file, or name the official home.
- **Mailboxes** (one word) → **Mail Boxes**.

## Core Terms

**Vault**  
The Obsidian vault folder on disk. This is the durable shared office. Getting Things Done (David Allen) may be an influence; do not brand the Building as GTD.

**Persona**  
The role or character loaded from Main Lobby (Core) or a domain contractors folder. Examples might include a campus operations secretary or a specialist. A persona is not the same thing as a model.

**Model**  
The reasoning engine being used at the moment, such as ChatGPT/Codex, Grok, Claude, or a future local LLM. The model is the vehicle.

**Host**  
The machine or environment where the model is working: MacBook Pro, Mac mini, terminal, desktop app, remote session, or another computer.

**Front Channel**  
The live conversation in ChatGPT, Grok, Claude, terminal, phone, or another interface.

**Back Channel**  
The durable Markdown record in the vault: Daily notes, work logs, project notes, message boards, and context notes.

**Handoff Summary**  
A short note written into the vault when an important front-channel conversation happens outside the current agent session. It should capture decisions, useful context, next actions, and open questions.

**AI Handoff Packet**  
A structured, size-limited update from another AI platform so the receiving Building can retain the useful result without reading an entire conversation. Use the current Building's approved AI Handoff Packet Template. Town Hall keeps a distribution copy in its Mail Room Packet Kit.

**Project Candidate**  
A consequence-only packet from a Building Director to your campus operations secretary (optional multi-Building campus seat) proposing an outcome for the official action record. It identifies whether the consequence is an accepted commitment or a pending candidate; that seat (or {{OWNER}}) decides whether to create, merge, plan, defer, file as reference, or record no commitment.

**Session Update**  
A bundled recap of work performed during a session. Routine Session Updates are retired. Use one only when {{OWNER}}, your campus operations secretary, or an applicable local procedure explicitly requests it.

**Morning Flight Check**  
A morning sweep of the vault (often run by a campus ops seat when one exists). Read the boot loop, check today's Daily note, journal, calendar, message boards, open `@Persona` items, and the highest-priority due items. Return a short morning readout with a Must Do list.

**Source of Truth**  
The Markdown vault, especially project notes, boot instructions, access boundaries, calendar tracker, and AI work logs.

**Memory**  
Optional model/platform recall from prior chats. Helpful when available, but never the source of truth for vault work.

## Working Model

Think of personas as workers who report to the vault. Different models are different cars used to drive to the same office.

If a useful conversation happens in a front channel, summarize the durable parts into the back channel so another model can pick up the work later.

## Handoff Summary Format

Use the current Building's approved AI Handoff Packet Template when information must move from another AI platform into a durable record. A suitable request is:

```text
Give me a handoff packet for the campus operations secretary (or {{OWNER}}) using the AI Handoff Packet Template. Keep within the field limits.
```

## Morning Flight Check Format

Use this near the top of the Daily note:

```md
## Morning Readout

### Must Do
- [ ] Project-linked must-do item
- [ ] Project-linked must-do item

### Watchlist
- Important but secondary item

### Ops Notes
- Short operating guidance for the day
```

## Safety Rule

Capabilities differ by host. A terminal agent may technically be able to reach more of {{OWNER}}'s computer, but the current Building's local Access Boundaries still apply: work only in the approved vault by default and ask {{OWNER}} before doing anything broader.
