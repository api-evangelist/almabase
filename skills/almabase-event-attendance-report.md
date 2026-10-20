---
name: almabase-event-attendance-report
description: Pull an Almabase event with its registrations and guests to report attendance.
api: almabase:almabase-events-api
generated: '2026-10-20'
method: generated
operations:
  - listEvent
  - getEvent
  - listEventRegistration
  - listEventGuest
---
1. `listEvent` to find the event; note its `id`.
2. `getEvent` with `pk` = the event id for venue, schedule and registration configuration.
3. `listEventRegistration` with `parent_id` = the event id.
4. `listEventGuest` with `parent_id` = the event id; count guests per registration.

Every call needs authenticated credentials; an anonymous call returns 403 `{"detail": ...}`. The API is read-only.
