<h1 align="center">Koushik Chowdary</h1>

<p align="center">
  <b>AI Engineering · Data Engineering · LLM/RAG/Agent Evaluation · AI Security</b><br>
  University of South Florida · Graduate focus: Cybersecurity, AI, Data & Cloud · Python · SQL/PostgreSQL · Airflow · Terraform · FastAPI · AWS/Azure/GCP
</p>

<p align="center">
  <a href="https://linkedin.com/in/koushik-chowdary"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="mailto:kowshiksc610@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>
</p>

---

## What I build

I build AI and data systems that can be inspected, tested, and reproduced. My current work spans LLM/RAG/agent evaluation, AI guardrails, Airflow/PostgreSQL ETL, Terraform/GCP data infrastructure, and security automation. I prefer measurable behavior, explicit limitations, idempotent pipelines, and CI-backed engineering over portfolio-only demos.

### Recruiter quick tour

| Project | What to inspect |
|---|---|
| **[EvalForge](https://github.com/koushikchowdary6/EvalForge)** | Offline-testable RAG and agent evaluation: rank-aware retrieval metrics, benchmark fingerprints, safety/latency coverage, and [non-empty corpus validation](https://github.com/koushikchowdary6/EvalForge/pull/76). [Agent benchmark integrity](https://github.com/koushikchowdary6/EvalForge/pull/75). |
| **[Prompt Injection Detector](https://github.com/koushikchowdary6/prompt-injection-detector)** | Hybrid heuristic + TF-IDF/Logistic Regression guardrail, adversarial text normalization, and [feature-consistent training and leakage-aware grouped CV](https://github.com/koushikchowdary6/prompt-injection-detector/pull/22). Not injection immunity. |
| **[SigmaForge](https://github.com/koushikchowdary6/sigmaforge)** | FastAPI/React detection-engineering platform with RBAC, bounded Sigma structural preflight, and Docker CI. Full pySigma validation and rule persistence remain planned. |
| **[Airflow/PostgreSQL ETL](https://github.com/koushikchowdary6/airflow-postgres-etl)** | Incremental ETL, idempotent upserts, transactional watermarks, nine quality checks, and database integration tests. |
| **[Terraform GCP Data Pipeline](https://github.com/koushikchowdary6/terraform-gcp-data-pipeline)** | Python/DuckDB ingestion, GCS/BigQuery infrastructure design, and integrity-checked incremental state. No live-cloud deployment claim. |
| **[IAM Policy Auditor](https://github.com/koushikchowdary6/iam-policy-auditor)** | Offline AWS IAM risk analysis with conservative principal/Condition validation and [non-finite numeric rejection](https://github.com/koushikchowdary6/iam-policy-auditor/pull/22); not an authorization simulator. |
| **[LLM PII Redactor](https://github.com/koushikchowdary6/llm-pii-redactor)** | Pattern-based sensitive-data redaction for prompts and logs, including JSON credentials and folded HTTP headers. |
| **[Flask AppSec Lab](https://github.com/koushikchowdary6/flask-appsec-lab)** | Paired vulnerable/secure SQLi, XSS, IDOR, and CSRF examples, with regression tests and [SQLite ID boundary hardening](https://github.com/koushikchowdary6/flask-appsec-lab/pull/11). Local teaching lab only. |
| **[Security Findings Translator](https://github.com/koushikchowdary6/security-findings-translator)** | LLM-backed and offline security explanations with redaction at both request and output boundaries; not complete DLP. |

### Selected engineering evidence

- **Evaluation integrity:** [EvalForge #76](https://github.com/koushikchowdary6/EvalForge/pull/76) rejects empty corpora, blank retrieval evidence, and padded document IDs before indexing; [EvalForge #75](https://github.com/koushikchowdary6/EvalForge/pull/75) rejects duplicate JSON keys in agent task labels and nested expected arguments before model evaluation; [EvalForge #73](https://github.com/koushikchowdary6/EvalForge/pull/73) syncs atomic JSON report rename metadata on POSIX after file fsync, with failure-path tests; [EvalForge #71](https://github.com/koushikchowdary6/EvalForge/pull/71) fingerprints validated RAG corpora and question labels while recording embedding/judge model identifiers; [#72](https://github.com/koushikchowdary6/EvalForge/pull/72) prevents stale evaluation rows from being attributed to newly loaded benchmarks; [EvalForge #70](https://github.com/koushikchowdary6/EvalForge/pull/70) prevents failed agent calls from improving latency/turn averages while reporting safety denominators; [#69](https://github.com/koushikchowdary6/EvalForge/pull/69) separates successful RAG-stage latency from outages; [#68](https://github.com/koushikchowdary6/EvalForge/pull/68) makes equal-similarity retrieval rankings independent of corpus order; [#67](https://github.com/koushikchowdary6/EvalForge/pull/67) and [#66](https://github.com/koushikchowdary6/EvalForge/pull/66) reject ambiguous question/corpus JSON; [#62](https://github.com/koushikchowdary6/EvalForge/pull/62) adds AP@k/MAP@k; [#63](https://github.com/koushikchowdary6/EvalForge/pull/63) redacts sensitive provider exception messages from agent reports.
- **AI and cloud security:** [IAM Auditor #22](https://github.com/koushikchowdary6/iam-policy-auditor/pull/22) rejects NaN and infinite numeric Condition values even for direct Python-dictionary audits; [Prompt Injection Detector #22](https://github.com/koushikchowdary6/prompt-injection-detector/pull/22) prevents identical TF-IDF unigram/bigram count vectors from receiving contradictory labels or crossing CV folds; [Prompt Injection Detector #21](https://github.com/koushikchowdary6/prompt-injection-detector/pull/21) aligns grouped cross-validation with the fitted TF-IDF analyzer, preventing false Unicode label conflicts while preserving feature-equivalent fold isolation; [Prompt Injection Detector #20](https://github.com/koushikchowdary6/prompt-injection-detector/pull/20) aligns training-label conflict checks with the actual TF-IDF analyzer instead of mismatched Unicode case folding; [Prompt Injection Detector #19](https://github.com/koushikchowdary6/prompt-injection-detector/pull/19) covers encoded instructions; [LLM PII Redactor #10](https://github.com/koushikchowdary6/llm-pii-redactor/pull/10) protects JSON credentials and [#11](https://github.com/koushikchowdary6/llm-pii-redactor/pull/11) masks folded HTTP credential continuations; [Security Findings Translator #9](https://github.com/koushikchowdary6/security-findings-translator/pull/9) redacts recognizable secrets from both outbound LLM requests and returned explanations/metadata; [IAM Auditor #20](https://github.com/koushikchowdary6/iam-policy-auditor/pull/20) prevents malformed IAM principal ARN strings from lowering public-access risk; [#21](https://github.com/koushikchowdary6/iam-policy-auditor/pull/21) rejects deceptive Condition identifiers before classification; [Flask AppSec Lab #10](https://github.com/koushikchowdary6/flask-appsec-lab/pull/10) hardens login hash handling; [#11](https://github.com/koushikchowdary6/flask-appsec-lab/pull/11) returns 404 for note IDs outside SQLite's signed integer range instead of raising a server error.
- **Data and ML reliability:** [Terraform GCP Pipeline #5](https://github.com/koushikchowdary6/terraform-gcp-data-pipeline/pull/5) rejects ambiguous or malformed incremental watermark state; [Airflow ETL #6](https://github.com/koushikchowdary6/airflow-postgres-etl/pull/6) validates quality-gate outcomes before watermark advancement; [Network Anomaly Detector #4](https://github.com/koushikchowdary6/network-anomaly-detector/pull/4) rejects invalid labels/scores in alert-budget metrics; [#5](https://github.com/koushikchowdary6/network-anomaly-detector/pull/5) removes holdout-row-order bias when scores tie at the alert cutoff. The anomaly dataset is synthetic.

All selected pull requests are merged with passing PR checks; links show the implementation and tests, not unverified production performance.

---

## Data engineering & platform

| Project | Engineering signal |
|---|---|
| **[airflow-postgres-etl](https://github.com/koushikchowdary6/airflow-postgres-etl)** | Daily seven-task Airflow DAG over PostgreSQL with incremental watermarks, natural-key upserts, nine integrity-enforced SQL quality checks, atomic CSV handoffs, restart-safe recovery, PostgreSQL integration tests, and an end-to-end idempotency smoke test. |
| **[terraform-gcp-data-pipeline](https://github.com/koushikchowdary6/terraform-gcp-data-pipeline)** | Reproducible Python ingestion into DuckDB locally, plus a Terraform-defined GCS/BigQuery architecture with partitioning, clustering, least-privilege IAM, revision lookback, delivery tracking, Terraform validation, TFLint, and Checkov. |

Both repositories are intentionally explicit about what was actually executed versus what remains unproven in cloud runtime. That keeps the portfolio useful for data-engineering interviews without overstating deployment experience.

---

## Open-source contributions

- **[Wheat FHB Forecasting PR #1](https://github.com/priakhatik/wheat-fhb-forecasting/pull/1)** *(merged Oct 16, 2026)* — moves preprocessing inside cross-validation folds and removes machine-specific paths so model evaluation is less leakage-prone and more reproducible.
- **[Corn Belt Drought Risk PR #1](https://github.com/priakhatik/corn-belt-drought-risk/pull/1)** *(merged Oct 16, 2026)* — aligns drought labels, prevents future-date joins, and builds climatology from training years only for cleaner held-out evaluation.
- **[Spotify Azure Project PR #2](https://github.com/priakhatik/spotify_azure_project/pull/2)** *(merged Oct 16, 2026)* — repairs a Lakeflow SCD Type 2 CDC definition using the current `pyspark.pipelines` API and the ADF `updated_at` watermark.

- **[Wheat FHB Forecasting PR #2](https://github.com/priakhatik/wheat-fhb-forecasting/pull/2)** *(merged Oct 26, 2026)* — makes prediction portable and import-safe, with reproducible inputs and offline tests.
- **[Corn Belt Drought Risk PR #2](https://github.com/priakhatik/corn-belt-drought-risk/pull/2)** *(merged Oct 26, 2026)* — improves model-artifact reproducibility and validates held-out class coverage.
- **[Spotify Azure Project PR #3](https://github.com/priakhatik/spotify_azure_project/pull/3)** *(merged Oct 26, 2026)* — removes an exposed signed Logic App callback from an ADF pipeline; the maintainer still needs to confirm rotation or revocation of the previously exposed credential.

These six merged pull requests were authored as contributions to repositories owned by **Priya Khatik**. They do not imply ownership of those projects or production deployment. The three October 26 merges passed their post-merge main-branch CI.

---

## Security engineering foundation

| Project | Focus |
|---|---|
| **[flask-appsec-lab](https://github.com/koushikchowdary6/flask-appsec-lab)** | Vulnerable-vs-secure Flask lab with CI-tested SQLi, XSS, IDOR, and CSRF attack/fix pairs; session-bound CSRF tokens and request-size limits protect authenticated note edits ([PR #5](https://github.com/koushikchowdary6/flask-appsec-lab/pull/5)) and unauthenticated secure login parsing ([PR #6](https://github.com/koushikchowdary6/flask-appsec-lab/pull/6)); bounded secure search request targets ([PR #7](https://github.com/koushikchowdary6/flask-appsec-lab/pull/7)) reject oversized URLs before query parsing; unpredictable per-instance signing keys ([PR #8](https://github.com/koushikchowdary6/flask-appsec-lab/pull/8)) prevent forging secure sessions with a public development fallback. Secure login verifies salted password hashes ([PR #9](https://github.com/koushikchowdary6/flask-appsec-lab/pull/9)) and fails closed on malformed hashes while reducing unknown-user timing differences ([#10](https://github.com/koushikchowdary6/flask-appsec-lab/pull/10)); oversized SQLite note IDs return 404 instead of server errors ([#11](https://github.com/koushikchowdary6/flask-appsec-lab/pull/11)); the lab is not production-safe. |
| **[ssh-log-threat-detector](https://github.com/koushikchowdary6/ssh-log-threat-detector)** | Detection logic for SSH brute force, password spraying, and suspicious post-authentication activity. |
| **[phishing-url-detector](https://github.com/koushikchowdary6/phishing-url-detector)** | ML classifier using lexical URL features without fetching potentially hostile pages. |
| **[network-anomaly-detector](https://github.com/koushikchowdary6/network-anomaly-detector)** | Isolation Forest over explicitly synthetic NetFlow-style traffic, with internally consistent packet rates, held-out ROC-AUC/PR-AUC, top-5% analyst alert-budget metrics ([PR #3](https://github.com/koushikchowdary6/network-anomaly-detector/pull/3)) with fail-closed label/score validation ([#4](https://github.com/koushikchowdary6/network-anomaly-detector/pull/4)) and tie-aware expected metrics ([#5](https://github.com/koushikchowdary6/network-anomaly-detector/pull/5)), validated inputs, and atomic model refits. Synthetic-only benchmark; no production accuracy claim. |
| **[lamport-signatures](https://github.com/koushikchowdary6/lamport-signatures)** | Hash-based one-time signatures implemented from first principles. |
| **[aes-modes-of-operation](https://github.com/koushikchowdary6/aes-modes-of-operation)** | AES mode implementations and verification exercises. |

---

## Stack

**AI / LLM:** LLM evaluation · RAG evaluation · agent/tool-call evaluation · prompt injection · guardrails · scikit-learn · benchmark design  
**Engineering:** Python · FastAPI · SQL/PostgreSQL · Airflow · DuckDB · Terraform · GCP/BigQuery · React/TypeScript · Docker · GitHub Actions · Linux  
**Security:** AI security · Detection engineering · AppSec · IAM · Cloud security · OWASP · MITRE ATT&CK · SIEM/SOC

<p>
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white">
  <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white">
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white">
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white">
  <img src="https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white">
  <img src="https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonaws&logoColor=white">
  <img src="https://img.shields.io/badge/Azure-0078D4?style=flat-square&logo=microsoftazure&logoColor=white">
</p>

---

## What I am targeting

**AI Engineering · Data Engineering · LLM/RAG/Agent Evaluation · AI Security · Applied ML · Platform Engineering**

<p align="center">
  <i>Building toward AI and data engineering roles with a portfolio grounded in reproducible evaluation, idempotent pipelines, cloud infrastructure, guardrails, and security engineering.</i>
</p>
