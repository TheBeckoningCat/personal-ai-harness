# Town Hall Connection

**Optional for a solo Building.** If you have no campus meeting house yet, leave this sheet unwired. Skip Town Hall boxes. Local Message Board and local mailboxes still work. Consequence mail and cross-Building packets can wait until a campus layer exists.

When you do have a campus Town Hall, complete this sheet during hatch. It is the one route map for cross-Building mail.

## Connection

| Item | Path or name |
|---|---|
| Town Hall root | `{{TOWN_HALL_PATH}}` |
| Packet Kit | `{{TOWN_HALL_PATH}}/Mail Room/Packet Kit` |
| Building Architect | `{{ARCHITECT_NAME}}` |
| Architect's canonical role box | `{{ARCHITECT_BOX}}` |
| Architect's Town Hall box | `{{TOWN_HALL_PATH}}/Mail Room/Architects/{{ARCHITECT_BOX}}` |
| Architect's local mailbox | `Mail Room/Mailboxes/{{ARCHITECT_NAME}}/` |
| Building Director | `{{DIRECTOR_NAME}}` |
| Director's canonical role box | `{{DIRECTOR_BOX}}` |
| Director's Town Hall box | `{{TOWN_HALL_PATH}}/Mail Room/Directors/{{DIRECTOR_BOX}}` |
| Director's local mailbox | `Mail Room/Mailboxes/{{DIRECTOR_NAME}}/` |
| Mail to campus operations secretary | `{{TOWN_HALL_PATH}}/Mail Room/Directors/{{CAMPUS_OPS_SECRETARY}}` |
| Architecture mail to vault architect | `{{TOWN_HALL_PATH}}/Mail Room/Architects/{{VAULT_ARCHITECT}}` |

`{{CAMPUS_OPS_SECRETARY}}` and `{{VAULT_ARCHITECT}}` are **optional campus seats** for a multi-Building campus. They are not required on day one for a solo Building. Fill them only when those seats exist on your campus.

Do not call this connection live while any required placeholder remains. For solo use, mark the sheet "not wired" and stop.

## Standing Access

When wired: the Director may read the Town Hall Packet Kit, pull files from this Building's Director role box, and write consequence-only return mail, Project Candidates, or accepted commitments to your campus operations secretary or the sender named on a work slip.

When wired: the Architect may read the Town Hall Packet Kit, pull files from this Building's Architect role box, and write shared-edge architecture mail to your vault architect or the sender named on an architecture work order.

Both seats verify that a local copy opens and is complete before deleting the Town Hall transit copy. Specialists have no Town Hall pull access by default. They route findings, recommendations, and Project Candidates to the Director locally. This grant does not permit browsing another seat's incoming mail or entering another Building.

## Packet Chooser

| What happened | Use |
|---|---|
| A Director's work slip changed something the sender or campus ops must remember | Director returns the consequence to the named sender or uses Town Hall Packet Kit mail-to-ops template |
| Local work produced a possible or accepted commitment | Specialist routes it to the Director locally; Director uses Town Hall Packet Kit `Project Candidate.md` |
| A shared address, access rule, packet field, migration, or architecture work order needs the vault architect | Architect sends one short shared-edge packet to your vault architect |
| Architecture work produced a possible commitment | Architect routes it locally to the Director; Director decides whether to send a Project Candidate |
| Only local staff need to act | Local Message Board or local mailbox; do not use Town Hall |
| A session ended but no outside consequence exists | Send nothing; no routine Session Update |

Town Hall is transit. Pull into the local mailbox, verify the local copy, then delete the Town Hall copy. Do not place mail in `Spent`.

## Minimum Packet Fields

Every outgoing Town Hall packet names:

```text
Type:
Building / sender:
Outcome or decision:
As-of time or deadline, if relevant:
Authorized local source:
```

Add a source work slip or ticket, status, blocker, or requested next action only when the recipient needs it to act. Keep domain records and session history local.

## Hatch Proof

Skip this section for a solo Building with no Town Hall.

- [ ] Both canonical role boxes exist and have a README identifying the seat, occupant, Building, and local pull path.
- [ ] Architect pulled one test packet into the local Architect mailbox and cleared the transit copy.
- [ ] Director pulled one test packet into the local Director mailbox and cleared the transit copy.
- [ ] Both seats opened and verified the local test copy before clearing the transit copy.
- [ ] Director can identify the minimal packet fields, the campus ops box (if any), and the consequence-only / Project Candidate routes.
- [ ] Architect can identify the minimal packet fields, the vault architect box (if any), and the shared-edge route.
- [ ] Both seats can explain that specialists route locally to the Director and receive no Town Hall pull access by default.
- [ ] Both seats can explain that no routine Session Update is sent because a session ended.
- [ ] Test files were removed after the route was proved.
