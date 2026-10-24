# Task 1 Report — Investigation and Redesign of the Hostel Leave Workflow

## 1. Executive Summary

This report investigates the reported hostel-leave permission process at ICFAI Foundation for Higher Education (IFHE) and proposes a small digital coordination tracker to improve visibility, completeness checks, handoffs, and status tracking.

The investigation focuses on a specific administrative workflow: a hostel resident requests permission to leave the hostel, the request is reviewed by authorised personnel, required parent notification is handled, and the permission process is completed according to institutional rules.

The preliminary investigation identified possible friction points, including physical paperwork, repeated visits to obtain signatures, waiting when a required person is unavailable, and uncertainty about the status of a request. However, the detailed modern workflow was described informally by a hostel resident and has not yet been independently verified through direct observation or an official staff interview.

The official 2018 IFHE Hostel Rules and Regulations document states that a hosteller must inform the institution in writing of the reasons for and duration of the proposed absence and obtain written permission from the Faculty Coordinator, Warden, or Assistant Warden before leaving. Parents are also to be informed. The proposed improvement therefore supports the existing process rather than replacing its approval requirements.

The proposed solution is a lightweight status tracker that records requests, checks for missing information and duplicates, identifies the next responsible person, and maintains an auditable history. It does not automatically grant permission, remove required signatures, or replace parent notification.

Five synthetic test cases are proposed to evaluate normal processing, missing information, duplicate requests, unauthorised actions, and failed steps. An illustrative return-on-investment analysis estimates that the base scenario could save 690 minutes per month after support effort. This is a scenario calculation, not a measured outcome.

The principal conclusion is that a simple coordination tool may reduce avoidable administrative effort, but its actual benefit must be established through a baseline study and a limited pilot approved by the institution.

## 2. Purpose and Objectives

The purpose of this investigation is to understand how a small college administrative workflow operates and identify a practical improvement that can be evaluated without building a full production system.

The specific objectives are to:

1. Document the reported current hostel-leave workflow.
2. Distinguish official rules from informal reports and unverified details.
3. Identify potential delays, repeated effort, handoffs, and failure points.
4. Estimate the scale of the problem without presenting assumptions as measured facts.
5. Propose a redesigned workflow with defined inputs, statuses, owners, approvals, and fallback procedures.
6. Test the proposed design against five synthetic cases.
7. Estimate potential net time savings after accounting for review and support effort.
8. Identify privacy, security, operational, and implementation risks.

## 3. Scope and Boundaries

### 3.1 Included in scope

The investigation covers:

- Submission of a hostel-leave request.
- Completeness checks.
- Identification of the appropriate reviewer.
- Approval and parent-notification tracking.
- Request-status visibility.
- Recording handoffs and exceptions.
- Recovery from incomplete or failed processing.
- Estimation of administrative time savings.

### 3.2 Outside the scope

The proposal does not attempt to:

- Change the institution's hostel rules.
- Replace the authorised Faculty Coordinator, Warden, or Assistant Warden.
- Automatically approve leave requests.
- Remove required written permission.
- Eliminate parent notification requirements.
- Modify official student information systems.
- Create a production application connected to institutional databases.
- Claim that the proposed workflow has been implemented or accepted by the institution.

The proposed tracker is a coordination aid only. The institution's authorised personnel remain responsible for approval and compliance with the applicable rules.

## 4. Evidence and Source Quality

The investigation uses two types of evidence: an official institutional document and an informal account of the current process.

### 4.1 Official source

**Source:** IFHE Hostel Rules and Regulations, 2018.

Official document:  
https://www.ifheindia.org/IFHE-Hostel-Rules-and-Regulations-2018.pdf

The rules state that a hosteller must inform the institution in writing about the reasons for and duration of an absence and obtain written permission from the Faculty Coordinator, Warden, or Assistant Warden before leaving. Parents are to be informed.

