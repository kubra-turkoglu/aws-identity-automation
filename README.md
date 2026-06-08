
# AWS IAM Security Audit Toolkit

This repository functions as an AWS IAM Security Audit & Access Governance Toolkit designed from a SOC Analyst perspective. Instead of focusing on infrastructure provisioning, this toolkit automates risk mitigation, privilege minimization, threat hunting, and compliance verification across AWS Identity and Access Management (IAM).

It addresses the fundamental question asked by security auditors, compliance teams, and SOC analysts: 
# **"What identities currently exist in our AWS environment, and what is their actual security posture?"**

## 📂 Repository Structure

```text
aws-identity-automation/
│
├── src/                # Core production-ready Python automation modules
├── reports/            # Generated audit evidence (CSV/JSON formats) [Git Ignored]
├── screenshots/        # Proof of execution for documentation
├── notebooks/          # Interactive security reviews and threat hunting playbooks
├── docs/               # Compliance mapping guides (CIS, SOC 2, ISO 27001)
├── .gitignore          # Prevents local audit reports from leaking into GitHub
├── README.md           # Project documentation and setup guide
└── requirements.txt    # Project dependencies
```
## 🛠️ Features Roadmap
### 📦 Phase 1: Identity Baseline & Reporting (Current)
**IAM Identity Inventory Collection:** Automated discovery of all IAM assets.

**Auditor-Ready Outputs:** Point-in-time snapshot reporting in Excel/CSV format for compliance evidence.

**SIEM-Ready Logs:** Structured JSON outputs optimized for ingestion into SIEM platforms (Splunk, Microsoft Sentinel, Elastic).

### 🛡️ Phase 2: Access Governance & Risk Assessment (Upcoming)
**MFA Compliance Verification:** Identification of active accounts missing Multi-Factor Authentication.

**Credential Lifecycle Auditing:** Detection of stale IAM Access Keys exceeding 90 days (Credential Exposure risks).

**Dormant Account Discovery:** Flagging inactive users to support the Principle of Least Privilege (PoLP).

## 🚀 Getting Started
### 1. Prerequisites
Ensure you have **Python 3.8+** installed and a local emulator like **LocalStack** running for safe, non-destructive testing.
### 2. Installation
Clone the repository and install the required security dependencies:
  
```Bash
git clone [https://github.com/kubra-turkoglu/aws-identity-automation.git](https://github.com/kubra-turkoglu/aws-identity-automation.git)
cd aws-identity-automation
pip install -r requirements.txt
```
### 3. Running the Audit
Navigate to the notebooks/ directory and execute the interactive playbooks, or run the baseline inventory script directly.
The tool will automatically create a persistent directory structure and output your data:
📊 **CSV Evidence:** Saved to reports/iam_inventory_[timestamp].csv
🗂️ **JSON SIEM Feed:** Saved to reports/iam_inventory_[timestamp].json

## 📊 Sample Output Format
The toolkit standardizes IAM metadata into actionable security logs:
Markdown
| Audit_Date | Entity_Type | Username | User_Id | Arn | Created_At | Status |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 2026-06-09 UTC | IAM_User | admin_test | AIDAX... | arn:aws:iam:... | 2026-01-10 | Active |

## 👉 View Full Artifacts:

Download Auditor Excel Report (CSV)

View SIEM JSON Stream

## 🤝 Contributing
Contributions focusing on Cloud Security Posture Management (CSPM), Incident Response playbooks, and IAM threat vector detection are highly welcome. Please open an issue or submit a pull request.
