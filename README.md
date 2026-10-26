<h1 align="center">Koushik Chowdary</h1>

<p align="center">
  <b>AI Engineering · Data Engineering · LLM/RAG/Agent Evaluation · AI Security</b><br>
  M.S. Information Technology (Cybersecurity & AI focus), University of South Florida · Python · SQL/PostgreSQL · Airflow · Terraform · FastAPI · AWS/Azure/GCP
</p>

<p align="center">
  <a href="https://linkedin.com/in/koushik-chowdary"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="mailto:kowshiksc610@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/CompTIA-CySA%2B-E31837?style=flat-square&logo=comptia&logoColor=white">
  <img src="https://img.shields.io/badge/AWS-Security%20Specialty-FF9900?style=flat-square&logo=amazonaws&logoColor=white">
  <img src="https://img.shields.io/badge/Azure-Security%20Engineer-0078D4?style=flat-square&logo=microsoftazure&logoColor=white">
</p>

---

## What I build

I build AI and data systems that can be inspected, tested, and reproduced. My current work spans LLM/RAG/agent evaluation, AI guardrails, Airflow/PostgreSQL ETL, Terraform/GCP data infrastructure, and security automation. I prefer measurable behavior, explicit limitations, idempotent pipelines, and CI-backed engineering over portfolio-only demos.

### Recruiter quick tour

