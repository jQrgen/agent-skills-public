---
name: client-pipeline-list
description: >-
  Use when keeping a small company's client and lead (pipeline) list: adding a
  client or lead, promoting an idea to a concrete opportunity, updating stage or
  next step, or reviewing concentration risk.
---
# Client and pipeline list

A simple, internal list of a company's clients and concrete sales opportunities. It is never published (no financial data on public pages).

## Rules
- One file is the source of truth for the list (e.g. `<company>/strategi/kundeliste.md`). Keep it short.
- Contract dates, renewals and notice periods are NOT stored here. Each row points to its entry in the contract register owned by admin; that register is the only place for dates and reminders.
- Revenue figures are not invented. Use only numbers confirmed by the CFO or the books, with source and date.
- Ideas from business development enter only once they are concrete opportunities (named counterpart, a need, and a next step). Unvalidated ideas stay in business development's own notes.
- New leads are added only after any blocking legal check is done (e.g. existing client contract reviewed for exclusivity, IP, non-compete).

## Columns
| Name | Type (client/lead) | Stage (idé-sjekket / kontaktet / møte / tilbud / vunnet / tapt) | Owner | Next step + date | Contract register ref | Source/notes |

## Steps
1. Read the current list and the contract register; check nothing duplicates or contradicts the register.
2. Add or update the row; set exactly one owner and one dated next step.
3. If a lead needs the owner's decision or contact with an outsider, put it on the chief of staff's open-questions list instead of contacting anyone.
4. Recompute concentration: share of revenue from the largest client (from CFO-confirmed numbers). If one client is above ~50%, flag it to the CFO and chief of staff.
5. Log what changed and the date at the bottom of the file.

## Weekly review
- Stale rows (next step date passed): chase the owner.
- Won/lost: move to an archive section, never delete.
- Report a 3-line status: clients, active leads, biggest risk.
