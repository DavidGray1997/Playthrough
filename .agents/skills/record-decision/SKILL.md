---
name: record-decision
description: Record or amend an attributable requirements, design, build, or release decision with stable IDs, evidence, status, rationale, and effects. Use when a material choice, proposal, approval, or supersession needs an auditable record.
---

# Record an SDLC decision

Read [the shared document contract](references/document-contract.md) at the start of **every** run. Read the target phase log in full, plus affected requirements/design/build/release records and decisions before adding or changing an entry.

Read relevant phase `questions.md` entries before drafting. Use [resolve-questions](../resolve-questions/SKILL.md) to record newly raised questions and unconfirmed assumptions, link their owning entries from this record, and reconcile answers through the concerned skills. The shared contract governs timestamps, raising/concerned skills, options, response history, and reconciliation status.

## Select the phase and ID

Use the existing phase path or `docs/initiatives/<initiative>/<phase>/decisions.md`:

| Phase | Prefix | Scope |
| --- | --- | --- |
| `requirements` | `REQ-###` | Product scope, priority, and business rules |
| `design` | `DES-###` | Domain, UX, architecture, API, and database choices |
| `build` | `BLD-###` | Implementation and delivery-sequencing choices |
| `release` | `REL-###` | Rollout, support, outcome, and follow-up choices |

Keep IDs initiative-scoped and stable. Allocate the next number above the highest existing ID, including superseded or historical entries. Never renumber, reuse, or silently replace an entry. Create a missing phase log with [the decision-log template](assets/decisions.md); retain equivalent established format where it already exists.

## Record evidence without upgrading it

Use the table columns exactly: `Index | Date | Decision or proposal | Source | Status | Rationale and effects`.

Describe the choice or proposal precisely enough to act on; name the authority as product owner, implementer, assistant proposal, or another evidenced source. Status must accurately say `Proposed`, `Approved`, `Rejected`, `Superseded`, or a qualified project convention. Cite real approval evidence and only its stated scope. A request to draft, a design review, or a passing test is not product approval unless the source says so.

For an amendment, add a new ID that links to the earlier ID and says whether it clarifies, amends, or supersedes it. Preserve the original entry's ID, date, source, and decision text; update its status/effects to link to the replacing ID so an obsolete decision cannot still read as unqualified approval. Record dependencies and downstream effects, using relative Markdown links to affected records. Do not claim a related document was updated, an approval was obtained, or an outcome was observed without evidence.

## Reconcile and check

Product-rule changes normally require the PRD and requirements log to agree; design/build/release changes must identify impacted records. When the user authorizes drafting or updating this decision record, maintain directly affected SDLC records as part of that work. Report any broader, out-of-scope inconsistency and the exact needed action.

Before handoff, verify prefix/sequence, date/status/source, working links, supersession history, and the distinction between proposal, approval, verification, and release evidence. Report the new or amended ID and any remaining checkpoint.
