<h1 align="center">Koushik Chowdary</h1>

<p align="center"><strong>AI Engineering · LLM/RAG & Agent Evaluation · AI Security · Data Engineering</strong></p>
<p align="center">Python · FastAPI · PostgreSQL · scikit-learn · Airflow · Terraform · Docker · GitHub Actions</p>
<p align="center"><a href="https://linkedin.com/in/koushik-chowdary">LinkedIn</a> · <a href="mailto:kowshiksc610@gmail.com">Email</a></p>

I build evaluation infrastructure, AI guardrails, security automation, and data pipelines. My master's-level work at the University of South Florida focused on cybersecurity, AI, data, and cloud. Below are **specific engineering changes and tests**, not production-performance claims.

## Start here — four projects worth reviewing

| Project | Engineering evidence |
|---|---|
| **[EvalForge](https://github.com/koushikchowdary6/EvalForge)** · LLM/RAG/agent evaluation | Retrieval metrics, [benchmark and rubric validation](https://github.com/koushikchowdary6/EvalForge/pull/105), [agent cost coverage](https://github.com/koushikchowdary6/EvalForge/pull/106), [duplicate-call prevention](https://github.com/koushikchowdary6/EvalForge/pull/110), [crash-safe JSON reporting](https://github.com/koushikchowdary6/EvalForge/pull/111), [bounded embedding preflight](https://github.com/koushikchowdary6/EvalForge/pull/112), and [Unicode-safe exact-match grading](https://github.com/koushikchowdary6/EvalForge/pull/114). [Tests/CI](https://github.com/koushikchowdary6/EvalForge/actions). |
| **[Prompt Injection Detector](https://github.com/koushikchowdary6/prompt-injection-detector)** · applied ML/guardrails | Hybrid heuristics + TF-IDF/Logistic Regression; [group-disjoint evaluation](https://github.com/koushikchowdary6/prompt-injection-detector/pull/22), [error-rate uncertainty](https://github.com/koushikchowdary6/prompt-injection-detector/pull/30), and [fail-closed configuration validation](https://github.com/koushikchowdary6/prompt-injection-detector/pull/34), and [bounded regex work](https://github.com/koushikchowdary6/prompt-injection-detector/pull/35). [Tests/CI](https://github.com/koushikchowdary6/prompt-injection-detector/actions). |
| **[SigmaForge](https://github.com/koushikchowdary6/sigmaforge)** · detection engineering/backend | FastAPI, RBAC, PostgreSQL-backed draft revisions, [owner-scoped structural version comparisons](https://github.com/koushikchowdary6/sigmaforge/pull/33), and [stored-snapshot integrity checks](https://github.com/koushikchowdary6/sigmaforge/pull/36). [Backend, database and Docker CI](https://github.com/koushikchowdary6/sigmaforge/actions). |
| **[Airflow/PostgreSQL ETL](https://github.com/koushikchowdary6/airflow-postgres-etl)** · data engineering | Incremental loads, idempotent upserts, transactional watermarks, [last-good snapshot preservation](https://github.com/koushikchowdary6/airflow-postgres-etl/pull/9), and [truncated-source checks](https://github.com/koushikchowdary6/airflow-postgres-etl/pull/10). [Tests/CI](https://github.com/koushikchowdary6/airflow-postgres-etl/actions). |

## Additional security and cloud/data engineering

- **[Flask AppSec Lab](https://github.com/koushikchowdary6/flask-appsec-lab):** paired vulnerable/hardened routes, [note-scoped one-time CSRF tokens](https://github.com/koushikchowdary6/flask-appsec-lab/pull/18), [legacy database upgrade tests](https://github.com/koushikchowdary6/flask-appsec-lab/pull/19), and [startup repair of malformed CSRF schemas](https://github.com/koushikchowdary6/flask-appsec-lab/pull/20).
- **[LLM PII Redactor](https://github.com/koushikchowdary6/llm-pii-redactor):** targeted sensitive-data masking, including [numeric JSON credentials](https://github.com/koushikchowdary6/llm-pii-redactor/pull/18) and [YAML multiline/quoted-key credentials](https://github.com/koushikchowdary6/llm-pii-redactor/pull/20), and [structured session/cookie masking](https://github.com/koushikchowdary6/llm-pii-redactor/pull/21).
- **[IAM Policy Auditor](https://github.com/koushikchowdary6/iam-policy-auditor):** static AWS IAM risk analysis with [strict SourceIp CIDR validation](https://github.com/koushikchowdary6/iam-policy-auditor/pull/27) and [negative/optional condition handling](https://github.com/koushikchowdary6/iam-policy-auditor/pull/28).
- **[Terraform GCP Data Pipeline](https://github.com/koushikchowdary6/terraform-gcp-data-pipeline):** reproducible infrastructure design and Python/DuckDB ingestion; no live-cloud deployment claim.

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