This establishes the importance of written permission and parent notification. It does not independently establish every step of the current SIS, printing, signature, stamping, or register-entry process.

### 4.2 Informal workflow account

A hostel resident informally described a process involving an SIS form, printing, a mentor's signature on weekdays, a visit to the Warden, parent contact, multiple stamped copies, and entries in registers.

This account is useful for forming an initial workflow hypothesis, but it is not equivalent to a formal interview, direct observation, or official confirmation.

### 4.3 Evidence classification

| Evidence item | Classification | What it supports | Limitation |
|---|---|---|---|
| Written permission is required before leaving | Officially documented rule | The approval requirement must be preserved. | The current applicability of the 2018 document should be confirmed. |
| Parents must be informed | Officially documented rule | Parent notification must remain part of the process. | The exact current notification method is not established by the evidence collected. |
| SIS form is filled and printed | Informal report | A possible current submission step. | Not directly observed or confirmed by staff. |
| Mentor signature is reportedly required on weekdays | Informal report | A possible handoff or availability dependency. | The current requirement and exceptions are unverified. |
| Warden review and parent contact occur | Informal report, consistent with the general approval context | Potential review and notification steps. | Current roles, sequence, and accepted methods need confirmation. |
| Multiple copies and register entries are used | Informal report | Potential duplicate administrative effort. | Not directly observed. |
| Requests may be delayed when staff are unavailable | Hypothesis based on the reported workflow | A possible source of waiting time. | Frequency and actual delay duration are unknown. |

## 5. Current Workflow

The following is a **provisional reconstruction** based on the informal account. It must not be represented as a fully verified description of current institutional practice.

See `workflow/current-workflow.md` for the detailed workflow map.

### 5.1 Reported sequence

1. The student completes a hostel-leave form through the Student Information System (SIS).
2. The student prints the form.
3. The student obtains a mentor's signature, reportedly on weekdays.
4. The student visits the Warden during the available office period.
5. The Warden reviews the request and contacts a parent or guardian, according to the reported process.
6. Permission is documented, reportedly through stamped copies.
7. Copies are distributed to relevant parties or security points.
8. Information is entered into registers.
9. The student follows the applicable procedure when leaving and returning.

The exact order, required copies, responsible roles, and current recordkeeping practices must be verified with authorised staff.

### 5.2 Handoffs and potential bottlenecks

| Stage | Reported activity | Potential issue | Evidence status |
|---|---|---|---|
| Form submission | Complete the SIS form | Incomplete or incorrect information | Process detail reported informally; error frequency unknown. |
| Printing | Print the form | Printer access or repeated printing | Potential issue, not measured. |
| Mentor review | Obtain a signature | Staff availability and weekday dependency | Reported informally; current requirement unverified. |
| Warden review | Present the request | Queueing or office-hour constraints | Reported informally; waiting time unknown. |
| Parent notification | Contact parent or guardian | Unanswered calls or unavailable contact details | Reported informally; frequency unknown. |
| Permission documentation | Stamp or distribute copies | Repeated manual handling | Reported informally; current process unverified. |
| Recordkeeping | Update registers | Duplicate entry or inconsistent records | Reported informally; error rate unknown. |
| Departure or return | Follow permission and security procedures | Uncertainty if records are unavailable | Possible failure mode; requires staff confirmation. |

### 5.3 Initial problem statement

The initial problem is not that the approval process is unnecessary. Rather, the reported process may require students and staff to coordinate several physical steps without a single visible view of request completeness, current status, responsible person, and next action.

If confirmed, this could lead to avoidable visits, waiting, repeated data entry, and uncertainty about whether a request is complete.

The investigation does not yet establish how often these problems occur or how much time they consume.

## 6. Problem Scale and Baseline

### 6.1 Current evidence limitations

The investigation does not have:

