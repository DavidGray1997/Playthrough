---
name: record-release
description: "Create or update an SDLC release record covering evidenced readiness, actual rollout events, outcomes, and a continue-adjust-stop decision."
---

# Release record

Create or update a release-and-learning record that separates preparation from events that actually happened. Release planning is documentation only; it does not authorize a deployment, migration, support message, external change, or new success claim.

Read relevant phase `questions.md` entries before drafting. Use [resolve-questions](../resolve-questions/SKILL.md) to record newly raised questions and unconfirmed assumptions, link their owning entries from this record, and reconcile answers through the concerned skills. The shared contract governs timestamps, raising/concerned skills, options, response history, and reconciliation status.

## Required context

At the start of every use, read [the shared SDLC document contract](references/document-contract.md). Locate the project root and initiative, then read the PRD and its measures, relevant requirements/release decisions, delivery backlog, verification record, affected design/operations records, existing release record, and actual rollout/monitoring/feedback evidence.

Apply project conventions and explicit user instructions first. Do not transfer a source initiative's release duration, rollout strategy, metrics, stack, support model, owners, or thresholds. Update the relevant phase decisions when the current task includes a new choice or proposal; existing authorization for document work covers directly related record maintenance. Do not create decisions for mere observations.

## Deliverable and format

Use the established release path, or create `docs/initiatives/<initiative>/release/release-record.md`. Use a descriptive H1, explicit status and ISO update date, and preserve the history of release attempts and observations.

Start a new substantive record from [the release record template](assets/release-record-template.md). Copy and adapt it into the initiative; do not edit the skill asset. Retain an established project structure when it already captures the same information.

Make readiness traceable to required scope, verification evidence, approvals/acceptance, operational runbooks, migration and rollback readiness, monitoring, support, and fallback where each applies. Mark genuinely inapplicable operations with a reason. A plan belongs in the deployment/support section; completed actions belong only in actual rollout events, with evidence and timestamps when known.

Compare observed outcomes with PRD success measures. Preserve each measure's stated baseline and target; use `unknown` where they or observations are absent. Do not invent a numerical threshold, baseline, target, monitoring result, feedback, or causal conclusion. Clearly label interpretations and limitations. Link feedback to a durable source when available, while protecting confidential details.

Record the accountable owner and a supported `continue`, `adjust`, or `stop` decision, rationale, evidence, and follow-up. A proposal is not a decision, and an assistant cannot assign an owner or claim that a release is accepted. If the decision or its authority is pending, state the next action instead.

## Status and handoff

Before handoff, verify canonical/existing paths, relative links, stable story/task and decision IDs, actual-versus-planned separation, measure traceability, and accurate readiness state. Reconcile scope or outcome changes with affected PRD, backlog, verification, and decision records when authorized; otherwise report the necessary follow-up. Report documents changed, unresolved release gates, and the next usable action.
