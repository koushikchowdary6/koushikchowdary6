<h1 align="center">Koushik Chowdary</h1>

<p align="center">
  <b>AI Engineering · Data Engineering · LLM/RAG/Agent Evaluation · AI Security</b><br>
  University of South Florida · Graduate focus: Cybersecurity, AI, Data & Cloud · Python · SQL/PostgreSQL · Airflow · Terraform · FastAPI · AWS/Azure/GCP
</p>

<p align="center">
  <a href="https://linkedin.com/in/koushik-chowdary"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="mailto:kowshiksc610@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>
</p>

---

## What I build

I build AI and data systems that can be inspected, tested, and reproduced. My current work spans LLM/RAG/agent evaluation, AI guardrails, Airflow/PostgreSQL ETL, Terraform/GCP data infrastructure, and security automation. I prefer measurable behavior, explicit limitations, idempotent pipelines, and CI-backed engineering over portfolio-only demos.

### Recruiter quick tour

| Project | What to inspect |
|---|---|
| **[EvalForge](https://github.com/koushikchowdary6/EvalForge)** | Reproducible RAG/agent evaluation with retrieval metrics, benchmark fingerprints, and offline tests. [Strict RAG judge evidence (#92)](https://github.com/koushikchowdary6/EvalForge/pull/92), [text-answer boundary grading (#91)](https://github.com/koushikchowdary6/EvalForge/pull/91), and [fail-closed general LLM judge JSON (#89)](https://github.com/koushikchowdary6/EvalForge/pull/89). Separates provider failures from model quality. |
| **[Prompt Injection Detector](https://github.com/koushikchowdary6/prompt-injection-detector)** | Hybrid heuristic + TF-IDF/Logistic Regression guardrail, adversarial text normalization; evidence includes [leakage-aware grouped CV](https://github.com/koushikchowdary6/prompt-injection-detector/pull/22), [pooled confusion/FNR metrics (#27)](https://github.com/koushikchowdary6/prompt-injection-detector/pull/27), and [multi-threshold grouped-CV sweep (#28)](https://github.com/koushikchowdary6/prompt-injection-detector/pull/28) with fit-once folds, plus [bounded regex scanning (#29)](https://github.com/koushikchowdary6/prompt-injection-detector/pull/29) to limit CPU amplification on long obfuscated prompts. Exploratory CV, not calibrated risk or deployment validation. |
| **[SigmaForge](https://github.com/koushikchowdary6/sigmaforge)** | FastAPI/React detection-engineering platform with RBAC, Docker CI, bounded Sigma structural preflight, and [atomic draft + initial-version persistence (#27)](https://github.com/koushikchowdary6/sigmaforge/pull/27), with [migrated PostgreSQL HTTP/persistence and rollback tests (#28)](https://github.com/koushikchowdary6/sigmaforge/pull/28) and [authenticated owner-only draft retrieval (#29)](https://github.com/koushikchowdary6/sigmaforge/pull/29). Listing, editing, pySigma semantic validation, and deployment remain future work. |
| **[Airflow/PostgreSQL ETL](https://github.com/koushikchowdary6/airflow-postgres-etl)** | Incremental ETL, idempotent upserts, transactional watermarks, nine quality checks, database integration tests, and [upstream schema-drift snapshot protection (#8)](https://github.com/koushikchowdary6/airflow-postgres-etl/pull/8) and [CSV shape validation (#7)](https://github.com/koushikchowdary6/airflow-postgres-etl/pull/7). |
| **[Terraform GCP Data Pipeline](https://github.com/koushikchowdary6/terraform-gcp-data-pipeline)** | Python/DuckDB ingestion, GCS/BigQuery infrastructure design, integrity-checked incremental state, and [empty-download snapshot preservation](https://github.com/koushikchowdary6/terraform-gcp-data-pipeline/pull/6). No live-cloud deployment claim. |
| **[IAM Policy Auditor](https://github.com/koushikchowdary6/iam-policy-auditor)** | Offline AWS IAM risk analysis with conservative principal/Condition validation and [fail-closed principal wildcard validation](https://github.com/koushikchowdary6/iam-policy-auditor/pull/24), plus [invisible-only Unicode identifier rejection (#25)](https://github.com/koushikchowdary6/iam-policy-auditor/pull/25); not an authorization simulator. |
| **[LLM PII Redactor](https://github.com/koushikchowdary6/llm-pii-redactor)** | Offline prompt/log guardrail with provider-key and sensitive-header detection, [folded credential coverage](https://github.com/koushikchowdary6/llm-pii-redactor/pull/12), [YAML credential masking (#15)](https://github.com/koushikchowdary6/llm-pii-redactor/pull/15), and [AWS shared-credential masking across env/YAML/JSON (#16)](https://github.com/koushikchowdary6/llm-pii-redactor/pull/16). Not complete DLP. |
| **[Flask AppSec Lab](https://github.com/koushikchowdary6/flask-appsec-lab)** | Paired vulnerable/secure SQLi, XSS, IDOR, and CSRF examples, with regression tests, [SQLite ID boundary hardening](https://github.com/koushikchowdary6/flask-appsec-lab/pull/11), [ambiguous note-form rejection](https://github.com/koushikchowdary6/flask-appsec-lab/pull/12), [duplicate login-field rejection](https://github.com/koushikchowdary6/flask-appsec-lab/pull/13), and [ambiguous search-query rejection](https://github.com/koushikchowdary6/flask-appsec-lab/pull/14). Local teaching lab only. |
| **[Security Findings Translator](https://github.com/koushikchowdary6/security-findings-translator)** | LLM-backed and offline security explanations with redaction at both request and output boundaries; not complete DLP. |

### Evidence and limits

All linked engineering PRs are merged and include tests. Benchmarks are reproducible prototypes, not claims of production accuracy or deployment.

---

## Open-source contributions

- **[Wheat FHB Forecasting PR #1](https://github.com/priakhatik/wheat-fhb-forecasting/pull/1)** *(merged Oct 16, 2026)* — moves preprocessing inside cross-validation folds and removes machine-specific paths so model evaluation is less leakage-prone and more reproducible.
- **[Corn Belt Drought Risk PR #1](https://github.com/priakhatik/corn-belt-drought-risk/pull/1)** *(merged Oct 16, 2026)* — aligns drought labels, prevents future-date joins, and builds climatology from training years only for cleaner held-out evaluation.
- **[Spotify Azure Project PR #2](https://github.com/priakhatik/spotify_azure_project/pull/2)** *(merged Oct 16, 2026)* — repairs a Lakeflow SCD Type 2 CDC definition using the current `pyspark.pipelines` API and the ADF `updated_at` watermark.

- **[Wheat FHB Forecasting PR #2](https://github.com/priakhatik/wheat-fhb-forecasting/pull/2)** *(merged Oct 26, 2026)* — makes prediction portable and import-safe, with reproducible inputs and offline tests.
- **[Corn Belt Drought Risk PR #2](https://github.com/priakhatik/corn-belt-drought-risk/pull/2)** *(merged Oct 26, 2026)* — improves model-artifact reproducibility and validates held-out class coverage.
- **[Spotify Azure Project PR #3](https://github.com/priakhatik/spotify_azure_project/pull/3)** *(merged Oct 26, 2026)* — removes an exposed signed Logic App callback from an ADF pipeline; the maintainer still needs to confirm rotation or revocation of the previously exposed credential.

These six merged pull requests were authored as contributions to repositories owned by **Priya Khatik**. They do not imply ownership of those projects or production deployment. The three October 26 merges passed their post-merge main-branch CI.

---

## Additional security foundations

[Network Anomaly Detector](https://github.com/koushikchowdary6/network-anomaly-detector) (synthetic-data Isolation Forest and tie-aware alert-budget metrics) · [SSH Log Threat Detector](https://github.com/koushikchowdary6/ssh-log-threat-detector) · [Phishing URL Detector](https://github.com/koushikchowdary6/phishing-url-detector) · [Lamport Signatures](https://github.com/koushikchowdary6/lamport-signatures) · [AES Modes](https://github.com/koushikchowdary6/aes-modes-of-operation).

---

## Stack

**AI / LLM:** LLM evaluation · RAG evaluation · agent/tool-call evaluation · prompt injection · guardrails · scikit-learn · benchmark design  
**Engineering:** Python · FastAPI · SQL/PostgreSQL · Airflow · DuckDB · Terraform · GCP/BigQuery · React/TypeScript · Docker · GitHub Actions · Linux  
**Security:** AI security · Detection engineering · AppSec · IAM · Cloud security · OWASP · MITRE ATT&CK · SIEM/SOC

---

## What I am targeting

**AI Engineering · Data Engineering · LLM/RAG/Agent Evaluation · AI Security · Applied ML · Platform Engineering**

<p align="center">
  <i>Building toward AI and data engineering roles with a portfolio grounded in reproducible evaluation, idempotent pipelines, cloud infrastructure, guardrails, and security engineering.</i>
</p>
