# Prompt Flow – ISO 20022 Interpretation

## Objective
Interpret ISO 20022 messages with deterministic, explainable outputs.

## Input Example
<FIToFICstmrCdtTrf>
<GrpHdr>...</GrpHdr>
<CdtTrfTxInf>...</CdtTrfTxInf>
</FIToFICstmrCdtTrf>


## Expected Output
- Transaction type
- Mandatory field validation
- Risk indicators
- Missing regulatory fields
- Explainable reasoning

## Guardrails
- No hallucinated fields
- No fabricated regulatory text
- Deterministic output

