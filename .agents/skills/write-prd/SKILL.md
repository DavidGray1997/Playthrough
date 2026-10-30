---
name: write-prd
description: Create or update a testable product requirements document with scope, user experience, requirements, measures, risks, and decision traceability. Use for a substantial feature or release, not routine implementation notes.
---

# Write a PRD

Read [the shared document contract](references/document-contract.md) at the start of **every** run. Read the existing PRD, requirements decisions, relevant evidence, and dependent records before changing the document.

Read relevant phase `questions.md` entries before drafting. Use [resolve-questions](../resolve-questions/SKILL.md) to record newly raised questions and unconfirmed assumptions, link their owning entries from this record, and reconcile answers through the concerned skills. The shared contract governs timestamps, raising/concerned skills, options, response history, and reconciliation status.

Use the [current-phase interview guardrail](../resolve-questions/SKILL.md#keep-the-interview-within-the-current-phase) to distinguish unresolved product choices from design/operations details. When the requirements queue is exhausted, consolidate the PRD and present reviewable content for product-owner approval; report remaining evidence blockers and deferred details separately.

## Choose the record and scope

Use the established PRD path or `docs/initiatives/<initiative>/requirements/prd.md`. Keep one PRD for a substantial feature or release; add a focused story update for a small change unless a separate PRD is needed to avoid ambiguity. Preserve existing useful structure and references. Never import the source project’s domain rules, stack, terminology, styling, duration, metrics, approvals, or test outcomes.

Start from [the PRD template](assets/prd-template.md) when creating a record. Retain these sections in this order: Summary; Problem and goals; Out of scope; Users and experience; Requirements; Success measures; Rollout, dependencies, and risks; Decisions. The document has a descriptive H1 and an `Owner · Status · Updated` line; use ISO dates only when known or current to the actual edit.

## Fill the information contract

- State the problem, intended outcome, affected users, and the main flow in plain terms. Put non-goals in **Out of scope** so they cannot become implied commitments.
- Use the exact requirements table columns: `Priority | Requirement | Acceptance criteria`. Give each requirement an observable criterion; include permissions, accessibility, error/recovery behaviour, privacy, and operational needs where relevant. Use project-defined priorities or `Must`/`Should`; do not invent priority policy.
- Use the exact success table columns: `Measure | Baseline | Target`. Use `TBD` or `Unknown` for unmeasured values. Missing measurement or target input is an open question, not an exclusion, unless the user expressly puts it out of scope. Do not fabricate a baseline, numerical target, research finding, or validation result.
- State rollout intent, material dependencies, risks, and open questions. Planning a rollout is not release approval.
- Keep the Decisions table in the exact form `Date | Decision | Owner`. Each row is a concise pointer to a requirements decision; link its stable ID in `decisions.md` when one exists. The decision log remains the detailed authority record.

## Status and approval

Use an explicit status that distinguishes draft, review, approved scope, and pending evidence. Do not mark the PRD approved without actual product-owner approval evidence. Approval covers only its expressed scope and does not prove design review, implementation verification, slice acceptance, or release readiness.

When a new or changed requirement affects an approved decision, record or amend it through [record-decision](../record-decision/SKILL.md) and reconcile the PRD. When scope changes after stories exist, update directly affected backlog, design, verification, and release records as part of the authorized documentation work; report a broader, out-of-scope follow-up precisely.

## Check before handoff

Confirm every populated requirement has acceptance criteria, each success measure has an honest baseline/target state, decisions link to the requirement decision log, and status/owner/date are clear. Report unresolved questions and the PRD approval checkpoint separately from completed writing work.
