# First Run — optional local helper

The main first-run path is: unzip, drop the folder into any chatbot, say **Start Here** or **go**.

This package does **not** include a double-click installer. If someone wants a file for their computer, the Startup guide asks once and fills **one** template from `launcher-templates/`.

## What the optional helper does

Eight screens, one question at a time, then a review before any write:

1. Welcome and use rules
2. Your name
3. Hub name
4. Folder location
5. Time zone
6. Names for the two helper seats
7. Optional first Inbox sentence
8. Review, then write

It copies `Operational Hub/`, fills names and paths, and writes `00 Inbox/Welcome.md`. It will not overwrite a folder that already exists. It does not connect email or calendar.

## How the person gets the file

They do not need this. If they want it:

- The Startup guide asks Mac, Windows, or Linux
- Fills the matching template
- They save it as an ordinary `.command` or `.bat` in a place they choose

Python 3 is required only for that optional helper. Chat first-run does not need Python.

## Honesty

Hatch helper, not a one-click AI Campus. Review is still human work. Do not put runnable shell in the public zip.
