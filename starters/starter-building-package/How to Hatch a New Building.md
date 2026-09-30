# How to Hatch a New Building

Package version: v0.2-public. Copy this skeleton. Do not invent extra rooms on day one. Do not copy another Building's mission, Departments, or leftover household files.

Easier path: drop this unzipped package into a chatbot and say **Start Here** or **go**. If the chat cannot take a folder, paste `START HERE.md` first. The guide will walk names, Access Boundaries, and one Inbox note. This zip has no runnable shell.

The rest of this file is the manual checklist.

## 1. Fill One-time Setup

Copy the skeleton first if the inner vault does not exist yet, then open `Main Lobby/One-time Setup.md` and write every input in that table. The rest of this page is how the Architect applies those values once. If an input is still blank, stop.

## 2. Copy the skeleton

The Area folder may already exist on the Desktop. The operational vault is the inner Building folder — the same shape used by other live Buildings.

```bash
mkdir -p "{{DESKTOP}}/{{AREA_FOLDER}}"
cp -R "{{STARTER_PACKAGE_PATH}}/Building" "{{DESKTOP}}/{{AREA_FOLDER}}/{{BUILDING_NAME}}"
```

Open the inner copy as an Obsidian vault (or any Markdown folder). Do not write back into this starter package unless you are improving the package itself.

## 3. Replace placeholders and rename seats

Use only the values from `Main Lobby/One-time Setup.md`. Replace `{{BUILDING_NAME}}`, `{{VAULT_PATH}}`, `{{WRITE_FENCE}}`, `{{OWNER}}`, `{{MODEL}}`, `{{TOWN_HALL_PATH}}`, `{{ARCHITECT_NAME}}`, `{{ARCHITECT_BOX}}`, `{{DIRECTOR_NAME}}`, and `{{DIRECTOR_BOX}}` in the copy.

Rename:

- `Offices/Building Architect/` to `Offices/{{ARCHITECT_NAME}}/`
- `Offices/Building Director/` to `Offices/{{DIRECTOR_NAME}}/`
- `Mail Room/Mailboxes/Architect/` to `Mail Room/Mailboxes/{{ARCHITECT_NAME}}/`
- `Mail Room/Mailboxes/Director/` to `Mail Room/Mailboxes/{{DIRECTOR_NAME}}/`
- `Mail Room/Public Filing Cabinet/Architect/` to `Mail Room/Public Filing Cabinet/{{ARCHITECT_NAME}}/`
- `Mail Room/Public Filing Cabinet/Director/` to `Mail Room/Public Filing Cabinet/{{DIRECTOR_NAME}}/`

Create Role and Persona files named for the occupants from `Templates/Role.md` and `Templates/Persona.md`. Do not leave live files named only Building Architect or Building Director.

Start with `Main Lobby/Mission.md`, `Main Lobby/Access Boundaries.md`, and — if you have a campus meeting house — `Mail Room/Town Hall Connection.md`.

## 4. Fill the Main Lobby

Set Mission, Staff Directory, and the write fence. The boot stack is Start Here, Boot Instructions, Access Boundaries, Role, Persona, Lessons, [[Building/Main Lobby/Campus Communication Standard]], then When I Walk In. Keep `AI Host and Context Glossary.md` as a reference, not a boot step. {{OWNER}} writes at the table with `Templates/00 Edit mark Owner.md` and `Templates/01 Owner Table Talk Note.md`. Do not add a second Communication Standard file. Do not hire a third seat so the directory looks full.

`Current Period.md` may stay in the copy. Fill it only when there is a period to name. It is not required to call the Building ready.

## 5. Seat the two offices

Leave When I Walk In, When I Go Home, Left on the Desk, Scratch Pad, Lessons, and Work Log ready. Do not add Handoff or Session Resume to the desk. Do not add a domain office yet.

## 6. Wire Town Hall mail (optional for a solo Building)

**Solo Building:** If you have no campus meeting house yet, skip Town Hall boxes. Leave `Mail Room/Town Hall Connection.md` marked optional / not wired. Consequence mail and cross-Building packets can wait until a campus layer exists. Local Message Board and local mailboxes still work.

**Multi-Building campus:** Create or verify one Town Hall role box for the Architect and one for the Director. Occupant names live on the README and in the local Mail Box folder. The Town Hall folder stays the Building role. Complete `Building/Mail Room/Town Hall Connection.md`, grant only those exact paths in Access Boundaries, and run every Hatch Proof checkbox on the connection sheet.

Campus seats such as a campus operations secretary or a vault architect belong to a multi-Building campus. They are not required on day one for a solo Building. If your campus has those seats, the Director proves a consequence-mail route to your campus operations secretary; the Architect proves the shared-edge architecture route to your vault architect. No seat sends a routine Session Update merely because a session ended.

## 7. Live floor

Inbox and Cases already exist. Departments stay empty. Do not open a Case until {{OWNER}} names work that belongs here. When a Case is named, follow [[Building/Procedures/Make a Case]].

## 8. Name the first Work Table sheet

{{OWNER}} names the first topic. Copy `Templates/Work Table Topic.md` onto `Conference Room/Work Table/`. Do not ship a Welcome sitting as the first sheet. Do not start Talk on a Docket sheet.

## 9. Confirm the fence

`Main Lobby/Access Boundaries.md` must name `{{WRITE_FENCE}}`. Never delete unless {{OWNER}} says to delete.

## 10. Optional launcher

This zip has no runnable `.command` or `.bat`. If you want a double-click file later, ask the Startup guide for one text template. Do not keep a Launchers folder in the vault. Do not start a Mail Clerk until two live sessions need a doorbell.

## 11. Obsidian

Command-Shift-I inserts a template. Confirm Core plugin Templates is on after the first open. Any Markdown folder works if you prefer not to use Obsidian.

## 12. First boot

Each seat runs the lobby stack in [[Building/Main Lobby/Start Here]], then `When I Walk In`. Close with `When I Go Home`: rewrite the desk note and add one dated line to each Lessons file.

## Done when

The copy has a named job, named occupants, a write fence, Role and Persona files, Inbox, Cases, and Make a Case. Departments are empty. There is no second Communication Standard file.

For a solo Building, Town Hall wiring is optional. For a multi-Building campus, also require two verified Town Hall boxes, a completed Town Hall Connection sheet, and a passed mail-route proof.

This starter package is unchanged except when {{OWNER}} asks to revise it.
