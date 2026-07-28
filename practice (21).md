# 📊 Charts & Graphs in Google Sheets

<p align="center">
<img src="https://img.shields.io/badge/Google%20Sheets-Charts%20%26%20Graphs-34A853?style=for-the-badge&logo=googlesheets&logoColor=white"/>
<img src="https://img.shields.io/badge/Level-Beginner%20→%20Intermediate-blue?style=for-the-badge"/>
<img src="https://img.shields.io/badge/Status-Completed-success?style=for-the-badge"/>
</p>

---

# 📖 Overview

Charts transform raw numbers into meaningful visual insights.

Instead of reading thousands of rows, charts help identify:

- 📈 Trends
- 📊 Comparisons
- 🥧 Proportions
- 📉 Growth & Decline
- 🎯 KPIs

Google Sheets provides interactive visualizations that are widely used in Data Analytics, MIS Reporting, Business Intelligence, Marketing Analytics, Finance, and Operations.

---

# 🧠 Visualization Workflow

```text
                 Raw Data
                     │
                     ▼
           Clean & Organize Data
                     │
                     ▼
              Select Data Range
                     │
                     ▼
               Insert Chart
                     │
                     ▼
           Customize Visualization
                     │
                     ▼
            Business Decision
```

---

# 🎯 Learning Objectives

After completing this module, you will be able to:

- ✅ Create Column Charts
- ✅ Create Bar Charts
- ✅ Create Line Charts
- ✅ Create Pie Charts
- ✅ Create Combo Charts
- ✅ Use SPARKLINE()
- ✅ Customize Chart Styles
- ✅ Build Dashboard Visualizations

---

# 📊 Dataset Used

| Month | Revenue | Profit Margin (%) |
|--------|---------|-------------------|
| Jan | 15000 | 18 |
| Feb | 17500 | 20 |
| Mar | 19000 | 22 |
| Apr | 22000 | 21 |
| May | 24500 | 24 |
| Jun | 27000 | 26 |
| Jul | 28500 | 25 |
| Aug | 30000 | 28 |
| Sep | 31500 | 27 |
| Oct | 34000 | 29 |
| Nov | 36000 | 30 |
| Dec | 39000 | 32 |

---

# 📈 Exercise 1 — Monthly Sales Column Chart

### Objective

Visualize monthly revenue using a Column Chart.

### Steps

1. Select **Month** and **Revenue**
2. Go to

```
Insert → Chart
```

3. Choose

```
Column Chart
```

4. Customize

- Chart Title
- Axis Titles
- Data Labels
- Legend

---

### Example


::contentReference[oaicite:0]{index=0}


---

# 📊 Exercise 2 — Revenue vs Profit Margin (Combo Chart)

### Objective

Compare Revenue and Profit Margin simultaneously.

### Steps

```
Select Month + Revenue + Profit Margin
```

↓

```
Insert
```

↓

```
Chart
```

↓

```
Combo Chart
```

---

### Configure

Revenue

✅ Column

Profit Margin

✅ Line

Profit Margin Axis

✅ Right Axis

---

### Visualization

```text
Revenue

██████
██████████
██████████████

Profit Margin

────────●────────●────────●
```

---

# ⚡ Exercise 3 — SPARKLINE()

## What is SPARKLINE?

A Sparkline is a tiny chart inside a single cell.

Instead of large charts, Sparklines quickly show trends.

Example:

| Sales Trend |
|--------------|
| 📈 |
| 📉 |
| 📊 |

---

## Formula

```excel
=SPARKLINE(D2:F2)
```

---

### Column Sparkline

```excel
=SPARKLINE(D2:F2,{"charttype","column"})
```

---

### Win/Loss Sparkline

```excel
=SPARKLINE(D2:F2,{"charttype","winloss"})
```

---

### Color Sparkline

```excel
=SPARKLINE(D2:F2,{"color","green"})
```

---

### Example

| Product A | Product B | Product C | Trend |
|------------|------------|------------|-------|
|120|135|140|📈|
|125|140|145|📈|
|130|145|150|📈|

---

# 📊 Types of Charts

| Chart | Best Use |
|---------|----------|
| 📊 Column | Compare categories |
| 📈 Line | Time trends |
| 📉 Area | Cumulative growth |
| 🥧 Pie | Percentage contribution |
| 🍩 Donut | Part-to-whole |
| 📌 Scatter | Correlation |
| 📦 Bar | Rankings |
| 📋 Combo | Compare two metrics |
| ⚡ Sparkline | Mini trend |

---

# 💡 Best Practices

✅ Use meaningful titles

✅ Label axes

✅ Avoid excessive colors

✅ Highlight key KPIs

✅ Keep charts simple

✅ Use consistent formatting

---

# 🚀 Real-World Applications

- Sales Dashboard
- Financial Reports
- Marketing Analytics
- Customer Analysis
- Inventory Reports
- HR Dashboard
- Operations Dashboard
- Business Intelligence
- Executive KPI Reports

---

# 🎯 Practice Exercises

- [x] Build a Monthly Sales Column Chart
- [x] Build a Revenue vs Profit Margin Combo Chart
- [x] Add SPARKLINE() Trend Column
- [ ] Create a Pie Chart
- [ ] Create a Line Chart
- [ ] Create a Scatter Plot
- [ ] Build a Mini Dashboard

---

# 📝 Interview Questions

### Q1. When should you use a Column Chart?

To compare values across different categories.

---

### Q2. Why use a Combo Chart?

To compare two metrics with different scales (e.g., Revenue and Profit Margin).

---

### Q3. What is a Sparkline?

A miniature chart displayed inside a single cell that shows trends without occupying much space.

---

### Q4. Which chart is best for trends over time?

📈 Line Chart

---

### Q5. Which chart is best for showing proportions?

🥧 Pie Chart

---

# 📂 Deliverables

- ✔ Google Sheets Workbook
- ✔ Monthly Sales Column Chart
- ✔ Revenue vs Profit Margin Combo Chart
- ✔ SPARKLINE() Examples
- ✔ Dashboard Ready Visualizations

---

## 🔗 Google Sheet

```text
https://docs.google.com/spreadsheets/d/your-sheet-id
```

*(Replace with your shared Google Sheet link.)*

---

<div align="center">

### ⭐ If you found this module helpful, don't forget to star the repository!

**Made with ❤️ by Harsh Pandey**

</div>
