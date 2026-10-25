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
| **[EvalForge](https://github.com/koushikchowdary6/EvalForge)** | LLM/RAG/agent evaluation with separate retrieval and generation failure accounting, token-truncation detection, strict LLM-judge parsing, credential-safe provider failure reporting, incomplete-judge rejection, agent safety/trajectory grading, benchmark data validation, and offline regression tests. |
| **[airflow-postgres-etl](https://github.com/koushikchowdary6/airflow-postgres-etl)** | Production-style Airflow + PostgreSQL batch ETL with atomic incremental watermarks, idempotent upserts, real integration tests, fail-closed nine-check quality-suite integrity, and recovery semantics. |
| **[terraform-gcp-data-pipeline](https://github.com/koushikchowdary6/terraform-gcp-data-pipeline)** | Python/DuckDB market-data pipeline with a Terraform-managed GCS + BigQuery path, deterministic keys, revision lookback, fail-closed CSV shape validation, CI validation, and security scanning. |
| **[SigmaForge](https://github.com/koushikchowdary6/sigmaforge)** | Early-stage FastAPI/React detection-engineering platform with RBAC-protected structural Sigma preflight, bounded field values, field-modifier syntax checks, bounded boolean-condition parsing, and selector-reference checks before aggregation, JWT auth, Postgres, Celery/Redis wiring, and Docker CI. Full pySigma validation, rule execution, and AI assistant remain planned. |
| **[prompt-injection-detector](https://github.com/koushikchowdary6/prompt-injection-detector)** | Hybrid heuristic + ML input guardrail with explicit prompt-size limits, bounded zero-width character evasion checks, privileged-role delimiter spoofing detection, validated binary labels, leakage-aware TF-IDF-equivalent grouped cross-validation, contradiction checks on training labels, and regression tests for obfuscation, thresholds, and safe failed refits. |
| **[llm-pii-redactor](https://github.com/koushikchowdary6/llm-pii-redactor)** | PII and secret redaction for LLM pipelines, including AWS/GitHub/OpenAI/Anthropic tokens, private-key blocks, validated IPv4/IPv6 addresses, opaque HTTP authorization, API-key and cookie headers, signed-URL query credentials, and regression tests. |
| **[security-findings-translator](https://github.com/koushikchowdary6/security-findings-translator)** | Claude/offline security-finding explanations with nested credential-field, recognizable free-text secret, and signed webhook URL query-token redaction before API calls; explicit untrusted-JSON boundaries and offline regression tests. |

### Selected engineering work — Oct 2026

- **LLM/RAG/agent evaluation:** [EvalForge PR #36](https://github.com/koushikchowdary6/EvalForge/pull/36) prevents raw provider errors and malformed judge responses from leaking into evaluation reports; [PR #35](https://github.com/koushikchowdary6/EvalForge/pull/35) rejects incomplete judge responses; [PR #34](https://github.com/koushikchowdary6/EvalForge/pull/34) excludes truncated generations; [PR #33](https://github.com/koushikchowdary6/EvalForge/pull/33) prevents stalled agents from inflating safety rates; [PR #32](https://github.com/koushikchowdary6/EvalForge/pull/32) separates retrieval outages from generation failures. All have deterministic regression tests.
- **AI guardrails:** [Prompt Injection Detector PR #12](https://github.com/koushikchowdary6/prompt-injection-detector/pull/12) adds ChatML/Llama privileged-role spoofing checks with benign controls; [PR #11](https://github.com/koushikchowdary6/prompt-injection-detector/pull/11) bounds untrusted prompt inputs; [PR #10](https://github.com/koushikchowdary6/prompt-injection-detector/pull/10) tests invisible-character evasion; [LLM PII Redactor PR #6](https://github.com/koushikchowdary6/llm-pii-redactor/pull/6) redacts opaque API-key and cookie headers; [PR #5](https://github.com/koushikchowdary6/llm-pii-redactor/pull/5) and [Security Findings Translator PR #4](https://github.com/koushikchowdary6/security-findings-translator/pull/4) redact signed URL credentials before downstream use.
- **Data engineering:** [Airflow ETL PR #3](https://github.com/koushikchowdary6/airflow-postgres-etl/pull/3) prevents incomplete or duplicate quality checks from advancing incremental watermarks; [GCP pipeline PR #1](https://github.com/koushikchowdary6/terraform-gcp-data-pipeline/pull/1) validates input CSV shape before processing.
- **Security/detection engineering:** [SigmaForge PR #13](https://github.com/koushikchowdary6/sigmaforge/pull/13) rejects malformed boolean conditions; [PR #12](https://github.com/koushikchowdary6/sigmaforge/pull/12) rejects malformed field modifiers; [PR #11](https://github.com/koushikchowdary6/sigmaforge/pull/11) checks selector references before aggregation; [PR #10](https://github.com/koushikchowdary6/sigmaforge/pull/10) catches undefined selector references; [IAM Auditor PR #9](https://github.com/koushikchowdary6/iam-policy-auditor/pull/9) detects broad resource ARN patterns; [Flask AppSec PR #5](https://github.com/koushikchowdary6/flask-appsec-lab/pull/5) bounds secure note edits and tests oversized-write rejection; [PR #4](https://github.com/koushikchowdary6/flask-appsec-lab/pull/4) demonstrates CSRF attack/fix pairs.


The linked pull requests and repository CI provide implementation and test evidence; older changes remain available in project history.

---

## Data engineering & platform

| Project | Engineering signal |
|---|---|
| **[airflow-postgres-etl](https://github.com/koushikchowdary6/airflow-postgres-etl)** | Daily seven-task Airflow DAG over PostgreSQL with incremental watermarks, natural-key upserts, nine integrity-enforced SQL quality checks, restart-safe recovery, PostgreSQL integration tests, and an end-to-end idempotency smoke test. |
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
| **[flask-appsec-lab](https://github.com/koushikchowdary6/flask-appsec-lab)** | Vulnerable-vs-secure Flask lab with CI-tested SQLi, XSS, IDOR, and CSRF attack/fix pairs; session-bound CSRF tokens and request-size limits protect authenticated note edits ([PR #5](https://github.com/koushikchowdary6/flask-appsec-lab/pull/5)); login identities remain isolated across the intentionally vulnerable and secure routes. |
| **[ssh-log-threat-detector](https://github.com/koushikchowdary6/ssh-log-threat-detector)** | Detection logic for SSH brute force, password spraying, and suspicious post-authentication activity. |
| **[phishing-url-detector](https://github.com/koushikchowdary6/phishing-url-detector)** | ML classifier using lexical URL features without fetching potentially hostile pages. |
| **[network-anomaly-detector](https://github.com/koushikchowdary6/network-anomaly-detector)** | Isolation Forest anomaly detection over synthetic NetFlow-style traffic with held-out evaluation and CI-tested fail-closed feature validation. |
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
