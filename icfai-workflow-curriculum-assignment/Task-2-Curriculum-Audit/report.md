# Task 2 — Audit and redesign my curriculum for work in 2030

**Student proposal, not an official ICFAI syllabus revision**  
**Campus/institution:** IcfaiTech, IFHE Hyderabad, Telangana, India  
**Programme:** B.Tech, Computer Science & Engineering (Artificial Intelligence & Data Science)  
**Admission batch:** 2023  
**Programme credit total supplied for this audit:** 166 credits  
**Review/access date:** 24 October 2026  

## Executive summary

This audit asks what the programme should KEEP, UPDATE, REDUCE or ADD to prepare graduates for data science, data engineering and applied AI work by 2030. The proposal preserves mathematics, programming, algorithms, databases, systems and core AI/ML. It prioritises more assessed practice in data quality, reproducible experiments, model evaluation, data pipelines, testing, deployment, monitoring, responsible AI and technical communication.

The stated programme total is 166 credits. A 20–25% redesign target is therefore **33.2–41.5 credits**. This report proposes a **35-credit affected-course scope (35/166 = 21.08%)**, with changes made primarily to learning outcomes and assessments within existing courses. It does **not** propose adding 35 credits on top of the degree. Programme total remains 166 credits in the proposal; any change to compulsory course credits or elective rules is conditional on faculty and regulatory approval.

**Important baseline limitation:** the official public IcfaiTech programme-structure webpage is the source selected for this audit. It lists the CSE (AI & DS) structure but does not itself establish that every displayed code, semester placement and final-year credit arrangement is identical to the 2023 admission batch. It also displays incomplete/ambiguous final-year elective and internship/thesis information. The user-provided 166-credit total is used for the target calculation, but the semester-by-semester historical allocation cannot be represented as independently verified until the applicable 2023 batch scheme is confirmed. This limitation is explicit rather than filled with guessed numbers.

## 1. Scope and method

The audit has four evidence categories:

- **Official published fact:** information visible on the linked IFHE/IcfaiTech programme-structure page.
- **User-supplied baseline:** the stated 166-credit programme total.
- **Proposal:** a recommended change, not current university policy.
- **Unverified/unknown:** a batch-specific detail the selected public source does not settle.

Method: review the published programme structure; identify foundations and course areas relevant to applied AI/data roles; compare five official employer listings; propose ten specific curriculum reasons; document five AI-assisted exercises; design a lab derived from Task 1; and identify what still needs validation. This is a qualitative student audit, not a representative labour-market study or an official syllabus evaluation.

## 2. Programme identity and source baseline

The programme selected is B.Tech CSE (Artificial Intelligence & Data Science), IcfaiTech/IFHE Hyderabad, 2023 admission batch. The official programme structure page is linked in [`curriculum/official-syllabus-links.md`](curriculum/official-syllabus-links.md), with access date 24 October 2026. The page includes course names/codes such as DS202 Database Management Systems, DS204 Design and Analysis of Algorithms, DS205 Operating Systems, DS212 Machine Learning, DS302 Computer Networks, DS305 Data Wrangling and Visualization, DS308 Big Data Systems and DS310 Deep Learning. These are **published-page entries**, not a guarantee that the same codes and placement applied to every 2023-batch student.

The detailed course inventory in [`curriculum/course-credit-map.md`](curriculum/course-credit-map.md) records the published semester entries, their displayed credits and the missing/ambiguous information. Elective alternatives are listed separately; they are not added together because students choose from alternatives. The displayed page does not provide enough unambiguous information to calculate a fully reconciled semester-by-semester total for the 2023 batch. The supplied programme total of 166 is used only for the overall target calculation.

## 3. Main audit finding

The curriculum provides a strong base in mathematics, programming, algorithms, databases, operating systems, networks, machine learning and advanced AI topics. The main proposed improvement is not to replace the foundations with fashionable tools. It is to make students demonstrate that they can build **reliable, reproducible and responsibly evaluated systems** from those foundations.

The job-description sample repeatedly mentions programming, SQL, data preparation and pipelines, statistical/ML evaluation, cloud or production workflows, version control/testing, data quality, monitoring, and communication. These postings include experienced positions as well as an entry-level/associate role; they are used as evidence of skill themes, not as a promise that every listed job is suitable for a fresh graduate.

## 4. KEEP / UPDATE / REDUCE / ADD proposal

### KEEP — preserve core foundations

1. **KEEP — BS103 Linear Algebra and Ordinary Differential Equations; BS105 Probability & Statistics; BS104 Higher Calculus; DS207 Discrete Mathematics (published structure codes).** These support optimisation, uncertainty, model evaluation and algorithmic reasoning. Confirm the exact 2023-batch codes before implementation.
2. **KEEP — ES105 Computer Programming; ES201 Object Oriented Programming; ES106 Data Structures; DS204 Design and Analysis of Algorithms.** Programming and algorithmic foundations remain transferable across AI tools and frameworks.
3. **KEEP — DS202 Database Management Systems; DS205 Operating Systems; DS302 Computer Networks; DS309 Cloud Computing where present in the applicable scheme.** Reliable AI/data products depend on storage, runtime, networking and deployment concepts.

