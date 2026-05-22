# ISO 20022 Use Case – pacs.008 Interpretation

## 📨 Input ISO 20022 Message (Simplified pacs.008)

<FIToFICstmrCdtTrf>
  <GrpHdr>
    <MsgId>ABC-REF-9981</MsgId>
    <CreDtTm>2025-04-12T10:15:00Z</CreDtTm>
    <NbOfTxs>1</NbOfTxs>
  </GrpHdr>

  <CdtTrfTxInf>
    <PmtId>
      <EndToEndId>E2E-445522</EndToEndId>
    </PmtId>

    <IntrBkSttlmAmt Ccy="USD">15000</IntrBkSttlmAmt>
    <IntrBkSttlmDt>2025-04-12</IntrBkSttlmDt>

    <Dbtr>
      <Nm>John Carter</Nm>
    </Dbtr>
    <DbtrAcct>
      <Id><IBAN>US123456789000111222</IBAN></Id>
    </DbtrAcct>

    <Cdtr>
      <Nm>Global Trade LLC</Nm>
    </Cdtr>
    <CdtrAcct>
      <Id><IBAN>AE009988776655443322</IBAN></Id>
    </CdtrAcct>

    <RmtInf>
      <Ustrd>Invoice 5541</Ustrd>
    </RmtInf>
  </CdtTrfTxInf>
</FIToFICstmrCdtTrf>

---

## 🧠 BankingSLM Reasoning Output

### **1. Transaction Summary**
- **Type:** Customer Credit Transfer (pacs.008)
- **Amount:** USD 15,000  
- **Debtor:** John Carter (US)  
- **Creditor:** Global Trade LLC (UAE)  
- **Purpose:** Invoice Payment  
- **Settlement Date:** 2025‑04‑12  

---

## **2. Semantic Interpretation**
- Debtor and creditor accounts extracted via ISO 20022 semantic mapping  
- Payment classified as **cross‑border B2B transfer**  
- Purpose code inferred from unstructured remittance text (“Invoice 5541”)  
- No regulatory reporting fields present  

---

## **3. Risk Indicators (from Risk Matrix)**
| Indicator | Value | Score |
|----------|--------|-------|
| High‑risk jurisdiction | UAE | **4** |
| Unusual amount | Above customer’s historical average | **3** |
| Missing regulatory fields | `<RegulatoryReporting>` absent | **4** |
| Counterparty mismatch | None detected | **1** |
| Purpose code inconsistency | Not applicable | **1** |

---

## **4. Composite Risk Severity Score (RSS)**


