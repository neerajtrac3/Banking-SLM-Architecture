# SLM Evaluation Metrics for Banking  
### Performance, Risk, Compliance & Tier‑0/Tier‑1 Benchmarks  
### Author: Neeraj Aggarwal

Evaluating Small Language Models (SLMs) for banking requires a specialized set of metrics that go far beyond traditional AI evaluation. Banking systems demand ultra‑low latency, deterministic behavior, regulatory compliance, auditability, and zero‑tolerance for hallucinations. This document defines the evaluation metrics used to validate Banking SLMs across mission‑critical financial systems.

These metrics align with ERMI (risk scoring), UICS (context stitching), UAMMF (model governance), and Tier‑0/Tier‑1 modernization requirements.

---

## 1. Evaluation Categories

Banking SLM evaluation spans four major categories:

1. **Performance Metrics** — latency, throughput, efficiency  
2. **Accuracy & Precision Metrics** — retrieval accuracy, domain precision  
3. **Risk & Safety Metrics** — hallucination rate, compliance violations  
4. **Governance & Auditability Metrics** — lineage, reproducibility, drift  

Each category is essential for safe deployment in regulated financial environments.

---

## 2. Performance Metrics (Tier‑0/Tier‑1)

### **2.1 Latency**
- **Tier‑0 Target:** <50ms  
- **Tier‑1 Target:** <100ms  
- Required for payments, custody, liquidity, fraud detection.

### **2.2 Throughput**
- **Target:** 10,000+ transactions per second (TPS)  
- Supports high‑volume financial operations.

### **2.3 Efficiency Improvement**
- **Target:** ≥35% improvement  
- Based on modernization benchmarks (e.g., State Street).

### **2.4 Cost Reduction**
- **Target:** ≥40% reduction  
- Achieved through SLM inference optimization and GPU reduction.

---

## 3. Accuracy & Precision Metrics

### **3.1 Retrieval Accuracy**
- **Target:** >98%  
- Ensures correct retrieval of regulated documents.

### **3.2 Domain Precision**
- **Target:** >95%  
- Measures alignment with banking ontologies:
  - ISO 20022  
  - BIAN  
  - AML/KYC schemas  
  - Custody operations ontology  

### **3.3 Context Integrity (UICS)**
- **Target:** 100% context consistency  
- Prevents cross‑domain contamination (e.g., lending vs payments).

### **3.4 Deterministic Output Rate**
- **Tier‑0 Target:** 100% deterministic  
- **Tier‑1 Target:** ≥95% deterministic with HITL approval for exceptions.

---

## 4. Risk & Safety Metrics

### **4.1 Hallucination Rate**
- **Target:** <0.5%  
- **Tier‑0 Requirement:** 0%  
- Enforced through ERMI risk scoring and multi‑source validation.

### **4.2 Compliance Violation Rate**
- **Target:** 0%  
- Violations include:
  - Incorrect AML/KYC reasoning  
  - Sanctions misclassification  
  - Wrong ISO 20022 mapping  
  - Incorrect regulatory interpretation  

### **4.3 Risk‑Weighted Output Blocking**
- **Target:** 100% blocking of high‑risk outputs  
- ERMI assigns risk scores (0–1.0) and blocks outputs above threshold.

### **4.4 PII/PCI Leakage Prevention**
- **Target:** 100% masking  
- Required for PCI‑DSS, GDPR, CCPA compliance.

---

## 5. Governance & Auditability Metrics

### **5.1 Model Lineage Completeness (UAMMF)**
- **Target:** 100% lineage tracking  
- Includes:
  - Model version  
  - Training dataset  
  - Retrieval sources  
  - Risk scores  
  - Compliance checks  

### **5.2 Reproducibility**
- **Target:** 100% reproducible outputs  
- Required for OCC/FFIEC audits.

### **5.3 Drift Detection**
- **Target:** Drift detected within 24 hours  
- Prevents degradation in regulated environments.

### **5.4 Audit Log Completeness**
- **Target:** 100% logging of:
  - Inputs  
  - Outputs  
  - Retrieval sources  
  - Risk scores  
  - Compliance checks  
  - Human approvals  

---

## 6. Banking‑Specific Evaluation Tests

### **6.1 ISO 20022 Alignment Test**
- Validates message structure mapping  
- Required for payments modernization

### **6.2 AML/KYC Entity Graph Test**
- Ensures correct entity linking  
- Prevents false positives/negatives

### **6.3 Sanctions Screening Test**
- Zero‑tolerance for misclassification  
- High‑risk regulatory domain

### **6.4 Custody Operations Test**
- Validates settlement, reconciliation, and asset servicing logic

### **6.5 Lending & Credit Risk Test**
- Ensures deterministic reasoning in lending workflows

---

## 7. Tier‑0/Tier‑1 Evaluation Matrix

| Metric | Tier‑0 Requirement | Tier‑1 Requirement |
|--------|--------------------|--------------------|
| Latency | <50ms | <100ms |
| Determinism | 100% | ≥95% |
| Hallucination | 0% | <0.5% |
| Retrieval Accuracy | >98% | >95% |
| Compliance Violations | 0% | 0% |
| Audit Logging | 100% | 100% |
| Risk Scoring | Mandatory | Mandatory |
| HITL | Optional | Required for high‑risk |

---

## 8. Evaluation Evidence from Real Modernization Programs

### **State Street — Tier‑0 Modernization**
- 40% cost reduction  
- 35% efficiency improvement  
- Deterministic SLM retrieval for critical systems  
- Zero service disruption  

### **Citizens Bank — Lending Modernization**
- SLM used for dependency mapping  
- Improved processing speed by 30%  
- Ensured safe modernization of 94 applications  

### **RBS, NAB, Thomson Reuters**
- SLM evaluation used for Assembler modernization  
- Ensured safe migration of legacy systems  
- Reduced risk in regulatory separation programs  

---

## 9. Summary

Banking SLM evaluation requires:

- Ultra‑low latency  
- High throughput  
- High domain precision  
- Zero hallucinations  
- Full regulatory compliance  
- Complete auditability  
- Deterministic behavior for Tier‑0/Tier‑1  
- Integration with ERMI, UICS, UAMMF  

These metrics ensure Banking SLMs operate safely and reliably across mission‑critical financial systems.

---

