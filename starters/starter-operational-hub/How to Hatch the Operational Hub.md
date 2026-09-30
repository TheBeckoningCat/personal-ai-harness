# How to Hatch the Operational Hub

Package version: v0.1-public-hub. Copy this skeleton. Do not invent extra floors on day one. Do not copy another person's live projects, Daily notes, or household files into the hatch.

Easier path: drop this unzipped package into a chatbot and say **Start Here** or **go**. If the chat cannot take a folder, paste `START HERE.md` first. The guide will ask for the next file by name. This zip does not include runnable shell.

The rest of this file is the manual checklist.

## 1. Copy the skeleton

```bash
mkdir -p "{{DESKTOP}}/{{AREA_FOLDER}}"
cp -R "{{STARTER_PACKAGE_PATH}}/Operational Hub" "{{DESKTOP}}/{{AREA_FOLDER}}/{{HUB_NAME}}"
```

Suggested defaults: `{{AREA_FOLDER}}` = your personal-organization folder; `{{HUB_NAME}}` = `Operational Hub` (or your own name for The Brain).

Open the inner copy as an Obsidian vault (or any Markdown folder). Do not write back into this starter package unless you are improving the package itself.

## 2. Replace placeholders

Replace in the copy (boot scripts included):

| Token | Meaning |
|---|---|
| `{{OWNER}}` | Human who owns yes |
| `{{HUB_NAME}}` | Display name of this hub vault |
| `{{VAULT_PATH}}` | Absolute path of the hatched vault |
| `{{WRITE_FENCE}}` | Outer folder staff may write |
| `{{MODEL}}` | Default launcher model, not a vault law |
| `{{OPS_SECRETARY_NAME}}` | Name you give the Operations Secretary seat |
| `{{VAULT_ARCHITECT_NAME}}` | Name you give the Vault Architect seat |
| `{{DESKTOP}}` | Your Desktop path |
| `{{AREA_FOLDER}}` | Parent folder on disk |
| `{{STARTER_PACKAGE_PATH}}` | Path to this starter package |
| `{{NEXT_ACTIONS_INDEX_PATH}}` | Optional external next-actions spreadsheet path |

Rename offices and mailboxes after you choose seat names:

- `70 Strategy & Operations/Offices/Operations Secretary/` → `.../{{OPS_SECRETARY_NAME}}/`
- `70 Strategy & Operations/Offices/Vault Architect/` → `.../{{VAULT_ARCHITECT_NAME}}/`
- Matching `Mail Room/Mail Boxes/` folders
- Matching `Main Lobby/Personas/` Role and Persona filenames

## 3. Fill the Main Lobby

1. `Start Here.md` — confirm boot lines name your seats
2. `Access Boundaries.md` — set `{{VAULT_PATH}}` and `{{WRITE_FENCE}}`
3. `Owner - Profile.md` — short placeholders only
4. Role + Persona shells for both seats
5. Keep [[Campus Communication Standard]] as the shared prose standard

## 4. Fill Areas & Contexts

Edit `20 Areas & Contexts/Areas of Life.md` and `Contexts.md` with **your** vocabulary. The shipped lists are generic placeholders.

## 5. Seat the offices

Leave When I Walk In, When I Go Home, Left on the Desk, Scratch Pad, empty Lessons, and empty Work Log ready. Do not import live Work Logs.

## 6. Optional launcher (only if you asked for one)

If you want a double-click file, have the Startup guide fill one template from `launcher-templates/` for your computer. Mail Clerk is not Core and is not day one.

## 7. First-week checklist

- [ ] Place one capture in `00 Inbox/` and process it into a project or trash
- [ ] Create one real project from `Templates/Project Template.md`
- [ ] Write today's Daily note from `Templates/Daily Note.md`
- [ ] Glance `70 Strategy & Operations/The Control Room.md`
- [ ] Run one seat through Walk In → small task → Go Home
- [ ] Do **not** hatch a Building until an Area truly needs its own stacked office

## 8. Relate to Buildings

When an Area of Life needs a domain vault, hatch a **Building** from the separate Building starter. Keep life-level next actions and review in this Hub. Buildings extend Areas; they do not replace the Brain.
