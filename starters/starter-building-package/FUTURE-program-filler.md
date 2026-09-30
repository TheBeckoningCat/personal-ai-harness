# Later: program filler for the kernel seed

**Status:** Idea only. Not in the current downloadable zip.

## What ships today

The Building starter is a **kernel seed**: folder skeleton, design notes, Role/Persona shells, walk-in/go-home checklists, and a hatch checklist with placeholders such as `{{OWNER}}` and `{{BUILDING_NAME}}`. A human (or Architect) fills those by hand.

## What we could add later

A **program filler** inside the downloadable package that:

1. Asks for the hatch inputs once (owner name, building name, seat names, write fence, optional meeting-house paths).
2. Copies the kernel seed to the chosen folder.
3. Replaces placeholders across the copy.
4. Renames the two office and mailbox folders to the named seats.
5. Leaves Role and Persona shells ready to edit, without inventing mission text the owner did not supply.

## Honesty limits (keep these even after a filler exists)

- The filler populates structure and names. It does not invent commitments, Cases, or review outcomes.
- It does not silently connect email, calendar, or bank accounts.
- It does not become a one-click AI Campus. Multi-Building Town Hall wiring stays optional and explicit.
- The owner still runs one review alone before trusting the desk.

## Suggested shape when built

- A small local script or guided form (for example a `.command` on Mac, or a short Python/CLI wizard) living **beside** the seed, not inside the live vault as a third Core seat.
- Input table mirrors `Main Lobby/One-time Setup.md`.
- Dry-run mode that prints what it would change before writing.

When this exists, update `HONEST_LIMITS.md` and the public README so the article and X thread stay accurate.
