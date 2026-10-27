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
| **[EvalForge](https://github.com/koushikchowdary6/EvalForge)** | Reproducible RAG/agent evaluation with retrieval metrics, benchmark fingerprints, and offline tests. [fail-closed LLM judge JSON (#89)](https://github.com/koushikchowdary6/EvalForge/pull/89), [numeric-answer grading (#88)](https://github.com/koushikchowdary6/EvalForge/pull/88), and [dataset snapshot checks (#84)](https://github.com/koushikchowdary6/EvalForge/pull/84). Separates provider failures from model quality. |
| **[Prompt Injection Detector](https://github.com/koushikchowdary6/prompt-injection-detector)** | Hybrid heuristic + TF-IDF/Logistic Regression guardrail, adversarial text normalization, and [feature-consistent training and leakage-aware grouped CV](https://github.com/koushikchowdary6/prompt-injection-detector/pull/22) and [pooled false-alarm/F1/confusion metrics](https://github.com/koushikchowdary6/prompt-injection-detector/pull/26). Not injection immunity or production validation. |
| **[SigmaForge](https://github.com/koushikchowdary6/sigmaforge)** | FastAPI/React detection-engineering platform with RBAC, bounded Sigma structural preflight, and Docker CI. [Invisible-only aggregation rejection (#26)](https://github.com/koushikchowdary6/sigmaforge/pull/26) and [identifier validation (#25)](https://github.com/koushikchowdary6/sigmaforge/pull/25); full pySigma validation and rule persistence remain planned. |
| **[Airflow/PostgreSQL ETL](https://github.com/koushikchowdary6/airflow-postgres-etl)** | Incremental ETL, idempotent upserts, transactional watermarks, nine quality checks, database integration tests, and [upstream schema-drift snapshot protection (#8)](https://github.com/koushikchowdary6/airflow-postgres-etl/pull/8) and [CSV shape validation (#7)](https://github.com/koushikchowdary6/airflow-postgres-etl/pull/7). |
| **[Terraform GCP Data Pipeline](https://github.com/koushikchowdary6/terraform-gcp-data-pipeline)** | Python/DuckDB ingestion, GCS/BigQuery infrastructure design, integrity-checked incremental state, and [empty-download snapshot preservation](https://github.com/koushikchowdary6/terraform-gcp-data-pipeline/pull/6). No live-cloud deployment claim. |
| **[IAM Policy Auditor](https://github.com/koushikchowdary6/iam-policy-auditor)** | Offline AWS IAM risk analysis with conservative principal/Condition validation and [fail-closed principal wildcard validation](https://github.com/koushikchowdary6/iam-policy-auditor/pull/24); not an authorization simulator. |
| **[LLM PII Redactor](https://github.com/koushikchowdary6/llm-pii-redactor)** | Offline prompt/log guardrail with provider-key and sensitive-header detection, [folded credential coverage](https://github.com/koushikchowdary6/llm-pii-redactor/pull/12), [quoted `.env` secret masking](https://github.com/koushikchowdary6/llm-pii-redactor/pull/14), and [YAML credential masking](https://github.com/koushikchowdary6/llm-pii-redactor/pull/15). Not complete DLP. |
| **[Flask AppSec Lab](https://github.com/koushikchowdary6/flask-appsec-lab)** | Paired vulnerable/secure SQLi, XSS, IDOR, and CSRF examples, with regression tests, [SQLite ID boundary hardening](https://github.com/koushikchowdary6/flask-appsec-lab/pull/11), [ambiguous note-form rejection](https://github.com/koushikchowdary6/flask-appsec-lab/pull/12), and [duplicate login-field rejection](https://github.com/koushikchowdary6/flask-appsec-lab/pull/13). Local teaching lab only. |
| **[Security Findings Translator](https://github.com/koushikchowdary6/security-findings-translator)** | LLM-backed and offline security explanations with redaction at both request and output boundaries; not complete DLP. |

### Selected engineering evidence

| Focus | Code and tests worth reviewing |
|---|---|
| **RAG / agent evaluation** | [EvalForge #89](https://github.com/koushikchowdary6/EvalForge/pull/89) rejects ambiguous judge JSON; [#88](https://github.com/koushikchowdary6/EvalForge/pull/88) prevents numeric grading false credit; [#80](https://github.com/koushikchowdary6/EvalForge/pull/80) fingerprints benchmark inputs. |
| **AI guardrails / security** | [Prompt Injection Detector #26](https://github.com/koushikchowdary6/prompt-injection-detector/pull/26) reports held-out F1 and false positives; [LLM PII Redactor #15](https://github.com/koushikchowdary6/llm-pii-redactor/pull/15) tests YAML secret masking; [SigmaForge #26](https://github.com/koushikchowdary6/sigmaforge/pull/26) validates detection-rule syntax. |
| **Data / applied ML reliability** | [Airflow ETL #8](https://github.com/koushikchowdary6/airflow-postgres-etl/pull/8) preserves valid source snapshots on schema drift; [Terraform GCP #6](https://github.com/koushikchowdary6/terraform-gcp-data-pipeline/pull/6) preserves the last good source on empty downloads; [Network Anomaly #5](https://github.com/koushikchowdary6/network-anomaly-detector/pull/5) removes tie-order bias from synthetic alert-budget evaluation. |

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
| **[flask-appsec-lab](https://github.com/koushikchowdary6/flask-appsec-lab)** | Local vulnerable/secure Flask teaching lab for SQLi, XSS, IDOR, and CSRF with regression tests. Secure routes use bounded inputs, password hashing, CSRF/session protections, [SQLite note-ID boundary validation](https://github.com/koushikchowdary6/flask-appsec-lab/pull/11), [HTTP form-parameter ambiguity checks](https://github.com/koushikchowdary6/flask-appsec-lab/pull/12), and [duplicate credential-field rejection](https://github.com/koushikchowdary6/flask-appsec-lab/pull/13). Not production-safe. |
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
