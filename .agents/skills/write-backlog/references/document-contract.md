# Shared SDLC document contract

Read this reference whenever generating or updating an SDLC document. Apply explicit user instructions and existing project conventions first; use these defaults when the project has no equivalent convention. This contract is a reusable process, not any source project's product specification.

## Scope and paths

Resolve the project root and initiative from the current task and existing documents. Do not assume the current working directory or invent an initiative name when ambiguity affects existing work. Default to `docs/initiatives/<initiative>/` with `requirements/`, `design/`, `build/`, and `release/` phases. For a substantial feature/release keep one PRD; a small change may stay in its existing story. Keep content proportional to risk and change size. Create `decisions.md` and `questions.md` in all four phases when scaffolding an initiative, even if no entries exist; targeted edits need not scaffold unrelated phases.

Canonical deliverables: `requirements/prd.md`; `requirements/decisions.md`; `design/domain-model.md`; `design/ux-design.md`; `design/architecture-design.md`; `design/api-design.md`; `design/database-design.md`; `design/decisions.md`; `build/delivery-backlog.md`; `build/verification-record.md`; `build/decisions.md`; `release/release-record.md`; `release/decisions.md`. Optional supporting records include `design/design-language.md`, `design/database-schema.md`, `design/database-erd-source.md`, `design/database-erd.md`, and diagram assets. Preserve equivalent established project paths and link them explicitly rather than create competing sources of truth.

The canonical question and assumption logs are `requirements/questions.md`, `design/questions.md`, `build/questions.md`, and `release/questions.md`. Use them for open items and reconciliation tracking; never create a separate reconciliation or handoff file.

Create or revise lifecycle files only at these canonical paths or at an explicitly linked established equivalent. Do not create ad hoc handoff, status, summary, progress, or next-steps artifacts. Record those details in the relevant lifecycle documents; provide task-specific handoff in the task report rather than a new project file.

Use Markdown, a descriptive H1, explicit status and ISO `YYYY-MM-DD` update date, and owner where relevant. Status must state what is approved and what is still pending. Templates define the information contract; retain existing sections and useful detail when updating. Briefly mark genuinely inapplicable topics with a reason; never fabricate content to fill a heading.

## Artifact privacy

Treat every generated or revised repository artifact as commit-visible unless the user gives explicit disclosure requirements. Keep traceability by recording roles and stable pseudonymous IDs (for example, `Product owner` or `Authority-01`), decision IDs, and project-relative evidence links instead of personal names, email addresses, usernames, account IDs, or raw quotations that identify people.

Use project-relative paths or portable placeholders such as `<project-root>/…`. Exclude credentials, tokens, authentication/configuration dumps, private hostnames or addresses, personal catalogue data, and other sensitive values. Use synthetic fixtures when examples need realistic values. Preserve meaningful public provenance, source attribution, required citations, and package metadata or licences; redact only private information.

Before handoff, inspect the intended output, including document metadata, comments, hidden content, embedded material, and historical claims. Remove or generalize sensitive content found there. Report what was checked and any remaining limits; do not claim an artifact contains no sensitive information without evidence. Follow any user-specified disclosure rules.

When the authorized task also commits or publishes these artifacts, inspect the exact staged Git blobs and the author/committer identities on commits and tagger identities on annotated tags being sent. Use an already approved public or pseudonymous identity, such as the user's configured GitHub no-reply identity, and verify the published metadata when the hosting service may create different commit metadata (for example, a squash commit). Prior public exposure does not authorize republishing private information. Invoking this document workflow alone does not authorize changing global Git/account settings or rewriting history; those require authorization for the actual task.

## Sources, decisions, and consistency

Read relevant existing requirements, phase decisions, and dependent documents before drafting. Product scope comes from the PRD and approved requirements decisions; current decisions must be read with later amendments/supersession, not by ID alone. Separate approved product behaviour from proposed technical mechanisms. Never transfer a source project's stack, domain rules, terminology, theme, pilot duration, or metrics to another project unless chosen there.

Each phase decision uses a stable sequential ID: `REQ-###`, `DES-###`, `BLD-###`, `REL-###`. IDs are initiative-scoped; allocate above the highest existing ID, including superseded or moved historical entries. Never renumber/reuse IDs. Record date, decision/proposal, source/authority, status, rationale and effects. Distinguish product-owner choices, implementer choices, and assistant proposals. Approval must cite actual approval evidence and cover only its expressed scope; an instruction to draft documents is not approval of their content. Do not invent names, dates, approvals, research, tests, baselines, or outcomes.

