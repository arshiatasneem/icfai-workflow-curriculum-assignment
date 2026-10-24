# Proposed workflow — coordination tracker, not approval automation

## Required inputs

Student's authenticated institutional identity; leave start/end; stated reason; destination/contact only if current policy requires it; mentor details only if applicable; request timestamp; and any required supporting document. Minimize collection and restrict access. Do not store parent phone numbers in a demo or synthetic dataset.

## Statuses

`Draft → Submitted → Needs information → Ready for review → Awaiting authorized decision → Approved / Rejected → Parent notification pending → Notification recorded → Departure record completed → Closed`.

Additional terminal states: `Withdrawn`, `Cancelled`, `System exception`. Use separate timestamps and actor IDs for status changes.

## Accountability and approval boundary

- **Student:** submits accurate information and responds to requests.
- **Process owner:** the institution-designated warden/hostel administration confirms statuses, routing and retention.
- **Authorized approver:** only the Faculty Coordinator/Warden/Assistant Warden or whichever authority current regulations name can grant written permission.
- **Parent notification:** remains a required step when current rules require it; tracker records completion, not inferred consent.
- **Security/gate:** sees only the minimum approved departure details needed for its function.

## Controls

Validate required fields; detect likely duplicates by student + overlapping leave interval; require role-based access; log decisions and changes; never let a student change approval/notification flags; do not use an AI model to make the approval decision; display clear errors; back up data and set retention/deletion rules with institutional authorization.

## Fallback

If the tracker or network fails, stop electronic state changes and follow the currently approved SIS/paper procedure. Authorized staff must reconcile records after recovery; do not treat a draft or stale cached screen as permission. Pilot only with institutional approval.
