# Five Synthetic Test Cases

All cases below are fictional and contain no real student data.

| Case | Input / Condition | Expected Result | Recovery / Audit Evidence |
|---|---|---|---|
| **Normal** | All required fields are completed correctly, and an authenticated student submits a request. | Status changes to `Submitted`, then `Ready for Review`. An authorised officer makes the approval decision. Required notifications and departure records are completed according to hostel rules. | Record timestamps, status changes, and the authorised officer's decision. No automatic approval. |
| **Missing Information** | The leave end date is missing. | Submission is blocked, or the request is marked `Needs Information`, with a clear explanation. | The student provides the missing information. Record the validation result without storing unnecessary sensitive data. |
| **Duplicate** | The same student submits two requests for overlapping leave periods. | The system flags the possible duplicate for review without automatically deleting either request. | An authorised staff member reviews the requests and records the decision. |
| **Unauthorised Action** | A student attempts to approve their own request or access another student's request. | The action is denied, and no approval or unauthorised access occurs. | Record the security event with minimal necessary information and review access permissions. |
| **Failed Step** | The application or network fails during submission or parent-notification recording. | The system does not display false success or treat the request as approved. The student is directed to the existing authorised procedure. | Follow the approved paper/SIS fallback, reconcile records after recovery, and document the failure. |

## Pass Criteria

- Status changes follow the defined workflow.
- Only authorised staff can approve leave.
- Students cannot falsely mark parent notification as complete.
- Duplicate requests are flagged for review.
- System failures never imply approval or permission to leave.
- Audit records capture the actor, time, and action without unnecessary sensitive information.