- A measured monthly request count.
- A direct observation log of complete request journeys.
- A representative sample of processing times.
- An official count of incomplete or duplicate requests.
- An interview with the Warden or administrative staff.
- Measured time spent on review, parent notification, and recordkeeping.

Consequently, the actual scale of the problem remains unknown.

### 6.2 Baseline data to collect

Before implementation, a short baseline study should record the following, using approved and privacy-conscious methods.

| Metric | How to measure it | Why it matters |
|---|---|---|
| Requests per month | Count requests over an agreed observation period. | Establishes workflow volume. |
| Total elapsed processing time | Record submission and completion timestamps. | Measures how long students wait for completion. |
| Active staff handling time | Sample the time spent reviewing and recording requests. | Distinguishes actual work from waiting time. |
| Incomplete requests | Count requests returned for missing information. | Identifies opportunities for better validation. |
| Duplicate records | Count confirmed duplicate submissions or entries. | Measures repeated effort. |
| Availability-related delays | Record delays attributed to staff availability. | Identifies handoff constraints. |
| Failed processing steps | Record failures and recovery effort. | Measures reliability and support needs. |
| Parent-contact outcomes | Record completion status without collecting unnecessary details. | Identifies notification-related bottlenecks. |

The baseline should avoid collecting sensitive details beyond what is necessary to evaluate the process. Student identities and reasons for leave should not be included in the analytical dataset unless explicitly authorised and necessary.

## 7. Proposed Workflow Improvement

### 7.1 Proposed solution

The proposed improvement is a lightweight hostel-leave request tracker.

Its purpose is to make the current process easier to coordinate by showing whether a request is complete, who is responsible for the next action, whether the authorised approval has been recorded, and what remains outstanding.

It is not an automated approval engine and does not independently establish permission to leave.

### 7.2 Proposed inputs

Subject to institutional approval, a request record could contain:

- A unique request ID.
- The minimum student identifier required by the institution.
- Submission date and time.
- Requested departure and return dates or times.
- Reason or category, only to the extent required by the official process.
- Required supporting information, if applicable.
- Current workflow status.
- Current responsible role.
- Approval status and authorised approver reference.
- Parent-notification status.
- Last-updated timestamp.
- A short operational note for exceptions, avoiding unnecessary sensitive information.

Access to student identifiers and leave details must be restricted to authorised users.

### 7.3 Proposed workflow statuses

| Status | Meaning | Next action |
|---|---|---|
| Draft | Request has been started but not submitted. | Student completes the request. |
| Submitted | Request has been received. | Tracker checks required fields. |
| Incomplete | Required information is missing or invalid. | Student corrects the request. |
| Awaiting mentor review | A mentor review is required under the confirmed process. | Authorised mentor reviews it. |
| Awaiting authorised approval | Request is ready for the designated approval authority. | Faculty Coordinator, Warden, or Assistant Warden reviews it as applicable. |
| Awaiting parent notification | Required parent or guardian notification is not yet recorded as complete. | Follow the authorised notification procedure. |
| Approved and documented | Authorised approval and required documentation are recorded. | Student follows the existing departure procedure. |
| Rejected | An authorised person has declined the request. | Student follows the communicated decision. |
| Withdrawn | Student has withdrawn the request before completion, where permitted. | Record the withdrawal. |
| Failed / requires recovery | A technical or operational failure prevents normal processing. | Responsible staff use the documented fallback. |
| Closed | The request has reached the institution-defined completion point. | Retain records according to approved policy. |

The final status definitions and sequence must be confirmed with institutional staff. In particular, the institution must determine when a request is considered complete and what evidence is required before a student may leave.

### 7.4 Ownership and approval boundaries

| Role | Responsibility |
|---|---|
| Student | Submit accurate information and respond to requests for corrections. |
| Mentor, if required | Review the request and complete the assigned review step. |
| Faculty Coordinator / Warden / Assistant Warden | Exercise the approval authority specified by the applicable rules. |
| Designated administrative staff | Record required documentation and maintain authorised records. |
| Parent or guardian | Participate in the notification process where required. |
| Tracker administrator | Maintain access controls, availability, backups, and operational logs. |

