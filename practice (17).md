 # 📖 Google Sheets Basics — Complete Notes

---

## 1. Spreadsheet vs. Sheet (Workbook vs. Tab)

* **Spreadsheet (Workbook):** The entire file itself. It acts as a container for all your tabs, formulas, scripts, and settings (e.g., `Sales_Report_2026.xlsx` or your main Google Sheets file).
* **Sheet (Tab):** An individual worksheet within the spreadsheet file.
* Located at the bottom of the screen.
* You can create multiple tabs (e.g., `Formulas`, `Charts`, `Automation`) by clicking the **`+`** button in the bottom-left corner.
* **Analogy:** A *Spreadsheet* is like an entire notebook, and each *Sheet* is an individual page inside that notebook.



---

## 2. Rows & Columns

Google Sheets is organized as a grid of horizontal rows and vertical columns.

* **Columns (Vertical):** Identified by **Letters** (`A`, `B`, `C`, ... `Z`, `AA`, `AB`).
* **Rows (Horizontal):** Identified by **Numbers** (`1`, `2`, `3`, ... `1000`).

### Essential Operations:

* **Inserting/Deleting:** Right-click any row number or column letter to insert new rows/columns or delete existing ones.
* **Resizing:** Drag the border between column letters or row numbers to adjust width or height. Double-click the line to auto-fit.
* **Freezing (Locking Headers):**
* **Why:** Keeps key headers visible while scrolling through large datasets.
* **How:** Go to **View** $\rightarrow$ **Freeze** $\rightarrow$ Select **1 row** or **1 column** (or drag the thick gray border line from the top-left corner box down past Row 1).



---

## 3. Cells & Ranges

### Cell & A1 Notation

* **Cell:** The single box formed by the intersection of a column and a row.
* **A1 Notation:** The standard naming convention where the **Column Letter** comes first, followed by the **Row Number**.
* *Example:* **`B5`** refers to Column B, Row 5.



### Ranges

* **Range:** A collection of two or more adjacent cells.
* **Syntax:** Represented using a colon (`:`) between the top-left cell and bottom-right cell.
* *Example:* **`A1:C10`** spans from cell `A1` down to cell `C10`.
* *Entire Column:* **`A:A`** selects all cells in Column A.
* *Entire Row:* **`1:1`** selects all cells in Row 1.



### Selecting Ranges (3 Methods):

1. **Name Box:** Click the Name Box (top-left box showing cell name), type `D5:G20`, and press `Enter`.
2. **Shift + Click:** Click the first cell (e.g., `B2`), hold `Shift`, and click the ending cell (e.g., `E15`).
3. **Click-Drag:** Click and hold the left mouse button on the starting cell, drag across to the ending cell, and release.

---

## 4. Cell References: Relative vs. Absolute ($A$1)

Understanding cell references is essential for writing efficient formulas.

| Reference Type | Example | Behavior when copied/dragged | Best Used For |
| --- | --- | --- | --- |
| **Relative** | `A1` | **Changes** automatically based on position (e.g., moving down changes `A1` $\rightarrow$ `A2`). | Standard row-by-row calculations (e.g., `Quantity * Price`). |
| **Absolute** | `$A$1` | **Stays fixed** on cell `A1` regardless of where the formula is dragged. | Fixed parameters like Tax Rate, Discount %, or Exchange Rates. |
| **Mixed** | `$A1` or `A$1` | Fixes only the column (`$A1`) **or** only the row (`A$1`). | Cross-tabulation matrices and lookup tables. |

> 💡 **Shortcut:** Press **`F4`** (or `Fn + F4`) while highlighting a cell reference in a formula to toggle between relative (`A1`), absolute (`$A$1`), and mixed (`A$1` / `$A1`).

---

### 🎯 Quick Self-Check Checklist

* [x] Know the difference between a Spreadsheet file and individual Sheet tabs.
* [x] Freeze the top row so column headers stay pinned while scrolling.
* [x] Select ranges using the Name Box, Shift + Click, or Dragging.
* [x] Use `$A$1` when referencing a fixed input cell (like tax rate or discount %) in a formula.
