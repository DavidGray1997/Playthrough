---
name: write-backlog
description: Create or update a traceable delivery backlog of ordered user stories and technical tasks with stable IDs, readiness, completion checks, PRD coverage, and review notes. Use after requirements are sufficiently clear to plan build slices.
---

# Write a delivery backlog

Read [the shared document contract](references/document-contract.md) at the start of **every** run. Read the PRD, phase decision logs, relevant design records, existing backlog, and verification evidence before changing the backlog.

Read relevant phase `questions.md` entries before drafting. Use [resolve-questions](../resolve-questions/SKILL.md) to record newly raised questions and unconfirmed assumptions, link their owning entries from this record, and reconcile answers through the concerned skills. The shared contract governs timestamps, raising/concerned skills, options, response history, and reconciliation status.

## Use the durable structure

Use the established path or `docs/initiatives/<initiative>/build/delivery-backlog.md`. Start from [the backlog template](assets/delivery-backlog.md) when creating it. Preserve existing IDs and coverage links. The document needs a descriptive H1 plus explicit status and ISO update date, followed by these sections in order:

1. Delivery order
2. Readiness and completion rules
3. User stories
4. Technical tasks and completion checks
5. PRD coverage
6. Review notes

Use delivery order to explain small usable slices and real dependencies. It is a planning sequence, not a claim of completion or a rigid barrier against independently ready work.

## Write stable records

Allocate `US-###` and `TT-###` only above the highest existing ID; retain IDs if priority changes or stories split. Use the compact story and technical-task shapes in [the backlog template](assets/delivery-backlog.md) for both new records and updates. Preserve useful existing evidence and traceability when shortening records.

Keep each record focused on one outcome:

- Use a short, concrete title and one sentence for the story or task purpose.
- Aim for at most about 150 words per story and 100 words per technical task, excluding linked evidence. These are editing guides, not limits that justify omitting necessary criteria.
- Usually use 3–5 numbered acceptance criteria per story and 2–4 numbered completion checks per task. Each should state one observable result or required piece of evidence; add only what the scope needs, without padding to meet a count.
- Keep dependencies and references to compact lists of IDs and links. Link the relevant PRD, design, decisions, and verification records instead of repeating their rules, rationale, implementation detail, or evidence in every item.
- If an item remains long because it contains independently deliverable outcomes, split it while preserving ID history and coverage. Keep inseparable criteria together.

Stories express user value and independently demonstrable criteria. Technical tasks cover enabling, risk-reduction, operational, or verification work that is not a user story. Preserve the source requirement's `Must`/`Should` priority in the slice scope: do not silently promote optional work or drop cross-cutting criteria. When a `Should` is bundled into a `Must` story, label that criterion optional or record the approved scope decision. Criteria and completion checks must be observable; mark unavailable evidence pending rather than inventing it. Do not create external issues, tickets, or messages unless the user explicitly asks.

## Traceability and state

Map each material PRD requirement to its primary story or task in a `PRD requirement | Primary stories` table. Link requirement headings or their source record; do not mistake a `REQ-###` decision ID for a requirement label. Note cross-cutting requirements only where they are actually inherited and checked. Release-required coverage maps every `Must`; keep `Should` coverage explicit so it is neither silently treated as required nor lost.

The readiness rules must state that stories need a clear user outcome, criteria, dependencies, and required design decisions; technical tasks need purpose and completion checks. Completion remains separate: a slice requires demonstrated criteria, relevant passing checks, required review, operational/documentation work, and product-owner acceptance. Approval of backlog scope does not mark any slice done.

Use Review notes for unresolved design, evidence gaps, assumptions, changes to sequencing, and any authorized follow-up. Link build decisions for meaningful sequencing changes through [record-decision](../record-decision/SKILL.md).

## Check before handoff

Verify story/task ID stability and sequence, each story/task shape, concise wording without lost scope, numbered criteria and completion checks, non-circular dependencies, PRD coverage, decision references, and accurate status. Report missing readiness evidence or acceptance evidence as distinct next actions.

## Offer issue publication

After preparing and checking a new backlog, or a material revision to its stories/tasks, ask whether the user wants the reviewed items raised in an issue tracker. Suggest GitHub Issues without making it mandatory: “Would you like me to create these stories and tasks as GitHub issues, or use another tracker?” Refer to the prepared backlog so the proposed scope is concrete. If a tracker is already agreed, use that destination in the offer instead.

This offer is not authorization to publish. Respect an earlier decline for the same scope; if issue creation is already explicitly authorized, proceed within that scope rather than asking again. Resolve the target repository/tracker from context and ask only for missing details. For authorized publication, preserve story/task IDs and criteria, check for existing matching issues to avoid duplicates, and record resulting issue links against the local backlog items. Do not infer permission to commit, push, or publish unrelated work.
