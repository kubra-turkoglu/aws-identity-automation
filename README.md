# \# AWS IAM Security Audit Toolkit

# 

# This repository functions as an AWS IAM Security Audit \& Access Governance Toolkit designed from a SOC Analyst perspective. Instead of focusing on infrastructure provisioning, this toolkit automates risk mitigation, privilege minimization, threat hunting, and compliance verification across AWS Identity and Access Management (IAM).

# 

# It addresses the fundamental question asked by security auditors, compliance teams, and SOC analysts: \*\*"What identities currently exist in our AWS environment, and what is their actual security posture?"\*\*

# 

# \## 📂 Repository Structure

# 

# ```text

# aws-identity-automation/

# │

# ├── src/                # Core production-ready Python automation modules

# ├── reports/            # Generated audit evidence (CSV/JSON formats) \[Git Ignored]

# ├── screenshots/        # Proof of execution for documentation

# ├── notebooks/          # Interactive security reviews and threat hunting playbooks

# ├── docs/               # Compliance mapping guides (CIS, SOC 2, ISO 27001)

# ├── .gitignore          # Prevents local audit reports from leaking into GitHub

# ├── README.md           # Project documentation and setup guide

# └── requirements.txt    # Project dependencies





\## 📊 Sample Output Format

The toolkit standardizes IAM metadata into actionable security logs:





| Audit\_Date | Entity\_Type | Username | User\_Id | Arn | Created\_At | Status |

| :--- | :--- | :--- | :--- | :--- | :--- | :--- |

| 2026-06-09 UTC | IAM\_User | admin\_test | AIDAX... | arn:aws:iam:... | 2026-01-10 | Active |



👉 \*\*View Full Artifacts:\*\*

\*   \[Download Auditor Excel Report (CSV)](./reports/iam\_inventory\_SAMPLE.csv)

\*   \[View SIEM JSON Stream](./reports/iam\_inventory\_SAMPLE.json)



