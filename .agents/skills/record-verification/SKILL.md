---
name: record-verification
description: "Create or update an evidence-based verification record for delivered SDLC slices, mapping stories and acceptance criteria to observed checks and acceptance."
---

# Verification record

Create or update an honest build verification record. It records observed delivery evidence; it does not turn a test plan, an approval to draft, or a passing command into broader approval.

Read relevant phase `questions.md` entries before drafting. Use [resolve-questions](../resolve-questions/SKILL.md) to record newly raised questions and unconfirmed assumptions, link their owning entries from this record, and reconcile answers through the concerned skills. The shared contract governs timestamps, raising/concerned skills, options, response history, and reconciliation status.

## Required context

At the start of every use, read [the shared SDLC document contract](references/document-contract.md). Locate the project root and initiative, then read the relevant PRD, requirements and build decisions, delivery backlog, design records/contracts touched by the slice, existing verification record, and actual available test/review evidence.

Keep established paths and terminology. Do not copy another initiative's users, stack, environments, checks, quality targets, deployment process, or business rules. Update the relevant phase decisions when the current task includes a new choice or proposal; existing authorization for document work covers directly related record maintenance. Do not create decisions for mere observations.

## Deliverable and format

Use the established verification path, or create `docs/initiatives/<initiative>/build/verification-record.md`. Use a descriptive H1, explicit status and ISO update date, and retain earlier slice history. Add one section per delivered or proposed slice rather than overwriting prior evidence.

Start a new substantive record from [the verification record template](assets/verification-record-template.md). Copy and adapt it into the initiative; do not edit the skill asset. Retain an established project structure when it already captures the same information.

Map each relevant story acceptance criterion and technical-task completion check to a precise check, durable evidence source/link, and result. A result must say `pass`, `fail`, `blocked`, `not run`, `planned`, or another equally specific observed state. Keep planned and not-run work visibly separate from observed passes. Link evidence to its source such as a test run, command output, review record, demonstration note, issue, artifact, or authorized acceptance record; never invent evidence URLs, revisions, dates, environments, reviewers, outcomes, or acceptance.

Record relevant automated checks with scope and outcome, and manual checks with setup, expected/observed behaviour, and limitations where that changes confidence. Record review outcomes separately from test results. State operational/documentation work required to use the slice and whether it is complete, pending, or inapplicable with a reason. Failures and incomplete checks need their effect on done/readiness plus a concrete next action.

Product-owner acceptance requires explicit, evidenced acceptance of the relevant slice/criteria. A PRD approval, technical review, or request to prepare this record is not slice acceptance. If it is pending, say so.

## Status and handoff

A slice can be marked done only when the shared contract's demonstrated criteria, relevant passing checks, required review, necessary operational/documentation work, and evidenced product-owner acceptance are all present. It is valid to record partial evidence while work continues; label the remaining gate.

Before handoff, verify stable story/task IDs, decision and document links, criterion coverage, status accuracy, and consistency with the backlog and affected designs. Report what record changed, evidence still missing, and the next usable action. Drafting or updating the record never authorizes tests against an external environment, deployment, messaging, or release.
