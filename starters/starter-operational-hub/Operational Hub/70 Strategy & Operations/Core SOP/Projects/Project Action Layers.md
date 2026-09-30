# Project Action Layers

**Status:** #status/active · approved by Owner 2026-08-12 · `NEXT` mark approved 2026-08-16  
**Architect:** Vault Architect · **Operator:** Operations Secretary  
**Scope:** How actions are organized inside a project note. This procedure complements [[Project Priority]] for project priority and [[20 Areas & Contexts/Contexts]] for action Contexts.

[[Templates/Project Template]] uses these sections. Do not convert every existing project at once. Apply the structure to new projects and to existing projects when they are being updated.

## Principle

The project note supports thinking and planning. The Next Actions section identifies work that can be done now.

Do not record every possible future step at the expense of identifying the actions that are currently available.

## Three Sections

| Section | Purpose | Context tags? | Who chooses |
|---|---|---|---|
| **Next Actions** | Actions that can be performed now | **Yes**, from [[Contexts]] | Owner chooses. He marks a Planned Action with `NEXT`, and Operations Secretary moves it. |
| **Planned Actions** | Possible future actions and project planning that are not ready now | **No**, except on a line marked `NEXT` to tell Operations Secretary which Context to retain | Owner develops the plan; Operations Secretary may identify possible actions for his review. |
| **Waiting For** | Work blocked by another person, organization, event, or condition | Not applicable; name the dependency | Anyone may record the dependency; Owner decides when to follow up. |

### Next Actions

- Write a physical and visible action that Owner, or a named person in the Context, can perform now.
- Keep one or a few genuine current actions rather than copying the entire plan.
- Put applicable Contexts here, such as `[Computer]` or `[WITH Operations Secretary]`.

### Planned Actions

- Record likely future actions, sequences, and planning notes.
- Keep an action here when information, timing, or the Owner's selection is still missing.
- Do not add Contexts to ordinary Planned Actions. A line marked `NEXT` may include the Context that Operations Secretary should retain when she moves it.

### Waiting For

- Record a dependency outside the Owner's current physical action.
- When the dependency ends, Owner may select the item as a Next Action or return it to Planned Actions.

## How Owner Selects Next Actions

Owner does not need to copy a Planned Action into Next Actions himself. He reviews Planned Actions and marks each action he wants to make current. Operations Secretary then moves the selected lines.

After the checkbox, Owner writes `NEXT`, adds a Context when useful, and leaves the action wording unchanged:

```markdown
- [ ] NEXT [Computer] Confirm Time Machine is covering the vault
```

Owner may mark more than one line when several actions should become current together. `NEXT` means Owner selected the action now; it does not limit a project to one Next Action.

When Operations Secretary sees one or more Planned Actions marked `NEXT`, she:

1. Moves every marked line to Next Actions.
2. Removes the word `NEXT` while retaining the Context and action.
3. Removes the original lines from Planned Actions so they do not appear in both sections.

Operations Secretary does not move an unmarked Planned Action or select the next action for Owner. If a selected line has no Context, she still moves it and may ask Owner whether one is needed.

## Contexts That Require Another Action

Ordinary Contexts such as `[Desk]`, `[Computer]`, and `[Phone]` only describe where or how Owner can act. The Contexts below require an additional response when Operations Secretary promotes a newly marked line.

| Context on the new Next Action | What Operations Secretary does |
|---|---|
| `[Work Table]` | Treat it as a marker only. Do not create a Table Topic unless Owner names the topic or places a proposal on The Docket and asks Operations Secretary to bring it to the Work Table. |
| `[WITH Operations Secretary]` | Create a one-to-one starter note in the Operations Secretary's Mail Box. Follow [[Communications Board Standard]]. |
| `[WITH Vault Architect]` | Create a one-to-one starter note in the Vault Architect's Mail Box. Operations Secretary does not write the Vault Architect's response or move the Vault Architect's note to Owner. |
| `[WITH outside personal assistant]` | Treat it as a marker only. Do not create a vault note because that work occurs outside this vault. |

This additional action applies only when Operations Secretary promotes a newly marked `NEXT` line. Do not search older Next Actions and create Mail Box notes afterward.

## Sequence

```text
Record future work in Planned Actions.
Owner marks one or more Planned Actions with NEXT and an optional Context.
Operations Secretary moves every marked line into Next Actions and removes the word NEXT.
When completed, check or remove the action as appropriate.
When blocked externally, move it to Waiting For.
When no longer relevant, delete or revise it.
```

## Responsibilities

| Role | Responsible for | Not responsible for |
|---|---|---|
| **Owner** | Selecting current actions and marking Planned Actions with `NEXT` and an optional Context | Copying selected lines into Next Actions himself |
| **Operations Secretary** | Moving every marked line, identifying projects without a usable Next Action, explaining ambiguity, and filing explicit capture | Selecting an unmarked Planned Action for Owner |

Operations Secretary may ask, “This project has no action that can be done now. Do you want to mark one?” She does not invent the answer without the Owner's instruction or a `NEXT` mark.

## Context Views

- Contexts belong primarily on Next Actions rather than projects or ordinary Planned Actions.
- Only Next Actions should appear in views intended to show work that can be done now.
- Bases remain project-level views for Area, status, and priority. Do not require Bases to distinguish Planned Actions from Next Actions yet.
- Section-aware Tasks or Dataview queries may be considered later, but they are not required by this procedure.

## Applying The Structure

- Every active project should contain Next Actions, Planned Actions, and Waiting For headings. Empty lists are acceptable. Operations Secretary adds missing headings without selecting actions or inventing Contexts.
- Owner decides which content belongs in Next Actions. When reviewing a project, Operations Secretary may move an action that cannot currently be performed from Next Actions to Planned Actions, or move an external dependency to Waiting For. She still does not select a new Next Action.
- Do not add these headings to every Someday-Maybe note. When Owner changes a note to `status: active`, Operations Secretary applies the project structure. See [[Project Lifecycle]].
- New projects use [[Templates/Project Template]].
- Do not build a Context or Next Action view until the applicable Contexts are recorded on the Next Action lines.

## Related

- [[Templates/Project Template]]
- [[20 Areas & Contexts/Contexts]]
- [[Project Priority]]
- [[Project Lifecycle]]
- [[Calendar/Bring-Back Index]]
- [[Bring-Back Index|Core SOP v2]]

