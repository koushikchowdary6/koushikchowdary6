<h1 align="center">Koushik Chowdary</h1>

<p align="center"><strong>AI Engineering · LLM/RAG & Agent Evaluation · AI Security · Python Backend</strong></p>
<p align="center">Python · FastAPI · scikit-learn · PostgreSQL · Airflow · Terraform · Docker · GitHub Actions</p>
<p align="center"><a href="https://linkedin.com/in/koushik-chowdary">LinkedIn</a> · <a href="mailto:kowshiksc610@gmail.com">Email</a></p>

I build evaluation tooling, AI guardrails, backend systems, and data pipelines. My graduate work at the University of South Florida focused on cybersecurity, AI, data, and cloud. **The links below lead to working code, regression tests, and CI—not claims of production deployment or independently validated model accuracy.**

## Start here: three flagship projects

| Project | What to inspect | Verified evidence |
|---|---|---|
| **[EvalForge](https://github.com/koushikchowdary6/EvalForge)** · LLM/RAG/agent evaluation | API-free BM25 baseline; retrieval precision, nDCG and AP; evidence-only hit bounds; paired RAG comparisons and agent tool-call evaluation | [Offline retrieval demo](https://github.com/koushikchowdary6/EvalForge/pull/138) · [BM25 tie-bound regression tests](https://github.com/koushikchowdary6/EvalForge/pull/154) · [Python 3.10–3.12 CI](https://github.com/koushikchowdary6/EvalForge/actions/runs/41212766457) |
| **[Prompt Injection Detector](https://github.com/koushikchowdary6/prompt-injection-detector)** · applied ML / AI guardrails | Hybrid heuristics + TF-IDF/logistic regression; grouped cross-validation; encoded/Unicode attack patterns; leakage checks and bounded error analysis for user-supplied holdouts | [Grouped-CV evidence](https://github.com/koushikchowdary6/prompt-injection-detector/pull/22) · [External holdout tooling](https://github.com/koushikchowdary6/prompt-injection-detector/pull/53) · [Near-overlap audit](https://github.com/koushikchowdary6/prompt-injection-detector/pull/62) · [Strict holdout overlap gate](https://github.com/koushikchowdary6/prompt-injection-detector/pull/63) · [Within-holdout duplicate screening](https://github.com/koushikchowdary6/prompt-injection-detector/pull/64) · [CI](https://github.com/koushikchowdary6/prompt-injection-detector/actions/runs/41222880684) |
| **[SigmaForge](https://github.com/koushikchowdary6/sigmaforge)** · detection engineering / backend security | FastAPI, PostgreSQL, RBAC, Sigma rule revisions and integrity checks; transactional refresh-token rotation and replay containment | [PostgreSQL concurrency tests](https://github.com/koushikchowdary6/sigmaforge/pull/44) · [Correlated error logging #45](https://github.com/koushikchowdary6/sigmaforge/pull/45) · [Backend, worker and Docker CI](https://github.com/koushikchowdary6/sigmaforge/actions/runs/41227507348) |

## More systems with executable evidence

| Project | Focus |
|---|---|
| **[EdgeWatch IoT](https://github.com/koushikchowdary6/edgewatch-iot)** | Python telemetry ingestion, offline replay, deduplication, and event-bound acknowledgments that prevent dequeueing the wrong telemetry sample · [Regression PR #9](https://github.com/koushikchowdary6/edgewatch-iot/pull/9) · [Post-merge CI](https://github.com/koushikchowdary6/edgewatch-iot/actions/runs/41236900197) |
| **[Document Review Pipeline](https://github.com/koushikchowdary6/document-review-pipeline)** | Privacy/security automation, approval-bound exports, synthetic PII evaluation and bounded no-follow CLI ingestion · [Input safety tests](https://github.com/koushikchowdary6/document-review-pipeline/pull/6) · [CI](https://github.com/koushikchowdary6/document-review-pipeline/actions/runs/41222857173) |
| **[Airflow/PostgreSQL ETL](https://github.com/koushikchowdary6/airflow-postgres-etl)** | Incremental loads, quality checks, transactional staging/upserts and malformed-row auditing before watermark filtering · [PR #16](https://github.com/koushikchowdary6/airflow-postgres-etl/pull/16) · [CI](https://github.com/koushikchowdary6/airflow-postgres-etl/actions/runs/41231765057) |
| **[Terraform GCP Data Pipeline](https://github.com/koushikchowdary6/terraform-gcp-data-pipeline)** | Infrastructure-as-code design, Python/DuckDB ingestion, quality checks and bounded HTTP source streaming · [PR #9](https://github.com/koushikchowdary6/terraform-gcp-data-pipeline/pull/9) · [Python CI](https://github.com/koushikchowdary6/terraform-gcp-data-pipeline/actions/runs/41231871639) · [Terraform CI](https://github.com/koushikchowdary6/terraform-gcp-data-pipeline/actions/runs/41231871655) |
| **[IAM Policy Auditor](https://github.com/koushikchowdary6/iam-policy-auditor)** | Offline AWS IAM risk linting, bounded JSON input, privilege-escalation heuristics, and [SARIF 2.1.0 export with regression tests](https://github.com/koushikchowdary6/iam-policy-auditor/pull/38) · [CI](https://github.com/koushikchowdary6/iam-policy-auditor/actions/runs/41217406864) |
| **[Flask AppSec Lab](https://github.com/koushikchowdary6/flask-appsec-lab)** | Side-by-side vulnerable/hardened routes; CSRF, XSS, SQL injection and IDOR tests · [CI](https://github.com/koushikchowdary6/flask-appsec-lab/actions/runs/41191264943) |
| **[LLM PII Redactor](https://github.com/koushikchowdary6/llm-pii-redactor)** | Targeted masking and fail-closed input handling · [CI](https://github.com/koushikchowdary6/llm-pii-redactor/actions/runs/41195037790) |

## Recent verified engineering changes

- **[Airflow/PostgreSQL ETL #16](https://github.com/koushikchowdary6/airflow-postgres-etl/pull/16):** rejects truncated CSV rows *before* incremental watermark filtering, retaining row-numbered audit evidence rather than silently skipping malformed historical records. Tests cover both historical and current rows. [Post-merge CI passed](https://github.com/koushikchowdary6/airflow-postgres-etl/actions/runs/41231765057).
- **[Terraform GCP Data Pipeline #9](https://github.com/koushikchowdary6/terraform-gcp-data-pipeline/pull/9):** streams raw HTTP feeds with a 20 MiB transfer cap and atomic snapshot replacement. Tests cover early oversize termination, interrupted downloads, byte-limit boundaries and cleanup. [Python CI](https://github.com/koushikchowdary6/terraform-gcp-data-pipeline/actions/runs/41231871639) and [Terraform CI](https://github.com/koushikchowdary6/terraform-gcp-data-pipeline/actions/runs/41231871655) passed. This is not a live GCP deployment.
- **[SigmaForge #45](https://github.com/koushikchowdary6/sigmaforge/pull/45):** backend middleware records request-correlated exception events before clearing request context, without logging query values, request bodies, headers or exception messages. [Post-merge CI passed](https://github.com/koushikchowdary6/sigmaforge/actions/runs/41227507348).
- **[EdgeWatch IoT #9](https://github.com/koushikchowdary6/edgewatch-iot/pull/9):** the receiver echoes each persisted device/sequence identity, and the replay client refuses to remove a queued event when a valid-looking HTTP acknowledgment belongs to another event. Regression tests cover mismatched, missing, and boolean sequence values. [Post-merge Python 3.10/3.12 CI passed](https://github.com/koushikchowdary6/edgewatch-iot/actions/runs/41236900197). This does not cryptographically authenticate the receiver.

## Verified contributions to other maintainers' repositories

These are **merged pull requests authored by my account**, not repositories I own. Open PRs are not counted.

| Repository | Merged contributions |
|---|---|
| [Wheat FHB Forecasting](https://github.com/priakhatik/wheat-fhb-forecasting) | [Cross-validation leakage fix #1](https://github.com/priakhatik/wheat-fhb-forecasting/pull/1) · [Portable prediction #2](https://github.com/priakhatik/wheat-fhb-forecasting/pull/2) |
| [Corn Belt Drought Risk](https://github.com/priakhatik/corn-belt-drought-risk) | [Leakage-safe temporal features #1](https://github.com/priakhatik/corn-belt-drought-risk/pull/1) · [Reproducible artifacts #2](https://github.com/priakhatik/corn-belt-drought-risk/pull/2) |
| [Spotify Azure Project](https://github.com/priakhatik/spotify_azure_project) | [Lakeflow CDC correction #2](https://github.com/priakhatik/spotify_azure_project/pull/2) · [Remove exposed signed callback #3](https://github.com/priakhatik/spotify_azure_project/pull/3) |

## Scope and roles

These are tested portfolio and research projects. EvalForge is **evaluation infrastructure**, not proven model accuracy; Prompt Injection Detector has **no independently collected external benchmark supplied**; IAM findings are heuristics, not AWS effective-permission simulation; the cloud/data projects do not imply a live production deployment.

**Target roles:** AI Engineer · Applied AI / ML Engineer · LLM/RAG Evaluation · AI Security Engineer · Python Backend Engineer · Data Engineer
