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
| **[EvalForge](https://github.com/koushikchowdary6/EvalForge)** | LLM, RAG, and agent evaluation with reproducible benchmarks, fail-closed dataset validation, strict numeric-answer grading, tool-trajectory grading, prompt-injection trust boundaries, numerically stable cosine retrieval, privacy-conscious hashed embedding-cache keys, corrupt-cache entry isolation, and CI-tested regressions. |
| **[airflow-postgres-etl](https://github.com/koushikchowdary6/airflow-postgres-etl)** | Production-style Airflow + PostgreSQL batch ETL with atomic incremental watermarks, idempotent upserts, real integration tests, data-quality gates, and recovery semantics. |
| **[terraform-gcp-data-pipeline](https://github.com/koushikchowdary6/terraform-gcp-data-pipeline)** | Python/DuckDB market-data pipeline with a Terraform-managed GCS + BigQuery path, deterministic keys, revision lookback, fail-closed CSV shape validation, CI validation, and security scanning. |
| **[SigmaForge](https://github.com/koushikchowdary6/sigmaforge)** | Early-stage FastAPI + React detection-engineering platform: implemented auth/RBAC with validated JWT identity claims, fail-closed password verification, and expired-lockout recovery, Postgres schema, Celery/Redis task wiring, Docker CI, and threat-model docs. Rule authoring, AI assistant, and research experiments are planned, not implemented. |
| **[prompt-injection-detector](https://github.com/koushikchowdary6/prompt-injection-detector)** | Hybrid heuristic + ML input guardrail with Unicode normalization, validated binary labels, leakage-aware TF-IDF-equivalent grouped cross-validation, contradiction checks on training labels, and regression tests for obfuscation, thresholds, and safe failed refits. |
| **[llm-pii-redactor](https://github.com/koushikchowdary6/llm-pii-redactor)** | PII and secret redaction for LLM pipelines, including AWS/GitHub/OpenAI/Anthropic tokens, private-key blocks, validated IPv4/IPv6 addresses, opaque HTTP authorization headers, and regression tests. |
| **[security-findings-translator](https://github.com/koushikchowdary6/security-findings-translator)** | Claude/offline security-finding explanations with nested credential-field and recognizable free-text secret redaction before API calls; explicit untrusted-JSON boundaries and offline regression tests. |

### Recent engineering work — Oct 2026

- **Agent and RAG evaluation:** [EvalForge PR #22](https://github.com/koushikchowdary6/EvalForge/pull/22) isolates malformed embedding-cache entries so unrelated corruption cannot block a valid RAG run; [EvalForge PR #21](https://github.com/koushikchowdary6/EvalForge/pull/21) rejects malformed and oversized cached/API embedding components without crashing or producing false similarity scores; [EvalForge PR #20](https://github.com/koushikchowdary6/EvalForge/pull/20) avoids persisting raw document text in embedding-cache keys; [EvalForge PR #19](https://github.com/koushikchowdary6/EvalForge/pull/19) stabilizes cosine rankings for extreme finite embedding values; [EvalForge PR #18](https://github.com/koushikchowdary6/EvalForge/pull/18) prevents comma-separated values from being mistaken for numeric answers; [PR #17](https://github.com/koushikchowdary6/EvalForge/pull/17) rejects malformed benchmark labels before paid model calls; [PR #16](https://github.com/koushikchowdary6/EvalForge/pull/16) validates RAG ground truth before embedding.
- **AI guardrails:** [Prompt-injection detector PR #9](https://github.com/koushikchowdary6/prompt-injection-detector/pull/9) rejects contradictory TF-IDF-equivalent training examples and feature-empty prompts before fitting; [PII redactor PR #4](https://github.com/koushikchowdary6/llm-pii-redactor/pull/4) redacts opaque Bearer/Basic/Token authorization headers before LLM calls; [Prompt-injection detector PR #8](https://github.com/koushikchowdary6/prompt-injection-detector/pull/8) prevents punctuation-equivalent prompts from leaking across ML evaluation folds; [PR #7](https://github.com/koushikchowdary6/prompt-injection-detector/pull/7) prevents whitespace-variant train/test leakage; [PR #6](https://github.com/koushikchowdary6/prompt-injection-detector/pull/6) corrects grouped cross-validation metrics; [PII redactor PR #3](https://github.com/koushikchowdary6/llm-pii-redactor/pull/3) prevents partial IPv4 redaction from leaking IPv6 prefixes. These are tested defenses, not claims of comprehensive protection.
- **Data pipelines:** [GCP pipeline PR #1](https://github.com/koushikchowdary6/terraform-gcp-data-pipeline/pull/1) rejects duplicate CSV headers and ragged records before they can corrupt warehouse observations; [Airflow ETL PR #2](https://github.com/koushikchowdary6/airflow-postgres-etl/pull/2) prevents failed data-quality checks from advancing incremental watermarks, with PostgreSQL-backed tests.
- **Application and identity security:** [Flask AppSec PR #3](https://github.com/koushikchowdary6/flask-appsec-lab/pull/3) adds no-store caching controls to login and private-note responses; [SigmaForge PR #4](https://github.com/koushikchowdary6/sigmaforge/pull/4) resets failed-login counters after timed lockouts without falsifying login timestamps; [PR #3](https://github.com/koushikchowdary6/sigmaforge/pull/3) hardens JWT claim and password-hash validation. SigmaForge rule authoring and AI assistance remain planned.
- **Cloud security and secure AI integrations:** [IAM auditor PR #6](https://github.com/koushikchowdary6/iam-policy-auditor/pull/6) catches collectively unrestricted CIDR ranges; [security findings translator PR #3](https://github.com/koushikchowdary6/security-findings-translator/pull/3) covers complete Authorization header values; [PR #2](https://github.com/koushikchowdary6/security-findings-translator/pull/2) redacts recognizable free-text credentials; [PR #1](https://github.com/koushikchowdary6/security-findings-translator/pull/1) covers structured credentials. Both are bounded, test-backed safeguards rather than comprehensive DLP.

Older engineering changes and CI evidence are available in each repository's pull-request history.

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

Additional [Corn Belt Drought Risk reproducibility PR #2](https://github.com/priakhatik/corn-belt-drought-risk/pull/2) and [Wheat FHB Forecasting portability PR #2](https://github.com/priakhatik/wheat-fhb-forecasting/pull/2) are **open for maintainer review**, with passing Python 3.11/3.12 CI; neither is a merged contribution. These are contributions to repositories owned by **Priya Khatik**, not projects I own.

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
