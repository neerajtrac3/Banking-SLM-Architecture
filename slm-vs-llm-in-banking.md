# SLM vs LLM in Banking  
### Why Small Language Models Are Superior for Regulated Financial Systems  
### Author: Neeraj Aggarwal

Large Language Models (LLMs) are powerful general-purpose systems, but they are not designed for the strict regulatory, latency, auditability, and determinism requirements of banking. Small Language Models (SLMs), when built with domain-specific vocabularies, ontologies, and banking schemas, outperform LLMs across every dimension that matters in financial services.

This document explains the differences between SLMs and LLMs in banking, and why Banking SLMs — such as the one co-developed under Infosys Topaz with NVIDIA and Sarvam AI — are the correct architectural choice for Tier‑0/Tier‑1 modernization.

---

## 1. Fundamental Differences Between SLMs and LLMs

### LLMs
- Trained on trillions of tokens of general-purpose data  
- Broad knowledge but low domain precision  
- High hallucination risk  
- High compute cost  
- Slow inference  
- Hard to govern and audit  
- Not aligned with banking schemas (ISO 20022, BIAN, AML/KYC)

### SLMs
- Trained on curated banking-specific corpora  
- High domain precision  
- Low hallucination rate  
- Fast inference suitable for Tier‑0/Tier‑1  
- Lower compute cost  
- Easy to govern under UAMMF  
- Natively aligned with banking ontologies and regulatory constraints  

---

## 2. Why LLMs Are Problematic in Banking

### 2.1 High Hallucination Risk
LLMs generate plausible but incorrect answers — unacceptable in:
- AML/KYC decisions  
- Sanctions screening  
- Credit risk scoring  
- Payments routing  
- Custody operations  
- Regulatory reporting  

### 2.2 Lack of Determinism
Tier‑0 systems require deterministic outputs.  
LLMs are probabilistic → unpredictable → unsafe.

### 2.3 Regulatory Misalignment
LLMs do not natively understand:
- ISO 20022 message structures  
- BIAN service domains  
- Basel III risk-weighting  
- OCC/FFIEC compliance rules  
- SOX auditability requirements  

### 2.4 High Compute Cost
LLMs require:
- Large GPU clusters  
- High inference cost  
- High latency  
- Complex governance  

This contradicts modernization goals (e.g., 40% cost reduction at State Street).

---

## 3. Why SLMs Are Ideal for Banking

### 3.1 Domain-Specific Vocabulary
SLMs use banking-specific tokenization:
- Payments  
- Custody  
- Liquidity  
- Lending  
- AML/KYC  
- Treasury  
- Regulatory reporting  

This increases precision and reduces hallucinations.

### 3.2 Deterministic Behavior for Tier‑0/Tier‑1
SLMs can operate in:
- Retrieval-only mode  
- Deterministic generation mode  
- Strict guardrail mode  

This aligns with mission-critical systems.

### 3.3 Ultra-Low Latency
SLMs deliver:
- <50ms inference for Tier‑0  
- <100ms for Tier‑1  
- High throughput (10K TPS)  

Essential for:
- Payments  
- Real-time fraud detection  
- Market data pipelines  

### 3.4 Lower Compute Cost
SLMs reduce:
- GPU usage  
- Cloud cost  
- Operational overhead  

Matches modernization metrics:
- **40% cost reduction**  
- **35% efficiency improvement**  

### 3.5 Native Regulatory Alignment
SLMs can be trained on:
- ISO 20022 schemas  
- BIAN service domains  
- AML/KYC ontologies  
- OCC/FFIEC rules  
- SOX audit requirements  

This ensures compliance-by-design.

---

## 4. SLM vs LLM: Banking-Specific Comparison Table

| Dimension | LLM | SLM |
|----------|-----|-----|
| **Domain Precision** | Medium | **High** |
| **Hallucination Risk** | High | **Low** |
| **Latency** | High | **Low (<50ms)** |
| **Compute Cost** | High | **Low** |
| **Regulatory Alignment** | Weak | **Strong** |
| **Auditability** | Difficult | **Easy (UAMMF)** |
| **Determinism** | Low | **High** |
| **Suitability for Tier‑0/Tier‑1** | Poor | **Excellent** |

---

## 5. How Banking SLMs Integrate with Modernization Frameworks

### ERMI — Enterprise Risk‑Mitigated Intelligence
- Risk scoring  
- Multi-source validation  
- Regulatory compliance enforcement  

### UICS — Unified Intelligent Context System
- Context stitching across payments, custody, lending  
- ISO 20022 + BIAN normalization  

### UAMMF — Unified AI Model Management Framework
- Model lineage  
- Drift detection  
- Auditability  
- Governance  

SLMs integrate seamlessly with these frameworks.  
LLMs do not.

---

## 6. SLM Advantages in Real Banking Modernization Programs

### State Street (Tier‑0 Modernization)
- 50+ mission-critical components modernized  
- 40% cost reduction  
- 35% efficiency improvement  
- SLMs used for deterministic retrieval and modernization governance  

### Citizens Bank (Lending Modernization)
- 94 applications modernized  
- SLMs used for dependency mapping and documentation intelligence  

### RBS, NAB, Thomson Reuters
- SLMs used for Assembler modernization  
- Legacy code analysis  
- Regulatory separation support  

---

## 7. Summary

SLMs are the correct architectural choice for banking because they provide:

- High precision  
- Low hallucination  
- Deterministic behavior  
- Regulatory alignment  
- Ultra-low latency  
- Lower cost  
- Full auditability  
- Seamless integration with ERMI, UICS, UAMMF  

LLMs are powerful, but they are **not suitable for mission-critical, regulated financial systems**.

Banking SLMs — purpose-built, domain-trained, and modernization-aligned — are the future of AI in financial services.

---

