# Task 2 — Curriculum audit and redesign for work in 2030

**Candidate context:** B.Tech CSE, ICFAI University / ICFAITech, Hyderabad; expected graduation 2027 (candidate-reported; confirm official programme and batch)  
**Status:** Candidate-specific course list integrated; official batch regulations, unknown credits and later semesters remain unverified  
**Date prepared:** 23 October 2026

## 1. Executive summary

The proposal is to preserve computer-science foundations and improve evidence-based practical learning in software delivery, databases, cloud, testing, security, AI-assisted development, and responsible evaluation where the candidate's actual syllabus and assessments show a gap. The proposal does not treat existing subjects as obsolete simply because technologies change.

The public ICFAITech B.Tech structure page lists a general CSE programme and several separate CSE specialisations. It lists subjects including Data Structures, Database Management Systems, Web Enabled Technologies, Cloud Computing, Software Testing, Computer Networks, Machine Learning, and Software Engineering in the general CSE structure. The same page also lists other structures with different course codes. Therefore, course codes and credits below are provisional until matched to the candidate's exact admission batch and programme. See official source links in `../evidence/sources-and-limitations.md`.

The candidate reports a 168-credit programme total. The current proposal affects 38 unique existing course credits (22.62% of 168), which falls within the 20–25% band if the reported total is correct. The exact curriculum version, mutually exclusive electives, and programme regulations are not independently verified, so the percentage remains conditional. The semester-level proposal is documented below and should not be described as officially verified.

## 2. Baseline and method

### Programme identity to verify
- Institution/campus: ICFAITech / IFHE Hyderabad (confirm exact official wording)
- Degree: B.Tech
- Branch/specialisation: Computer Science and Engineering (confirm whether general CSE or a named specialisation)
- Admission batch: candidate-reported 2023; confirm official record
- Applicable curriculum version/regulations: **not yet verified**
- Public reference accessed: 20 October 2026

### Public curriculum observations
The public general CSE structure page includes:
- ES 106 Data Structures (4 credits in the displayed table)
- CS202 Database Management System (4 credits in the displayed table)
- CS208 Web Enabled Technologies (4 credits in the displayed table)
- CS309 Cloud Computing (4 credits in the displayed table)
- CS311 Software Testing (3 credits in the displayed table)
- CS302 Computer Networks (4 credits in the displayed table)
- CS304 Machine Learning (4 credits in the displayed table)
- CS305 Software Engineering (3 credits in the displayed table)

These are facts about the public page as accessed, not confirmation that the same codes/credits apply to the candidate's batch. The page shows separate programme/specialisation tables, so codes can differ between structures. Do not mix rows from different programme variants. For the candidate-specific 38-credit proposal in Section 6, use the course codes from `candidate-reported-curriculum.csv`; the public-page codes in the initial recommendation table are reference examples only.

### Required baseline validation
1. Obtain the syllabus and academic regulations for the candidate's admission batch from an official source or authorised office.
2. Check every semester and course code/title/credit.
3. Mark elective baskets and mutually exclusive choices; do not add all options together.
4. Confirm internship, thesis, summer term, and zero-credit requirements.
5. Sum required credits and compare with the official programme total.
6. Save a PDF/screenshot or official source URL and access date where permitted.

## 3. Initial recommendations (provisional, subject to syllabus and assessment review)

The 10 proposals below are provisional recommendations based on the public structure and candidate-reported course list. Confirm course codes, outcomes, contact hours, assessments, and student practice opportunities against the candidate's official batch syllabus before treating them as final curriculum changes.

