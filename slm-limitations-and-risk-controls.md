# Limitations of Banking SLMs & Risk Controls  
### Safe Deployment of Small Language Models in Regulated Financial Systems  
### Author: Neeraj Aggarwal

Small Language Models (SLMs) provide high precision, low latency, and strong regulatory alignment for banking. However, like any AI system, SLMs have limitations that must be addressed through robust risk controls. This document outlines the key limitations of Banking SLMs and the risk‑mitigation mechanisms required for safe deployment across Tier‑0/Tier‑1 financial systems.

This framework integrates directly with ERMI (risk scoring), UICS (context stitching), and UAMMF (model governance).

---

## 1. Limitations of Banking SLMs

### **1.1 Domain Narrowness**
SLMs are intentionally trained on banking‑specific corpora.  
This improves precision but limits general knowledge.

**Impact:**  
- Cannot answer broad, non‑banking questions  
- Requires fallback to enterprise LLMs for general queries

---

### **1.2 Sensitivity to Training Data Quality**
SLMs rely heavily on curated domain data.  
Any gaps or biases in training data directly affect model performance.

**Impact:**  
- Missing ISO 20022 variants → incorrect message mapping  
- Incomplete AML/KYC datasets → entity misclassification  
- Legacy documentation gaps → modernization errors

---

### **1.3 Limited Reasoning Outside Banking Ontologies**
SLMs excel within structured banking schemas but struggle with:
- Unstructured cross‑domain reasoning  
- Ambiguous queries without context  
- Non‑standard terminology

**Impact:**  
- Requires UICS for context stitching  
- Requires strict guardrails for ambiguous queries

---

### **1.4 Risk of Hallucination (Low but Non‑Zero)**
SLMs hallucinate far less than LLMs, but hallucinations can still occur.

**Impact:**  
- Incorrect regulatory interpretation  
- Wrong AML/KYC reasoning  
- Misaligned payments routing  
- Incorrect custody operations logic

**Tier‑0 Requirement:** 0% hallucination  
**Tier‑1 Requirement:** <0.5% hallucination

---

### **1.5 Determinism Challenges in Complex Queries**
SLMs are deterministic by design, but:
- Multi‑step reasoning  
- Ambiguous queries  
- Missing context  
can introduce variability.

**Impact:**  
- Requires deterministic mode for Tier‑0  
- Requires HITL for Tier‑1 regulatory decisions

---

### **1.6 Limited Generalization Across Global Banking Variants**
Banking rules differ across:
- Regions  
- Regulators  
- Payment networks  
- Custody models  

SLMs trained on U.S. banking may not generalize to:
- EU PSD2  
- UK FCA  
- APAC MAS  
- India RBI  

**Impact:**  
- Requires region‑specific SLM variants  
- Requires regulatory alignment layer

---

## 2. Risk Controls for Safe Banking SLM Deployment

### **2.1 ERMI — Enterprise Risk‑Mitigated Intelligence**
ERMI enforces:
- Multi‑source validation  
- Confidence scoring  
- Risk‑weighted output blocking  
- Regulatory rule checks  
- Sanctions/AML/KYC validation  

**Outcome:**  
High‑risk outputs are blocked before reaching the user.

---

### **2.2 UICS — Unified Intelligent Context System**
UICS prevents:
- Context drift  
- Cross‑domain contamination  
- Incorrect schema mapping  
- Misinterpretation of banking terminology  

**Outcome:**  
SLMs always operate within correct banking context.

---

### **2.3 UAMMF — Unified AI Model Management Framework**
UAMMF governs:
- Model versioning  
- Drift detection  
- Bias monitoring
