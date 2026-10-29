# [Initiative] domain model

**Status:** [What is approved, proposed, and pending] · **Updated:** YYYY-MM-DD

This model covers [scope]. It describes business concepts and rules; physical storage choices belong in the database design. [Link to PRD and relevant decisions.]

## Core concepts and relationships

```mermaid
erDiagram
    [CONCEPT_A] ||--o{ [CONCEPT_B] : [relationship]
```

| Concept | Meaning and owner | Key relationships and rules |
| --- | --- | --- |
| **[Concept]** | [Business meaning and accountable owner.] | [Relationships, boundaries, and rules.] |

## Ownership and access

- **[Actor or role]:** [Authority, visibility, and boundary.]
- **Data ownership and isolation:** [Who owns records and what must not cross a boundary.]
- **History and audit ownership:** [What historical information survives change or removal.]

## Lifecycle and invariants

### [Concept or workflow]

1. [State, transition, or business invariant.]
2. [State, transition, or business invariant.]

## Integrity and transaction boundaries

| Boundary | Changes that must remain consistent | Concurrent or failure outcome | Status / reference |
| --- | --- | --- | --- |
| [Business operation] | [Changes that succeed or fail together.] | [Observable outcome.] | [Approved/proposed; link.] |

## Remaining review

1. [Question, assumption, or risky rule to validate; owner or next action.]
