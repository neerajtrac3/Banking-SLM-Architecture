# ISO 20022 Use Case – pacs.009 AML/KYC Evaluation

## 📨 Input ISO 20022 Message (Simplified pacs.009)

<FIToFICstmrDrctDbt>
  <GrpHdr>
    <MsgId>BNK-4455-XYZ</MsgId>
    <CreDtTm>2025-05-02T09:00:00Z</CreDtTm>
  </GrpHdr>

  <DrctDbtTxInf>
    <PmtId>
      <InstrId>DD-998877</InstrId>
      <EndToEndId>E2E-778899</EndToEndId>
    </PmtId>

    <InstdAmt Ccy="EUR">9800</InstdAmt>

    <Dbtr>
      <Nm>Alpha Holdings Ltd</Nm>
      <CtctDtls>
        <Email>info@alpha-hold.com</Email>
      </CtctDtls>
    </Dbtr>

    <DbtrAcct>
      <Id><IBAN>CY550011223344556677</IBAN></Id>
    </DbtrAcct>

    <CdtrAgt>
      <FinInstnId>
        <BIC>DEUTDEFFXXX</BIC>
      </FinInstnId>
    </CdtrAgt>
  </DrctDbtTxInf>
</FIToFICstmrDrctDbt>

---

## 🧠 BankingSLM Reasoning Output

### **1. Transaction Summary**
- **Type:** FI‑to‑FI Direct Debit (pacs.009)
- **Amount:** EUR 9,800  
- **Debtor:** Alpha Holdings Ltd (Cyprus)  
- **Creditor Agent:** Deutsche Bank (Germany)  

---

## **2. AML/KYC Interpretation**
- Debtor jurisdiction: **Cyprus** (medium‑risk AML jurisdiction)  
- Corporate structure: “Holdings Ltd” → flagged for enhanced due diligence  
- Email domain mismatch:  
  - Company name: *Alpha Holdings Ltd*  
  - Email domain: *alpha-hold.com*  
  → **Potential synthetic identity signal**  

---

## **3. Risk Indicators (from Risk Matrix)**

| Indicator | Value | Score |
|----------|--------|-------|
| Jurisdiction risk | Cyprus | **3** |
| Beneficial owner complexity | “Holdings Ltd” | **4** |
| Synthetic identity signals | Email mismatch | **4** |
| Sanctions match | None | **1** |
| Unusual amount | No | **1** |

---

## **4. Composite Risk Severity Score (RSS)**


