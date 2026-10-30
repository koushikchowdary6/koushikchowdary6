<h1 align="center">Koushik Chowdary</h1>

<p align="center"><strong>AI Engineering · LLM/RAG & Agent Evaluation · AI Security · Data Engineering</strong></p>
<p align="center">Python · FastAPI · PostgreSQL · scikit-learn · Airflow · Terraform · Docker · GitHub Actions</p>
<p align="center"><a href="https://linkedin.com/in/koushik-chowdary">LinkedIn</a> · <a href="mailto:kowshiksc610@gmail.com">Email</a></p>

I build evaluation infrastructure, AI guardrails, security automation, and data pipelines. My master's-level work at the University of South Florida focused on cybersecurity, AI, data, and cloud. Below are **specific engineering changes and tests**, not production-performance claims.

## Start here — four projects worth reviewing

| Project | Engineering evidence |
|---|---|
| **[EvalForge](https://github.com/koushikchowdary6/EvalForge)** · LLM/RAG/agent evaluation | Offline evaluation runners; [paired RAG comparisons with bootstrap intervals](https://github.com/koushikchowdary6/EvalForge/pull/128), [macro/micro tool-call F1 and coverage tests](https://github.com/koushikchowdary6/EvalForge/pull/135), [bounded agent prompts, mock evidence and tool arguments](https://github.com/koushikchowdary6/EvalForge/pull/137), and [Python 3.10–3.12 CI](https://github.com/koushikchowdary6/EvalForge/actions). |
| **[Prompt Injection Detector](https://github.com/koushikchowdary6/prompt-injection-detector)** · applied ML/guardrails | Hybrid heuristics + TF-IDF/logistic regression; [leakage-aware grouped CV](https://github.com/koushikchowdary6/prompt-injection-detector/pull/22), [encoded instruction and role-boundary detection](https://github.com/koushikchowdary6/prompt-injection-detector/pull/48), [machine-readable CV reports](https://github.com/koushikchowdary6/prompt-injection-detector/pull/45), and [tests/CI](https://github.com/koushikchowdary6/prompt-injection-detector/actions). |
| **[SigmaForge](https://github.com/koushikchowdary6/sigmaforge)** · detection engineering/backend | FastAPI, RBAC and PostgreSQL-backed rule revisions; [selector-pattern preflight](https://github.com/koushikchowdary6/sigmaforge/pull/38), [stored-snapshot integrity checks](https://github.com/koushikchowdary6/sigmaforge/pull/36), [bounded historical snapshot decoding](https://github.com/koushikchowdary6/sigmaforge/pull/39), [corrupt-history revision protection](https://github.com/koushikchowdary6/sigmaforge/pull/41), and [backend/database/Docker CI](https://github.com/koushikchowdary6/sigmaforge/actions). |
| **[Airflow/PostgreSQL ETL](https://github.com/koushikchowdary6/airflow-postgres-etl)** · data engineering | Incremental loads, idempotent upserts and transactional watermarks; [bounded streaming CSV downloads with atomic last-good snapshots](https://github.com/koushikchowdary6/airflow-postgres-etl/pull/13), [strict SQL quality evidence](https://github.com/koushikchowdary6/airflow-postgres-etl/pull/12), and [PostgreSQL/DAG CI](https://github.com/koushikchowdary6/airflow-postgres-etl/actions). |

## Additional security and cloud/data engineering

- **[Flask AppSec Lab](https://github.com/koushikchowdary6/flask-appsec-lab):** paired vulnerable/hardened routes, [note-scoped one-time CSRF tokens](https://github.com/koushikchowdary6/flask-appsec-lab/pull/18), [cross-origin browser POST rejection with regression tests](https://github.com/koushikchowdary6/flask-appsec-lab/pull/23), and [secure form-target CSP hardening](https://github.com/koushikchowdary6/flask-appsec-lab/pull/21).
- **[LLM PII Redactor](https://github.com/koushikchowdary6/llm-pii-redactor):** targeted sensitive-data masking with [bounded, fail-closed prompt input](https://github.com/koushikchowdary6/llm-pii-redactor/pull/25), [forwarded authorization-header protection](https://github.com/koushikchowdary6/llm-pii-redactor/pull/23), and [JSON-safe custom masks](https://github.com/koushikchowdary6/llm-pii-redactor/pull/22).
- **[IAM Policy Auditor](https://github.com/koushikchowdary6/iam-policy-auditor):** offline AWS IAM risk linter with [boundary replacement escalation checks](https://github.com/koushikchowdary6/iam-policy-auditor/pull/36), [trust-policy/group escalation detection](https://github.com/koushikchowdary6/iam-policy-auditor/pull/35), and [bounded untrusted JSON input](https://github.com/koushikchowdary6/iam-policy-auditor/pull/34); findings are heuristics, not effective-permission simulation.
- **[Network Anomaly Detector](https://github.com/koushikchowdary6/network-anomaly-detector):** synthetic NetFlow / Isolation Forest with [strict numeric telemetry and analyst-budget validation](https://github.com/koushikchowdary6/network-anomaly-detector/pull/6) and [integer-only held-out label checks](https://github.com/koushikchowdary6/network-anomaly-detector/pull/7); no real-network accuracy claim.
- **[Security Findings Translator](https://github.com/koushikchowdary6/security-findings-translator):** offline and Claude-backed security explanations with [duplicate-key and nonfinite evidence guards](https://github.com/koushikchowdary6/security-findings-translator/pull/10) plus [bounded, prevalidated LLM batches](https://github.com/koushikchowdary6/security-findings-translator/pull/11) and [terminal-safe incident output and token redaction](https://github.com/koushikchowdary6/security-findings-translator/pull/12); targeted redaction, not comprehensive DLP or a spending cap.
- **[Terraform GCP Data Pipeline](https://github.com/koushikchowdary6/terraform-gcp-data-pipeline):** reproducible infrastructure design and Python/DuckDB ingestion, with [fail-closed quality-suite coverage](https://github.com/koushikchowdary6/terraform-gcp-data-pipeline/pull/7) and [strict SQL result evidence types](https://github.com/koushikchowdary6/terraform-gcp-data-pipeline/pull/8); no live-cloud deployment claim.

## Verified contributions to other maintainers' repositories

These are **merged PRs authored by me**, not repositories I own. Open PRs are not counted.

| Repository owned by Priya Khatik | My merged PRs |
|---|---|
| [Wheat FHB Forecasting](https://github.com/priakhatik/wheat-fhb-forecasting) | [Cross-validation leakage fix (#1)](https://github.com/priakhatik/wheat-fhb-forecasting/pull/1) · [Portable prediction (#2)](https://github.com/priakhatik/wheat-fhb-forecasting/pull/2) |
| [Corn Belt Drought Risk](https://github.com/priakhatik/corn-belt-drought-risk) | [Leakage-safe temporal features (#1)](https://github.com/priakhatik/corn-belt-drought-risk/pull/1) · [Reproducible artifacts (#2)](https://github.com/priakhatik/corn-belt-drought-risk/pull/2) |
| [Spotify Azure Project](https://github.com/priakhatik/spotify_azure_project) | [Lakeflow CDC correction (#2)](https://github.com/priakhatik/spotify_azure_project/pull/2) · [Remove exposed signed callback (#3)](https://github.com/priakhatik/spotify_azure_project/pull/3) |

## Scope and limitations

EvalForge provides evaluation infrastructure, **not** proven production model accuracy. Prompt Injection Detector reports exploratory grouped-CV results, **not** calibrated deployment risk. SigmaForge's Sigma validation is structural, **not** pySigma semantic validation or deployment approval. Security tools are educational/static, not comprehensive DLP or cloud-authorization simulation.

**Roles I'm targeting:** AI Engineer · Applied AI / ML Engineer · LLM/RAG Evaluation · AI Security Engineer · Data Engineer · Python Backend Engineer
