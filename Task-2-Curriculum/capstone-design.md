# Proposed lab/capstone — Student Request Workflow Automation

**Host course:** Proposed within an existing Web Technologies / Software Engineering / Special Project course, subject to the actual batch syllabus and faculty approval.  
**Prerequisites:** Basic programming, HTML/forms, database CRUD, HTTP/API fundamentals, testing basics, and introductory access control.  
**Dataset:** Synthetic request records only. No real student records or private college data.

## Learning outcomes

By the end of the lab, a student should be able to:
1. Translate a process map into a state machine and data model.
2. Implement form validation and duplicate detection.
3. Enforce role-based permissions and human approval boundaries.
4. Record auditable status transitions without storing unnecessary personal data.
5. Test normal and failure cases and document recovery.
6. Measure time/effort with explicit assumptions and explain limitations.
7. Evaluate whether AI adds value compared with deterministic rules.

## Milestones

1. **Process definition:** draw current/hypothetical and proposed workflow; identify owners and approval boundary.
2. **Data model and UI:** build a form, request reference, and status view using synthetic data.
3. **Controls:** required-field validation, duplicate flag, role checks, and audit events.
4. **Testing:** automate five cases: normal, missing field, duplicate, unauthorised request, failed notification.
5. **Measurement:** compare baseline and proposed handling time using a declared synthetic scenario; include support and maintenance effort.
6. **Review and release:** README, test evidence, known limitations, and demo walkthrough.

## Acceptance tests

- Every successful synthetic submission receives a unique ID and timestamp.
- Missing required data cannot enter the approval queue.
- A likely duplicate is flagged and reviewed rather than silently deleted.
- An unauthorised actor cannot approve or retrieve restricted output.
- A failed notification leaves the request intact and creates a recoverable work item.
- All approval and override events are logged with role and timestamp.
- The app contains no live integration or real college records.
- The report clearly labels simulated data and calculated estimates.

## AI boundary

AI is optional. A deterministic state machine should handle validation, permissions, status, and audit records. If an AI FAQ helper is explored, it must use approved content, disclose uncertainty, provide a human escalation path, and never approve a request or decide eligibility.

## Assessment rubric (proposed)

- Workflow and stakeholder clarity: 15%
- Correct controls and approval boundary: 20%
- Test coverage and recovery: 20%
- Auditability and privacy: 15%
- Measured value and assumptions: 15%
- Documentation, reproducibility and reflection: 15%

This is a proposal for academic discussion, not an approved ICFAI course change.