Cite decisions by ID and relative Markdown link to their phase file. Maintain traceability from PRD requirements to stories, acceptance evidence, and release outcomes. Requirement decision IDs are not requirement IDs; use existing requirement labels/headings or explicit links. Stable story/task IDs (`US-###`, `TT-###`) must also survive resequencing. Later changes amend/supersede decisions with links and reconcile affected earlier records; preserve history rather than silently overwrite it. If scope does not authorize a dependent edit, report the inconsistency and needed update.

## Questions, assumptions, and answers

On every invocation, read the current phase's `questions.md` and entries in other phase logs that concern this skill or the records being changed. Record newly identified questions and unconfirmed assumptions in the phase log, naming the actual raising skill and all concerned skills. Before recording, listing, or resolving items, read [resolve-questions](../../resolve-questions/SKILL.md) and its required record reference. Each entry needs a stable phase/type ID, statement, actual recorded timestamp with timezone, raising skill, concerned skills, relevant record links, answer options where practical, resolution history, and reconciliation state. Never treat an assumption as approved because it was recorded. Other records link to these entries rather than maintain competing question lists.

For an initiative-wide request, list open questions and unconfirmed assumptions across all four phases; honor a requested phase filter. Include answered items with unfinished reconciliation separately. Offer to guide the user through resolution after listing. A listing is read-only: missing logs mean tracking is absent, not proof that no questions exist.

When a question is answered or an assumption is approved, rejected, or corrected, immediately use resolve-questions to record the response and reconcile affected records through the raising and concerned skills. Prefer subagents for independent work; retain one coordinator for shared logs and overlapping records. Read and apply each concerned skill within the authorized scope. Keep questions answered and reconciliation pending/blocked until affected records agree; do not claim approval, verification, or release evidence from a response that did not provide it.

## Stage checkpoints

Requirements: problem, users, evidence/assumptions, desired outcomes, scope/exclusions, business rules, testable requirements/acceptance criteria, measures, risks, and open questions; product owner approves the PRD before detailed design. Prior explicit approval remains valid within its stated scope. Drafting or discussing design options to resolve requirements is allowed; label it preliminary and do not claim the checkpoint passed.

Design: domain, UX, architecture, API, database, meaningful trade-offs, unresolved proposals and risky assumptions/spike evidence. Required design review covers changes to core domain rules, user journeys, security, or deployment. Do not infer detailed contract/schema approval from approval of an approach.

Build: stories have user outcome, acceptance criteria, dependencies and needed design decisions; technical tasks have purpose and completion checks. Order small usable slices using actual dependencies, not rigid group barriers. A slice is done only with demonstrated criteria, relevant passing checks, required review, necessary operational/documentation work and product-owner acceptance. Distinguish design/planning checks gating readiness from implementation-dependent checks gating completion or launch. Drafting a backlog does not require pretending those checks are complete.

Release/learn: prepare deployment, migration, rollback and support as needed; record actual rollout, monitor errors/outcomes, compare observations against PRD success measures and collect feedback. Record the owner decision to continue, adjust, or stop and feed findings to the next requirements cycle. Do not invent numerical success thresholds or treat a partial usable demonstration as approval to release incomplete required scope.

## Evidence and autonomy

Scope approval, design review, technical verification, slice acceptance and release readiness are separate. Record missing evidence as unknown/pending/not run, with the next relevant action. Continue independently useful authorized drafting/checking; ask only for information or approval that is genuinely required for a dependent step. Existing authorization persists.

Treat the user's requested work as active until it meets its stated completion conditions, the user changes or stops it, or an actual blocker prevents further progress. Preparatory, partial, or unverified work does not complete the request. If work must stop, state that it is incomplete, identify the unmet condition and blocker, and give the action needed to resume. Do not frame unfinished requested work as an ordinary subsequent task.

Documentation tasks do not authorize deployment, external issue creation, messaging, or other external mutations. Release planning does not itself perform a release.

## Handoff checks

Verify canonical/existing paths, working relative links, decision/story/task ID stability, clear authority and status, traceability, and consistency across affected documents. Confirm that every created or revised lifecycle file has a canonical or established equivalent path. Report document changes, whether the requested work is complete, outstanding decisions/checkpoints and next usable action. Place any incomplete status and its blocker before proposed follow-on work. Structural checks cannot prove business approval or evidence quality.
