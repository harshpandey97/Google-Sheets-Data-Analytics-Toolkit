# 🛠️ Data Tools in Google Sheets

<p align="center">

<img src="https://img.shields.io/badge/Google%20Sheets-Data%20Tools-34A853?style=for-the-badge&logo=googlesheets&logoColor=white"/>

<img src="https://img.shields.io/badge/Module-Data%20Preparation-blue?style=for-the-badge"/>

<img src="https://img.shields.io/badge/Level-Beginner%20→%20Intermediate-success?style=for-the-badge"/>

<img src="https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge"/>

</p>

---

# 📚 Table of Contents

- 📖 Introduction
- 🎯 Learning Objectives
- 🛠️ Data Tools Overview
- 📊 Practice Dataset
- ✅ Remove Duplicates
- ✂️ Split Text to Columns
- 📋 Data Validation
- ⚡ Smart Fill & Autofill
- 🔄 Workflow Diagram
- 💼 Real-World Applications
- 💡 Best Practices
- ❓ Interview Questions
- 📝 Practice Checklist
- 🚀 Mini Projects

---

# 📖 Introduction

Raw datasets are often messy, inconsistent, and difficult to analyze. Google Sheets provides powerful **Data Tools** to clean, organize, validate, and automate repetitive tasks before performing analysis.

These tools help transform raw data into structured datasets that are ready for dashboards, reports, and business intelligence.

---

# 🎯 Learning Objectives

After completing this module, you will be able to:

- ✅ Remove duplicate records
- ✅ Split text into multiple columns
- ✅ Create dropdown menus
- ✅ Restrict invalid user input
- ✅ Apply number validation
- ✅ Use Smart Fill
- ✅ Use Autofill efficiently
- ✅ Prepare clean datasets for analysis

---

# 🛠️ Data Tools Overview

| Tool | Purpose |
|------|----------|
| 📋 Data Validation | Restrict invalid inputs |
| 🧹 Remove Duplicates | Delete repeated records |
| ✂️ Split Text | Separate text using delimiters |
| ⚡ Autofill | Continue patterns automatically |
| 🤖 Smart Fill | Detect and complete data intelligently |

---

# 📊 Practice Dataset

Create the following table in **Google Sheets**.

| Full Name | Role | Score |
|------------|------------|------:|
| Rahul Sharma | Admin | 85 |
| Priya Verma | Developer | 92 |
| Rahul Sharma | Admin | 85 |
| Amit Patel | Manager | 78 |
| Sneha Gupta | Developer | 90 |

---

# 🔄 Data Cleaning Workflow

```text
Raw Dataset

      │

      ▼

Remove Duplicates

      │

      ▼

Split Text

      │

      ▼

Validate Data

      │

      ▼

Smart Fill

      │

      ▼

Clean Dataset Ready for Analysis
```

---

# 🧹 Exercise 1 — Remove Duplicates

## Objective

Delete repeated records while keeping only unique entries.

---

## Steps

Select

```
A1:C6
```

↓

```
Data

↓

Data Cleanup

↓

Remove Duplicates
```

↓

✔ Data has header row

↓

Remove Duplicates

---

## Result

Before

| Name | Role |
|------|------|
| Rahul Sharma | Admin |
| Rahul Sharma | Admin |

↓

After

| Name | Role |
|------|------|
| Rahul Sharma | Admin |

Only one record remains.

---

# ✂️ Exercise 2 — Split Text to Columns

## Objective

Separate Full Name into First Name and Last Name.

---

## Steps

Select

```
A2:A5
```

↓

```
Data

↓

Split Text to Columns
```

↓

Choose Separator

```
Space
```

---

## Before

| Full Name |
|------------|
| Rahul Sharma |

↓

## After

| First Name | Last Name |
|------------|-----------|
| Rahul | Sharma |

---

## Supported Delimiters

| Delimiter | Example |
|------------|----------|
| Space | Rahul Sharma |
| Comma | Rahul,Sharma |
| Dash | Rahul-Sharma |
| Semicolon | Rahul;Sharma |
| Custom | Any Character |

---

# 📋 Exercise 3 — Data Validation

## What is Data Validation?

Data Validation ensures users enter only valid information.

Examples:

- Dropdown Lists
- Number Limits
- Date Restrictions
- Custom Formulas

---

## Create a Dropdown List

Select

```
D2
```

↓

```
Data

↓

Data Validation

↓

+ Add Rule
```

↓

Criteria

```
Dropdown
```

Values

```
Pass

Fail

Pending
```

---

### Output

```
▼ Pass
▼ Fail
▼ Pending
```

