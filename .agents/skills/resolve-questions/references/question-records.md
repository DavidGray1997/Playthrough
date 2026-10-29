# Phase question and assumption records

## Paths and identity

Use `docs/initiatives/<initiative>/<phase>/questions.md`, or an explicitly linked established equivalent. Supported phases and prefixes are requirements/REQ, design/DES, build/BLD, and release/REL. Scaffold all four logs when creating an initiative. For targeted recording create only the needed log; do not scaffold on a read-only listing. Keep answered, rejected, superseded and deferred entries for history.

Question IDs are `REQ-Q-001`, `DES-Q-001`, `BLD-Q-001`, or `REL-Q-001`; assumption IDs use `-A-` instead of `-Q-`. Allocate above the highest used number in that initiative's phase/type, including historical entries. Never reuse or renumber IDs. These IDs are distinct from phase decision IDs. A question or assumption belongs to one phase log; other records link to that entry. Deduplicate by meaning before allocating. If an assumption is rejected and a replacement must be decided, open a linked question instead of silently changing the assumption into a question.

## Required fields

Each file has a descriptive H1, phase/initiative, explicit status, and actual ISO update date. Each entry records:

| Field | Meaning |
| --- | --- |
| ID and kind | Stable question or assumption ID; `Question` or `Assumption`. |
| Statement | The exact question or proposed assumption in actionable language. |
| Recorded at | Actual ISO 8601 timestamp with timezone offset, obtained from an available clock. Preserve the original timestamp; use `Unknown` with a reason for legacy entries without evidence. Never invent historic precision. |
| Raising skill | Actual skill that identified it, such as `design-api`; use `User` or `Unknown — reason` when appropriate, never attribute a user-originated question to an uninvolved skill. |
| Concerned skills | Actual skill names with a short reason/record link for each potential impact; use `None identified` only after reviewing impact. |
| Context and references | Why it matters; affected records/sections and decision/story/task IDs. Use portable relative links. |
| Options | Labelled answers with consequences and a recommendation when justified. Permit free-text alternatives. For assumptions, approval/rejection/correction may suffice. If multiple choice would be misleading, record why free text or evidence is required. |
| Resolution state | `Open`, `Deferred`, `Answered`, `Approved`, `Rejected`, or `Superseded`. Questions begin Open; assumptions remain Open until explicitly approved, rejected or corrected. Deferral remains unresolved. A materially corrected assumption supersedes the old assertion and records or links the approved replacement; no silent rewrite. |
| Response history | Revision, exact meaning of the response, actual response timestamp with timezone, authority/source role, evidence, and any superseding response link. Initially `No response`. |
| Decision links | Related material choices in phase `decisions.md`, or `None required — reason`. An answer does not automatically grant a broader checkpoint approval. |
| Reconciliation | Current answer revision, status, affected skills/records, observed adjustments or justified no-change review, evidence and blockers. |

Reconciliation states are `Not started` (unanswered), `Pending`, `In progress`, `Complete`, `Blocked`, or `Not needed — rationale`. Per-skill statuses distinguish pending/in progress/complete/blocked/no change. An unanswered or deferred item cannot claim complete reconciliation. Every response revision starts a new impact assessment; preserve results for older revisions as history and label them superseded. Reconciliation evidence links to actual affected sections or observed checks; never fabricate approvals or test results.

An initiative-wide open list includes Open/Deferred entries of both kinds. Separately list Answered/Approved/Rejected/Superseded entries with Pending/In progress/Blocked reconciliation or unresolved blocking replacements. For a phase filter, show the owning phase's items and identify relevant external dependencies. Missing logs or malformed/partial tracking are limitations to report, not empty results. When recording work is authorized, migrate unresolved legacy questions/assumptions into the owning log, preserve their source/known dates, and replace competing tracking with links without losing context.

## Review and scope

Use existing question sections in PRDs/designs/backlogs for linked context and risks; the phase log owns question state, responses and reconciliation. Keep rollout events and verification results in their canonical records. Reconciliation tables live inside the owning entry, never in an extra file. Read-only discovery and listing do not change records. Record timestamp/answer evidence honestly and protect private identities according to the shared contract. Previously approved assumptions or settled decisions need not be reopened without contradictory evidence or a user request.
