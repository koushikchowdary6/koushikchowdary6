<h1 align="center">Koushik Chowdary</h1>

<p align="center"><strong>AI Engineering · LLM/RAG & Agent Evaluation · AI Security · Data Engineering</strong></p>
<p align="center">Python · FastAPI · PostgreSQL · scikit-learn · Airflow · Terraform · Docker · GitHub Actions</p>
<p align="center"><a href="https://linkedin.com/in/koushik-chowdary">LinkedIn</a> · <a href="mailto:kowshiksc610@gmail.com">Email</a></p>

I build and test AI evaluation, security automation, and data systems. My graduate work at the University of South Florida focused on cybersecurity, AI, data, and cloud. This portfolio emphasizes **reviewable code, reproducible tests, honest benchmark denominators, and clear implementation limits**.

## Start here — engineering evidence

| Project | What to inspect |
|---|---|
| **[EvalForge](https://github.com/koushikchowdary6/EvalForge)** · LLM/RAG/agent evaluation | Reproducible retrieval metrics ([top-k correctness](https://github.com/koushikchowdary6/EvalForge/pull/100)), [judge coverage](https://github.com/koushikchowdary6/EvalForge/pull/102), [strict benchmark/rubric validation](https://github.com/koushikchowdary6/EvalForge/pull/105), and [agent cost coverage](https://github.com/koushikchowdary6/EvalForge/pull/106) and [missing-usage handling](https://github.com/koushikchowdary6/EvalForge/pull/107), plus [invisible-only response scoring safeguards](https://github.com/koushikchowdary6/EvalForge/pull/108) and [Unicode-safe minimum-length grading](https://github.com/koushikchowdary6/EvalForge/pull/109), and [duplicate paid-sweep prevention](https://github.com/koushikchowdary6/EvalForge/pull/110). Offline regression tests guard benchmark integrity before paid API calls. |
| **[Prompt Injection Detector](https://github.com/koushikchowdary6/prompt-injection-detector)** · applied ML/guardrails | Hybrid heuristics + TF-IDF/Logistic Regression, [leakage-aware grouped cross-validation](https://github.com/koushikchowdary6/prompt-injection-detector/pull/22), [error-rate uncertainty](https://github.com/koushikchowdary6/prompt-injection-detector/pull/30), [classifier integrity](https://github.com/koushikchowdary6/prompt-injection-detector/pull/32), and [invalid-Unicode rejection](https://github.com/koushikchowdary6/prompt-injection-detector/pull/33), and [fail-closed threshold/weight configuration](https://github.com/koushikchowdary6/prompt-injection-detector/pull/34). |
| **[SigmaForge](https://github.com/koushikchowdary6/sigmaforge)** · detection engineering/backend | FastAPI, RBAC, PostgreSQL-backed immutable Sigma draft revisions, [owner-scoped history](https://github.com/koushikchowdary6/sigmaforge/pull/32), [structural version diffs](https://github.com/koushikchowdary6/sigmaforge/pull/33), and [fail-closed JSON and structural snapshot validation](https://github.com/koushikchowdary6/sigmaforge/pull/36). Backend, database, and Docker CI tests. |
| **[Airflow/PostgreSQL ETL](https://github.com/koushikchowdary6/airflow-postgres-etl)** · data engineering | Incremental ETL, idempotent upserts, transactional watermarks, data-quality checks, and [last-good CSV snapshot preservation](https://github.com/koushikchowdary6/airflow-postgres-etl/pull/9), [minimum-record completeness checks](https://github.com/koushikchowdary6/airflow-postgres-etl/pull/10), and offline integration tests. |

### More AI-security and cloud/data work

- **[LLM PII Redactor](https://github.com/koushikchowdary6/llm-pii-redactor):** offline sensitive-header and credential redaction, including [cloud provider token headers](https://github.com/koushikchowdary6/llm-pii-redactor/pull/17) and [numeric JSON credential masking](https://github.com/koushikchowdary6/llm-pii-redactor/pull/18), plus [multiline YAML secret-block redaction](https://github.com/koushikchowdary6/llm-pii-redactor/pull/19) and [quoted YAML credential-key handling](https://github.com/koushikchowdary6/llm-pii-redactor/pull/20).
- **[IAM Policy Auditor](https://github.com/koushikchowdary6/iam-policy-auditor):** static AWS IAM risk analysis with [condition-value validation](https://github.com/koushikchowdary6/iam-policy-auditor/pull/26) [strict SourceIp CIDR checks](https://github.com/koushikchowdary6/iam-policy-auditor/pull/27), and [negative/optional condition handling](https://github.com/koushikchowdary6/iam-policy-auditor/pull/28).
- **[Flask AppSec Lab](https://github.com/koushikchowdary6/flask-appsec-lab):** paired vulnerable/hardened web routes with [SQLite-backed one-time CSRF token consumption](https://github.com/koushikchowdary6/flask-appsec-lab/pull/17).
- **[Terraform GCP Data Pipeline](https://github.com/koushikchowdary6/terraform-gcp-data-pipeline):** reproducible infrastructure design and Python/DuckDB ingestion; **no live-cloud deployment claim**.

## Verified contributions to other maintainers' repositories

These are **merged pull requests authored by me**, not repositories I own or maintain.

| Repository owned by Priya Khatik | Merged contributions |
|---|---|
| **[Wheat FHB Forecasting](https://github.com/priakhatik/wheat-fhb-forecasting)** | [Cross-validation leakage fix (#1)](https://github.com/priakhatik/wheat-fhb-forecasting/pull/1) · [Portable, testable prediction (#2)](https://github.com/priakhatik/wheat-fhb-forecasting/pull/2) |
| **[Corn Belt Drought Risk](https://github.com/priakhatik/corn-belt-drought-risk)** | [Leakage-safe temporal features (#1)](https://github.com/priakhatik/corn-belt-drought-risk/pull/1) · [Reproducible model artifacts (#2)](https://github.com/priakhatik/corn-belt-drought-risk/pull/2) |
| **[Spotify Azure Project](https://github.com/priakhatik/spotify_azure_project)** | [Lakeflow CDC correction (#2)](https://github.com/priakhatik/spotify_azure_project/pull/2) · [Remove exposed signed callback (#3)](https://github.com/priakhatik/spotify_azure_project/pull/3) |

All six PRs above were merged in October 2026. Other open PRs are **not** counted as merged contributions.

## Scope and limitations

- EvalForge provides evaluation infrastructure and regression tests; it does **not** establish production model accuracy. Historical benchmark results are not automatically recomputed when grading contracts change.
- Prompt Injection Detector reports exploratory grouped-CV metrics, **not calibrated production risk**.
- SigmaForge currently performs **structural** Sigma preflight and draft/version management; pySigma semantic validation, approval, and deployment are **not implemented**.
- Security labs and scanners are educational/static tools, not comprehensive DLP, AWS authorization simulation, or production-ready security guarantees.

**Roles I'm targeting:** AI Engineer · Applied AI / ML Engineer · LLM/RAG Evaluation · AI Security Engineer · Data Engineer · Python Backend Engineer
