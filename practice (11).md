 

## 📖 Best Practices Module Notes & Action Items

---
https://docs.google.com/spreadsheets/d/1el-V3ntx0i6GeLpcpmJ-usP5FZFCCjigyA-1AwdlVgQ/edit?usp=sharing

### 1. Filter Views vs. Raw Filters (For Shared Sheets)

* **The Rule:** Never apply a standard Filter (`Data > Create a filter`) on a sheet shared with multiple people, because it changes the view for *everyone* working on the sheet at the same time.
* **Best Practice:** Use **Filter Views** (`Data > Filter views > Create new filter view`).
* **Why:** Filter Views allow you to sort and filter data privately without affecting what other collaborators see.

---

### 2. Comments & Named Ranges (For Clarity & Documentation)

* **Named Ranges:**
* Select a cell range (e.g., `C2:C100`).
* Go to **Data > Named ranges** and give it a clean name like `TotalRevenue`.
* Now, instead of writing `=SUM(C2:C100)`, you can write `=SUM(TotalRevenue)`.


* **Comments & Notes:**
* Right-click any complex formula cell and select **Insert comment** (or **Insert note**) to explain *why* a specific logic or calculation was used.



---

### 3. Avoid Merged Cells in Data Tables

* **The Rule:** Do **not** merge cells within raw data rows or columns (e.g., merging `A2` and `A3` for a single category name).
* **Why It Breaks Things:**
* Merged cells break standard formulas (`VLOOKUP`, `INDEX/MATCH`).
* They prevent proper sorting (A to Z / Z to A) and filtering.
* They corrupt copy-pasting ranges.


* **Alternative:** Keep data unmerged in flat rows, or use formatting like **Center across selection** if available, or restrict merged cells solely to top title headers outside the dataset grid.

---

### 🛠️ Practice Checklist for Your Sheet

To mark this module complete, perform these 3 quick actions in your **`Best Practices`** tab:

1. **1. Create a Filter View:** Set up a non-destructive filter.
Highlight your data table $\rightarrow$ Click **Data** $\rightarrow$ **Filter views** $\rightarrow$ **Create new filter view**.


2. **2. Create a Named Range:** Replace cell coordinates with a readable name.
Select any numeric column $\rightarrow$ Go to **Data** $\rightarrow$ **Named ranges** $\rightarrow$ Name it `SalesData` $\rightarrow$ Use `=SUM(SalesData)` in a cell.


3. **3. Unmerge Any Data Cells:** Clean up data layout.
Select your table grid $\rightarrow$ Click the **Unmerge** icon in the toolbar to ensure every data cell is individual and clear for formulas.


---

Once completed, click the green **Share** button in the top-right corner, ensure access is set to **Anyone with the link**, copy the link, and paste it into your submission box!