### UPDATE — improve assessment within existing credits

4. **UPDATE — DS202 DBMS:** add a practical data model, constraints, normalisation justification, SQL queries, data validation and a small migration/change exercise. Assess correctness and integrity, not just query syntax.
5. **UPDATE — DS212 Machine Learning:** require a baseline, justified split strategy, appropriate metrics, leakage check, error analysis and limitations. Students must explain why a result is trustworthy, not only report accuracy.
6. **UPDATE — DS305 Data Wrangling and Visualization:** include missing/duplicate/outlier checks, reproducible transformations, clear chart choice, accessible labels and a short stakeholder interpretation.
7. **UPDATE — DS308 Big Data Systems and DS309 Cloud Computing (if present in the applicable batch scheme):** assess a small pipeline/API, versioned configuration, logs, failure recovery, access control and cost/availability trade-offs. Use tools as examples, not as the learning outcome itself.
8. **UPDATE — SP301 Special Project / equivalent project course:** require a problem statement, dataset provenance, baseline, tests, reproducible run instructions, limitations, individual contribution and a demonstration of results.

### REDUCE — remove duplication, not essential foundations

9. **REDUCE — repeated introductory explanations across AI, ML, deep learning, computer vision and NLP:** map learning outcomes first and reduce only genuinely repeated lecture-level coverage. Reinvest that time in experiments and evaluation. This is conditional on faculty mapping; no compulsory course is declared obsolete.
10. **REDUCE — tool demonstrations that are not assessed:** replace a portion of passive demonstrations with guided practical work where students submit a working artifact, tests and reflection. Retain demonstrations when they teach a new concept or accessibility need.

### ADD — introduce through approved elective, project or practical component

11. **ADD — data engineering and MLOps practical module:** data validation, SQL/ETL, version control, experiment tracking, tests, API deployment, logging and basic monitoring. Preferred route: approved elective or practical component, or integration into existing course credits; do not increase the degree total without approval.
12. **ADD — responsible data/AI and experiment-design practicum:** privacy and data minimisation, bias checks, documentation, evaluation sets, failure analysis, hypothesis definition and measurable success criteria. This can be delivered as an approved elective or cross-course assessment if a new compulsory course is not permitted.

The ten core rationales are also summarised in [`curriculum/proposed-curriculum.md`](curriculum/proposed-curriculum.md). The numbered KEEP/UPDATE/REDUCE/ADD actions above exceed the minimum of 8–12 specific reasons; implementation should prioritise the 35-credit scope in the credit table rather than treating every recommendation as a separate credit addition.

## 5. Job-description evidence and curriculum implications

The five official postings are recorded in [`job-market/job-description-comparison.md`](job-market/job-description-comparison.md). The strongest recurring skill themes are:

- Python/programming and SQL/data storage → KEEP programming, DBMS and algorithms; UPDATE practical assignments.
- Data preparation, quality, pipelines and troubleshooting → UPDATE data wrangling and DBMS; ADD data engineering practicals.
- Model building, validation, evaluation and error analysis → KEEP ML/statistics; UPDATE ML/DL assessment.
- Git, testing, reproducibility, cloud deployment and monitoring → UPDATE coding practice, cloud and projects; ADD MLOps practicals.
- Communication and business problem framing → UPDATE project reports, dashboards and presentations.
- Privacy, governance and responsible use → ADD practical governance checks across projects.

The sample is small and roles differ in seniority and specialisation. It indicates skill signals, not universal hiring requirements. Course coverage and assessment gaps are distinguished: databases and ML already appear in the published structure, so the recommendation is more assessed practice rather than claiming these subjects are absent.

## 6. Credit target and balance

The programme total used for calculation is 166 credits, as supplied for this audit.

- 20% target = 166 × 0.20 = **33.2 credits**.
- 25% target = 166 × 0.25 = **41.5 credits**.
- Proposed affected scope = **35 credits**.
- Share affected = 35 ÷ 166 × 100 = **21.08%**.
- Net change to programme total = **0 credits**; proposed total = **166 credits**, subject to approval.

The 35 credits are the full credit values of existing courses whose learning outcomes/assessments are substantively redesigned. They are **not new credits**, and no course is counted twice. A course-level scope register is in [`curriculum/proposed-curriculum.md`](curriculum/proposed-curriculum.md). This count is a proposal mapped to the currently published course inventory and must be reconciled against the 2023 batch code/credit table before being treated as a final institutional accounting.

### Semester-level balancing rule

