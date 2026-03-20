# devsecops-ci-cd-pipeline-jenkins-k8s-security

## 🚀 DevSecOps End-to-End Pipeline

Terraform | Jenkins | AWS | Docker | Kubernetes | SonarCloud | Snyk | OWASP ZAP
---

📌 Project Overview

This project demonstrates a production-style DevSecOps pipeline where:

- Infrastructure is provisioned using Terraform

- CI/CD is orchestrated via Jenkins

- Applications are containerized using Docker

- Images are stored in AWS ECR

- Workloads are deployed to Kubernetes (EKS)

- Security is enforced using:

  -- SAST → SonarCloud

  -- SCA → Snyk

  -- DAST → OWASP ZAP

---
🔹 Repo 1 — Infrastructure (Terraform)

👉 devsecops-infra-aws-jenkins-eks

Responsible for:

- EC2 provisioning (Jenkins server)

- Security groups

- IAM roles

- Jenkins installation via bootstrap script

- EKS interaction setup
##
🔹 Repo 2 — DevSecOps Pipeline

👉 devsecops-ci-cd-pipeline-jenkins-k8s-security

Responsible for:

- Application build (Maven)

- Security scanning (SAST + SCA + DAST)

- Docker image creation

- Push to AWS ECR

- Kubernetes deployment

- Automated vulnerability testing
##
🔗 How Both Repos Work Together
<img width="4143" height="526" alt="mermaid-diagram" src="https://github.com/user-attachments/assets/6719f892-322b-4c37-a691-a9c0d782a70f" />
## 🏗️ Architecture Diagram
<img width="952" height="1616" alt="mermaid-diagram2" src="https://github.com/user-attachments/assets/97a9155c-78e5-4ce1-a9cd-2528dbc578b7" />
##

| Stage     | Tool       | Purpose                        |
| --------- | ---------- | ------------------------------ |
| SAST      | SonarCloud | Code quality & vulnerabilities |
| SCA       | Snyk       | Dependency vulnerabilities     |
| Container | Docker     | Secure packaging               |
| Runtime   | Kubernetes | Isolation & scaling            |
| DAST      | OWASP ZAP  | Live vulnerability scanning    |


##

📊 ZAP Scan Summary (From Your Report)

- ✅ 54 PASS checks

- ⚠️ 13 WARNINGS

- ❌ 0 Critical issues

Key Findings
⚠️ Medium Risk

- Missing Content Security Policy (CSP)

- Missing Anti-CSRF tokens

- Session ID exposed in URL

- Debug error messages exposed

⚠️ Low Risk

- Missing security headers

- Cookie security flags missing

- Information disclosure via responses
##

---
⭐ Final Result

✔ Fully automated DevSecOps pipeline
✔ Secure infrastructure provisioning
✔ Real-world vulnerability scanning
✔ Production-ready architecture