The tracker must not allow a student, ordinary user, or system administrator acting only in a technical capacity to approve a request outside their institutional authority.

Technical administrators should not gain access to sensitive leave details merely because they maintain the system. Permissions should follow the principle of least privilege.

### 7.5 Proposed validation and duplicate handling

The tracker should check for:

- Missing mandatory fields.
- Invalid date or time ranges.
- Departure times that precede the submission time, where not permitted.
- Duplicate submissions with the same request identifier or matching request details.
- Requests submitted by an unauthorised user.
- Attempts to change approval status without the correct permissions.
- Inconsistent or missing required approval and notification records.

A possible duplicate should be flagged for review rather than automatically deleting an existing request. Staff must retain the ability to distinguish a genuine duplicate from a legitimate revised request.

## 8. Five Synthetic Test Cases

The following cases are proposed tests of the design. They are synthetic examples, not evidence of actual system execution.

### Test 1: Normal request

**Scenario:** A student submits a complete request with valid dates and all required information.

**Expected behaviour:**
1. The tracker creates a unique request ID.
2. Required fields pass validation.
3. The request is assigned to the appropriate reviewer.
4. Each handoff and status change is recorded.
5. The authorised person makes the approval decision.
6. Required parent notification and written permission are recorded according to the approved process.
7. The tracker shows the correct next action or completion status.

**Expected result:** The request progresses through the authorised workflow without unnecessary repeat entry.

**Recovery:** If the next reviewer is unavailable, the request remains pending and displays the responsible role. It is not automatically approved.

### Test 2: Missing information

**Scenario:** A student submits a request without a required departure time or other mandatory field.

**Expected behaviour:**
1. The tracker identifies the missing field.
2. The request is marked `Incomplete`.
3. The student receives a clear correction instruction.
4. The request is not passed to the approval stage until the required information is supplied.

**Expected result:** Incomplete requests are identified early, reducing avoidable review effort.

**Recovery:** The student edits the request and resubmits it. The tracker records the correction without erasing the previous status history.

### Test 3: Duplicate request

**Scenario:** The same student submits the same leave request twice.

**Expected behaviour:**
1. The tracker detects a likely duplicate.
2. The new submission is flagged for review.
3. The original request remains intact.
4. An authorised user confirms whether the new entry is a duplicate or a legitimate change.

**Expected result:** Duplicate processing is reduced without losing legitimate revised requests.

**Recovery:** If the second request is a duplicate, it is linked to or marked against the original record according to the approved data policy. If it is a genuine revision, the authorised process determines how it should proceed.

### Test 4: Unauthorised action

**Scenario:** A student attempts to approve their own request, or a user without approval authority attempts to change a pending request to `Approved`.

**Expected behaviour:**
1. The system checks the user's role and permissions.
2. The action is denied.
3. The request's approval status remains unchanged.
4. The attempted action is logged without unnecessarily exposing sensitive information.

**Expected result:** Only authorised personnel can record the approval decision.

**Recovery:** The request remains with the appropriate authorised reviewer. If the permission configuration is wrong, the administrator corrects it through the approved access-management process.

### Test 5: Failed step

**Scenario:** The tracker becomes unavailable or a required record cannot be saved during processing.

**Expected behaviour:**
1. The failure is reported clearly.
2. The request is not falsely shown as approved or completed.
3. Any successfully saved status remains consistent.
4. The responsible staff member is informed of the issue.

**Expected result:** The system fails safely and does not create a false approval record.

**Recovery:** Staff follow the institution-approved manual process, including the existing written-permission requirements. After service is restored, authorised staff reconcile records to prevent duplicate or inconsistent entries.

### Test summary

