# FIRST RUN — Capability Ladder

> **Audience:** Hosts and package maintainers. Not primary end-user copy.  
> **Purpose:** Stop overclaiming. Make “drop into chat and say Start Here” work across write-capable agents, read-only agents, and upload-only chat UIs.

---

## The product promise (two human actions)

1. Download the starter zip.
2. Drop the unzipped starter into any chatbot that can take a folder, **or** paste `START HERE.md` first if the chat only takes one file (free Gemini and similar), then type **Start Here** or **go**.

No Terminal. No required launcher file. No assumed local CLI.

---

## Ladder

| Rung | Capability | Valid first-run behavior | Forbidden claims |
| --- | --- | --- | --- |
| **WRITE** | Agent can create/edit files in the user’s vault / starter tree | Fill placeholders, create first Inbox note, update Access Boundaries with answers | That email/calendar were connected; that hatch is a finished AI Campus |
| **READ** | Agent can read attached or mounted files only | Same walkthrough; emit paste-ready file contents and exact paths for the human | “I updated your vault” / “I saved that file” |
| **PASTE-BACK** | Upload-only or one-file paste (Gemini free and similar) | Same as READ; one file at a time; first reply is still the use notice even if `START HERE.md` is the only file you have; then name the next file | Any implication that disk changed; any “auto-installed” language; skipping the use notice |

If the host is unsure, it must ask once: write for me, or paste-back?

---

## What “auto-launch” means here

**Auto-launch** means: when the user says Start Here / go and the agent can see `START HERE.md` (package root) or is instructed by a paste-ready prompt, the agent **adopts the Startup guide job** and begins the walkthrough.

A **launcher** is optional and not in the zip as a runnable file. After hatch, the Startup guide may ask once whether the person wants a double-click starter, then fill **one** template from `launcher-templates/` for their computer. It is not silent, and it is not required.

It does **not** mean:

- Silent installation of software
- Silent Obsidian vault registration
- Silent running of shell boot scripts
- Silent access to mail, calendar, or phone
- A finished multi-Building AI Campus

---

## Package root vs Main Lobby

| File | Job |
| --- | --- |
| `START HERE.md` (package / zip root) | **First-run Startup guide** for any AI (this ladder) |
| `Operational Hub/Main Lobby/Start Here.md` | **Seat boot** for Operations Secretary / Vault Architect after hatch |

Do not conflate them. First-run ≠ seat boot.

---

## Launcher templates

Plain text in `launcher-templates/`. Not runnable in the zip. The Startup guide offers **one** filled file if the person asks, for the computer they are on. Never the default first-run path. Never required.

---

## Zip notes (for rebuild — not this pass)

- Prefer `START HERE.md` at the **zip root** of the public Hub starter (same file as package-root `START HERE.md`, or a one-liner pointer).
- Keep Main Lobby `Start Here.md` for seat boot.
- Building starter needs a **parallel** `START HERE.md` later (Domain hatch). Not blocking Hub first-run drafts.
- Do not freeze zips until public wording is signed.

---

## Grandma bar (usability acceptance)

A grandmother with no developer background should complete WRITE or PASTE-BACK first-run without:

- Hearing unexplained jargon dumps
- Being told to open Terminal
- Being told a launcher file is required
- Being asked five decisions in one message

If a host cannot meet that bar, the copy is wrong — not the user.
