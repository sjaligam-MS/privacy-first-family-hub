# Architecture

## Current data flow

```mermaid
flowchart TD
    A[Parent-selected inputs] --> B[Dedicated inbox or schedule upload]
    B --> C[Local deterministic extraction]
    C --> D[Parent review]
    D -->|Approve| E[Local family schedule]
    D -->|Dismiss| F[Remove review item]
    E --> G[Today, tasks, updates, conflicts]
```

## Trust boundaries

| Boundary | Current behavior |
|---|---|
| Personal mailbox | Not connected |
| Dedicated Gmail inbox | Contains messages intentionally forwarded by the parent |
| Local ingestion process | Reads approved inbox inputs and creates structured proposals |
| Review queue | Stores minimum extracted fields; not full message bodies or attachments |
| Browser dashboard | Stores parent-approved schedule information locally |
| Third-party AI model | Not used in the current prototype |
| Public demo | Uses independently created fictional data |

## Core information model

```mermaid
erDiagram
    FAMILY ||--o{ CHILD : includes
    CHILD ||--o{ EVENT : attends
    CHILD ||--o{ TASK : requires
    SOURCE ||--o{ EVENT : proposes
    SOURCE ||--o{ TASK : proposes
    EVENT }o--o{ EVENT : may_conflict_with
```

The model centers on family logistics—not a comprehensive child profile.

