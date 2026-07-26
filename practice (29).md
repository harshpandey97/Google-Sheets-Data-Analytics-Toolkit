  🛠️ Data Tools — Notes & Practice Guide

---

## 1. Key Concepts & Overview

* **Data Validation:** Restricts what users can enter into a cell (e.g., creating drop-down lists, setting number/date limits, or using custom formulas like preventing future dates).
* **Remove Duplicates:** Automatically scans selected rows/columns and deletes identical duplicate records to keep datasets clean.
* **Split Text to Columns:** Separates text from a single cell into multiple columns based on a delimiter (like a space, comma, or dash)—perfect for separating full names into First and Last names.
* **Autofill / Smart Fill:** Automatically detects patterns in your typing (e.g., dates, sequence numbers, or formatting text) and fills adjacent cells for you.

---

## 🛠️ Step-by-Step Practice Exercises

Set up your **`Data Tools`** tab by creating a simple table in cells **`A1:C6`**:

| Cell | A (Full Name) | B (Role) | C (Score) |
| --- | --- | --- | --- |
| **1** | **Full Name** | **Role** | **Score** |
| **2** | Rahul Sharma | Admin | 85 |
| **3** | Priya Verma | Developer | 92 |
| **4** | Rahul Sharma | Admin | 85 |
| **5** | Amit Patel | Manager | 78 |
| **6** | Sneha Gupta | Developer | 90 |

---

1. **Exercise 1: Remove Duplicates:** Clean up redundant rows in your dataset.
1. Highlight your table **`A1:C6`**.
2. In the top menu, go to **Data** $\rightarrow$ **Data cleanup** $\rightarrow$ **Remove duplicates**.
3. Check the box for **Data has header row**.
4. Click **Remove duplicates**.

* *Result:* The duplicate row for *Rahul Sharma* is removed automatically!


2. **Exercise 2: Split Text to Columns:** Separate combined text fields easily.
1. Highlight the names in column A (**`A2:A5`**).
2. Go to **Data** $\rightarrow$ **Split text to columns**.
3. In the small separator popup near your mouse, select **Space** as the delimiter.

* *Result:* First names stay in Column A, and Last names automatically move to Column B!


3. **Exercise 3: Data Validation (Dropdown & Range):** Restrict inputs using dropdowns and ranges.
* **Create a Dropdown:**
1. Click an empty cell (e.g., **`D2`**).
2. Go to **Data** $\rightarrow$ **Data validation** $\rightarrow$ Click **+ Add rule**.
3. Under **Criteria**, choose **Dropdown** and enter values like `Pass`, `Fail`, `Pending`.


* **Set a Number Range Rule:**
1. Select cells **`C2:C5`** (Scores).
2. Click **+ Add rule** $\rightarrow$ Under Criteria, choose **Number is between** $\rightarrow$ Enter `0` and `100`.




4. **Exercise 4: Smart Fill & Autofill:** Let Google Sheets complete repetitive patterns.
1. In cell **`E1`**, type `Email Domain`.
2. In cell **`E2`**, start typing `gmail.com` or an email pattern based on Column A.
3. Google Sheets will display a grayed-out **Smart Fill** suggestion for the rest of the column.
4. Press **`Ctrl + Enter`** (or click the green checkmark) to auto-complete the pattern for all rows!


---

### Submission Reminder

When finished, click the green **Share** button (top-right), ensure access is set to **Anyone with the link**, copy the link, and paste it into your assignment portal!
