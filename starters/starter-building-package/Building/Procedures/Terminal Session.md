# Procedure: Terminal Session

Use this when a seat runs in a local terminal agent. The files are the seat. The model is a lamp. Change `{{MODEL}}` or open the same `{{VAULT_PATH}}` in another CLI.

## Grok Build example

```bash
cd "{{VAULT_PATH}}"
exec screen -S building-architect grok --always-approve -m {{MODEL}} --cwd "{{VAULT_PATH}}" "YOUR BOOT PROMPT"
```

Later:

```bash
screen -S building-architect -X stuff $'See Work Table for new updates and comments\r'
```

Never paint `/dev/ttys*`. Put the boot `.command` in the Area folder beside this vault, not inside it.

## Other hosts

Claude, Codex, Cursor, or a local model may open the same vault. They run the same boot path. They do not get a second official copy of any fact.

## Doorbell versus worker

A chat-app copy of a seat may wave. It does not write vault markdown.
