<h1 align="center">Koushik Chowdary</h1>

<p align="center">
  <b>AI Engineering · LLM/RAG/Agent Evaluation · AI Security</b><br>
  M.S. Cybersecurity, University of South Florida · Python · FastAPI · AWS/Azure · LLM/RAG/Agent Evals
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

I build AI evaluation and security tooling that can be inspected, tested, and reproduced. My current focus is LLM/RAG/agent evaluation, prompt-injection and data-leakage defenses, AI-assisted detection engineering, and cloud/application security. I prefer measurable behavior, explicit limitations, and CI-backed engineering over portfolio-only demos.

### Recruiter quick tour

| Project | Why it is worth opening |
|---|---|
| **[EvalForge](https://github.com/koushikchowdary6/EvalForge)** | LLM, RAG, and tool-calling evaluation framework with auditable reports, automated graders, safety-oriented agent evals, benchmark artifacts, and a CI-backed regression suite. |
| **[prompt-injection-detector](https://github.com/koushikchowdary6/prompt-injection-detector)** | Hybrid heuristic + ML input guardrail with regression tests around jailbreak signals, scoring semantics, thresholds, and pre-training fallback behavior. |
| **[llm-pii-redactor](https://github.com/koushikchowdary6/llm-pii-redactor)** | PII and secret redaction for LLM pipelines, including credential-like token detection and validation logic. |
| **[SigmaForge](https://github.com/koushikchowdary6/sigmaforge)** | FastAPI + React detection-engineering platform and AI-security research testbed with auth/RBAC, Postgres, Celery/Redis, Docker, threat modeling, and CI. |
| **[security-findings-translator](https://github.com/koushikchowdary6/security-findings-translator)** | Translates structured security findings into concise remediation guidance with an LLM-backed path and deterministic offline mode. |
| **[iam-policy-auditor](https://github.com/koushikchowdary6/iam-policy-auditor)** | Offline AWS IAM policy analyzer that flags wildcards, public principals, and privilege-escalation paths and can fail CI on high-risk findings. |

### Recent engineering work — Oct 2026

- **EvalForge:** hardened RAG and agent evaluation correctness, including model-aware embedding caches, malformed/non-finite judge outputs, duplicate tool-call grading, argument scoring, and state isolation across repeated evaluation sweeps.
- **AI guardrails:** strengthened prompt-injection and PII/secret defenses with configuration validation, false-positive regressions, complete/malformed PEM redaction coverage, and safe audit-logging guidance.
- **IAM analysis:** expanded wildcard-action handling and regression coverage for partial IAM action patterns such as `s3:Get*`.
- **Applied ML:** moved network-anomaly evaluation to a held-out train/test methodology and added a regression check for evaluation isolation.
- **Security automation:** hardened security-finding ingestion so malformed JSON fails clearly instead of propagating ambiguous downstream errors.
- **Current direction:** AI engineering + AI security, with measurable evaluation quality, reproducibility, and security engineering depth.

---

## Open-source contributions

- **[Wheat FHB Forecasting PR #1](https://github.com/priakhatik/wheat-fhb-forecasting/pull/1)** *(open)* — moves preprocessing inside cross-validation folds and removes machine-specific paths so model evaluation is less leakage-prone and more reproducible.
- **[Corn Belt Drought Risk PR #1](https://github.com/priakhatik/corn-belt-drought-risk/pull/1)** *(open)* — aligns drought labels, prevents future-date joins, and builds climatology from training years only for cleaner held-out evaluation.
- **[Spotify Azure Project PR #2](https://github.com/priakhatik/spotify_azure_project/pull/2)** *(open)* — repairs a Lakeflow SCD Type 2 CDC definition using the current `pyspark.pipelines` API and the ADF `updated_at` watermark.

These are contributions to repositories owned by **Priya Khatik**; they are listed here as reviewable pull requests, not as projects I own.

---

## Security engineering foundation

| Project | Focus |
|---|---|
| **[flask-appsec-lab](https://github.com/koushikchowdary6/flask-appsec-lab)** | Vulnerable-vs-secure Flask lab demonstrating SQL injection, XSS, IDOR, security headers, and regression-tested remediations. |
| **[ssh-log-threat-detector](https://github.com/koushikchowdary6/ssh-log-threat-detector)** | Detection logic for SSH brute force, password spraying, and suspicious post-authentication activity. |
| **[phishing-url-detector](https://github.com/koushikchowdary6/phishing-url-detector)** | ML classifier using lexical URL features without fetching potentially hostile pages. |
| **[network-anomaly-detector](https://github.com/koushikchowdary6/network-anomaly-detector)** | Isolation Forest anomaly detection over NetFlow-style traffic. |
| **[lamport-signatures](https://github.com/koushikchowdary6/lamport-signatures)** | Hash-based one-time signatures implemented from first principles. |
| **[aes-modes-of-operation](https://github.com/koushikchowdary6/aes-modes-of-operation)** | AES mode implementations and verification exercises. |

---

## Stack

**AI / LLM:** LLM evaluation · RAG evaluation · agent/tool-call evaluation · prompt injection · guardrails · scikit-learn · benchmark design  
**Engineering:** Python · FastAPI · SQL/PostgreSQL · React/TypeScript · Docker · GitHub Actions · Linux  
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

**AI Engineering · LLM/RAG/Agent Evaluation · AI Security · Applied ML · Security Automation**

<p align="center">
  <i>Building toward AI engineering and AI security roles with a portfolio grounded in reproducible evaluation, guardrails, applied ML, data pipelines, and security engineering.</i>
</p>
