# Snippet Shortcuts (Obsidian-native)

These live **in the vault**, not in macOS System Settings. They will not vanish when iCloud rewrites keyboard text replacements.

## How to use (2 steps)

1. Press **`Cmd+Shift+I`** (Insert template).  
   - If that hotkey does nothing: **Settings → Hotkeys → search "Insert template"** and set `Cmd+Shift+I` yourself, then restart Obsidian if needed.
2. Type a short filter name and press **Enter**:

| Type  | Inserts                                               |
| ----- | ----------------------------------------------------- |
| `ops` | `- [ ] @OperationsSecretary: `                                        |
| `specialist`| `- [ ] @Specialist: `                                       |
| `opspass`  | `ops-pass:: YYYY-MM-DD` (today’s date via `{{date}}`) |
| `ltops` | `Letter to Operations Secretary` (dated letter into Operations Secretary’s mailbox) |
| `owner` | Owner edit mark (`edit-owner`) |
| `architect` | Vault Architect edit mark (`edit-architect`) |
| `katmark` | Operations Secretary edit mark (`edit-ops`) |
| `topic` | `Table Topic` (Work Table sheet with footer) |

Template files (vault-only):

- `Templates/Snippet - Message Board note to.md` (and any short-named templates you add)
- `Templates/(removed)` — if present, inserts `ops-pass::` (or use `opspass` filter if configured)
- `Templates/Letter to Operations Secretary.md` — dated letter into Operations Secretary’s mailbox (`ltops`)
- `Templates/Table Topic.md` — Work Table sheet (`topic`)

Project lifecycle is **not** a snippet: set frontmatter / Projects Base `status` (`active` · `someday` · `close` · `delete`). See [[Project Lifecycle]].

## Meaning

| Marker | Purpose |
|---|---|
| `- [ ] @OperationsSecretary:` | Intentional action for Operations Secretary |
| `- [ ] @Specialist:` | Intentional action for John |
| `ops-pass:: YYYY-MM-DD` | Custodian pass only — not a task; not lifecycle |
| `<span class="edit-owner">` | Owner’s words in a shared note |
| `<span class="edit-architect">` | Vault Architect’s words in a shared note |
| `<span class="edit-ops">` | Operations Secretary’s words in a shared note |

## Add a new short insert later (no system settings)

1. Create a small file in `Templates/` with a **short name** you can type in the filter (e.g. `home.md`).
2. Put the exact text you want inserted (use `{{date}}` if you need today’s date).
3. In a note: `Cmd+Shift+I` → type that name → Enter.

No macOS Text Replacement. No agent system access. Survives as long as the vault does.

## Optional upgrade later: true one-key hotkeys

Core Obsidian can only hotkey **“Insert template”** (then you pick).  
For **one keystroke per snippet** (e.g. `Cmd+Shift+K` always inserts Operations Secretary), install a community plugin such as **QuickAdd** or **Templater**, then assign a hotkey per choice. Ask Operations Secretary to configure it after you enable the plugin.

## Old macOS `;kat` / `;john` / `;kp`

Those were system-wide and can disappear when prefs sync. Prefer the Obsidian method above. You may delete the macOS ones under **System Settings → Keyboard → Text Replacements** if they reappear and confuse you.
