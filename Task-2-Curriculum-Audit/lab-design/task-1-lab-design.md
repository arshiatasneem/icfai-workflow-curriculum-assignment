# Task 1-Derived Lab/Capstone: Improving the Hostel-Leave Permission Workflow

## 1. Host Course and Prerequisites

**Proposed host course:** A suitable software engineering, database, or project-based course in the student's applicable B.Tech CSE (AI & Data Science) curriculum. The final course and course code must be confirmed against the official curriculum for the 2023 admission batch and with faculty.

**Prerequisites:** Basic programming, relational database concepts, form validation, test-case design, introductory spreadsheet calculations, and basic privacy and access-control concepts.

## 2. Connection to Task 1

This lab extends Task 1, which investigates the hostel-leave permission workflow at IFHE/ICFAI. The current-state description draws on an informal account from a hostel resident and the available official hostel rules. The operational details that have not been directly confirmed are treated as reported information, estimates, or assumptions.

The proposed prototype explores whether clearer request tracking, status visibility, duplicate detection, and failure recovery could improve the administration of the workflow.

It is an educational prototype, not an official campus system. It must not replace the existing SIS, written permission, authorised faculty or warden approval, parent notification, or applicable hostel rules.

Only synthetic data may be used. Students must not enter real student names, IDs, phone numbers, leave reasons, or staff contact information.

## 3. Synthetic Dataset

Create 25 fictional hostel-leave requests. Each record should contain:

- `request_id`
- `student_alias`
- `submitted_at`
- `departure_at`
- `return_at`
- `reason_category`
- `required_fields_complete`
- `duplicate_key`
- `requester_role`
- `approver_role`
- `approval_status`
- `parent_notification_status`
- `last_action`
- `failure_code`
- `resolved_at`

Generate all names and identifiers. Include normal requests, incomplete requests, duplicate submissions, an unauthorised approval attempt, a failed notification or database operation, and recovery attempts.

No real student or institutional records should be copied into the dataset.

## 4. Proposed Workflow and Statuses

The prototype should support the following statuses:

`DRAFT → SUBMITTED → NEEDS_INFORMATION → PENDING_AUTHORIZED_REVIEW → APPROVED / REJECTED → NOTIFICATION_PENDING → COMPLETE`

A processing failure moves the request to `RECOVERY_REQUIRED`.

Only an authorised human approver may approve or reject a request. The prototype must record the actor role and timestamp for each transition.

A duplicate submission must link to or reference the existing request rather than create a second approval path. Failed notifications or database operations must not cause a request to be falsely marked complete.

## 5. Milestones

**M1 — Current-state map and evidence (20%)**

Document the hostel-leave workflow investigated in Task 1. Distinguish official rules, second-hand reports, estimates, and assumptions. Identify handoffs, approval points, exceptions, and evidence gaps.

**M2 — Proposed workflow and prototype (25%)**

Define the request fields, statuses, user roles, approval boundaries, duplicate handling, audit trail, and fallback process.

**M3 — Testing and recovery (25%)**

Test the five required scenarios using synthetic data. Record expected results, actual results, pass/fail status, and recovery actions.

**M4 — Value and risk analysis (20%)**

Use the same ROI assumptions and calculation method as Task 1. Examine privacy, access control, failed operations, duplicate requests, and the risks of incorrect status reporting.

**M5 — Demonstration and reflection (10%)**

Demonstrate the prototype, summarise the test results, state the limitations, document individual contributions, and identify what additional evidence would be needed before considering a real-world pilot.

## 6. Acceptance Tests

| Test | Input | Expected result | Pass condition |
|---|---|---|---|
| Normal request | Complete synthetic hostel-leave request | Request enters authorised review; the approver's decision and notification status are recorded | The system never approves automatically, and transitions record timestamps and actor roles |
| Missing information | Required departure or return information is absent | Request enters `NEEDS_INFORMATION` | Missing fields are identified, and the request can be corrected before review |
| Duplicate request | The same synthetic request is submitted twice | Second submission is linked to or flagged against the original | Only one active approval path exists |
| Unauthorised action | A requester attempts to perform an approver-only action | Action is denied and logged | Approval status remains unchanged, and the audit trail records the denied action |
| Failed step | Notification or database operation fails | Request enters `RECOVERY_REQUIRED` | The system does not falsely mark the request complete; retry or manual fallback is available and logged |

The five cases must be tested against the actual prototype or a clearly documented simulation. Students must report the results they observe rather than assume every test passes.

## 7. Measuring Value

Use the same scenarios and assumptions as Task 1 so that the lab and report remain consistent.

**Net time saved:**

`(Monthly requests × affected proportion × minutes saved per affected request) − review/support minutes`

Task 1's illustrative scenarios are:

| Scenario | Assumptions | Illustrative net time saved per month |
|---|---|---:|
| Low | 50 requests; 10% affected; 10 minutes saved per affected request; 30 support minutes | 20 minutes |
| Base | 150 requests; 25% affected; 20 minutes saved per affected request; 60 support minutes | 690 minutes (11.5 hours) |
| High | 300 requests; 40% affected; 30 minutes saved per affected request; 120 support minutes | 3,480 minutes (58 hours) |

These figures are assumptions, not measured institutional results. Students must explain the uncertainty in the request volumes, affected proportions, time savings, and support effort. Synthetic tests alone cannot establish actual campus-wide savings.

## 8. Learning Outcomes and Assessment

By completing the lab, students should be able to:

- Distinguish official requirements from reported information and assumptions.
- Map a real-world administrative process, including handoffs and exceptions.
- Design explicit statuses, roles, and access controls.
- Preserve human approval and existing institutional rules.
- Test duplicate handling, unauthorised actions, and failure recovery.
- Calculate potential value without presenting assumptions as measured results.

**Assessment rubric:**

| Criterion | Weight |
|---|---:|
| Evidence quality and current-state mapping | 20% |
| Workflow, status, and approval-control design | 20% |
| Five test cases and recovery handling | 25% |
| Value calculation and assumptions | 15% |
| Privacy, security, and fallback | 10% |
| Demonstration, clarity, and reflection | 10% |

## 9. Deliverables

Students submit:

1. Current-state hostel-leave workflow map.
2. Evidence log distinguishing facts, reported information, estimates, and assumptions.
3. Proposed workflow, status definitions, role permissions, and fallback procedure.
4. Synthetic CSV or JSON dataset containing 25 fictional requests.
5. Five test records with expected results, actual results, pass/fail status, and recovery details.
6. ROI calculation consistent with Task 1.
7. Risk register and privacy safeguards.
8. Demonstration instructions and individual contribution log.
9. Limitations and reflection, including what additional evidence would be required before a real-world pilot.

The final submission must make clear that the prototype is a student proposal and does not grant permission to leave the hostel or replace the official permission process.