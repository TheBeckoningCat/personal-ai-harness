# Communications Board Standard

**Status:** #status/active · version 2 approved 2026-08-14  
**Architect:** Vault Architect · **Routine maintenance:** Operations Secretary

Use the Message Board for short notices to more than one Core person. Use a person's Mail Box for direct correspondence. Put long explanations in the appropriate project, Work Table topic, Work Log, or Scratch Pad and link that file from the notice.

## Names And Locations

| Term | Meaning |
|---|---|
| **message boards** | The shared [[Mail Room/Message Board]] and each person's Mail Box |
| **our message board** or **your Mail Box** | When addressed to a Core person, that person's `Mail Room/Mail Boxes/<name>/` |
| **Message Board** | Shared notices addressed to more than one Core person |
| **Mail Box** or **mailbox** | `Mail Room/Mail Boxes/<name>/` in this vault or the person's Town Hall Mail Box. It is not `00 Inbox`. |
| **Town Hall mail** | A packet transferred from another Building. Copy it into the recipient's local Mail Box, verify the local copy, and then delete the Town Hall transfer copy. |
| **Project Candidate** | A possible or accepted commitment created in another Building that GTD may not yet record. The Director sends it to Operations Secretary, who processes it according to [[Project Candidates]]. |
| **raw capture** | the Owner's unstructured notes in Daily Capture or `00 Inbox` |
| **`00 Inbox`** | Unprocessed information Owner gives Operations Secretary. Building mail does not go here. |

During every startup and substantive GTD review, check the Message Board and your own Mail Box. Retrieve Town Hall mail into the local Mail Box before processing it.

## Responsibilities

| Person | Responsibility |
|---|---|
| **Operations Secretary** | Mark handled messages, file completed Mail Box notes in the Public Filing Cabinet, and maintain the active Message Board. |
| **Vault Architect** | Maintain Mail Room architecture and shared procedures. |
| **Owner** | Approve new communication methods and changes to this standard. |

## Direct Mail

A direct conversation begins as a dated Markdown file in the recipient's Mail Box:

```text
70 Strategy & Operations/Mail Room/Mail Boxes/<recipient>/YYYY-MM-DD From <sender> - short title.md
```

Every Mail Box note uses this footer:

```markdown
## Footer
Owner marks the result, then asks Operations Secretary to process it.

- [ ] Finished
- [ ] File
- [ ] Delete
```

Owner marks Finished and then chooses File or Delete. For File, move the same note to `Mail Room/Public Filing Cabinet/<recipient>/From <sender>/`. For Delete, Operations Secretary deletes it. Operations Secretary does not process the footer until both Finished and one disposition are marked.

Do not maintain a second shared `Operations Secretary & Owner` file. Earlier shared boards remain under `_Retired Communications/`.

## Mail Created From `[WITH Operations Secretary]` Or `[WITH Vault Architect]`

This procedure applies only when Operations Secretary promotes a Planned Action marked `NEXT` and its Context is `[WITH Operations Secretary]` or `[WITH Vault Architect]`. See [[30 Resources/Table Topics (Ref)/20 Area Directory Design table talk - 2026-08-16]] and [[Project Action Layers]].

Operations Secretary creates a dated note in the named person's Mail Box, written from Owner and linked to the applicable project. A Context on an unselected Planned Action does not create mail. Do not search older Next Actions and create notes after the fact.

The recipient writes what they understand, recommend, or need to ask. Use complete sentences. When more information from Owner is required, state the question clearly.

The recipient then places the completed note in the Owner's Mail Box. Operations Secretary files her own notes to Owner, and Vault Architect files her own. Operations Secretary does not read the Vault Architect's direct correspondence to determine whether it is ready.

Use this opening format:

```markdown
# YYYY-MM-DD From Owner - short title

**Project:** [[10 Projects/Name]]
**Context:** [WITH Operations Secretary] or [WITH Vault Architect]
**Next Action:** the line Operations Secretary moved

Owner marked this as a Next Action and wants to discuss it with you.

## Draft

(write here)

## Footer
Owner marks the result, then asks Operations Secretary to process it.

- [ ] Finished
- [ ] File
- [ ] Delete
```

## Message Board

The active board is [[Mail Room/Message Board]].

```markdown
# Message Board

## Open Notices

## Messages

- [ ] YYYY-MM-DD - From: <name> - To: @<name or All> - One short message with a link when needed.

## Decisions
```

Place new messages first. Address another person with `@Name` or address the Core group with `@All`. The recipient marks the item complete after reading it. Answer with a new dated message placed above the one you are answering. Do not write a reply under another person's message. Use a Mail Box note when the response becomes a direct or substantial discussion.

Move checked messages to a dated file under `Mail Room/Public Filing Cabinet/_Retired Communications/` during routine maintenance. Preserve the messages as written. Do not leave a long resolved history in the active board.

## Where Longer Information Belongs

| Information | Location |
|---|---|
| Completed work by Operations Secretary or Vault Architect | That person's office `Work Log/` |
| the Vault Architect's temporary architecture notes | [[Offices/Vault Architect/Scratch Pad]] |
| the Operations Secretary's temporary processing notes | [[Offices/Operations Secretary/Scratch Pad]] |
| Shared design discussion | A Work Table topic linked to the applicable project |
| GTD work | Projects, Daily, or AI Handoff Inbox |
| Project Candidate from another Building | Town Hall, then the Operations Secretary's Mail Box, then [[Project Candidates]] |
| Durable decision | The authoritative procedure or project |
| Handled direct mail | Public Filing Cabinet |

## Public Filing Cabinet

| State | Location |
|---|---|
| Open direct mail | Recipient's `Mail Room/Mail Boxes/<name>/` |
| Handled direct mail | `Public Filing Cabinet/<recipient>/From <sender>/` |
| Active group notice | [[Mail Room/Message Board]] |
| Historical group notice | `Public Filing Cabinet/_Retired Communications/` |

Name a direct-mail file `YYYY-MM-DD From <sender> - short title.md`. Do not create separate Filing Cabinets inside individual offices or a README for every sender directory.

## One Official Location

Mail Boxes and former shared `Name & Owner` boards would create two locations for the same direct conversation. Mail Boxes therefore contain open direct correspondence, and the Public Filing Cabinet contains handled correspondence.

