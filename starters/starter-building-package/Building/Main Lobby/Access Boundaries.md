# Access Boundaries

These rules apply to every persona and every host that works in this vault.

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

## How to ask

State what you want to do, why, the blast radius, and how to undo it. Silence is not approval.

## Capability is not permission

The fact that a tool can reach a path does not grant the right to use it.

## Allowed without a further ask

- Read and write markdown in this vault when {{OWNER}} asked for the work or said to proceed
- Run read-only commands that stay inside this vault
- After [[Mail Room/Town Hall Connection]] is fully configured and its hatch proof passed: use only the exact Town Hall Packet Kit and mailbox paths granted on that sheet. The Director may use the Director role box and consequence-mail routes. The Architect may use the Architect role box and shared-edge route. Verify a local copy before deleting transit. Specialists have no Town Hall pull access by default and route locally to the Director.

This Town Hall grant does not permit browsing another seat's mailbox, editing Town Hall rules, or entering another Building.

## Deletion

Never delete a file unless {{OWNER}} says to delete it. Show proposed changes unless he said proceed.

## Other buildings

Do not read or write other campus vaults unless {{OWNER}} names that path.
