# Journal Review Standard (v1)

**Status:** #status/active · architecture 2026-08-09 (Vault Architect) · Operations Secretary executes  
**Canonical app format:** DailyJournal **V2**  
**Manual mirror:** [[Templates/Daily Journal]]  
**Home of files:** `JournalEntries/YYYY-MM-DD Daily Journal.md`

One canonical journal format. Multiple capture interfaces (app popup, manual Obsidian template). **No extra markup unless it earns its keep.**

---

## What Operations Secretary reviews

During a morning or evening review, Operations Secretary reads the complete relevant managed section for that half-day rather than reading only `## Captured Follow-Ups`.

| Session | Managed region | Markers |
|---|---|---|
| Morning | `## Morning` | `<!-- DAILYJOURNAL:MORNING:START/END -->` |
| Evening | `## Evening` | `<!-- DAILYJOURNAL:EVENING:START/END -->` |
| Always available | `## Captured Follow-Ups` | `<!-- DAILYJOURNAL:FOLLOWUPS:START/END -->` |

### V2 section map (stable headings)

**Morning**

1. Two Things I Must Get Done Today — No Matter What! (1/2)
2. What Would Make Today Meaningful?
3. What Could Derail Me Today?
4. Today I Will…
5. Morning Prayer → heading `### Morning Prayer`

**Evening**

1. What Created the Most Value or Progress Today?
2. What Created the Least Value — or Unnecessary Friction?
3. What's On My Mind? (1/2)
4. Gratitude & Thanksgiving (1/2)
5. System, Routine, or Approach to Improve?
6. Smallest Useful Adjustment?
7. How Do I Want Tomorrow to Go?
8. Evening Prayer → heading `### Evening Prayer`

---

## Classification (per answer / block)

When reviewing Morning or Evening content, classify each substantive line or block as one of:

| Class | Meaning | Operations Secretary action |
|---|---|---|
| **Commitment** | Explicit “I will / must / doing X” open loop | Route into GTD (project, next action, Calendar, or Bring-Back) |
| **Possible commitment** | An uncertain or implied open matter | Ask Owner when clarification materially affects GTD; otherwise record a brief watchlist note. |
| **Reflection only** | Meaning, gratitude, prayer, mood, process thought with no externalize-able next step | **Leave untouched** in the journal |

`## Captured Follow-Ups` is a **high-confidence** commitment signal (checkbox path from the app). It is **not** Operations Secretary’s only source. Free text in Morning/Evening can still hold commitments.

### Prayer blocks

- Predictable headings `### Morning Prayer` and `### Evening Prayer` live **inside** the existing Morning/Evening managed markers.
- **No separate `DAILYJOURNAL:PRAYER` markers** (architecture decision 2026-08-09).
- Default class for prayer body text: **reflection only**, unless Owner writes an explicit commitment there.
- Same default for gratitude and pure “what’s on my mind” fretting unless a concrete action is named.

---

## Edit rules

- Do **not** casually rewrite inside managed `DAILYJOURNAL` marker blocks (app owns those regions).
- Prefer routing meaning out to projects / Daily / Calendar / Bring-Back over editing journal prose.
- Manual template and app output should keep the **same markers and H2/H3 names** so Operations Secretary’s review path does not fork.

---

## Manual capture path

If the app is unavailable: Insert template **Daily Journal** from `Templates/Daily Journal.md` into `JournalEntries/` as `YYYY-MM-DD Daily Journal.md`. Fill sections; leave markers intact. Operations Secretary reviews with this same standard.

---

## Related

- [[10 Projects/DailyJournal Trial]]
- `JournalEntries/`
- [[JournalEntries/KNOWN_LIMITATIONS]]
- [[70 Strategy & Operations/The Control Room]]
- [[Main Lobby/Personas/Operations Secretary]] (secretary execution; this note is the interface contract)
