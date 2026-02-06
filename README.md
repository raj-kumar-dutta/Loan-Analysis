# 📊 Financial Loan Analysis – Power BI Dashboard

## 📌 Project Overview
This project presents a **Financial Loan Analysis Dashboard** built using **Microsoft Power BI**.  
The dashboard analyzes loan data to understand customer distribution, income levels, loan performance, interest rate trends, and repayment status through interactive visualizations.

The report contains **two dashboard pages**:
1. **Overview Dashboard** – high-level summary of loan data  
2. **Detailed Analysis Dashboard** – in-depth financial and categorical analysis  

---

## 🗂️ Dataset Information
- **Dataset Type:** Financial / Loan Dataset  
- **File Format:** Excel (.xlsx)  
- **Total Records:** 38,576  
- **Total Fields:** 24  

### 📋 Dataset Columns
id, member_id, address_state, application_type, emp_length, emp_title, grade, sub_grade, home_ownership, purpose, term, verification_status, issue_date, last_credit_pull_date, last_payment_date, next_payment_date, loan_status, annual_income, loan_amount, installment, int_rate, dti, total_acc, total_payment

---

## 🗂️ Project Structure

├── Financial_Loan_Analysis.pbix

├── loan_dataset.xlsx

├── README.md

├── screenshots/

│ ├── dashboard_page1_overview.png

│ └── dashboard_page2_analysis.png

---


---

## 🛠️ Tools & Technologies
- Microsoft Power BI Desktop  
- Power Query (Data Cleaning & Transformation)  
- DAX (Data Analysis Expressions)  
- Excel Dataset  

---

## 🚀 How to Run the Project

### Step 1: Install Power BI
Download and install **Microsoft Power BI Desktop** from the official Microsoft website.

### Step 2: Open the Report
1. Open Power BI Desktop  
2. Click **File → Open**  
3. Select `Financial_Loan_Analysis.pbix`

### Step 3: Refresh the Data
1. Click **Home → Refresh**  
2. If prompted, update the dataset path to `loan_dataset.xlsx`  
3. Apply changes

---

## 🧹 Data Cleaning & Preparation
Data preparation was performed using **Power Query**, including:
- Removing missing and duplicate values  
- Converting date columns to proper date format  
- Correcting numeric data types (income, loan amount, interest rate)  
- Standardizing categorical fields  

---

## 📐 Data Modeling & DAX
- Single-table data model  
- Calculated measures created using DAX  

### 📊 Sample DAX Measures
```DAX
Total Members = COUNT(Loans[id])
Total Loan Amount = SUM(Loans[loan_amount])
Good Loan Amount = CALCULATE(SUM(Loans[loan_amount]), Loans[loan_status] = "Fully Paid")
Bad Loan Amount = CALCULATE(SUM(Loans[loan_amount]), Loans[loan_status] = "Charged Off")
Average Annual Income = AVERAGE(Loans[annual_income])
Average Interest Rate = AVERAGE(Loans[int_rate])
```
---

## 📊 Dashboard Features

### Page 1 – Overview Dashboard
- Total Members  
- Max, Min, and Average Annual Income  
- Month-wise Loan Issues  
- Interest Rate (Top Months)  
- Good vs Bad Loan Distribution  
- Home Ownership Analysis  
- Loan Status Summary  

---

### Page 2 – Detailed Analysis Dashboard
- Total Loan Amount  
- Good Loan vs Bad Loan (Amount)  
- Verification Status Distribution  
- Purpose-wise Loan Issues  
- Loan Term Analysis (36 vs 60 months)  
- Interest Rate by Quarter  

---

## 📸 Screenshots

### 📊 Dashboard Page 1 – Overview
This page provides a high-level summary of loan members, income statistics, loan distribution, and overall loan performance.

![Dashboard Page 1 – Overview](screenshots/dashboard_page1_overview.png)

---

### 📈 Dashboard Page 2 – Detailed Analysis
This page focuses on detailed financial insights, loan purpose analysis, verification status, loan terms, and quarterly interest rate trends.

![Dashboard Page 2 – Detailed Analysis](screenshots/dashboard_page2_analysis.png)

---

## 🔍 Key Insights
- Majority of loans are good loans with successful repayment  
- Debt consolidation is the most common loan purpose  
- Most customers prefer 36-month loan terms  
- Interest rates peak in later quarters  
- Verified customers show stronger repayment patterns  

---

## 📤 Export Options
- Export report as PDF  
- Export report as PowerPoint  
- Publish to Power BI Service (optional)  

---

## 🔮 Future Enhancements
- Add loan default risk prediction  
- Create drill-through analysis pages  
- Improve dashboard UI with custom themes  
- Integrate real-time financial data  

---

## 👤 Author
**Name:** Raj Kumar Dutta  
**Project Type:** Power BI Data Analytics  
**Purpose:** Academic / Learning / Portfolio Project  

