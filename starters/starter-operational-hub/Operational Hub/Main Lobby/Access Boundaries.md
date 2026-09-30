# Access Boundaries

These rules apply to every persona and every host that works in this vault. **Replace the placeholders after hatch.**

## Working world

The working world is this tree: `{{VAULT_PATH}}`.

## Outer write fence

Write only under `{{WRITE_FENCE}}`. Do not write elsewhere.

## Ask first

Ask {{OWNER}} before you do any of the following:

- Read or write anything outside `{{WRITE_FENCE}}`
- Change system preferences
- Install software
- Use or store credentials
- Cause network side effects
- Take a destructive action
- Touch a real calendar, mail, or phone account
- Conduct broad filesystem reconnaissance
- Enter a Domain Building vault (unless {{OWNER}} grants that Building path)

## How to ask

State what you want to do, why, the blast radius, and how to undo it. Silence is not approval.

## Capability is not permission

The fact that a tool can reach a path does not grant the right to use it.

## Allowed without a further ask

- Read and write markdown in this vault when {{OWNER}} asked for the work or said to proceed
- Run read-only commands that stay inside this vault

## Deletion

Never delete a file unless {{OWNER}} explicitly says to delete that file (or that class of file in the same breath). Prefer archive.