| # | Course area / reference from public structure | Proposed classification | Reason to verify | Proposed change |
|---|---|---|---|---|
| 1 | ES 106 Data Structures | KEEP | Core data structures and algorithmic reasoning remain foundational | Preserve implementation and complexity analysis; use timed coding and test cases |
| 2 | CS204 Design and Analysis of Algorithms | KEEP | Algorithmic reasoning supports efficient software and problem solving | Keep proofs/analysis and add practical performance comparison if missing |
| 3 | CS202 Database Management System | UPDATE | Job requirements include data persistence and database systems | Add assessed SQL queries, schema design, transactions, indexing and safe parameterised queries if not already practiced |
| 4 | CS208 Web Enabled Technologies | UPDATE | Web APIs and application integration are common software delivery tasks | Assess API contracts, validation, authentication, accessibility and integration tests if not covered |
| 5 | CS309 Cloud Computing | UPDATE | Cloud roles require deployment, monitoring, security and cost awareness | Add a small deployment, least-privilege access, logs/metrics and budget guardrails if absent |
| 6 | CS311 Software Testing | UPDATE | Testing should cover unit, integration, negative and regression cases | Assess test design, CI execution, failure diagnosis and coverage limits |
| 7 | CS305 Software Engineering | UPDATE | Requirements, version control, reviews, collaboration and lifecycle ownership are useful across roles | Use a team-style issue/PR/review/release workflow in assessment |
| 8 | CS302 Computer Networks | KEEP | Networking concepts underpin cloud, security and distributed systems | Preserve fundamentals; use practical HTTP/DNS/TLS/network troubleshooting exercises where appropriate |
| 9 | CS304 Machine Learning | UPDATE | AI output needs evaluation, data quality checks, error analysis and responsible use | Assess baseline comparisons, test data separation, metrics, limitations and reproducibility |
| 10 | Proposed cross-course workflow automation lab | ADD, subject to regulations | Integrates databases, web development, testing, security, human approval and measurement | Credit-neutral lab/capstone using synthetic requests and explicit acceptance tests |

**Candidate-requested REDUCE candidates:** Essence of Indian Traditional Knowledge (0 credits), Environmental Sciences (2), Dynamics of Social Change (3), Constitution of India (0). Reduction means streamlining delivery/overlap, not deleting mandatory outcomes. The candidate reports that Integral Transforms and Probability & Statistics and Fundamentals of Signal Processing were already reduced for junior batches; this is unverified and **not** claimed as a new proposal. Data Science, Machine Learning, Power Skills I–IV, and Blockchain Technology remain KEEP. See `candidate-reported-curriculum.csv` for the candidate-specific audit.

## 4. Job-description comparison

See `job-description-comparison.md`. The three public postings reviewed include software-development lifecycle, programming, data structures/algorithms, testing, cloud/database exposure, monitoring/troubleshooting, and collaboration. They differ in seniority, so the comparison uses them as evidence of task/skill themes, not as a claim that all are suitable graduate vacancies. Save the exact job pages and access dates before final submission.

## 5. Five AI-assisted learning exercises

See `ai-exercise-log.md`. Five possible exercises cover data structures, databases, networks, software testing, and cloud computing. The exercise log records AI-generated examples and their desk-based checks; SQL, application tests and cloud deployment are not claimed as executed.

## 6. Credit proposal and 20–25% calculation

### What the available data supports
The candidate-provided course list contains **133 known credits** across the supplied first-six-semester rows plus Internship-I. The candidate now reports that the full programme requires **168 credits**. The 168-credit total is candidate-provided and has not been independently verified against official regulations; use it as the working denominator while clearly labelling that limitation. The 133-credit figure remains a known subtotal, not the full degree total: DS201 Artificial Intelligence has no supplied credit value, additional named subjects have unknown semester/credits, and semesters VII/VIII details are missing.

The revised proposal identifies **38 unique existing course credits** for substantive assessment updates. Each selected course credit is counted once even if its updated assessment also contributes to the capstone. No new degree credits are added and no existing course credits are deleted in this assessment-update scenario.

### Target calculation
- Candidate-reported programme total: **168 credits**
- Requested target: **22.5%**
- Exact mathematical target: `168 × 0.225 = 37.8 credits`
- Since this plan counts whole course credits, round up to **38 unique affected credits** to meet or exceed 22.5%.
- Proposed affected share: `38 ÷ 168 × 100 = 22.62%` (about **22.6%**).

This meets the requested 20–25% band **if 168 is the correct official total**. If the official total differs, recalculate the target using the verified denominator.

### Selected existing-course assessment updates

