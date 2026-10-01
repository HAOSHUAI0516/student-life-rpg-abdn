# Data Flow and Failure Behavior

> Designed behavior; implementation paths will be linked after code import.

## Task completion and progression

```mermaid
sequenceDiagram
  actor Student
  participant UI as Task UI
  participant App as Completion workflow
  participant DB as SQLite
  Student->>UI: Complete task
  UI->>App: Complete(taskId)
  App->>DB: Begin transaction and check task/reward
  alt First eligible completion
    App->>DB: Complete task + insert grant + update progress
    DB-->>App: Commit
    App-->>UI: Updated task and progress
  else Already granted
    App-->>UI: Existing result; no additional reward
  else Validation or write failure
    App->>DB: Roll back if transaction started
    App-->>UI: Failure; retain retryable state
  end
```

Serialize competing completion writes or handle the unique-constraint conflict by returning the existing committed result. Award quantities are stored with the grant so future rule changes do not rewrite history.

## Finance

| Stage | Behavior | Failure outcome |
| --- | --- | --- |
| Form | Collect type, positive amount, category and local date | Explain invalid fields |
| Application | Parse into exact minor units and validate | No write on invalid input |
| Repository | Insert or update a transaction | Return a typed failure |
| Commit | Make the write durable | Keep prior summaries on failure |
| Refresh | Recompute selected-period totals and budget remaining | Offer retry without inserting twice |

Income and expenses remain explicit types. Store money as integer minor units. Net balance is income minus expenses; budget usage includes only matching expenses.

## Calendar and GPA

Calendar presentation combines course occurrences, assignment deadlines, exam dates and general events using stable source identities. Date edits invalidate the affected calendar view. Recurrence generation must not create a second independent copy of a source record.

GPA uses a documented grade-to-point conversion and computes the sum of credits multiplied by points divided by total eligible credits. Ungraded courses are excluded. An empty denominator returns no GPA. Display rounding is separate from the calculation.

## Restart and recovery

Open the database, apply supported migrations, load repository state and render an empty or loaded state. Never silently replace a corrupt database. Explain the failure and preserve the existing file for recovery.

[Architecture index](README.md)
