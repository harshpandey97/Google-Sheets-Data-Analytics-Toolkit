# 📝 Data Entry & Formatting in Google Sheets

<p align="center">

<img src="https://img.shields.io/badge/Google%20Sheets-Data%20Entry%20%26%20Formatting-34A853?style=for-the-badge&logo=googlesheets&logoColor=white"/>

<img src="https://img.shields.io/badge/Module-01-blue?style=for-the-badge"/>

<img src="https://img.shields.io/badge/Level-Beginner-success?style=for-the-badge"/>

<img src="https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge"/>

</p>

---

# 📚 Table of Contents

- 📖 Introduction
- 🎯 Learning Objectives
- 📊 Sample Dataset
- ✨ Formatting Basics
- 🎨 Conditional Formatting
- 🔍 Detecting Duplicate Records
- 📋 Quick Menu Reference
- 💼 Real-World Applications
- 💡 Best Practices
- ❓ Interview Questions
- 📝 Practice Exercises
- 🔗 Google Sheet

---

# 📖 Introduction

Data formatting is one of the first skills every Data Analyst should master.

A well-formatted spreadsheet is:

- ✅ Easier to read
- ✅ Easier to analyze
- ✅ Easier to present
- ✅ More professional

Proper formatting improves data quality, minimizes errors, and enhances dashboard readability.

---

# 🎯 Learning Objectives

After completing this module, you will be able to:

- ✅ Format professional-looking tables
- ✅ Apply borders and themes
- ✅ Use alternating row colors
- ✅ Highlight important values
- ✅ Detect duplicate records
- ✅ Improve spreadsheet readability
- ✅ Prepare datasets for dashboards

---

# 📊 Sample Dataset

| Employee ID | Name | Department | Sales Amount ($) |
|-------------|----------------|-------------|----------------:|
| 101 | Rohan Sharma | Sales | 45000 |
| 102 | Priya Singh | Marketing | 62000 |
| 103 | Amit Kumar | IT | 28000 |

---

# 📈 Data Formatting Workflow

```text
Raw Data
    │
    ▼
Bold Headers
    │
    ▼
Borders
    │
    ▼
Alternating Colors
    │
    ▼
Conditional Formatting
    │
    ▼
Clean Professional Dataset
```

---

# ✨ Exercise 1 — Format a Professional Table

## Objective

Create a clean, readable spreadsheet using formatting tools.

### Step 1 — Bold Headers

Select the header row

```
Ctrl + B
```

or

```
Format
    ↓
Bold
```

Recommended:

- Dark header background
- White font
- Center aligned

---

### Step 2 — Add Borders

Select the table

```
Toolbar

↓

Borders

↓

All Borders
```

Recommended:

✔ Thin Gray Border

---

### Step 3 — Alternating Row Colors

```
Format

↓

Alternating Colors
```

Choose a built-in theme or create a custom color palette.

Example

| Header | Color |
|---------|--------|
| Header | Dark Green |
| Odd Rows | White |
| Even Rows | Light Green |

---

# 🎨 Exercise 2 — Conditional Formatting

Conditional formatting automatically highlights important values.

---

## Highlight Sales Above $50,000

Select

```
D2:D16
```

Navigate to

```
Format

↓

Conditional Formatting

↓

Greater Than

↓

50000
```

Choose

🟢 Green Fill

---

## Highlight Sales Below $20,000

Create another rule

```
Less Than

↓

20000
```

Choose

🔴 Red Fill

---

## Workflow

```text
Sales Data

      │

      ▼

Conditional Formatting

      │

      ▼

High Sales 🟢

Low Sales 🔴
```

---

# 🔍 Exercise 3 — Highlight Duplicate Records

Google Sheets allows custom formulas for advanced formatting.

---

## Full Duplicate Row Formula

```excel
=COUNTIFS($A$2:$A$16,$A2,$B$2:$B$16,$B2,$C$2:$C$16,$C2,$D$2:$D$16,$D2)>1
```

### What it does

Checks all columns simultaneously.

If an identical row appears more than once,

↓

Highlight Entire Row

---

## Duplicate ID Formula

```excel
=COUNTIF($A$2:$A$16,A2)>1
```

Perfect for checking repeated Employee IDs.

---

## Formula Logic

```text
Current Row

      │

      ▼

COUNTIFS()

      │

      ▼

Duplicate?

      │

 ┌────┴─────┐

Yes         No

 │           │

Highlight   Ignore
```

---

# 📋 Quick Menu Reference

| Task | Menu |
|------|------|
| Bold | **Ctrl + B** |
| Borders | Toolbar → Borders |
| Fill Color | Paint Bucket |
| Alternating Colors | Format → Alternating Colors |
| Conditional Formatting | Format → Conditional Formatting |
| Duplicate Highlight | Custom Formula |

---

# 💼 Real-World Applications

Data Entry & Formatting is widely used in:

- 📊 Sales Reports
- 💰 Financial Dashboards
- 📦 Inventory Management
- 👥 HR Analytics
- 📈 Marketing Reports
- 🏢 MIS Reporting
- 📋 Operations Dashboards
- 📉 Business Intelligence

---

# 💡 Best Practices

✔ Keep formatting consistent

✔ Use professional colors

✔ Freeze header rows

✔ Avoid excessive colors

✔ Align numbers correctly

✔ Format currency values

✔ Highlight important KPIs

✔ Remove duplicate records

✔ Validate data before analysis

---

# 🎯 Skills Gained

- Professional Spreadsheet Formatting
- Conditional Formatting
- Duplicate Detection
- Data Cleaning Basics
- Business Reporting
- Dashboard Preparation
- Spreadsheet Organization

---

# ❓ Interview Questions

### Q1. Why is formatting important?

It improves readability, presentation, and reduces errors.

---

### Q2. What is Conditional Formatting?

It automatically changes cell appearance based on rules.

---

### Q3. Which function detects duplicates?

```excel
COUNTIF()
```

or

```excel
COUNTIFS()
```

---

### Q4. Why use Alternating Colors?

Improves readability for large datasets.

---

### Q5. Difference between COUNTIF and COUNTIFS?

| COUNTIF | COUNTIFS |
|----------|----------|
| One Condition | Multiple Conditions |

---

# 📝 Practice Checklist

- [x] Create Sample Dataset
- [x] Bold Headers
- [x] Apply Borders
- [x] Apply Alternating Row Colors
- [x] Highlight High Sales
- [x] Highlight Low Sales
- [x] Detect Duplicate Rows
- [x] Detect Duplicate Employee IDs

---

# 📂 Deliverables

✔ Professional Spreadsheet

✔ Conditional Formatting Rules

✔ Duplicate Detection Formula

✔ Clean Business Table

✔ Recruiter-Friendly Formatting

---

# 🔗 Google Sheets Practice

📄 **Live Google Sheet**
https://docs.google.com/spreadsheets/d/1VIiwd7vO6vpBsdbQq-0TlVNAEbcPmRYYjkOg7e12Fls/edit?usp=sharing

 
---

# 🚀 What's Next?

➡️ Formulas & Functions

➡️ Charts & Graphs

➡️ Pivot Tables

➡️ QUERY Function

➡️ XLOOKUP

➡️ Dashboard Building

➡️ Automation with Apps Script

---
 
<div align="center">

## ⭐ If this project helped you, consider giving the repository a Star!

### Built with ❤️ by **Harsh Pandey**

**Google Sheets • Data Analytics • Business Intelligence**

</div>
