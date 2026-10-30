# [Initiative] API design

**Status:** [What is approved, proposed, and pending] · **Updated:** YYYY-MM-DD

This contract design covers [scope]. [Links to PRD, decisions, domain, UX, architecture, and database design.]

## Contract principles and identity

- [Versioning/convention, resource identity, ownership scope, and consistency principle.]

## Access and role projections

| Actor or role | Resource/action | Permitted behavior | Fields intentionally omitted or redacted | Status / reference |
| --- | --- | --- | --- | --- |
| [ ] | [ ] | [ ] | [ ] | [ ] |

## Operations

### [Resource or workflow]

| Operation / provisional route | Purpose | Authorization and preconditions | Success result | Errors and recovery | Status / reference |
| --- | --- | --- | --- | --- | --- |
| [METHOD /path] | [ ] | [ ] | [ ] | [ ] | [ ] |

### Request and response shape: [operation]

```json
{
  "[field]": "[example]"
}
```

**Input rules:** [Required/optional fields, validation, and preconditions.]  
**Response and projection:** [Fields returned or intentionally omitted by role.]  
**Consistency and retry:** [Precondition, idempotency, transaction outcome, or pending decision.]

## Errors

| Condition | Response shape/status convention | Client recovery | Privacy note |
| --- | --- | --- | --- |
| [Validation failure] | [ ] | [ ] | [ ] |
| [Conflict or stale state] | [ ] | [ ] | [ ] |

## Collections, evolution, and consistency

- **Pagination/filtering/sorting:** [Rule or inapplicability reason.]
- **Versioning and compatibility:** [Rule or pending review.]
- **Concurrency, idempotency, and transaction alignment:** [Observable contract and open mechanism.]

## Remaining review

1. [Open question, risk, owner, or validation action.]
