<h1 align="center">Koushik Chowdary</h1>

<p align="center">
  <b>AI Engineering · Data Engineering · LLM/RAG/Agent Evaluation · AI Security</b><br>
  M.S. Cybersecurity, University of South Florida · Python · SQL/PostgreSQL · Airflow · Terraform · FastAPI · AWS/Azure/GCP
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
| **[EvalForge](https://github.com/koushikchowdary6/EvalForge)** | LLM, RAG, and tool-calling evaluation framework with auditable reports, automated graders, safety-oriented agent evals, benchmark artifacts, CI-backed judge-failure accounting, validated corpus IDs/retrieval settings, fail-closed index builds, crash-safe validated embedding caches, finite/dimension-consistent embeddings, and explicit system-level trust boundaries for untrusted RAG context and judge inputs. |
| **[airflow-postgres-etl](https://github.com/koushikchowdary6/airflow-postgres-etl)** | Production-style Airflow + PostgreSQL batch ETL with atomic incremental watermarks, idempotent upserts, real integration tests, data-quality gates, and recovery semantics. |
| **[terraform-gcp-data-pipeline](https://github.com/koushikchowdary6/terraform-gcp-data-pipeline)** | Python/DuckDB market-data pipeline with a Terraform-managed GCS + BigQuery path, deterministic keys, revision lookback, CI validation, and security scanning. |
| **[SigmaForge](https://github.com/koushikchowdary6/sigmaforge)** | Early-stage FastAPI + React detection-engineering platform: implemented auth/RBAC with validated JWT identity claims and fail-closed password verification, Postgres schema, Celery/Redis task wiring, Docker CI, and threat-model docs. Rule authoring, AI assistant, and research experiments are planned, not implemented. |
| **[prompt-injection-detector](https://github.com/koushikchowdary6/prompt-injection-detector)** | Hybrid heuristic + ML input guardrail with shared Unicode normalization for rules and learned scoring, plus regression tests for obfuscated injection attempts, jailbreak signals, thresholds, and pre-training fallback behavior. |
| **[llm-pii-redactor](https://github.com/koushikchowdary6/llm-pii-redactor)** | PII and secret redaction for LLM pipelines, including AWS/GitHub token detection, private-key handling, and regression tests. |

### Recent engineering work — Oct 2026

- **EvalForge:** improved RAG and agent evaluation correctness, including model-aware embedding caches, malformed/non-finite judge outputs, duplicate tool-call grading, and argument scoring. [Merged PR #1](https://github.com/koushikchowdary6/EvalForge/pull/1) also isolates repeated evaluation sweeps, aborts provider-error responses before grading, and prevents stale report reuse. [Merged PR #2](https://github.com/koushikchowdary6/EvalForge/pull/2) excludes provider failures from per-category agent success-rate denominators; [PR #3](https://github.com/koushikchowdary6/EvalForge/pull/3) and [PR #4](https://github.com/koushikchowdary6/EvalForge/pull/4) prevent stale agent and RAG reports from being mistaken for current benchmark output. [Merged PR #5](https://github.com/koushikchowdary6/EvalForge/pull/5) reports tool-sequence accuracy separately from tool selection, exposing agents that call the right tools in the wrong order. [Merged PR #6](https://github.com/koushikchowdary6/EvalForge/pull/6) separates judge API/parse failures from correctness and groundedness scores, rejects invalid 0–10 grades, and reports judge coverage per retrieval configuration. [Merged PR #7](https://github.com/koushikchowdary6/EvalForge/pull/7) adds higher-priority untrusted-context instructions to Claude/GPT generation and judge requests, with API-free payload tests; this is defense in depth, not a measured guarantee against injection. [Merged PR #8](https://github.com/koushikchowdary6/EvalForge/pull/8) rejects duplicate/malformed RAG document IDs and invalid retrieval top-k settings, and prevents old corpus embeddings from contaminating new runs. [Merged PR #9](https://github.com/koushikchowdary6/EvalForge/pull/9) stages embedding indexes atomically so interrupted builds cannot expose incomplete retrieval state. [Merged PR #10](https://github.com/koushikchowdary6/EvalForge/pull/10) rejects non-finite, zero, malformed, and dimension-mismatched embeddings before they can distort retrieval metrics. [Merged PR #11](https://github.com/koushikchowdary6/EvalForge/pull/11) writes embedding caches atomically, rejects invalid API vectors, and refreshes corrupted cache entries rather than reusing them.
- **SigmaForge auth:** [Merged PR #3](https://github.com/koushikchowdary6/sigmaforge/pull/3) validates signed JWT subject/role/token-ID claims and handles corrupted Argon2 verification errors without leaking server failures; backend, security, worker, frontend, and Docker integration tests passed on the PR. Rule authoring and AI assistant features remain planned.
- **AI guardrails:** strengthened prompt-injection and PII/secret defenses with configuration validation, false-positive regressions, PEM redaction coverage, and safe audit-logging guidance, plus [GitHub-token redaction tests](https://github.com/koushikchowdary6/llm-pii-redactor/pull/1). [Merged PR #1](https://github.com/koushikchowdary6/prompt-injection-detector/pull/1) preserves high-confidence hybrid signals and explicit ML opt-out semantics, with deterministic regression tests. [Merged PR #2](https://github.com/koushikchowdary6/prompt-injection-detector/pull/2) adds Unicode normalization to catch zero-width and fullwidth obfuscation in heuristic injection rules. [Merged PR #3](https://github.com/koushikchowdary6/prompt-injection-detector/pull/3) applies the same normalization to ML training and inference, with regression tests for equivalent Unicode forms; neither change guarantees complete evasion resistance.
- **IAM analysis:** expanded partial-wildcard detection (e.g. `s3:Get*`) and [merged statement-validation tests](https://github.com/koushikchowdary6/iam-policy-auditor/pull/1), including malformed selectors and broad `NotResource` allow findings. [PR #2](https://github.com/koushikchowdary6/iam-policy-auditor/pull/2) also rejects absent or empty policy statements instead of presenting malformed input as clean. [Merged PR #3](https://github.com/koushikchowdary6/iam-policy-auditor/pull/3) also detects service-wide action wildcards paired with `NotResource` as HIGH risk. [Merged PR #4](https://github.com/koushikchowdary6/iam-policy-auditor/pull/4) keeps wildcard principals HIGH risk when conditions only enforce TLS/MFA or use negative operators, and validates malformed condition structures.
- **Applied ML:** moved network-anomaly evaluation to a held-out train/test methodology and added a regression check for evaluation isolation.
- **Security automation:** hardened security-finding ingestion so malformed JSON fails clearly instead of propagating ambiguous downstream errors.
- **Data engineering:** built CI-backed Airflow/PostgreSQL and Python/DuckDB/Terraform pipelines with incremental state, idempotent loads, quality gates, and explicit recovery behavior. [Merged Airflow PR #1](https://github.com/koushikchowdary6/airflow-postgres-etl/pull/1) makes watermark advancement atomic under concurrent workers and adds stale-read regression coverage.
- **Current direction:** AI engineering + AI security, backed by production-oriented data engineering and platform depth.

---

## Data engineering & platform

| Project | Engineering signal |
|---|---|
| **[airflow-postgres-etl](https://github.com/koushikchowdary6/airflow-postgres-etl)** | Daily seven-task Airflow DAG over PostgreSQL with incremental watermarks, natural-key upserts, nine SQL quality checks, restart-safe recovery, PostgreSQL integration tests, and an end-to-end idempotency smoke test. |
| **[terraform-gcp-data-pipeline](https://github.com/koushikchowdary6/terraform-gcp-data-pipeline)** | Reproducible Python ingestion into DuckDB locally, plus a Terraform-defined GCS/BigQuery architecture with partitioning, clustering, least-privilege IAM, revision lookback, delivery tracking, Terraform validation, TFLint, and Checkov. |

Both repositories are intentionally explicit about what was actually executed versus what remains unproven in cloud runtime. That keeps the portfolio useful for data-engineering interviews without overstating deployment experience.

---

## Open-source contributions

- **[Wheat FHB Forecasting PR #1](https://github.com/priakhatik/wheat-fhb-forecasting/pull/1)** *(merged Oct 16, 2026)* — moves preprocessing inside cross-validation folds and removes machine-specific paths so model evaluation is less leakage-prone and more reproducible.
- **[Corn Belt Drought Risk PR #1](https://github.com/priakhatik/corn-belt-drought-risk/pull/1)** *(merged Oct 16, 2026)* — aligns drought labels, prevents future-date joins, and builds climatology from training years only for cleaner held-out evaluation.
- **[Spotify Azure Project PR #2](https://github.com/priakhatik/spotify_azure_project/pull/2)** *(merged Oct 16, 2026)* — repairs a Lakeflow SCD Type 2 CDC definition using the current `pyspark.pipelines` API and the ADF `updated_at` watermark.

An additional [Corn Belt Drought Risk reproducibility PR #2](https://github.com/priakhatik/corn-belt-drought-risk/pull/2) is **open and ready for maintainer review**, with passing Python 3.11/3.12 CI; it is not a merged contribution. These are contributions to repositories owned by **Priya Khatik**, not projects I own.

---

## Security engineering foundation

| Project | Focus |
|---|---|
| **[flask-appsec-lab](https://github.com/koushikchowdary6/flask-appsec-lab)** | Vulnerable-vs-secure Flask lab demonstrating SQL injection, XSS, IDOR, security headers, and regression-tested fixes; [merged PR #2](https://github.com/koushikchowdary6/flask-appsec-lab/pull/2) isolates deliberately vulnerable login sessions from secure note authorization. |
| **[ssh-log-threat-detector](https://github.com/koushikchowdary6/ssh-log-threat-detector)** | Detection logic for SSH brute force, password spraying, and suspicious post-authentication activity. |
| **[phishing-url-detector](https://github.com/koushikchowdary6/phishing-url-detector)** | ML classifier using lexical URL features without fetching potentially hostile pages. |
| **[network-anomaly-detector](https://github.com/koushikchowdary6/network-anomaly-detector)** | Isolation Forest anomaly detection over NetFlow-style traffic. |
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
