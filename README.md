# 📊 Record-to-Report (R2R) — Month-End/Year-End Financial Close

### KIIT University | SAP Project 

---

## 🔍 Overview

This repository contains the complete **Record-to-Report (R2R)** project. The R2R cycle is an end-to-end business process in **SAP FI (Financial Accounting)** that covers every step from posting daily journal entries to locking the books at month-end and generating financial statements.

**Fictitious Company:** TechNova Manufacturing Pvt. Ltd.  
**Module:** SAP FI — Financial Accounting + SAP Business Data Cloud  
**SAP Functional Areas:** FI + CO + SAP BDC Analytics

---

## 📁 Repository Contents

| File | Description |
| --- | --- |
| `SAP_R2R_DataAnalytics.ipynb` | ✅ Full Python simulation — runs in Google Colab |
| `Project_Documentation.docx` | 📄 Complete project report with customisation steps |
| `README.md` | 📖 This file |

---

## 🔄 R2R Process Flow

```
Company & CoA Setup (OX02 / OB13)
        ↓
GL Master Data Creation (FS00)  ←── 20 GL Accounts | Chart of Accounts TNCA
        ↓
Journal Entry Postings — March 2026 (FB50)  ←── 13 Documents Posted
        ↓
Month-End Accruals (FBS1)  ←── Salary Accrual + Deferrals
        ↓
Depreciation Run (AFAB)  ←── Plant & Machinery ↓ | Accum. Depn ↑
        ↓
Open Item Clearing (F-44 / F-32)  ←── AP Cleared | AR Cleared
        ↓
Financial Statements (S_ALR_87012284)  ←── P&L ✅ | Balance Sheet ✅
        ↓
Lock Posting Period (OB52)  ←── March 2026 LOCKED 🔒
        ↓
SAP BDC Analytics  ←── KPIs | Dashboards | Trend Analysis
        ✅ R2R Complete
```

---

## 💻 How to Run in Google Colab

### Option A — Upload & Execute

