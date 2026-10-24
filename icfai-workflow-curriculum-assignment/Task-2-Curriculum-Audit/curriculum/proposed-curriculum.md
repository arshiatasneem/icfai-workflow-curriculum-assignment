# Proposed curriculum changes and credit-impact register

**Status:** Student proposal only; not an official IFHE syllabus revision.  
**Programme total used:** 166 credits (supplied baseline).  
**Target:** 33.2–41.5 affected credits.  
**Proposed affected scope:** 35 credits = 35 ÷ 166 × 100 = **21.08%**.

## Principles

1. Preserve essential mathematics, programming, algorithms, databases, operating systems, networks and core AI/ML.
2. Prioritise demonstrable learning outcomes over adding tool names to the syllabus.
3. Prefer assessment/lab updates inside existing credits; do not add extra degree credits without approval.
4. Count each course's credits once, even if more than one assessment is updated.
5. Course codes below follow the selected live published structure and must be mapped to the actual 2023-batch equivalent before implementation.

## Credit-impact register — 35 affected credits

| Published course reference | Credits counted once | Decision | Proposed change | Semester shown on published page | Prerequisite/approval note |
|---|---:|---|---|---|---|
| DS202 Database Management Systems | 4 | UPDATE | Add integrity constraints, normalisation justification, SQL validation and migration/change test | III | Programming prerequisite; verify batch code/placement |
| DS205 Operating Systems | 4 | UPDATE | Add concurrency/synchronisation exercise and diagnose a failed process/task with logs | III | Programming prerequisite; preserve OS foundations |
| DS204 Design and Analysis of Algorithms | 3 | UPDATE | Require complexity justification, edge cases and tests, not only final answers | IV in published page; placement/code needs reconciliation | Data structures prerequisite; map to actual batch course |
| DS212 Machine Learning | 4 | UPDATE | Baseline, leakage check, split strategy, suitable metrics, error analysis and limitations | IV | Statistics and programming prerequisites |
| DS302 Computer Networks | 4 | UPDATE | Add API/network failure diagnosis and protocol trade-off explanation | V | Systems/programming prerequisites |
| DS305 Data Wrangling and Visualization | 3 | UPDATE | Add data-quality report, reproducible transformations and accessible chart interpretation | V | Programming/statistics prerequisites |
| DS308 Big Data Systems | 3 | UPDATE | Add a small pipeline, schema/data checks, failure recovery and reproducibility | VI | DBMS/data preparation prerequisites |
| DS310 Deep Learning | 4 | UPDATE | Add experimental comparison, validation discipline, error analysis and model limitations | VI | ML and statistics prerequisites |
| SP301 Special Project | 3 | UPDATE | Require tests, provenance, reproducible run, contribution record and demo | VI | Use the actual project course in batch scheme |
| DS415 Data Integration Tools (published elective option) | 3 | ADD/conditional elective substitution | Proposed data-engineering practical: ETL/ELT, validation, lineage and pipeline recovery | Elective basket; semester depends on regulations | Only if offered/eligible; replace a same-credit elective, not add credits |
| **Total affected** | **35** | | | | **21.08% of 166 credits** |

**Interpretation:** The 35 credits are existing course credits whose learning outcomes or assessment would be substantively redesigned. They are not 35 new credits. The DS415 row is a conditional elective substitution and is counted only if an existing 3-credit elective is replaced by it. If the applicable 2023 batch does not offer DS415, use an approved equivalent elective or integrate the learning outcomes into an existing course; retain the same total. Because the live page does not certify 2023 course codes/placements, this register must be reconciled to the cohort scheme before it is final.

## Semester balance — proposed zero-net-credit change

| Semester | Proposed affected credits shown by current public inventory | Credit delta proposed | Proposed semester total |
|---|---:|---:|---|
| I | 0 | 0 | Existing verified 2023 semester total (not reconstructed from live page) |
| II | 0 | 0 | Existing verified 2023 semester total (not reconstructed from live page) |
| III | 8 (DS202 4 + DS205 4) | 0 | Unchanged; assessment redesign only |
| IV | 7 (DS204 3 + DS212 4) | 0 | Unchanged; assessment redesign only |
| V | 7 (DS302 4 + DS305 3) | 0 | Unchanged; assessment redesign only |
| VI | 10 (DS308 3 + DS310 4 + SP301 3) | 0 | Unchanged; assessment redesign only |
| VII | 0 | 0 | Unchanged; final-year allocation requires batch confirmation |
| VIII / elective basket | 3 conditional elective substitution (DS415 or approved equivalent) | 0 | Replace same-credit elective only; no net change |
| **Total scope** | **35** | **0 overall** | **166 credits, subject to cohort-specific reconciliation** |

The semester labels above follow the current published page and are provisional. The target calculation is mathematically correct for the supplied 166-credit denominator; the batch-specific course-to-semester mapping remains an explicit verification dependency. Do not treat the table as a final transcript.

## KEEP / UPDATE / REDUCE / ADD summary

### KEEP
- Mathematics, probability/statistics and discrete mathematics: support modelling, uncertainty and algorithmic reasoning.
- Programming, data structures and algorithms: foundational and transferable skills.
- DBMS, OS, networks and cloud/system foundations: required to understand data and AI products beyond a notebook.
- Core AI, ML, deep learning and data science outcomes: retain depth and prerequisites.

### UPDATE
- DBMS: graded data integrity, normalisation reasoning, SQL and validation.
- ML/DL: baselines, data leakage checks, appropriate metrics, error analysis and limitations.
- Data wrangling/visualisation: reproducible transformations, missing/duplicate checks and audience-aware explanation.
- Coding practice/cloud/projects: Git, tests, APIs, packaging, logs, monitoring and reproducible run instructions.

### REDUCE
- Repeated introductory coverage only after a faculty outcome map confirms genuine duplication.
- Tool demonstrations that do not assess student understanding; replace some with practical evidence.
- No compulsory course or core concept is proposed for deletion without faculty and regulatory review.

### ADD
- Data engineering/MLOps practicals: ETL, validation, version control, experiment tracking, tests, deployment and monitoring.
- Responsible AI/data governance and experiment design: privacy, data minimisation, bias review, evaluation set design and documented limitations.
- Prefer elective substitution or integration within existing credits. Any new mandatory course or credit transfer is conditional on formal approval.

## Ten reasons and evidence links

1. **Foundations remain essential:** programming, maths and algorithms support all later technical work.
2. **DBMS is present, but practice should deepen:** job listings require SQL, data storage and reliable data preparation.
3. **Data quality is operationally important:** add missing/duplicate/schema checks and validation evidence.
4. **ML requires evaluation beyond accuracy:** assess baselines, leakage, metrics and error analysis.
5. **Data pipelines recur across roles:** practice ETL/ELT, troubleshooting, lineage and recovery.
6. **Production work includes software discipline:** Git, tests, reproducibility and documentation should be assessed.
7. **Deployment is different from model training:** introduce APIs, cloud deployment, logging and monitoring.
8. **Responsible use is a practical skill:** projects should demonstrate privacy, access control and bias/limitation review.
9. **Communication matters:** require clear plots, concise reports and explanation of trade-offs.
10. **Credit constraints matter:** update assessments and use approved elective substitution before proposing extra credits.

Evidence comes from the official job listings in `../job-market/job-description-comparison.md`; they are a small sample and include experienced roles. The proposal should be reviewed against actual 2023-batch course outcomes before any implementation.

