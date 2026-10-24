# Task 1 — Investigating and redesigning the student document-request workflow

**Institution context:** ICFAI University / ICFAITech Hyderabad (candidate-reported)
**Working process:** Requesting an official student document
**Primary bottleneck reported:** Obtaining the Principal's signature
**Evidence status:** Current steps are based on the candidate's description dated 23 October 2026; no independent staff interview, timing study, or on-site observation is claimed.
**Date updated:** 23 October 2026

## 1. Executive summary

The candidate reports that a student requesting a document follows this sequence: (1) visit the Student Department, (2) write a request letter, (3) obtain the Principal's signature, (4) return to the Student Department for signature verification, and (5) receive the requested document. The candidate identifies obtaining the Principal's signature as the main delay.

The proposal focuses on making the signature step more predictable and visible without removing, bypassing, or automating the Principal's approval authority. A lightweight request register could record when a letter is submitted for signature, its status, and when it is ready for collection. If college policy permits, the office could also provide a known submission/collection window or an authorised routing process for signature requests. The Student Department would continue verifying the signature and issuing the document under its existing rules.

**Evidence limitation:** The current sequence and bottleneck are candidate-reported, not independently verified. The reasons for the delay (for example, availability, queueing, routing, or unclear timing) have not yet been confirmed. No request volumes or waiting times have been measured. All ROI numbers remain illustrative assumptions only.

## 2. Scope and method

### Scope
One process only: a student requests an official document through the Student Department and obtains the Principal's signature before the department verifies it and issues the document. The exact document type is not specified because no one document type has yet been confirmed as representative.

### Evidence collected so far
- **Candidate-reported process:** Received in a conversation on 23 October 2026.
- **Candidate-reported bottleneck:** Waiting to obtain the Principal's signature.
- **Independent staff/student interview:** Not conducted / not claimed.
- **Direct observation or timed study:** Not conducted / not claimed.
- **Measured request volume or wait time:** None available.

### Next evidence step (permission-first)
1. Ask the Student Department or another authorised process owner whether a short walkthrough or anonymised timing study is permitted.
2. Ask only process questions: when the letter is submitted for signature, how the student knows when to return, what status information is available, and what happens if the Principal is unavailable.
3. Do not photograph or copy real letters, signatures, student IDs, marks, fees, or private records. Record role labels and aggregate timings only, with permission.
4. If access is declined or unavailable, state that clearly and retain the candidate-reported/hypothetical limitations. Do not invent interview answers or timing data.

## 3. Current-state process map

This sequence reflects the candidate's description; it is not independently verified.

1. **Visit Student Department:** The student goes to the department to request an official document.
2. **Write a letter:** The student writes a request letter specifying the required document.
3. **Obtain Principal's signature — reported bottleneck:** The student must get the Principal's signature on the request letter. The candidate reports this as the step that takes the most time.
4. **Signature verification:** The student returns to the Student Department, which verifies the signature.
5. **Document issued:** After signature verification, the Student Department gives the requested document to the student.

### Handoffs and unknowns
The critical handoff is between the student and the Principal's signature step. We do not yet know whether the delay is caused by availability, a queue, travel between offices, limited submission hours, or another reason. Those are hypotheses to investigate, not established facts. We also need to confirm whether there is an existing register, appointment process, or standard turnaround time.

## 4. Problem statement

**Problem to investigate:** Students may have to wait or make repeat visits while trying to obtain the Principal's signature on a document request letter. The candidate reports this as the main delay, but the duration, frequency, and exact cause have not been measured.

**Success measures for a permitted pilot:**
- Median elapsed time from writing/submitting the letter to obtaining the signature.
- Number of visits needed per request.
- Percentage of requests where the student has to return without the signature.
- Staff time spent answering “is it ready?” questions.
- Percentage of requests completed with the existing signature-verification and document-issuance controls intact.

Record baseline and pilot values before claiming improvement.

## 5. Proposed improved workflow

### Minimal, low-cost option
1. Student continues to visit the Student Department and write the request letter, unless the college authorises an alternative.
2. The letter is logged in a simple controlled register with a reference number, submission date/time, requested document category, and status. Avoid storing unnecessary personal data in any public or demo record.
3. The request is routed to the Principal for signature using the college's approved procedure.
4. Status is updated to `Awaiting Principal signature`, then `Signed / ready for verification` when the authorised office confirms the step is complete.
5. The student is told when to return or collect the letter, using an approved channel. Do not send sensitive document details through an unauthorised channel.
6. The Student Department verifies the signature as it does today.
7. The department issues the requested document and marks the request `Completed`.
8. If the Principal is unavailable or the tracking tool fails, the existing approved manual process remains available and the record is reconciled later.

### Optional improvement to test
If the Principal's office and Student Department approve it, establish a predictable submission/collection window or a designated office-to-office routing schedule. This could reduce uncertainty and unnecessary trips. Do not assume the Principal can or should sign without reviewing the request, and do not promise a turnaround time until the office approves one.

### Status model
`Letter prepared → Submitted for signature → Awaiting Principal signature → Signed / ready for verification → Signature verified → Document issued → Completed`

