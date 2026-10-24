# Task 2 — AI Exercise Log (Five Subjects)

**Date of this working session:** 23 October 2026  
**Model used in this session:** ChatGPT, GPT-6  
**Purpose:** Test whether an AI assistant can help with subject exercises, then verify the output against independent technical references or explicit calculations.

**Evidence integrity note:** The prompts and outputs below are recorded from the AI-assisted work prepared in this session. The subnetting arithmetic is independently calculated. The SQL syntax is checked against the MySQL reference. Testing recommendations are compared with pytest documentation. Cloud-security recommendations are compared with AWS Well-Architected guidance. No external code execution, live database query, real cloud deployment, or pytest run is claimed. The candidate should personally review these records and can repeat the prompts in their own ChatGPT session if HKAIVERSE expects screenshots or a separately captured interaction.

---

## Exercise 1 — Data Structures (CS102): Binary search

**Prompt used:**  
“Explain binary search and find the index of target 7 in the sorted array [1, 3, 5, 7, 9, 11]. State the indexing convention, the precondition, and time complexity.”

**AI output recorded:**  
“Using zero-based indexing, the target 7 is at index 3. Binary search repeatedly compares the target with the middle element and discards the half that cannot contain the target. The input must be sorted. Its time complexity is O(log n) in the usual iterative/recursive implementation, and its auxiliary space is O(1) for an iterative implementation.”

**Verification:**  
Manual check: array positions are 0→1, 1→3, 2→5, 3→7, 4→9, 5→11; therefore index 3 is correct. The sorted-input requirement is essential. The complexity statement is correct for standard binary search. No code was executed.

**Result:** Correct for this example; includes necessary precondition and indexing convention.

**Reference:** Python documentation for the `bisect` module (a binary-search-based insertion-point tool): https://docs.python.org/3/library/bisect.html

---

## Exercise 2 — Database Management Systems (CS206): SQL query

**Prompt used:**  
“Assume a table `Employees(employee_id, name, department, salary)`. Write a SQL query to return the names and salaries of employees in the `Engineering` department earning more than 60000, sorted from highest salary to lowest. Explain how to verify it.”

**AI output recorded:**
```sql
SELECT name, salary
FROM Employees
WHERE department = 'Engineering'
  AND salary > 60000
ORDER BY salary DESC;
```
“The `WHERE` clause filters rows by department and salary; `ORDER BY salary DESC` sorts qualifying rows from highest salary to lowest.”

**Verification:**  
The query uses standard `SELECT`, `FROM`, `WHERE` and `ORDER BY` structure documented by MySQL. The predicate is strictly greater than 60000, so employees earning exactly 60000 are excluded as requested. Since no actual database or sample rows were provided, the query was syntax-reviewed but not executed against data.

**Result:** Logic and syntax are appropriate for the stated schema; runtime result not tested.

**Reference:** MySQL 8.4 Reference Manual, `SELECT` statement: https://dev.mysql.com/doc/refman/8.4/en/select.html

---

## Exercise 3 — Computer Networks (CS306): Divide an IPv4 network into four equal subnets

**Prompt used:**  
“Divide `192.168.10.0/24` into four equal-sized IPv4 subnets. For each subnet, give the network address, prefix, usable host range, and broadcast address. Show the calculation.”

**AI output recorded:**  
“To create four equal subnets, borrow 2 host bits because 2² = 4. The new prefix is `/26` (255.255.255.192). Each subnet has 64 addresses, normally 62 usable host addresses.”

| Subnet | Network/prefix | Usable host range | Broadcast |
|---|---|---|---|
| 1 | 192.168.10.0/26 | 192.168.10.1–192.168.10.62 | 192.168.10.63 |
| 2 | 192.168.10.64/26 | 192.168.10.65–192.168.10.126 | 192.168.10.127 |
| 3 | 192.168.10.128/26 | 192.168.10.129–192.168.10.190 | 192.168.10.191 |
| 4 | 192.168.10.192/26 | 192.168.10.193–192.168.10.254 | 192.168.10.255 |

