# Insurance Analysis – Power BI Report

A Power BI dashboard for analysing insurance policy and claims data, providing interactive visibility into claim statuses, premium performance, coverage distribution, and customer demographics.

---

## 📊 Report Overview

| Property | Detail |
|---|---|
| File | `insurance_analysis.pbix` |
| Tool | Microsoft Power BI Desktop |
| Pages | 2 |
| Data Source | `InsuranceData` (embedded data model) |

---

## 📁 Report Pages

### Page 1 – Executive Dashboard

The main interactive overview with slicers and KPI cards.

**Slicers (Filters)**
- Policy Number
- Claim Number
- Customer ID

**KPI Cards**
- Total Claim Amount
- Total Coverage Amount
- Total Premium Amount

**Visuals**
| Visual | Description |
|---|---|
| Ribbon Chart | Claim count by Claim Status over time/category |
| Bar Chart | Total Premium Amount by Policy Type |
| Line Chart | Total Claim Amount by Age Group |
| Donut Chart | Active vs Inactive Policies breakdown |
| Pivot Table | Coverage Amount by Policy Type × Claim Status |
| Multi-Row Card | Customer count by Gender |

---

### Page 2 – Detailed Data Table

A full drill-through table showing all individual records with the following columns:

`PolicyNumber` · `CustomerID` · `ClaimNumber` · `Age` · `Gender` · `CoverageAmount` · `PolicyType` · `ClaimAmount` · `PolicyStartDate` · `PolicyEndDate` · `ClaimStatus` · `ClaimDate` · `AgeGroup` · `Active/Inactive` · `PremiumAmount`

---

## 🗂️ Data Model

**Table:** `InsuranceData`

| Field | Type | Description |
|---|---|---|
| PolicyNumber | Text | Unique policy identifier |
| CustomerID | Text | Unique customer identifier |
| ClaimNumber | Text | Unique claim identifier |
| Age | Numeric | Customer age |
| Age group | Text | Derived age band (e.g., 18–30, 31–45) |
| Gender | Text | Customer gender |
| PolicyType | Text | Type of insurance policy |
| CoverageAmount | Numeric | Total coverage value of the policy |
| PremiumAmount | Numeric | Premium paid by the customer |
| ClaimAmount | Numeric | Amount claimed |
| ClaimStatus | Text | Status of the claim (e.g., Approved, Pending, Rejected) |
| ClaimDate | Date | Date the claim was filed |
| PolicyStartDate | Date | Policy commencement date |
| PolicyEndDate | Date | Policy expiry date |
| active/inactive | Text | Whether the policy is currently active |

---

## 🚀 Getting Started

### Prerequisites

- [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (latest version recommended)

### Opening the Report

1. Clone or download this repository.
2. Open **Power BI Desktop**.
3. Go to **File → Open report** and select `insurance_analysis.pbix`.
4. The report will load with the embedded data model — no additional data connection is required.

---

## 🔄 Refreshing / Updating Data

If you replace the embedded data with a live source:

1. Go to **Home → Transform data** to open Power Query Editor.
2. Update the data source connection under **Home → Data source settings**.
3. Click **Refresh** to reload data.

---

## 📌 Notes

- The data model is embedded directly within the `.pbix` file.
- A custom theme (`Custom_Theme`) and the Microsoft base theme (`CY25SU12`) are applied for consistent styling.
- All slicers on Page 1 are cross-filtering — selecting a Policy Number, Claim Number, or Customer ID will filter all visuals accordingly.

---


