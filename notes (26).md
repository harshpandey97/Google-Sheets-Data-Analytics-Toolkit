# 📊 Google Sheets Bootcamp – Charts & Graphs Practice

**Module:** Charts & Graphs

**Status:** ✅ Completed 


https://docs.google.com/spreadsheets/d/1el-V3ntx0i6GeLpcpmJ-usP5FZFCCjigyA-1AwdlVgQ/edit?usp=sharing
---

# 🎯 Learning Objectives

By the end of this module, you will be able to:

* Create Bar Charts
* Create Column Charts
* Create Line Charts
* Create Pie Charts
* Create Combo Charts
* Use Sparklines
* Customize charts
* Choose the right chart for different business scenarios

---

# Dataset

| Month | Revenue | Profit | Growth % |
| ----- | ------- | ------ | -------- |
| Jan   | 12000   | 2800   | 8%       |
| Feb   | 14500   | 3500   | 12%      |
| Mar   | 16000   | 4200   | 10%      |
| Apr   | 18500   | 4800   | 15%      |
| May   | 21000   | 5200   | 14%      |
| Jun   | 23500   | 6100   | 18%      |

---



<img width="540" height="293" alt="image" src="https://github.com/user-attachments/assets/08e5d7c8-7db8-4163-9df9-40f9c8c5655d" />



# Exercise 1 – Column Chart

### Goal

Compare monthly revenue.

### Steps

1. Select **A1:B7**
2. Click **Insert → Chart**
3. Google Sheets automatically creates a chart.
4. Change Chart Type to

```
Column Chart
```

### Best Used For

* Monthly Sales
* Revenue Comparison
* Product Sales
* Employee Performance

---

# Exercise 2 – Bar Chart

### Goal

Compare Profit.

### Steps

Select

```
A1:C7
```

Change Chart Type

```
Bar Chart
```

### Best Used For

* Category Comparison
* Ranking
* Survey Results

---

# Exercise 3 – Line Chart

### Goal

Show revenue trend over time.

### Steps

Select

```
A1:B7
```

Insert

```
Line Chart
```

### Best Used For

* Sales Trend
* Website Traffic
* Stock Prices
* Monthly Revenue

---

# Exercise 4 – Pie Chart

### Goal

Revenue Distribution

Select

```
Month + Revenue
```

Insert

```
Pie Chart
```

### Best Used For

* Market Share
* Budget Allocation
* Department Spending
* Revenue Contribution

---

# Exercise 5 – Combo Chart

### Goal

Compare Revenue and Growth %

### Dataset

| Month | Revenue | Growth |
| ----- | ------- | ------ |
| Jan   | 12000   | 8%     |
| Feb   | 14500   | 12%    |
| Mar   | 16000   | 10%    |
| Apr   | 18500   | 15%    |
| May   | 21000   | 14%    |
| Jun   | 23500   | 18%    |

---

### Steps

Select

```
A1:C7
```

Insert Chart

Choose

```
Combo Chart
```

Revenue

```
Column
```

Growth %

```
Line
```

### Best Used For

* Revenue vs Growth
* Sales vs Target
* Cost vs Profit
* Users vs Conversion Rate

---

# Exercise 6 – Sparkline

### Formula

```excel
=SPARKLINE(B2:G2)
```

Example

| Product | Jan | Feb | Mar | Apr | May | Jun | Trend |
| ------- | --: | --: | --: | --: | --: | --: | ----- |
| Laptop  | 120 | 140 | 150 | 180 | 170 | 200 | 📈    |

Formula

```excel
=SPARKLINE(B2:G2)
```

---

### Sparkline with Color

```excel
=SPARKLINE(B2:G2,{"charttype","line";"color","green"})
```

---

### Column Sparkline

```excel
=SPARKLINE(B2:G2,{"charttype","column"})
```

---

### Win/Loss Sparkline

```excel
=SPARKLINE(B2:G2,{"charttype","winloss"})
```

---

# Exercise 7 – Customize Chart

Change

* Chart Title
* Background
* Legend Position
* Axis Title
* Font
* Gridlines
* Labels
* Colors

---

# Real Business Example

### Sales Dashboard

| KPI                 | Chart     |
| ------------------- | --------- |
| Revenue Trend       | Line      |
| Profit by Region    | Bar       |
| Revenue by Category | Column    |
| Market Share        | Pie       |
| Revenue vs Growth   | Combo     |
| Product Performance | Sparkline |

---

# Which Chart Should You Use?

| Scenario            | Best Chart  |
| ------------------- | ----------- |
| Compare Products    | 📊 Bar      |
| Monthly Sales       | 📈 Line     |
| Revenue by Month    | 📊 Column   |
| Market Share        | 🥧 Pie      |
| Revenue vs Growth   | 📈 Combo    |
| Small Trend in Cell | ⚡ Sparkline |

---

# Mini Assignment

Create a **Sales Dashboard** containing:

* ✅ Column Chart (Revenue by Month)
* ✅ Line Chart (Profit Trend)
* ✅ Pie Chart (Revenue Share)
* ✅ Combo Chart (Revenue + Growth %)
* ✅ Sparklines for Product Trends

---

# Practice Challenge

Create a dashboard for the following data:

| Region | Sales | Profit |
| ------ | ----: | -----: |
| North  | 42000 |   8200 |
| South  | 39000 |   7100 |
| East   | 46000 |   9100 |
| West   | 37000 |   6500 |

Build:

<img width="550" height="300" alt="image" src="https://github.com/user-attachments/assets/e31cf8ef-0741-42f9-89e6-914c60483d60" />


* 📊 Bar Chart for Sales
* 📈 Column Chart for Profit
* 🥧 Pie Chart for Sales Distribution

---

# Skills Covered

* ✅ Bar Chart
* ✅ Column Chart
* ✅ Line Chart
* ✅ Pie Chart
* ✅ Combo Chart
* ✅ Sparklines
* ✅ Chart Formatting
* ✅ Dashboard Creation
* ✅ Business Data Visualization

---

<img width="619" height="462" alt="image" src="https://github.com/user-attachments/assets/89dda338-c91c-4236-a210-df6667037455" />


## 📌 Interview Tip

When explaining your choice of chart in an interview:

* **Bar Chart:** Compare values across categories (e.g., sales by region).
* **Column Chart:** Compare values over discrete periods (e.g., monthly revenue).
* **Line Chart:** Show trends over time.
* **Pie Chart:** Show proportions or percentage share (use only for a small number of categories).
* **Combo Chart:** Compare two related metrics with different scales (e.g., revenue and growth %).
* **Sparkline:** Display a compact trend inside a single cell without taking extra dashboard space.
