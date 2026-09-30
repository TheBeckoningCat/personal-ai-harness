# Design rationale — v0.1

This package is the default operating system for a new building. It keeps only what serves a stacked office with two seats, a boot loop, and a written table. It is based on earlier campus vault patterns, simplified for a clean starter package.

## 1. Identity

Everything important lives in local markdown. Chat is a water cooler. Agents reboot. Hosts do not share a brain. Role, Persona, When I Walk In, When I Go Home, Lessons, and Left on the Desk make a seat persistent-like without a vendor memory product. A transfer handoff can be created for real transfers, not daily resume.

## 2. Skin

The default skin is a stacked office building. Floors are mind-palace rooms a human can walk. Other skins (home, school, vehicle, city, transit) may rename labels later. Do not rename the jobs of the floors until a later version says so.

## 3. Why these floors

| Floor | Job | Lesson |
|---|---|---|
| Main Lobby | Shared static boot | One front door keeps access, mission, and boot rules from scattering. |
| Inbox | Unsorted new paper | {{OWNER}} drops files here. The Director files them. Inbox is not current state. |
| Cases | Named jobs | Cover sheet, Originals, and Derived. Not a Department. |
| Offices | One desk per seat | Each named seat gets the same durable furniture and its own walk-in/go-home loop. |
| Mail Room | Board + 1:1 | Group doorbells, 1:1 notes, and cross-Building packets live in one mail surface. Clerk is a placeholder, not Core. |
| Conference Room | Shared live work | Work Table, Docket, and How We Talk keep conversation separate from requests and archive. |
| Departments | Lasting homes later | Empty on hatch. A Case becomes a Department only when the first job has left work that will return. |
| Basement | Archive and reference | One basement keeps old paper out of the live table. |

## 4. Why only two seats

Hire a job, not a personality. A new building starts with two seats because that is enough to keep structure and mission separate. Architect owns the harness. Director owns the mission and the complexity budget. Domain seats wait for a real loop.

## 5. The boot loop

Earlier buildings tested long lobby lists, start-of-session files, handoffs, lessons, and desk notes. v0.1 uses the lighter walk-in loop:

1. **Front door and lobby stack** - the host is named Architect or Director, then reads shared rules and access boundaries.
2. **Named persona** - the lobby persona says who the seat is today and sends it to the correct office.
3. **Office Walk** - `When I Walk In` routes the seat through `Left on the Desk`, Lessons, mail, and the live table.
4. **Go Home** - `When I Go Home` closes the loop before the host dies or switches.

Staff may walk to Mail, Conference, or Departments during boot and return to the office. `When I Go Home` closes the loop: file the work, harvest lessons, clear scratch, log shipped work, and rewrite `Left on the Desk` last.

## 6. Two writing registers

Work Table talk is High School English: full sentences, natural conversation, as if sitting together. No Slack or Discord voice.

Message Board and personal mailboxes may be short and casual. Lighter style lives in the Mail Room so the table stays a meeting.

## 7. Model swap

Boot `.command` files live in the Area folder beside the inner vault. They pass `{{MODEL}}`. Role and transfer notes do not name a vendor. A chat-app copy of a seat is a doorbell. It does not write vault markdown.

## 8. Mail Clerk

Optional and interim. A `/loop` still spends a model turn on unchanged files. The intended replacement is a native watcher. Do not make the clerk a third Core seat.

## 9. What v0.1 removed from the previous skeleton

- `Reception/` as the lobby name
- A generic `_Example Seat` instead of the two real jobs
- `Start of Session.md` as a fifth living file (folded into When I Walk In)
- `Shared Work/` (board moved to Mail Room)
- A root-level Access Boundaries file (it now lives in the lobby)
- Treating Mail Clerk as a day-one procedure you must start

## 10. Complexity budget

Every new shelf must help the loop. If a file needs an agent to explain it, the file failed.
