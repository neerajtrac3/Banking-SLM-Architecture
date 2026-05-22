# pacs.008 Interpretation – Mermaid Diagram

```mermaid
flowchart TD
    A[ISO 20022 pacs.008 Message] --> B[Field Extraction]
    B --> C[Semantic Mapping<br/>ISO 20022 → Ontology]
    C --> D[Risk Indicator Evaluation]
    D --> E[Composite Risk Score (RSS)]
    E --> F[Explainability Layer]
    F --> G[Decision Recommendation<br/>(Approve / Review / Block)]