**Verification:**  
Independent arithmetic check: `/24` has 256 addresses. Four equal subnets contain 256 ÷ 4 = 64 addresses each. Block starts are 0, 64, 128 and 192; each broadcast address is one less than the next block start, and the last broadcast is .255. Subtracting network and broadcast addresses leaves 62 conventional usable host addresses per subnet. This assumes ordinary IPv4 subnetting, not special-purpose network configurations.

**Result:** Correct for the stated conventional IPv4 subnetting exercise.

---

## Exercise 4 — Software Engineering (CS304): Login feature test cases

**Prompt used:**  
“Create a concise test plan for a login feature. Include positive, negative, boundary/security, and reliability cases. Do not claim that tests have been executed.”

**AI output recorded:**

| Test | Input/condition | Expected result |
|---|---|---|
| Valid credentials | Correct username and password | Login succeeds and a session is established securely. |
| Wrong password | Valid username, incorrect password | Login fails with a generic error; no session is created. |
| Missing fields | Username or password is blank | Validation message appears; request is not accepted as a successful login. |
| Locked/disabled account | Credentials for a locked account | Access is denied and the appropriate safe recovery process is shown. |
| Injection-like input | Special characters or SQL-injection test string | Input is handled safely; no query manipulation or information disclosure occurs. |
| Repeated failures | Many unsuccessful attempts | Rate limiting or another approved abuse-control mechanism is applied. |
| Session handling | Logout, then attempt to reuse the old session | The invalidated session should not grant access. |

**Verification:**  
Reviewed as a proposed test plan: it covers normal, invalid, missing-input, abuse and session cases. Expected behaviour must be confirmed against the application's actual requirements and security design. These are test cases only; no application was available, and no tests were executed. The pytest documentation demonstrates how assertions can be used to verify expected behaviour and report failures.

**Result:** Useful initial test plan; execution and application-specific verification remain outstanding.

**Reference:** pytest documentation, “Get Started”: https://docs.pytest.org/en/stable/getting-started.html

---

## Exercise 5 — Cloud Computing (CS307): Secure document-request tracker

**Prompt used:**  
“Propose a high-level secure cloud design for a college document-request tracker. Students submit requests and receive a notification only after the Principal signs and authorised Student Department staff verify the signature. Include identity, access control, logging, data protection, availability and human approval. Do not claim that a cloud deployment was performed.”

**AI output recorded:**  
“Use a web form or authenticated application connected to an API and database. Give students access only to their own requests; allow authorised Student Department staff to review requests and update processing status; restrict approval/signature recording to the Principal or the authorised workflow. Store timestamps and status transitions in an audit log. Protect data in transit with TLS and at rest using the platform's encryption controls. Keep secrets out of source code, use managed identity/short-lived credentials where possible, back up the database, monitor failures, and restrict who can read logs. Send a notification only after the Principal's signature has been recorded and authorised staff have completed the required verification. Keep a manual fallback for outages and never let AI or the tracker approve/sign on behalf of the Principal.”

**Verification:**  
Compared with AWS Well-Architected security guidance: least privilege, separation of duties, traceability/audit logging, data protection and preparation for security events are consistent with the reference. The workflow preserves human approval and the college's signature-verification rule. This is a conceptual design review only: no cloud provider, IAM policy, application, notification service or deployment was configured or tested.

**Result:** Design is directionally consistent with the cited cloud-security principles; implementation would require threat modelling, college approval, privacy review and testing.

**Reference:** AWS Well-Architected Framework, Security design principles: https://docs.aws.amazon.com/wellarchitected/latest/framework/sec-design.html

---

## Overall reflection

These exercises suggest AI can help explain concepts, draft SQL, perform straightforward calculations, create test ideas and outline a cloud design. Its output still needs checking: database syntax was reviewed but not run, software test cases were not executed, and the cloud design was not deployed. For coursework, AI should support—not replace—understanding, source checking and independent verification.
