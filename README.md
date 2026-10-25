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
| **[EvalForge](https://github.com/koushikchowdary6/EvalForge)** | RAG retrieval/grounding and agent tool-call evaluation with offline regression tests. Tracks provider failures and safety evidence without inflating scores; JSON-structured untrusted evidence reduces prompt-boundary spoofing in generation and judging ([PR #51](https://github.com/koushikchowdary6/EvalForge/pull/51)). |
| **[airflow-postgres-etl](https://github.com/koushikchowdary6/airflow-postgres-etl)** | Airflow/PostgreSQL incremental ETL with idempotent upserts, transactional watermarks, atomic staged-CSV handoffs, quality gates, and integration tests. |
| **[terraform-gcp-data-pipeline](https://github.com/koushikchowdary6/terraform-gcp-data-pipeline)** | Python/DuckDB market-data ingestion with Terraform-defined GCS/BigQuery infrastructure, revision lookback, verified delivery receipts, and crash-safe Parquet batch/reject publishing ([PR #3](https://github.com/koushikchowdary6/terraform-gcp-data-pipeline/pull/3)). Local tests and Terraform CI are verified; live cloud deployment is not claimed. |
| **[SigmaForge](https://github.com/koushikchowdary6/sigmaforge)** | Early-stage FastAPI/React detection-engineering platform with RBAC, Sigma structural preflight, bounded condition parsing, and Docker CI. Full pySigma validation, rule execution, and an AI assistant remain planned. |
| **[prompt-injection-detector](https://github.com/koushikchowdary6/prompt-injection-detector)** | Hybrid ML + heuristic input guardrail with role-spoofing/Unicode-evasion tests, emoji false-positive controls, bounded inputs, and leakage-aware cross-validation. A detector, not a guarantee against injection. |
| **[llm-pii-redactor](https://github.com/koushikchowdary6/llm-pii-redactor)** | LLM data-protection utility for PII, API tokens, authorization headers, and signed-URL credentials, with regression tests for leaks and false positives. |
| **[security-findings-translator](https://github.com/koushikchowdary6/security-findings-translator)** | Claude/offline security-finding explanations with credential redaction, structured untrusted evidence, and fail-closed handling of incomplete provider responses. |

### Selected engineering evidence — Oct 2026

- **LLM/RAG/agent evaluation:** [EvalForge PR #51](https://github.com/koushikchowdary6/EvalForge/pull/51) keeps malicious answer/document delimiters inside JSON fields when prompting correctness and groundedness judges (boundary hardening, not full injection prevention); [EvalForge PR #50](https://github.com/koushikchowdary6/EvalForge/pull/50) encodes retrieved evidence and questions as JSON to prevent forged plain-text prompt sections (boundary hardening, not a guarantee against injection); [EvalForge PR #49](https://github.com/koushikchowdary6/EvalForge/pull/49) preserves executed tool traces and observed forbidden actions when a later provider call fails; [EvalForge PR #48](https://github.com/koushikchowdary6/EvalForge/pull/48) grades repeated tool calls against distinct expected argument targets; [EvalForge PR #47](https://github.com/koushikchowdary6/EvalForge/pull/47) rejects missing, mistyped, and unexpected tool arguments across both providers; [PR #46](https://github.com/koushikchowdary6/EvalForge/pull/46) rejects malformed provider tool-argument batches before any simulated action; [PR #45](https://github.com/koushikchowdary6/EvalForge/pull/45) rejects truncated/paused model turns; [PR #43](https://github.com/koushikchowdary6/EvalForge/pull/43) scores repeated tool calls correctly. These changes have offline regression tests and passing CI; earlier RAG and report-reliability work remains in repository history.
- **AI guardrails:** [LLM PII Redactor PR #8](https://github.com/koushikchowdary6/llm-pii-redactor/pull/8) redacts password and AWS signature query secrets while preserving query names; [Prompt Injection Detector PR #15](https://github.com/koushikchowdary6/prompt-injection-detector/pull/15) catches Unicode variation-selector obfuscation while exempting ordinary emoji; [PR #14](https://github.com/koushikchowdary6/prompt-injection-detector/pull/14) reduces emoji-ZWJ false positives; [PR #13](https://github.com/koushikchowdary6/prompt-injection-detector/pull/13) catches NUL/ESC/DEL obfuscation; [LLM PII Redactor PR #7](https://github.com/koushikchowdary6/llm-pii-redactor/pull/7) redacts multi-field Authorization headers; [Security Findings Translator PR #6](https://github.com/koushikchowdary6/security-findings-translator/pull/6) escapes injected XML-like delimiters in untrusted finding keys and values without changing decoded evidence; [PR #5](https://github.com/koushikchowdary6/security-findings-translator/pull/5) rejects nonfinal Claude remediation advice. These changes have CI-tested regression coverage.
- **Detection and cloud security:** [IAM Auditor PR #15](https://github.com/koushikchowdary6/iam-policy-auditor/pull/15) rejects unknown or misspelled policy/statement keys before issuing findings; [IAM Auditor PR #14](https://github.com/koushikchowdary6/iam-policy-auditor/pull/14) fails closed on unsupported AWS principal mapping keys; [PR #13](https://github.com/koushikchowdary6/iam-policy-auditor/pull/13) rejects malformed principal structures; [PR #12](https://github.com/koushikchowdary6/iam-policy-auditor/pull/12) avoids false assurance from self-referential condition variables. [SigmaForge PR #17](https://github.com/koushikchowdary6/sigmaforge/pull/17) rejects control characters, invisible separators, and bidi overrides in detection field identifiers; [PR #16](https://github.com/koushikchowdary6/sigmaforge/pull/16) validates optional timeframe metadata and bounds condition nesting; [PR #15](https://github.com/koushikchowdary6/sigmaforge/pull/15) rejects malformed aggregation boundaries. These are tested static checks, not full IAM/Sigma execution.
- **Data engineering:** [GCP pipeline PR #3](https://github.com/koushikchowdary6/terraform-gcp-data-pipeline/pull/3) atomically publishes Parquet observations and rejects, preserving verified files after failed writes; [Airflow ETL PR #4](https://github.com/koushikchowdary6/airflow-postgres-etl/pull/4) atomically publishes staged CSVs so failed retries cannot truncate valid Airflow task handoffs; [PR #3](https://github.com/koushikchowdary6/airflow-postgres-etl/pull/3) blocks incomplete or duplicate quality checks from advancing watermarks; [GCP pipeline PR #2](https://github.com/koushikchowdary6/terraform-gcp-data-pipeline/pull/2) retries invalid delivery receipts and safely publishes state; [PR #1](https://github.com/koushikchowdary6/terraform-gcp-data-pipeline/pull/1) validates CSV shape; [Network Anomaly Detector PR #2](https://github.com/koushikchowdary6/network-anomaly-detector/pull/2) fixes synthetic feature consistency and preserves fitted model state after failed retraining.

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
| **[flask-appsec-lab](https://github.com/koushikchowdary6/flask-appsec-lab)** | Vulnerable-vs-secure Flask lab with CI-tested SQLi, XSS, IDOR, and CSRF attack/fix pairs; session-bound CSRF tokens and request-size limits protect authenticated note edits ([PR #5](https://github.com/koushikchowdary6/flask-appsec-lab/pull/5)) and unauthenticated secure login parsing ([PR #6](https://github.com/koushikchowdary6/flask-appsec-lab/pull/6)); bounded secure search request targets ([PR #7](https://github.com/koushikchowdary6/flask-appsec-lab/pull/7)) reject oversized URLs before query parsing; login identities remain isolated across the intentionally vulnerable and secure routes. |
| **[ssh-log-threat-detector](https://github.com/koushikchowdary6/ssh-log-threat-detector)** | Detection logic for SSH brute force, password spraying, and suspicious post-authentication activity. |
| **[phishing-url-detector](https://github.com/koushikchowdary6/phishing-url-detector)** | ML classifier using lexical URL features without fetching potentially hostile pages. |
| **[network-anomaly-detector](https://github.com/koushikchowdary6/network-anomaly-detector)** | Isolation Forest over explicitly synthetic NetFlow-style traffic, with internally consistent packet rates, held-out evaluation, validated inputs, and atomic model refits. |
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