---

## Number Validation

Select

```
C2:C5
```

↓

```
Data Validation

↓

Number

↓

Between

↓

0

↓

100
```

Now only scores between **0 and 100** are accepted.

---

## Date Validation Example

Prevent future dates.

Criteria

```
Date

↓

Is Before

↓

Today
```

Perfect for attendance or joining date records.

---

# ⚡ Exercise 4 — Smart Fill & Autofill

## Autofill

Autofill detects simple patterns.

Example

| A |
|---|
|1|
|2|

↓

Drag

↓

```
3
4
5
6
7
```

---

## Smart Fill

Smart Fill predicts complex text patterns.

Example

| Full Name | Email |
|------------|------------------|
| Rahul Sharma | rahul@gmail.com |
| Priya Verma | *(Suggested)* |

Google Sheets automatically predicts the remaining values.

Accept with

```
Ctrl + Enter
```

or click the ✔ suggestion.

---

## Smart Fill Workflow

```text
Type Example

      │

      ▼

Google Detects Pattern

      │

      ▼

Gray Suggestion

      │

      ▼

Accept

      │

      ▼

Entire Column Completed
```

---

# 💼 Real-World Applications

These tools are widely used in:

- 📊 Sales Reports
- 👥 HR Employee Databases
- 💰 Finance & Accounting
- 📦 Inventory Tracking
- 🛒 E-commerce Data Cleaning
- 📈 Marketing Analytics
- 🏢 MIS Reporting
- 📋 Survey Data Processing

---

# 📈 Before vs After

| Before Cleaning | After Cleaning |
|----------------|----------------|
| Duplicate Records | Unique Records ✅ |
| Invalid Values | Valid Data ✅ |
| Mixed Text | Structured Columns ✅ |
| Manual Entry | Automated Input ✅ |

---

# 💡 Best Practices

✔ Validate user input

✔ Remove duplicates regularly

✔ Use dropdown menus

✔ Split combined text before analysis

✔ Avoid manual repetitive typing

✔ Review Smart Fill suggestions

✔ Keep datasets consistent

---

# 🎯 Skills Gained

- Data Cleaning
- Spreadsheet Validation
- Duplicate Detection
- Data Preparation
- Smart Automation
- Spreadsheet Productivity
- Business Reporting

---

# ❓ Interview Questions

### Q1. What is Data Validation?

A feature that restricts user input to predefined values or rules.

---

### Q2. Why remove duplicates?

To improve data quality and avoid inaccurate analysis.

---

### Q3. What is Split Text to Columns?

A tool that separates combined text into multiple columns using delimiters.

---

### Q4. Difference between Autofill and Smart Fill?

| Autofill | Smart Fill |
|----------|------------|
| Detects simple sequences | Detects intelligent patterns |
| Manual drag | AI-assisted suggestions |
| Numbers & Dates | Text & Complex Patterns |

---

### Q5. Why use dropdown lists?

To ensure consistent and error-free data entry.

---

# 📝 Practice Checklist

- [x] Create Practice Dataset
- [x] Remove Duplicate Records
- [x] Split Names into Separate Columns
- [x] Create Dropdown Menu
- [x] Apply Number Validation
- [x] Apply Date Validation
- [x] Test Smart Fill
- [x] Test Autofill

---

# 🚀 Mini Projects

### 🟢 Beginner

- Employee Database
- Student Marks Sheet
- Attendance Tracker

---

### 🟡 Intermediate

- Sales Entry System
- Customer Feedback Form
- Inventory Register

---

### 🔴 Advanced

- HR Management Dashboard
- CRM Data Cleaning Tool
- Automated Expense Tracker
- Dynamic Survey Dashboard

---

# 📂 Deliverables

✔ Clean Dataset

✔ Duplicate-Free Records

✔ Dropdown Menus

✔ Number Validation Rules

✔ Split Text Example

✔ Smart Fill Demonstration

✔ Autofill Demonstration

---

# 📖 Summary

| Feature | Status |
|----------|--------|
| Remove Duplicates | ✅ |
| Split Text to Columns | ✅ |
| Data Validation | ✅ |
| Dropdown Lists | ✅ |
| Number Validation | ✅ |
| Smart Fill | ✅ |
| Autofill | ✅ |

---

<div align="center">

## ⭐ Mastering Data Tools is the first step toward becoming a professional Data Analyst.

### If you found this repository helpful, don't forget to ⭐ Star it!

**Made with ❤️ by Harsh Pandey**

**Google Sheets • Data Analytics • Business Intelligence**

</div>
