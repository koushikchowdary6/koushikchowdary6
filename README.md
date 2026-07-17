# Hi, I'm Koushik 👋

**Cybersecurity engineer** focused on **detection engineering, application/cloud security, and the security of AI-assisted tooling.** Currently pursuing an **M.S. in Cybersecurity at the University of South Florida.** I like building things that actually run the projects below are working code with tests and CI, not just write-ups.

- 🔭 **Currently building:** [SigmaForge](https://github.com/koushikchowdary6/sigmaforge)  an AI-assisted detection-engineering platform with a research track on adversarial sabotage of LLM-generated detection rules.
- 🎯 **Interested in:** SOC / Detection Engineering, Security Platform Engineering, Cloud Security, and AI security.
- 🎖️ **Certified:** CompTIA CySA+ · AWS Security – Specialty · AWS Cloud Practitioner · Microsoft Azure Security Engineer Associate.

---

## 🚀 Featured Projects

### 🔹 [SigmaForge](https://github.com/koushikchowdary6/sigmaforge)  AI-assisted detection engineering platform
A detection-engineering platform built alongside a research question: **can adversarial context manipulation covertly sabotage LLM-generated Sigma detection rules, and does human review catch it?** The v0.1.0 foundation is real and tested  RS256 JWT auth with rotating refresh-token theft detection, RBAC across five roles, a 20-table Postgres schema, a Celery worker, a React front end, and a full CI/CD pipeline that boots the entire Docker Compose stack and runs dependency + container vulnerability scans on every push.
`FastAPI` · `React/TypeScript` · `PostgreSQL` · `Celery` · `Docker` · `GitHub Actions`

### 🔹 [flask-appsec-lab](https://github.com/koushikchowdary6/flask-appsec-lab)  hands-on web-security lab
Every vulnerability is shown **twice**  an exploitable `/vuln` route and a fixed `/secure` route with identical behavior  so the fix is a visible code diff. Covers **SQL injection, reflected XSS, and IDOR**, with an automated test suite (CI-enforced) proving each vuln is real on one side and closed on the other.
`Flask` · `pytest` · OWASP Top 10 / CWE mapping

### 🔹 [sha1-password-cracking-project](https://github.com/koushikchowdary6/sha1-password-cracking-project)  why fast hashes fail
A multi-process SHA-1 cracker demonstrating why unsalted fast hashes are unsuitable for passwords: digit, date, dictionary, transformation, word+digit, leetspeak, and word-pair strategies. Recovers the included demo set 10/10 in ~2 seconds.
`Python` · `multiprocessing` · `hashlib`

### 🔹 [Cryptography  Classical Cipher Breaker](https://github.com/koushikchowdary6/Cryptography-Password-Cracking-)  cryptanalysis by statistics
Breaks **Caesar and Vigenère** ciphers with no key and no wordlist  chi-squared frequency scoring for Caesar, index-of-coincidence key-length estimation for Vigenère. Test-covered and CI-enforced.
`Python` · frequency analysis · `pytest`

### 🔹 [DNS Lookup & Resolution](https://github.com/koushikchowdary6/DNS-lookup-and-resolution-project)  DNS internals, hands-on
A `dnspython` tool that resolves record types (A/AAAA/CNAME/NS/MX/TXT/SOA), does reverse PTR lookups, and performs an **iterative root → TLD → authoritative trace**  the concrete version of recursive-vs-iterative resolution  paired with a written analysis.
`Python` · `dnspython`

---

## 🛠️ Skills

**Security:** SOC operations & SIEM (Splunk), detection engineering, penetration testing, vulnerability management (Nessus, Nmap), packet analysis (Wireshark), threat modeling, RBAC/JWT auth design
**Cloud:** AWS (IAM, VPC, EC2, S3, Lambda, Security Hub, CloudTrail) · Azure (Defender for Cloud, Entra ID, Key Vault) · Zero Trust
**Engineering:** Python, FastAPI, Flask, SQL/PostgreSQL, Docker, GitHub Actions CI/CD, React/TypeScript
**Networking:** LAN/WAN, VLANs, routing & switching, firewalls & VPN (IPSec/SSL), DNS security

---

## 🎖️ Certifications
CompTIA CySA+ · AWS Certified Security – Specialty · AWS Certified Cloud Practitioner · Microsoft Certified: Azure Security Engineer Associate

---

📫 **Reach me:** kowshiksc610@gmail.com · [LinkedIn](https://linkedin.com/in/koushik-chowdary)

*Open to SOC Analyst, Detection Engineer, Security Platform Engineer, and Cloud Security roles.*
