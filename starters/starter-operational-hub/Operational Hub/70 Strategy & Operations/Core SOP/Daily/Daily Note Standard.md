# Daily Note Standard

**Status:** #status/active · approved by Owner 2026-08-09  
**Architect:** Vault Architect · **Operator:** Operations Secretary  
**Template:** [[Templates/Daily Note]]  
**Location:** `Daily/YYYY-MM-DD.md`

The Daily note is a simple daily overview and capture page that Owner can use without AI. It should remain no more complicated than paper GTD.

## Purpose And Boundaries

The Daily note helps Owner see what matters today and gives him an easy place to capture new thoughts. It is not the Operations Secretary's Work Log, a technical report, or a detailed record of how she processed information.

| Location | Purpose |
|---|---|
| **Daily note** in `Daily/` | Today's priorities, time-sensitive commitments, decisions Owner must make, and unprocessed capture |
| **Daily Journal** in `JournalEntries/` | Reflection and natural-language capture |
| **Projects, Waiting For, Bring-Back, and Calendar** | Official GTD records |
| **[[Offices/Operations Secretary/Scratch Pad]]** | the Operations Secretary's temporary processing notes |
| **Work Log and Session Brief** | Durable AI work history and orientation, not the Owner's daily page |

## Standard Structure

```markdown
# YYYY-MM-DD

## Today

### Must Do
- ...

### Today's Commitments
- ...

### Needs My Decision
- ...

## Capture
- ...

## Processed
~~+ original capture wording~~
→ [[destination or short disposition]]
```

A section may be empty or omitted when it adds no value. Do not add filler merely to preserve the complete outline.

## What Owner Should See

At a glance, the Daily note should answer:

1. What matters today?
2. What must happen today?
3. Does Operations Secretary need a decision from me?
4. Where can I record a new thought?
5. What happened to the information I captured?

Omit a section when it does not help answer one of these questions.

## Section Rules

### Must Do

- Use the morning Daily Journal response to “Two Things I Must Get Done Today - No Matter What!” as the source.
- Preserve the Owner's stated priorities.
- Operations Secretary may identify a genuine conflict, deadline, emergency, or impossibility.
- Operations Secretary does not replace the Owner's priorities with her own.

### Today's Commitments

- This section is not another Next Actions list.
- Include only items whose timing makes them relevant today, such as appointments, actual deadlines, Bring-Back items due today, or Waiting For follow-up that must occur today.
- Do not copy complete Calendar, Bring-Back, Waiting For, project, or watchlist inventories here.
- Include an item only when Owner needs to see it today because its timing matters.

### Needs My Decision

- Keep this optional section short.
- Include only decisions Operations Secretary cannot make under her normal authority, such as an ambiguous commitment, a choice of location, or approval to proceed.
- Do not use it as a general backlog of unresolved questions.

### Capture

- This is the Owner's unrestricted place for quick capture.
- Do not require tags, project names, properties, forms, or special syntax.
- Messy natural language is expected.
- Operations Secretary does not rewrite unprocessed Capture into polished prose.

### Processed

- This section shows Owner where Operations Secretary filed each Capture item.
- It is not a detailed account of every file Operations Secretary read or every judgment she made.

## Moving Capture To Processed

The purpose of this process is to preserve the Owner's words while showing that Operations Secretary handled the item.

1. Never delete an unprocessed Capture item merely because its meaning seems clear.
2. Process each item, or a small related group, and leave unfinished items in Capture.
3. Move each completed item from Capture to Processed.
4. Preserve the original wording or a clearly faithful copy. Prefer striking through the original line and adding one short disposition.
5. Do not replace this pattern with a large table listing every project or file.
6. Put temporary reasoning and file-review notes in [[Offices/Operations Secretary/Scratch Pad]] rather than Daily.

Preferred format:

```markdown
## Processed

~~+ call Noguchi about dryer~~
→ [[10 Projects/Example Home Operations]]

~~+ remind me mid-month about insurance~~
→ Bring-Back 2026-08-15

~~+ just venting about traffic~~
→ No action / discarded
```

Useful dispositions include:

- `→ [[project]]`
- `→ Waiting For [person or organization]`
- `→ Bring-Back YYYY-MM-DD`, only when Owner selected or confirmed the date
- `→ Calendar`
- `→ Reference only`
- `→ Someday-Maybe`
- `→ No action / discarded`

When one Capture item contains several outcomes, either give it one brief disposition or create separate Processed entries while preserving the original meaning. Do not rewrite the raw material as a long summary.

Owner should be able to match each Processed entry to what he originally wrote without reading the Operations Secretary's private working notes.

## the Operations Secretary's Daily Reviews

### Morning Review

Operations Secretary may:

- add the standard sections when they are needed;
- update Must Do from the morning Daily Journal;
- add time-sensitive items to Today's Commitments;
- add decisions that require Owner under Needs My Decision;
- process available Capture into GTD;
- move handled Capture into Processed;
- remove stale automatically generated material from an earlier Daily review.

Operations Secretary must preserve the Owner's original Capture wording by moving or striking it through in Processed. She does not silently erase it.

### Midday Or Additional Review

Operations Secretary may process new Capture, update Today's Commitments when circumstances change, add or remove decisions, and correct Processed destinations. Do not rebuild the note merely to improve its appearance.

### Evening Review

Operations Secretary may process remaining Capture, finish Processed entries, remove stale today-only items, and retain decisions Owner still needs to make. Do not turn the Daily note into an evening retrospective. Reflection belongs in the Daily Journal.

## Relationship To Daily Journal

| Information | Destination |
|---|---|
| Morning priorities | Daily Journal “Two Things...” response to Daily **Must Do** |
| Commitments and possible open work found during journal review | Process according to [[Journal Review Standard]] |
| Reflection | Remains in the Daily Journal rather than being copied into Daily |

## Keep These Out Of Daily

Use Scratch Pad, Work Log, Mail Room, or project notes instead of adding:

- headings that report the Operations Secretary's morning or later processing;
- routing tables and lists of every file changed;
- duplicate-search notes;
- AI Handoff Inbox maintenance;
- architecture or technical troubleshooting notes;
- detailed processing transcripts.

When the Operations Secretary's work produces something Owner must see today, include only the useful result under Today's Commitments or Needs My Decision.

## Related

- [[Templates/Daily Note]]
- [[Journal Review Standard]]
- [[Main Lobby/Personas/Operations Secretary]]
- [[Offices/Operations Secretary/Scratch Pad]]
- [[Signal Preservation Protocol]]
- [[House Rules]]
- [[Owner/Owner - How To Use This System]]