| Test | Main control | Expected outcome |
|---|---|---|
| Normal request | Required fields and status transitions | Request follows the authorised workflow. |
| Missing information | Completeness validation | Request returns for correction. |
| Duplicate request | Duplicate detection and review | Existing request is preserved. |
| Unauthorised action | Role-based access control | Approval attempt is rejected. |
| Failed step | Safe failure and fallback | No false approval; manual recovery remains possible. |

These tests define expected behaviour. Actual implementation would require execution, test evidence, and institutional review before the system could be considered reliable.

## 9. Return on Investment and Time-Saving Estimate

### 9.1 Calculation approach

The proposed tracker may reduce time spent on repeated visits, checking status, correcting incomplete requests, and coordinating handoffs. It will also introduce effort for administration, support, and reviewing exceptions.

The estimate therefore calculates net time savings as:

**Net time saved = gross avoidable time saved − additional review and support time**

The calculations below are illustrative scenarios, not measured outcomes.

### 9.2 Scenario assumptions

| Scenario | Requests per month | Share affected by avoidable delays | Avoidable time per affected request | Gross time saved | Additional support effort | Net time saved |
|---|---:|---:|---:|---:|---:|---:|
| Low | 50 | 10% | 10 minutes | 50 minutes | 30 minutes | 20 minutes |
| Base | 150 | 25% | 20 minutes | 750 minutes | 60 minutes | 690 minutes |
| High | 300 | 40% | 30 minutes | 3,600 minutes | 120 minutes | 3,480 minutes |

### 9.3 Calculation details

**Low scenario**

- Affected requests = 50 × 10% = 5.
- Gross savings = 5 × 10 = 50 minutes.
- Net savings = 50 − 30 = 20 minutes per month.

**Base scenario**

- Affected requests = 150 × 25% = 37.5 expected requests.
- Gross savings = 150 × 25% × 20 = 750 minutes.
- Net savings = 750 − 60 = 690 minutes.
- Net savings in hours = 690 ÷ 60 = **11.5 hours per month**.

**High scenario**

- Affected requests = 300 × 40% = 120.
- Gross savings = 120 × 30 = 3,600 minutes.
- Net savings = 3,600 − 120 = 3,480 minutes.
- Net savings in hours = 3,480 ÷ 60 = **58 hours per month**.

The base scenario is an illustration of how the model works. The request volume, percentage of affected requests, avoidable time, and support effort have not been measured.

### 9.4 Important interpretation

The calculation estimates potential time savings from avoidable administrative effort. It does not show that the tracker will shorten every request's total processing time or reduce the time needed for a proper approval decision.

The estimate must be revisited after collecting baseline measurements and conducting a limited pilot.

### 9.5 Pilot measurement plan

A pilot should compare the current process with the proposed tracker using approved, non-sensitive metrics:

- Requests processed.
- Median and range of elapsed processing time.
- Staff handling time.
- Number of incomplete requests.
- Number of duplicate records.
- Number of status enquiries.
- Failed steps and recovery time.
- Time spent maintaining the tracker.

The evaluation should include all additional effort introduced by the tracker. If support time exceeds the time saved, the process should be revised rather than described as beneficial.

## 10. Risks and Mitigations

| Risk | Potential impact | Proposed mitigation |
|---|---|---|
| Outdated or incomplete rules | The tracker could model the wrong approval process. | Obtain confirmation from authorised institutional staff before implementation. |
| Unauthorised approval | A request could appear approved without valid authority. | Enforce role-based access controls and audit approval changes. |
| Exposure of student information | Sensitive leave details could be disclosed. | Minimise stored data, restrict access, and apply approved retention rules. |
| False duplicate detection | A legitimate revised request could be blocked. | Flag possible duplicates for authorised review instead of automatically deleting them. |
| Technical outage | Staff may be unable to access the tracker. | Maintain a documented manual fallback consistent with institutional rules. |
| Incorrect status display | A student could misunderstand a pending request as approved. | Use clear status definitions and prevent approval status from being changed by unauthorised users. |
| Unmeasured benefits | The proposal could overstate its impact. | Measure baseline and pilot performance and report assumptions separately. |
| Low adoption | Staff may continue using separate records without reconciliation. | Obtain staff feedback and agree on a controlled pilot before wider use. |