1. Open [Google Colab](https://colab.research.google.com)
2. Click **File → Upload notebook**
3. Select `SAP_R2R_DataAnalytics.ipynb`
4. Click **Runtime → Run all**

### Option B — Copy & Paste

1. Open `SAP_R2R_DataAnalytics.ipynb` on GitHub
2. Copy each cell's code
3. Paste into a new Colab notebook cell by cell
4. Add `!pip install tabulate matplotlib pandas` as the first line
5. Run all cells

---

## 🗂️ What the Simulation Does

| Section | Feature | SAP Equivalent |
| --- | --- | --- |
| 1 | Company Code + 20 GL Accounts Setup | OX02, OB13, FS00 |
| 2 | Display Full Chart of Accounts TNCA | FS00 — Display |
| 3 | Post 13 Journal Entries — March 2026 | FB50 — Enter GL Document |
| 4 | Month-End Closing Checklist + Period Lock | FBS1, AFAB, OB52 |
| 5 | P&L Statement + Balance Sheet | S_ALR_87012284 |
| 6 | Trial Balance + Document Flow Summary | S_ALR_87012277, FB03 |
| 7 | SAP BDC Pipeline + KPIs + Q4 Trend | C_BCBDC Analytics |
| 8 | 4-Panel Visual Dashboard (saved as PNG) | SAP Analytics Cloud |
| 9 | Final R2R Summary | Project Completion |

---

## 📊 Sample Output

```
══════════════════════════════════════════════════════════════════════
  SECTION 6B: DOCUMENT FLOW SUMMARY  [T-Code: FB03]
══════════════════════════════════════════════════════════════════════

╒════╤════════════╤══════════════════════════════════════╤══════╤══════╤══════════════╤══════════════╤══════════════╕
│  # │ Date       │ Description                          │ Dr   │ Cr   │ Amount       │ Doc No       │ Status       │
╞════╪════════════╪══════════════════════════════════════╪══════╪══════╪══════════════╪══════════════╪══════════════╡
│  1 │ 01.03.2026 │ Opening cash — Share Capital         │ 1000 │ 4000 │ ₹5,00,000    │ 1000000001   │ Posted ✅    │
│  2 │ 02.03.2026 │ Cash deposited to HDFC bank          │ 1001 │ 1000 │ ₹4,00,000    │ 1000000002   │ Posted ✅    │
│  3 │ 05.03.2026 │ Raw material purchased on credit     │ 1200 │ 3000 │ ₹1,50,000    │ 1000000003   │ Posted ✅    │
│  4 │ 08.03.2026 │ Sales invoice raised to customer     │ 1100 │ 5000 │ ₹3,00,000    │ 1000000004   │ Posted ✅    │
│  5 │ 10.03.2026 │ COGS — goods transferred to sales    │ 6000 │ 1200 │ ₹80,000      │ 1000000005   │ Posted ✅    │
│  6 │ 15.03.2026 │ March salary payment                 │ 7000 │ 1001 │ ₹75,000      │ 1000000006   │ Posted ✅    │
│  7 │ 18.03.2026 │ March office rent payment            │ 7100 │ 1001 │ ₹25,000      │ 1000000007   │ Posted ✅    │
│  8 │ 20.03.2026 │ Electricity bill accrued             │ 7200 │ 3000 │ ₹12,000      │ 1000000008   │ Posted ✅    │
│  9 │ 22.03.2026 │ Customer payment received            │ 1001 │ 1100 │ ₹2,50,000    │ 1000000009   │ Posted ✅    │
│ 10 │ 28.03.2026 │ Vendor payment — AP clearing         │ 3000 │ 1001 │ ₹1,00,000    │ 1000000010   │ Posted ✅    │
│ 11 │ 31.03.2026 │ Month-end: Depreciation              │ 7300 │ 2100 │ ₹5,000       │ 1000000011   │ Posted ✅    │
│ 12 │ 31.03.2026 │ Month-end: Office supplies           │ 7400 │ 1001 │ ₹3,500       │ 1000000012   │ Posted ✅    │
│ 13 │ 31.03.2026 │ Month-end: Salary accrual balance    │ 7000 │ 3000 │ ₹10,000      │ 1000000013   │ Posted ✅    │
╘════╧════════════╧══════════════════════════════════════╧══════╧══════╧══════════════╧══════════════╧══════════════╛

  Total Documents Posted: 13
```

---

## 🏢 Organisational Setup

| SAP Element | Value | Description |
| --- | --- | --- |
| Company Code | TN01 | TechNova Manufacturing India |
| Chart of Accounts | TNCA | TechNova Chart of Accounts |
| Currency | INR | Indian Rupee |
| Fiscal Year Variant | V6 | April – March (Indian FY) |
| Posting Period | 12 / 2026 | March 2026 |
| GL Accounts | 20 | Assets, Liabilities, Equity, Revenue, Expense |
| Certification Track | C_BCBDC | SAP Business Data Cloud Associate |

---

## 💰 Financial Summary — March 2026

| Description | Amount (INR) |
| --- | --- |
| Sales Revenue (500000) | ₹3,00,000 |
| Cost of Goods Sold | -₹80,000 |
| **Gross Profit** | **₹2,20,000** |
| Salaries & Wages | -₹85,000 |
| Rent Expense | -₹25,000 |
| Electricity & Utilities | -₹12,000 |
| Depreciation | -₹5,000 |
| Office Supplies | -₹3,500 |
| **Net Profit** | **₹89,500** |
| Total Assets | ₹6,61,500 |
| Balance Sheet | ✅ Balanced |

---

## 📈 SAP BDC KPIs — Business Data Cloud Analytics

| KPI | Value | Target | Status |
| --- | --- | --- | --- |
| Gross Margin % | 73.3% | > 60% | ✅ Healthy |
| Net Profit Margin % | 29.8% | > 15% | ✅ Healthy |
| Operating Expense Ratio | 43.5% | < 50% | ✅ On Target |
| Days Sales Outstanding | ~5 days | < 30 days | ✅ Excellent |
| Days Payable Outstanding | ~14 days | > 15 days | ✅ Within Terms |

---

## 🛠️ Key SAP Transaction Codes

| T-Code | Description | Phase |
| --- | --- | --- |
| OX02 | Define Company Code | Setup |
| OB13 | Create Chart of Accounts | Setup |
| FS00 | Create GL Account Master | Master Data |
| FB50 | Enter GL Account Document | Transaction Posting |
| FBS1 | Post Accrual / Deferral Entry | Month-End Close |
| AFAB | Run Depreciation | Month-End Close |
| F-44 | Clear Vendor Open Items | Month-End Close |
| F-32 | Clear Customer Open Items | Month-End Close |
| OB52 | Lock / Open Posting Period | Month-End Close |
| S_ALR_87012284 | Financial Statements (P&L + BS) | Reporting |
| S_ALR_87012277 | Trial Balance | Reporting |
| FBL3N | GL Account Line Items | Reporting |
| FB03 | Display Posted Document | Verification |

---

## 📚 References

* SAP Help Portal: [help.sap.com](https://help.sap.com)
* KIIT SAP Project Work Guidance Document
* C_BCBDC Certification Guide — SAP Business Data Cloud Associate
* SAP Community: [community.sap.com](https://community.sap.com)


---



