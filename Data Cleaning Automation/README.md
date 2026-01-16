# Data Cleaning Automation using n8n & Google Sheets

This project demonstrates a **batch-based data cleaning automation** built using **n8n** and **Google Sheets**.  
The goal is to simulate real-world spreadsheet cleaning scenarios with inconsistent formats and missing values.

---

## 📌 Project Overview

The workflow reads raw data from a Google Sheet, applies JavaScript-based cleaning logic in n8n, and writes the cleaned data to a separate sheet.

This project focuses on **core data preprocessing**, not advanced analytics.

---

## 🔄 Workflow Architecture

Google Sheets (Raw Data)  
→ n8n (Get Rows)  
→ JavaScript Data Cleaning  
→ Google Sheets (Cleaned Data)

---

## 🧹 Data Cleaning Logic Implemented

- **Name normalization**
  - Converts names to consistent casing

- **Date formatting**
  - Handles mixed formats (`/` and `-`)
  - Standardizes output format

- **Sales cleanup**
  - Replaces missing or empty values with `0`

- **City normalization**
  - Maps shorthand and inconsistent values to standard city names

---

## 📷 Screenshots

- Raw data sheet
- Cleaned data output
- n8n workflow configuration

(See `/screenshots` folder)

---

## ⚠️ Current Limitations

- Does not yet handle:
  - Automatic deduplication
  - Incremental row processing
  - Advanced validation rules
- Workflow is batch-based and reprocesses all rows on execution

These limitations are intentional and documented as part of the learning process.

---

## 🔮 Planned Improvements

- Add deduplication logic
- Integrate Python-based cleaning using pandas
- Support incremental updates
- Prepare data for BI tools like Power BI / Tableau

---

## 🛠 Tools Used

- n8n
- Google Sheets
- JavaScript

---

## 🎯 Learning Outcome

This project helped me understand:
- Real-world data inconsistencies
- Automation workflow design

- Limitations of low-code tools
- Importance of state management in data pipelines
