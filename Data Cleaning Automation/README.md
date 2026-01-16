# Data Cleaning Automation using n8n & Google Sheets

This project demonstrates a **batch-based data cleaning automation** built using **n8n** and **Google Sheets**.  
It focuses on handling **real-world spreadsheet issues** such as inconsistent formats, missing values, and unstandardized text.

The goal of this project is to understand **automation workflow design** and **data preprocessing**, not to build a fully production-ready pipeline.

---

## 📌 Project Overview

The workflow reads raw data from a Google Sheet, applies JavaScript-based data cleaning logic in n8n, and writes the cleaned data to a separate Google Sheet.

This project simulates common data issues that occur in practice rather than working with ideal or perfectly formatted data.

---

## 🔄 Workflow Architecture

Google Sheets (Raw Data)
↓
Google Sheets (Get Rows)
↓
n8n – JavaScript Data Cleaning
↓
Google Sheets (Cleaned Data)
---

## 🧹 Data Cleaning Logic Implemented

The following cleaning steps are implemented inside the **Code (JavaScript)** node in n8n:

### ✅ Name Normalization
- Trims extra spaces
- Converts names to consistent casing

### ✅ Date Standardization
- Handles mixed date formats (`/` and `-`)
- Standardizes output format for consistency

### ✅ Missing Value Handling
- Replaces empty or missing sales values with `0`

### ✅ City Normalization
- Converts shorthand and inconsistent values into standard city names

---

## 📷 Screenshots

### 🟡 Raw Data
The original dataset containing mixed date formats, missing values, and inconsistent text.

![Raw Data](screenshots/raw-data.png)

---

### 🟢 Cleaned Data
The output after applying the data cleaning logic using n8n and JavaScript.

![Cleaned Data](screenshots/cleaned-data.png)

---

### 🔵 n8n Workflow
The automation workflow used to read, clean, and write the data.

![Workflow](screenshots/workflow.png)

---

## ⚠️ Current Limitations

This project intentionally focuses on **core cleaning logic**.  
The following features are **not yet implemented**:

- Automatic deduplication
- Incremental row processing
- Advanced data validation rules
- State management across executions

Each workflow execution currently processes all rows in batch mode.

---

## 🔮 Planned Improvements

Future enhancements planned for this project include:

- Adding deduplication logic
- Incremental processing of newly added rows
- Python-based cleaning using pandas
- Integration with BI tools such as Power BI or Tableau
- Improved validation and error handling

---

## 🛠 Tools & Technologies Used

- **n8n** – Workflow automation
- **Google Sheets** – Data source and destination
- **JavaScript** – Data transformation logic

---

## 🎯 Learning Outcomes

Through this project, I gained hands-on experience with:

- Designing batch-based automation workflows
- Handling real-world data inconsistencies
- Understanding Google Sheets date handling
- Writing JavaScript transformations in n8n
- Recognizing the importance of state and idempotency in data pipelines

---

## 📁 Repository Structure

