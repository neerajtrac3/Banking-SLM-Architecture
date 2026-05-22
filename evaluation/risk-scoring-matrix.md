# BankingSLM – Risk Scoring Matrix

This matrix defines how BankingSLM evaluates risk across payments, compliance, fraud, and operational domains.  
Each risk factor is scored on a **1–5 scale**, and aggregated into a composite **Risk Severity Score (RSS)**.

---

## 🧮 Scoring Scale

| Score | Severity | Meaning |
|-------|----------|---------|
| **1** | Very Low | No meaningful risk indicators |
| **2** | Low | Minor anomalies, low regulatory impact |
| **3** | Medium | Requires review, potential compliance or fraud relevance |
| **4** | High | Strong indicators of risk, manual intervention required |
| **5** | Critical | Regulatory breach, fraud likelihood, or operational failure |

---

# 🏦 1. Payment Risk Indicators

| Risk Factor | Description | Score Range |
|------------|-------------|-------------|
| **High-risk jurisdiction** | Country on sanctions/AML list | 1–5 |
| **Unusual transaction amount** | Deviates from customer profile | 1–5 |
| **Missing mandatory ISO 20022 fields** | Missing `RegulatoryReporting`, `CdtrAgt`, etc. | 1–5 |
| **Velocity anomalies** | Rapid repeated transfers | 1–5 |
| **Counterparty mismatch** | Name/IBAN inconsistency | 1–5 |
| **Purpose code inconsistency** | Purpose does not match transaction pattern | 1–5 |

---

# 🕵️‍♂️ 2. AML / KYC Risk Indicators

| Risk Factor | Description | Score Range |
|------------|-------------|-------------|
| **PEP involvement** | Politically exposed person | 1–5 |
| **Sanctions list match** | OFAC / EU / UN match | 1–5 |
| **Beneficial owner risk** | Complex ownership structures | 1–5 |
| **Source of funds unclear** | Missing documentation | 1–5 |
| **Customer risk rating** | Based on KYC profile | 1–5 |

---

# 💳 3. Fraud Risk Indicators

| Risk Factor | Description | Score Range |
|------------|-------------|-------------|
| **Behavioral anomalies** | Sudden pattern deviation | 1–5 |
| **Device / channel mismatch** | New device, new location | 1–5 |
| **Compromised credentials** | Known breach indicators | 1–5 |
| **High-risk merchant category** | MCC flagged for fraud | 1–5 |
| **Synthetic identity signals** | Inconsistent identity attributes | 1–5 |

---

# 🏛️ 4. Regulatory & Compliance Risk

| Risk Factor | Description | Score Range |
|------------|-------------|-------------|
| **Regulatory rule violation** | PSD2, OCC, MAS, FFIEC | 1–5 |
| **Missing audit trail** | No lineage or justification | 1–5 |
| **Explainability failure** | Model cannot justify output | 1–5 |
| **Data privacy breach** | PII leakage | 1–5 |
| **Incorrect classification** | Wrong risk category | 1–5 |

---

# 🖥️ 5. Legacy System Risk (COBOL / Assembler)

| Risk Factor | Description | Score Range |
|------------|-------------|-------------|
| **Unsupported code path** | Legacy logic not mapped | 1–5 |
| **Batch dependency risk** | Timing or ordering issues | 1–5 |
| **Data quality issues** | Missing or malformed fields | 1–5 |
| **Interface mismatch** | CICS/IMS inconsistencies | 1–5 |
| **Critical module involvement** | High-impact legacy component | 1–5 |

---

# 🧩 6. Operational Risk

| Risk Factor | Description | Score Range |
|------------|-------------|-------------|
| **System outage indicators** | Downstream system unavailable | 1–5 |
| **Duplicate transaction risk** | Repeated instructions | 1–5 |
| **Reconciliation mismatch** | Ledger vs. transaction mismatch | 1–5 |
| **Settlement failure** | RTGS/ACH settlement issues | 1–5 |
| **Exception escalation** | Multiple unresolved exceptions | 1–5 |

---

# 🧮 Composite Risk Severity Score (RSS)


