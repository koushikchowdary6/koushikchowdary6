<h1 align="center">Koushik Chowdary</h1>

<p align="center"><strong>AI Engineering · LLM/RAG & Agent Evaluation · AI Security · Data Engineering</strong></p>
<p align="center">Python · FastAPI · PostgreSQL · scikit-learn · Airflow · Terraform · Docker · GitHub Actions</p>
<p align="center"><a href="https://linkedin.com/in/koushik-chowdary">LinkedIn</a> · <a href="mailto:kowshiksc610@gmail.com">Email</a></p>

I build evaluation infrastructure, AI guardrails, security automation, and data pipelines. My master's-level work at the University of South Florida focused on cybersecurity, AI, data, and cloud. Below are **specific engineering changes and tests**, not production-performance claims.

## Start here — four projects worth reviewing

| Project | Engineering evidence |
|---|---|
| **[EvalForge](https://github.com/koushikchowdary6/EvalForge)** · LLM/RAG/agent evaluation | Offline benchmark runners and regression tests; [RAG retrieval-contract enforcement](https://github.com/koushikchowdary6/EvalForge/pull/119), [retrieval-adapter integrity checks](https://github.com/koushikchowdary6/EvalForge/pull/121), [Unicode benchmark validation](https://github.com/koushikchowdary6/EvalForge/pull/122), and [Python test matrix](https://github.com/koushikchowdary6/EvalForge/actions). |
| **[Prompt Injection Detector](https://github.com/koushikchowdary6/prompt-injection-detector)** · applied ML/guardrails | Hybrid heuristics and TF-IDF/logistic regression; [group-disjoint cross-validation](https://github.com/koushikchowdary6/prompt-injection-detector/pull/22), [validated held-out CV decisions](https://github.com/koushikchowdary6/prompt-injection-detector/pull/39), [bounded regex work](https://github.com/koushikchowdary6/prompt-injection-detector/pull/35), [typed ML probability validation](https://github.com/koushikchowdary6/prompt-injection-detector/pull/37), and [tests/CI](https://github.com/koushikchowdary6/prompt-injection-detector/actions). |
| **[SigmaForge](https://github.com/koushikchowdary6/sigmaforge)** · detection engineering/backend | FastAPI, RBAC and PostgreSQL-backed rule revisions; [selector-pattern preflight](https://github.com/koushikchowdary6/sigmaforge/pull/38), [stored-snapshot integrity checks](https://github.com/koushikchowdary6/sigmaforge/pull/36), and [backend/database/Docker CI](https://github.com/koushikchowdary6/sigmaforge/actions). |
| **[Airflow/PostgreSQL ETL](https://github.com/koushikchowdary6/airflow-postgres-etl)** · data engineering | Incremental loads, idempotent upserts and transactional watermarks; [last-good snapshots](https://github.com/koushikchowdary6/airflow-postgres-etl/pull/9), [truncated-source checks](https://github.com/koushikchowdary6/airflow-postgres-etl/pull/10), [CSV processing-size guard](https://github.com/koushikchowdary6/airflow-postgres-etl/pull/11), and [tests/CI](https://github.com/koushikchowdary6/airflow-postgres-etl/actions). |

## Additional security and cloud/data engineering

- **[Flask AppSec Lab](https://github.com/koushikchowdary6/flask-appsec-lab):** paired vulnerable/hardened routes, [note-scoped one-time CSRF tokens](https://github.com/koushikchowdary6/flask-appsec-lab/pull/18), [legacy database upgrade tests](https://github.com/koushikchowdary6/flask-appsec-lab/pull/19), and [secure form-target CSP hardening](https://github.com/koushikchowdary6/flask-appsec-lab/pull/21).
- **[LLM PII Redactor](https://github.com/koushikchowdary6/llm-pii-redactor):** targeted sensitive-data masking with [proxy API-key/client-secret header protection](https://github.com/koushikchowdary6/llm-pii-redactor/pull/24), [forwarded authorization-header protection](https://github.com/koushikchowdary6/llm-pii-redactor/pull/23), and [JSON-safe custom masks](https://github.com/koushikchowdary6/llm-pii-redactor/pull/22).
- **[IAM Policy Auditor](https://github.com/koushikchowdary6/iam-policy-auditor):** static AWS IAM risk analysis with [empty-set Allow correctness](https://github.com/koushikchowdary6/iam-policy-auditor/pull/32), [broad ARN detection](https://github.com/koushikchowdary6/iam-policy-auditor/pull/29), [global Resource wildcard checks](https://github.com/koushikchowdary6/iam-policy-auditor/pull/31), and [strict CLI exit-code tests](https://github.com/koushikchowdary6/iam-policy-auditor/pull/30).
- **[Network Anomaly Detector](https://github.com/koushikchowdary6/network-anomaly-detector):** synthetic NetFlow / Isolation Forest with [strict numeric telemetry and analyst-budget validation](https://github.com/koushikchowdary6/network-anomaly-detector/pull/6); no real-network accuracy claim.
- **[Security Findings Translator](https://github.com/koushikchowdary6/security-findings-translator):** offline and Claude-backed security explanations with [duplicate-key, nonfinite and API evidence-size guards](https://github.com/koushikchowdary6/security-findings-translator/pull/10); targeted redaction, not comprehensive DLP.
- **[Terraform GCP Data Pipeline](https://github.com/koushikchowdary6/terraform-gcp-data-pipeline):** reproducible infrastructure design and Python/DuckDB ingestion, with [fail-closed data-quality evidence checks](https://github.com/koushikchowdary6/terraform-gcp-data-pipeline/pull/7); no live-cloud deployment claim.

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
