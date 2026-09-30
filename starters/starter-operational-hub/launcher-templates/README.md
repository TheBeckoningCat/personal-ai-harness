# Launcher templates

These are **text templates**, not programs in the zip. They do not run when you unzip the starter.

The Startup guide (chat first-run) should ask **once**, after names and the folder path are known:

> Would you like a double-click starter for this computer? You can skip this.

If they say no, leave these files alone.

If they say yes, ask Mac, Windows, or Linux, then fill the matching template with their answers and give them **one** file to save. Do not hand them every template. Do not present this as required.

## Files

| Template | When to offer |
| --- | --- |
| `macos-first-run.txt` | Mac, optional hatch helper (needs Python 3) |
| `windows-first-run.txt` | Windows, optional hatch helper (needs Python 3) |
| `first-run-python.txt` | Any computer, if they want the form without a wrapper |
| `macos-boot-operations-secretary.txt` | Later, only if they already run a local AI program on a Mac |
| `macos-boot-vault-architect.txt` | Same |
| `macos-boot-mail-clerk.txt` | Later, optional mail clerk. Not Core. Not day one. |
| `macos-backup-hub.txt` | Later, a dated copy of the vault. Not a schedule. |
| `daily-START-HERE.txt` | After first-run: replacement for package-root `START HERE.md` so the next **go** boots a daily seat. The installer is copied to `40 Archive/First run/`. |

These are `.txt` files so they do not look like programs. Replace `{{…}}` tokens before saving. On a Mac, save the filled text as `Something.command` and allow it in Finder if asked. On Windows, save as `Something.bat`.

Do not put `.command`, `.bat`, or `.sh` files in the public zip, even as templates. Keep templates as `.txt`.
