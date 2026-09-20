# Product decisions and tradeoffs

## Dashboard before integrations

**Decision:** Establish the family information model and useful daily workflow before connecting every activity platform.

**Why:** Integrations are plumbing. The product must first prove that a unified view, task list, important-change feed, and conflict detection reduce real parent effort.

## Dedicated inbox instead of personal-mailbox access

**Decision:** Let the parent forward selected messages to a separate inbox.

**Benefit:** Smaller trust boundary and clearer user control.

**Tradeoff:** The parent must configure forwarding rules, and some messages may be missed.

## Parent approval instead of automatic writes

**Decision:** Every extracted item waits for review.

**Benefit:** Errors do not silently modify a sensitive family schedule.

**Tradeoff:** Approval adds friction. Automation should reduce review effort without removing accountability.

## Deterministic extraction before cloud AI

**Decision:** Start with local rules for obvious dates, times, tasks, and sources.

**Benefit:** Predictable behavior, minimal data movement, and a clear baseline.

**Tradeoff:** Complex language and ambiguous schedule changes require more parent correction.

## Important changes rather than a noisy activity feed

**Decision:** Keep routine imports in activity history while surfacing only cancellations, reschedules, closures, early dismissals, edits, and deletions on Overview.

**Why:** Parents need signal, not another stream of notifications.

