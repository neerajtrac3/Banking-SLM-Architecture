# BankingSLM Architecture

BankingSLM is a domain‑specific Small Language Model designed for regulated financial services environments. The model supports secure, compliant, and context‑aware AI capabilities across lending, payments, risk, compliance, and operations. This repository documents the architecture, design components, evaluation framework, and governance model used to operationalize BankingSLM at enterprise scale.


This repository documents the reference architecture, evaluation approach, and use cases for a domain-specific Small Language Model (SLM) for banking.

## Objectives

- Define an architecture for banking-focused SLMs
- Describe data, tokenization, and domain adaptation strategies
- Provide evaluation frameworks for accuracy, safety, and compliance
- Capture prompt flows and use cases across KYC, AML, and lending

## Repository structure

- `architecture/` – SLM architecture, data strategy, and diagrams
- `model-cards/` – Model documentation, risks, and limitations
- `evaluation/` – Test design, metrics, and reporting
- `prompt-flows/` – Task-specific prompt designs
- `use-cases/` – Applied banking scenarios

## Target audience

- AI and ML architects  
- Banking platform and risk teams  
- Compliance and model governance stakeholders

---

## Architecture Overview

```mermaid
flowchart LR
    subgraph DataSources[Banking Data Sources]
        Pol[Policies & Procedures]
        Reg[Regulatory Texts]
        Prod[Product Docs]
        Tickets[Service Tickets]
        Logs[Ops & Audit Logs]
    end

    DataSources --> Prep[Data Curation & Preprocessing]
    Prep --> Anon[PII Redaction & Anonymization]
    Anon --> DS[Domain-Specific Corpus]

    DS --> Train[SLM Training & Fine-Tuning]
    Train --> BankingSLM[(BankingSLM)]

    subgraph RAG[RAG Layer]
        VS[Vector Store]
        Retriever[Retriever]
    end

    DS --> VS
    UserQ[User Query] --> Orchestrator[Orchestration Layer]
    Orchestrator --> Retriever
    Retriever --> VS
    Retriever --> Context[Context Packager]

    Context --> PF[Prompt Flow]
    BankingSLM --> PF
    PF --> Resp[Response & Post-Processing]

    subgraph Governance[Governance & Controls]
        Eval[Evaluation & Metrics]
        Guard[Guardrails & Policies]
        Audit[Audit & Logging]
    end

    PF --> Eval
    PF --> Guard
    PF --> Audit