The public webpage does not provide a reliable, batch-specific final-year allocation, so this report does not invent semester totals. The proposed changes are designed as **assessment changes within existing credit-bearing courses**, producing zero credit delta in every semester once the applicable course placement is confirmed. Any ADD course should replace an existing elective of the same credit value or be integrated into an existing course; a standalone extra-credit addition is not proposed. REDUCE refers to duplicated teaching/assessment time, not cancellation of course credits. A final signed-off semester reconciliation must be completed from the official 2023 scheme before implementation.

## 7. Prerequisites and approval boundaries

- Programming precedes data structures and later software/pipeline work.
- Data structures/algorithms and probability/statistics underpin ML and data analysis.
- DBMS and data wrangling precede more advanced data pipeline tasks.
- ML foundations precede deep-learning evaluation and model deployment exercises.
- Cloud/network fundamentals precede production-service and monitoring exercises.
- A capstone should be scheduled after students have completed the relevant DBMS, software engineering/coding practice and statistics/visualisation prerequisites.

These are proposed learning dependencies; the official prerequisite rules for the 2023 batch must take precedence. Faculty/programme approval is required for any compulsory-course change, credit transfer, elective substitution, or modification to internship/thesis requirements. If regulations prevent a new course, use an assessment module within existing credits or an approved elective.

## 8. Five AI-assisted exercises

The `ai-exercises/` directory documents one authorised, non-confidential exercise in each of five subjects: DBMS normalisation; ML overfitting/underfitting; OS processes/threads; TCP vs UDP; and linear vs binary search. Each record identifies ChatGPT as the tool, date 23 October 2026, the prompt, output summary, review and takeaway. The initial review reported no correction; it did not claim a textbook comparison or code experiment that had not been done. This matches the requirement not to fabricate errors.

To strengthen verification, the remaining recommended action is to add a real check to each record (e.g., a worked dependency example, a small train/test demonstration, a short concurrency example, a protocol reference check, or a runnable search example). Record the actual result and correction, if any. Do not state that these checks were completed unless they were performed.

## 9. Task 1-derived lab/capstone

The proposal is in [`lab-design/task-1-lab-design.md`](lab-design/task-1-lab-design.md). It models the hostel-leave permission workflow using synthetic records only. It tests authorised approval, missing data, duplicates, unauthorised requests and failed steps; it measures elapsed time and support/review effort; and it preserves official human approval and fallback. The host course is proposed as the existing software engineering/industry coding practice or special project course, subject to the 2023 scheme and faculty approval.

## 10. Validation, reflection and limitations

**Validation status:** no completed faculty/recent-graduate interview is evidenced in the supplied project files. This report does not invent one. A validation attempt should ask whether the practical gaps identified are genuine and what regulatory or staffing constraint would block the changes. Record only the person's role, question, feedback and resulting revision, without identifying them. If access is unavailable before submission, retain this explicit limitation and add the attempt/status honestly.

**What could change my mind:** if course assessment documents show that students already complete rigorous, graded data-quality checks, model validation, reproducible pipelines, deployment, monitoring and responsible-AI reviews, the case for adding separate modules becomes weaker; the proposal should then focus on documented assessment quality rather than more content.

**Evidence that could disprove the strongest claim:** a course-outcome and assessment audit showing that the current programme already assesses these skills across multiple semesters, alongside recent graduate or employer feedback showing no practical gap. The job sample is small and includes experienced roles, so a larger local graduate/employer sample could also change the priorities.

Limitations: the selected public curriculum page is live and does not conclusively establish the exact 2023-batch syllabus; the supplied 166-credit total has not been independently reconciled against a full cohort-specific table in this report; several job listings may change; the AI exercise checks were initially conceptual; and no faculty/recent-graduate feedback was available in the supplied evidence. These limitations are disclosed rather than filled with invented facts.

## Appendices / supporting files

- [Official source register](curriculum/official-syllabus-links.md)
- [Course-credit map and unresolved entries](curriculum/course-credit-map.md)
- [Proposed curriculum and 35-credit scope register](curriculum/proposed-curriculum.md)
- [Job-description comparison](job-market/job-description-comparison.md)
- [AI exercise 1 — DBMS](ai-exercises/subject-1.md)
- [AI exercise 2 — Machine Learning](ai-exercises/subject-2.md)
- [AI exercise 3 — Operating Systems](ai-exercises/subject-3.md)
- [AI exercise 4 — Computer Networks](ai-exercises/subject-4.md)
- [AI exercise 5 — DSA](ai-exercises/subject-5.md)
- [Task 1-derived lab design](lab-design/task-1-lab-design.md)
- [Interactive course filter and credit calculator](interactive-course-view.html)

## Conclusion

The proposal retains the core foundations and uses assessment redesign to improve evidence-based, production-aware data science and AI skills. The 35-credit scope equals 21.08% of the stated 166-credit degree, with no net credit increase proposed. Before this is described as a fully verified 2023-batch redesign, the semester course table must be reconciled against the applicable cohort scheme, the credit allocation for final-year requirements confirmed, and an actual validation attempt recorded if access is available. This is a student proposal for discussion, not an official curriculum revision.

