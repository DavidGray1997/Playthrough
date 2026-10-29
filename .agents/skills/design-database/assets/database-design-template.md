# [Initiative] database design

**Status:** [approved/proposed/pending, including what remains] · **Updated:** YYYY-MM-DD

## Purpose and scope

[Links to requirements, domain, API, and current decisions. State the approved business behaviour separately from physical proposals.]

## Relationship overview

[Describe entities, ownership, lifecycle, and relationships. Add an editable Mermaid relationship diagram when it makes the model clearer.]

## Identity, ownership, and isolation

[Primary/external identity, ownership/access boundaries, archival/deletion rules, and sensitive-data handling where applicable.]

## Integrity and derived data

[Foreign keys, uniqueness, checks, immutable history, derived views/projections, and where each invariant is enforced.]

## Time and change semantics

[Authoritative time, local dates/timezones where applicable, timestamps, versions, effective dates, and stored versus derived values.]

## Transactions, concurrency, and retries

[Atomic operations, conflict/lock approach, idempotency, retries, and observable recovery behaviour.]

## Physical design and operations

[Indexes by access path; migrations/backfill/compatibility; retention/deletion/recovery; operational constraints.]

## Open technical review

[Proposals, risky assumptions, required spike/validation, and next action.]