Exception statuses: `Needs correction`, `On hold`, `Manual follow-up required`, `Cancelled`.

### Approval boundary
The Principal remains the authorised signer. The Student Department remains responsible for signature verification and document issuance under its current rules. The proposed register or tracker only records and communicates status; it does not approve requests, create signatures, or release documents automatically.

## 6. Five synthetic test cases

These are test designs, not observed college cases. Mark them “not run” until a prototype or tabletop test is actually performed.

| ID | Scenario | Expected behaviour | Human control / recovery |
|---|---|---|---|
| T1 | Normal request | Create reference; show `Submitted for signature` then `Awaiting Principal signature`; update only when authorised staff confirm progress | Principal signs; Student Department verifies and issues document |
| T2 | Missing information in the letter | Flag `Needs correction`; do not route an incomplete request if required fields are missing | Student corrects the letter; staff clarify required fields |
| T3 | Duplicate request | Flag a possible duplicate; retain both records until a person confirms whether they refer to the same request | Student Department resolves; do not silently delete a record |
| T4 | Unauthorised person attempts to change status or mark as signed | Deny the status change and log the attempt; no document is issued on the basis of an unauthorised update | Authorised staff review the record and follow existing policy |
| T5 | Tracking/notification failure while signature is pending | Preserve the request record, record the failure, and show `Manual follow-up required` | Named process owner uses the approved manual process and reconciles status later |

### Acceptance criteria
- Every request can be traced by a reference number and timestamps.
- Only authorised roles can update signature and verification statuses.
- The tracker never creates a signature or bypasses verification.
- A failed notification does not lose a request.
- A manual fallback remains available.
- Every override and correction is logged with a reason and responsible role.

## 7. ROI and measurement plan

No actual wait times, request volume, number of visits, or staff effort have been measured. The main benefit may be reduced elapsed waiting and fewer unnecessary visits, which is different from staff labour saved. Do not convert waiting time into labour savings unless the method justifies that conversion.

Collect, with permission, a small anonymised sample of requests or use a clearly described process walkthrough. For each request, record:
- elapsed time from submitting the letter for signature to receiving the signature;
- number of trips specifically made because the signature was not ready;
- staff minutes spent on status enquiries or repeated handling;
- whether the request required correction;
- any ongoing register/tracker maintenance time.

### Formulas
- Average signature wait = total elapsed signature-wait time ÷ number of requests observed.
- Repeat-trip rate = requests requiring at least one extra trip because the signature was unavailable ÷ total requests observed.
- Monthly staff time saved = monthly volume × (current staff minutes/request − proposed staff minutes/request) − monthly maintenance minutes.
- Monthly student trips avoided = monthly volume × (current average repeat trips − proposed average repeat trips), if supported by measured or explicitly estimated values.
- Break-even months = one-time implementation effort ÷ monthly net staff minutes saved, only if net savings are positive.

Do not mix student elapsed waiting time with staff labour time in one ROI number. Report them separately.

### Illustrative arithmetic only (not college data)
The earlier sample calculation of 100 requests/month, 20 current staff minutes/request, 10 proposed staff minutes/request, 120 support minutes/month, and 1,200 implementation minutes is retained only as a demonstration of the formula. It is not based on measurements at ICFAI and does not estimate the Principal-signature wait. Replace it with verified or explicitly justified inputs before making a benefit claim.

## 8. Is AI needed?

Not for the core workflow. A simple register, form, status tracker, and role-based permissions are more explainable and likely sufficient. AI should not judge the request, predict whether the Principal should sign, imitate a signature, or bypass the Student Department's verification. If an FAQ assistant is later considered, it should only answer from an approved information source and direct uncertain questions to staff.

## 9. Risks and safeguards

- **Approval bypass:** keep Principal signature and department verification mandatory.
- **False status:** restrict status changes to authorised roles and keep an audit log.
- **Privacy:** minimise fields, restrict access, set retention rules, and use synthetic data in a public demo.
- **False promise of speed:** publish no service-level target until authorised staff approve it.
- **Digital exclusion or outage:** retain the approved paper/manual process.
- **Unproven cause:** investigate why the signature step takes time before selecting a final intervention.
- **Unproven ROI:** measure elapsed wait, repeat trips, and staff effort separately.

## 10. What would change the proposal?

If a permitted walkthrough shows that signature requests are already handled promptly or an existing scheduling/register system works well, the proposal should focus on the remaining evidenced gap or be dropped. If the actual delay is caused by a policy requirement rather than poor coordination, a tracker alone may not shorten the wait. Any change must be approved by the relevant college office and must preserve existing authority and verification controls.

## 11. Completion status

Completed so far: candidate-reported current sequence and reported bottleneck captured; improvement concept and synthetic test designs updated.

Potential follow-up validation (not claimed as completed): seek permission for a process walkthrough, measure timing and request volume if access is granted, and execute the synthetic tests if a prototype is built. Update the ROI only when defensible inputs become available. No independent observation, deployment, or measured improvement is claimed in this desk-study submission.