| Project | Why it is worth opening |
|---|---|
| **[EvalForge](https://github.com/koushikchowdary6/EvalForge)** | LLM/RAG/agent evaluation with API-free regression tests, rank-aware nDCG@k and **MAP@k** ([PR #62](https://github.com/koushikchowdary6/EvalForge/pull/62)), fixed-denominator precision@k ([#59](https://github.com/koushikchowdary6/EvalForge/pull/59)), and fail-closed provider/judge/tool-response handling ([#61](https://github.com/koushikchowdary6/EvalForge/pull/61), [#58](https://github.com/koushikchowdary6/EvalForge/pull/58)). These are offline evaluation safeguards, not proof of production performance or injection immunity. |
| **[airflow-postgres-etl](https://github.com/koushikchowdary6/airflow-postgres-etl)** | Airflow/PostgreSQL incremental ETL with idempotent upserts, transactional watermarks, nine quality gates, and integration tests. Source downloads ([PR #5](https://github.com/koushikchowdary6/airflow-postgres-etl/pull/5)) and staged CSV handoffs ([#4](https://github.com/koushikchowdary6/airflow-postgres-etl/pull/4)) publish atomically and preserve previous artifacts on failure. |
| **[terraform-gcp-data-pipeline](https://github.com/koushikchowdary6/terraform-gcp-data-pipeline)** | Python/DuckDB market-data ingestion with Terraform-defined GCS/BigQuery infrastructure, revision lookback, and delivery receipts. Raw CSV snapshots ([PR #4](https://github.com/koushikchowdary6/terraform-gcp-data-pipeline/pull/4)) and Parquet batch artifacts ([#3](https://github.com/koushikchowdary6/terraform-gcp-data-pipeline/pull/3)) publish atomically with recovery tests. Local CI is verified; live GCP deployment is not claimed. |
| **[SigmaForge](https://github.com/koushikchowdary6/sigmaforge)** | Early-stage FastAPI/React detection-engineering platform with RBAC, Sigma structural preflight, bounded condition parsing, malformed-Unicode value rejection ([PR #20](https://github.com/koushikchowdary6/sigmaforge/pull/20)), and invisible-character checks for rule metadata ([#19](https://github.com/koushikchowdary6/sigmaforge/pull/19)) and detection fields ([PR #18](https://github.com/koushikchowdary6/sigmaforge/pull/18)), and Docker CI. Full pySigma validation, rule execution, and an AI assistant remain planned. |
| **[prompt-injection-detector](https://github.com/koushikchowdary6/prompt-injection-detector)** | Hybrid ML + heuristic input guardrail with role-spoofing, Unicode-evasion tests, including hidden-byte-separated mixed-script confusables ([PR #17](https://github.com/koushikchowdary6/prompt-injection-detector/pull/17)), emoji false-positive controls, bounded inputs, and leakage-aware cross-validation. A detector, not a guarantee against injection. |
| **[llm-pii-redactor](https://github.com/koushikchowdary6/llm-pii-redactor)** | LLM data-protection utility for PII, API tokens, authorization headers, signed-URL credentials, and OAuth fragment tokens ([PR #9](https://github.com/koushikchowdary6/llm-pii-redactor/pull/9)), with offline leak/false-positive tests. |
| **[security-findings-translator](https://github.com/koushikchowdary6/security-findings-translator)** | Claude/offline security-finding explanations with signed-cloud-URL credential redaction ([PR #7](https://github.com/koushikchowdary6/security-findings-translator/pull/7)), structured untrusted evidence, and fail-closed handling of incomplete provider responses. |

### Selected engineering evidence — October 2026

- **RAG and agent evaluation:** [EvalForge #62](https://github.com/koushikchowdary6/EvalForge/pull/62) adds duplicate-aware AP@k/MAP@k with rank-order and report-integration tests; [#60](https://github.com/koushikchowdary6/EvalForge/pull/60) adds nDCG@k; [#59](https://github.com/koushikchowdary6/EvalForge/pull/59) fixes precision@k under short retrievals. [#61](https://github.com/koushikchowdary6/EvalForge/pull/61), [#58](https://github.com/koushikchowdary6/EvalForge/pull/58), and [#57](https://github.com/koushikchowdary6/EvalForge/pull/57) reject incomplete or ambiguous model/judge/agent outputs rather than inflating benchmark credit. All linked work is merged and CI-tested.
- **AI guardrails:** [Prompt Injection Detector #17](https://github.com/koushikchowdary6/prompt-injection-detector/pull/17) catches mixed-script keyword spoofing combined with invisible separators; [#16](https://github.com/koushikchowdary6/prompt-injection-detector/pull/16) covers selected confusables; [LLM PII Redactor #9](https://github.com/koushikchowdary6/llm-pii-redactor/pull/9) covers OAuth fragment tokens; [#8](https://github.com/koushikchowdary6/llm-pii-redactor/pull/8) redacts sensitive URL parameters; [Security Findings Translator #7](https://github.com/koushikchowdary6/security-findings-translator/pull/7) redacts signed cloud URL credentials and [#6](https://github.com/koushikchowdary6/security-findings-translator/pull/6) hardens untrusted evidence serialization. These are bounded defenses, not guarantees against every attack.
- **Applied ML evaluation:** [Network Anomaly Detector #3](https://github.com/koushikchowdary6/network-anomaly-detector/pull/3) adds held-out PR-AUC, prevalence baseline, and top-score precision/recall under a fixed 5% review budget. The data and reported performance are synthetic.
- **Detection and IAM:** [IAM Auditor #18](https://github.com/koushikchowdary6/iam-policy-auditor/pull/18) rejects invisible Unicode, bidirectional controls, and padded principal identifiers before risk classification; [#17](https://github.com/koushikchowdary6/iam-policy-auditor/pull/17) validates policy versions and resource selectors. [SigmaForge #20](https://github.com/koushikchowdary6/sigmaforge/pull/20) rejects invalid surrogate values in Sigma drafts; [#19](https://github.com/koushikchowdary6/sigmaforge/pull/19) and [#18](https://github.com/koushikchowdary6/sigmaforge/pull/18) check reviewer-facing metadata and field names. These are static checks, not full policy execution or production detection.
- **Data engineering:** [GCP Pipeline #4](https://github.com/koushikchowdary6/terraform-gcp-data-pipeline/pull/4) atomically publishes raw CSV downloads after fsync, retaining the previous source snapshot on failed writes; [Airflow ETL #5](https://github.com/koushikchowdary6/airflow-postgres-etl/pull/5) atomically publishes downloaded source snapshots, retaining the previous file on network/filesystem failure; [GCP Pipeline #3](https://github.com/koushikchowdary6/terraform-gcp-data-pipeline/pull/3) atomically publishes Parquet artifacts; [Airflow ETL #4](https://github.com/koushikchowdary6/airflow-postgres-etl/pull/4) atomically publishes staged CSVs. Cloud deployment is not claimed without runtime evidence.

The linked pull requests and repository CI provide implementation and test evidence; older changes remain available in project history.

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

Additional [Corn Belt Drought Risk reproducibility PR #2](https://github.com/priakhatik/corn-belt-drought-risk/pull/2) and [Wheat FHB Forecasting portability PR #2](https://github.com/priakhatik/wheat-fhb-forecasting/pull/2) are **open for maintainer review**, with passing Python 3.11/3.12 CI. [Spotify Azure Project security PR #3](https://github.com/priakhatik/spotify_azure_project/pull/3) is also **open**; it proposes removing an exposed signed webhook callback, and the maintainer must rotate/revoke that credential. None of these are merged contributions. These are contributions to repositories owned by **Priya Khatik**, not projects I own.

---

## Security engineering foundation

| Project | Focus |
|---|---|
| **[flask-appsec-lab](https://github.com/koushikchowdary6/flask-appsec-lab)** | Vulnerable-vs-secure Flask lab with CI-tested SQLi, XSS, IDOR, and CSRF attack/fix pairs; session-bound CSRF tokens and request-size limits protect authenticated note edits ([PR #5](https://github.com/koushikchowdary6/flask-appsec-lab/pull/5)) and unauthenticated secure login parsing ([PR #6](https://github.com/koushikchowdary6/flask-appsec-lab/pull/6)); bounded secure search request targets ([PR #7](https://github.com/koushikchowdary6/flask-appsec-lab/pull/7)) reject oversized URLs before query parsing; unpredictable per-instance signing keys ([PR #8](https://github.com/koushikchowdary6/flask-appsec-lab/pull/8)) prevent forging secure sessions with a public development fallback. Secure login also verifies salted password hashes while the deliberately vulnerable demo still uses plaintext ([PR #9](https://github.com/koushikchowdary6/flask-appsec-lab/pull/9)); the lab is not production-safe. |
| **[ssh-log-threat-detector](https://github.com/koushikchowdary6/ssh-log-threat-detector)** | Detection logic for SSH brute force, password spraying, and suspicious post-authentication activity. |
| **[phishing-url-detector](https://github.com/koushikchowdary6/phishing-url-detector)** | ML classifier using lexical URL features without fetching potentially hostile pages. |
| **[network-anomaly-detector](https://github.com/koushikchowdary6/network-anomaly-detector)** | Isolation Forest over explicitly synthetic NetFlow-style traffic, with internally consistent packet rates, held-out ROC-AUC/PR-AUC, top-5% analyst alert-budget metrics ([PR #3](https://github.com/koushikchowdary6/network-anomaly-detector/pull/3)), validated inputs, and atomic model refits. Synthetic-only benchmark; no production accuracy claim. |
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