| Candidate-reported semester | Course | Credits counted as affected | Proposed change |
|---|---|---:|---|
| III | MA202 Discrete Mathematics | 3 | Add assessed graph/logic problem-solving with written reasoning and edge-case tests; preserve core mathematical outcomes |
| III | EC201 Introduction to IoT | 3 | Add a small secure device-to-service data-flow exercise with validation, threat notes and a test plan |
| IV | CS206 Database Management Systems | 4 | Assess SQL, schema design, transactions, indexing, parameterised queries and data security |
| IV | CS205 Web-Enabled Technologies | 4 | Assess API contracts, validation, authentication, accessibility and integration tests |
| V | CS302 Operating Systems | 4 | Practical troubleshooting, concurrency and resource diagnostics |
| V | CS301 Principle of Cryptography | 3 | Applied secure-development exercise and threat/limitations analysis |
| V | CS304 Software Engineering | 3 | Requirements, version control, review, testing and release workflow |
| VI | DS307 Big Data Systems | 3 | Reproducible data pipeline, validation and monitoring |
| VI | CS307 Cloud Computing | 4 | Deploy-and-observe lab with least privilege, logs and cost controls |
| VI | CS306 Computer Networks | 4 | DNS/TLS/network troubleshooting and evidence-based diagnosis |
| VI | SP301 Special Project | 3 | Integrated capstone with acceptance tests and a measured outcome plan |
| **Total unique affected credits** |  | **38** | **Assessment/learning-outcome changes within existing courses; credit-neutral** |

These changes update assessed learning within existing courses. They do **not** mean that 38 credits are newly added, removed, or replaced in the degree.

### Sensitivity check
The 38-credit proposal is within the 20–25% band for a 168-credit programme. Examples show why the denominator matters.

| Programme-total scenario | 38 affected credits as a share | Interpretation |
|---:|---:|---|
| 150 | 25.3% | Slightly above 25%; recheck the target |
| 160 | 23.8% | Within 20–25% |
| **168 (candidate-reported)** | **22.6%** | **Within 20–25%, if total is correct** |
| 170 | 22.4% | Within 20–25% |
| 180 | 21.1% | Within 20–25% |
| 200 | 19.0% | Below 20%; additional credits would need substantive assessment updates |

**Decision rule:** verify the official total and use `ceil(0.225 × total credits)` for a target of at least 22.5%, then confirm the resulting share does not exceed 25%. Do not count any course twice. If the official total is 168, 38 affected credits is the appropriate whole-credit target.

### Semester-by-semester balance
- **Semesters I–III:** preserve programming, mathematics, data structures, discrete mathematics and communication foundations; integrate small testing/version-control practices without claiming additional credits.
- **Semester IV:** update 8 unique credits across DBMS and Web-Enabled Technologies.
- **Semester V:** update 10 unique credits across Operating Systems, Cryptography and Software Engineering.
- **Semester VI:** update 14 unique credits across Big Data Systems, Cloud Computing, Computer Networks and Special Project.
- **Semesters VII–VIII:** keep the capstone/internship/thesis aligned with official prerequisites and credit rules once the applicable structure is confirmed; do not assign unknown credits or assume that public-page internship/thesis rows are additive.

This is a credit-neutral redesign of assessed learning in 38 existing credits, not a claim that 38 credits are removed or newly created. The candidate-requested REDUCE subjects remain as previously documented; the recommendation is to streamline delivery while preserving mandatory outcomes, not to remove required courses. The four requested REDUCE candidates carry 0, 2, 3 and 0 candidate-reported credits respectively, so they alone cannot constitute a 20–25% redesign of a full degree.

## 7. Task 1 capstone connection

The proposed capstone is a Student Request Workflow Automation Lab. It uses a synthetic dataset and demonstrates input validation, role-based approval, duplicate handling, audit logs, failure recovery, and measurable time/effort outcomes. See `capstone-design.md`.

## 8. Validation and falsification

No faculty member or recent graduate has validated this draft yet. If a willing person is available, ask one focused question: “Which practical task do new graduates most often struggle with that this curriculum could help them practise?” Record role only, date, question, anonymised summary, and what changed. If access is unavailable, state that plainly.

The strongest claim—that more integrated, assessed practice in testing, cloud delivery, and AI evaluation would improve work readiness—could be weakened if current course assessments already provide strong repeated practice and graduates can demonstrate those skills reliably. Evidence to collect includes actual syllabi, assignment rubrics, three job descriptions, exercise results, and optional feedback.

## 9. Limits and next steps

1. Verify exact programme/batch/curriculum version.
2. Official semester VII–VIII course details are unavailable; keep the limitation explicit.
3. Confirm credit total and elective rules.
4. Complete three job-description evidence records.
5. Review five documented AI exercises and retain their verification limitations.
6. Use the documented 38-credit scenario (22.62% of the candidate-reported 168-credit total) and recalculate if the official total differs.
7. Seek voluntary faculty/alumni feedback if feasible; otherwise record unavailable access.
8. Update README with final evidence and commit/release links.