## 11. Implementation Plan

A limited, staged approach is recommended.

### Stage 1: Confirm the current process

- Obtain the current approved hostel-leave rules.
- Confirm the required form, signatures, approval roles, parent-notification process, copies, and registers.
- Ask authorised staff to verify the provisional workflow.
- Record unresolved questions.

**Deliverable:** A validated current-workflow map.

### Stage 2: Establish a baseline

- Agree on a short measurement period.
- Record request counts and processing times using approved methods.
- Measure incomplete requests, duplicate entries, and delays.
- Avoid collecting unnecessary personal information.

**Deliverable:** A baseline evidence table.

### Stage 3: Design and review the tracker

- Define required inputs and statuses.
- Define roles and approval boundaries.
- Specify duplicate handling and validation.
- Agree on audit logging, privacy, retention, and backup requirements.
- Document the manual fallback.

**Deliverable:** A reviewed workflow design and test plan.

### Stage 4: Conduct controlled testing

- Run the five synthetic test cases.
- Record actual test outcomes if a prototype is built.
- Test permissions, failures, and recovery.
- Resolve defects before considering a pilot.

**Deliverable:** Test evidence and a list of outstanding risks.

### Stage 5: Evaluate a limited pilot

- Obtain institutional permission.
- Use a limited scope and agreed safeguards.
- Compare pilot metrics with the baseline.
- Collect feedback from authorised staff and participating students.
- Decide whether to revise, expand, or discontinue the approach.

**Deliverable:** A pilot evaluation based on measured evidence.

## 12. Limitations

This investigation has several important limitations:

1. The detailed modern workflow was reported informally and was not directly observed.
2. The institutional rules source is from 2018; its current applicability and any subsequent changes must be confirmed.
3. No official staff interview or administrative record review was conducted.
4. The number of monthly requests and the frequency of delays are unknown.
5. The proposed workflow and test cases are designs, not proof of a deployed system.
6. The ROI scenarios use assumptions and cannot establish actual savings.
7. The proposed statuses, data fields, and role assignments must be reviewed by authorised staff.
8. The tracker must not be used to bypass approval, parent notification, written permission, or other current requirements.

These limitations do not make the proposal unusable. They define what must be verified before any implementation decision.

## 13. Conclusion

The preliminary investigation suggests that hostel-leave processing may involve multiple handoffs and repeated administrative activities. A lightweight tracker could improve visibility, detect incomplete or duplicate requests, clarify responsibility, and make failures easier to recover from.

However, the detailed workflow and the scale of the problem remain unverified. The first priority should be to confirm the current rules and process with authorised staff and collect a small baseline dataset. Only then should the institution consider a controlled pilot.

The proposed tracker is intended to support existing administrative procedures, not replace them. Its value should be judged using measured processing time, staff effort, error rates, user feedback, and the additional effort required to maintain it.

## 14. Supporting Files

- `workflow/current-workflow.md` — Provisional map of the reported current process.
- `workflow/proposed-workflow.md` — Proposed tracker workflow, roles, statuses, and fallback.
- `evidence/evidence-log.md` — Evidence classification, observations, assumptions, and unresolved questions.
- `tests/synthetic-test-cases.md` — Five synthetic test scenarios and expected outcomes.
- `roi/roi-calculation.md` — Scenario assumptions and time-saving calculations.
- `sources.md` — Source register and access details.

---

**Report status:** Preliminary student investigation and design proposal.  
**Implementation status:** No production system is claimed to have been built or deployed.  
**Approval status:** Institutional review and approval would be required before a real workflow change or pilot.