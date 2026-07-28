# 🧮 Formulas & Functions (Complete Study Notes)

> **Status:**  completed 
> **Difficulty:** ⭐⭐⭐☆☆ (Beginner → Intermediate)
> **Duration:** 2–3 Hours
>[Architecting_Application_Grade_Spreadsheets.pdf](https://github.com/user-attachments/files/30455843/Architecting_Application_Grade_Spreadsheets.pdf)# 📊 Google Sheets Bootcamp – Module 3
> https://docs.google.com/spreadsheets/d/1kHBysXEZisfLnL7NvVNhSGCXRtm15GvXhIquC86oLi4/edit?usp=sharing

>  video playbook >https://notebook.google.com/notebook/e858f3dd-225b-416f-a003-e898adee188b/artifact/e26a5675-67d6-4600-aed9-161fc654393e?utm_source=nlm_web_share&utm_medium=google_oo&utm_campaign=art_share_1&utm_content=&utm_smc=nlm_web_share_google_oo_art_share_1_
  >audiobook https://notebook.google.com/notebook/e858f3dd-225b-416f-a003-e898adee188b/artifact/ac62abe7-dc17-4520-8843-3d0a003409c1?utm_source=nlm_web_share&utm_medium=google_oo&utm_campaign=art_share_1&utm_content=&utm_smc=nlm_web_share_google_oo_art_share_1_

---

# 📖 Introduction

Formulas and Functions are the **heart of Google Sheets**. They allow you to automate calculations, analyze data, summarize information, and build powerful dashboards without manual effort.

---

## 🧠 Formula Workflow

```text
        Raw Data
           │
           ▼
     Apply Formula
           │
           ▼
      Process Data
           │
           ▼
      Business Insight
           │
           ▼
      Better Decisions
```

---

## 🖼️ Formula Flow Diagram

```text
             +------------------+
             |   Raw Dataset    |
             +------------------+
                      │
                      ▼
            +-------------------+
            | Formula / Function|
            +-------------------+
                      │
        ┌─────────────┼─────────────┐
        ▼             ▼             ▼
     Calculate     Lookup       Condition
        │             │             │
        └─────────────┼─────────────┘
                      ▼
            +-------------------+
            | Final Dashboard   |
            +-------------------+
```

---

# 📌 Formula Syntax

Every formula begins with an **equal sign (=)**.

```excel
=Function_Name(arguments)
```

Example:

```excel
=SUM(A1:A10)
```

---

# 📊 Aggregate Functions

## 1️⃣ SUM()

### Purpose

Adds numbers together.

### Syntax

```excel
=SUM(range)
```

### Example

| Sales |
| ----: |
|  1200 |
|  1500 |
|  1800 |
|  2000 |

Formula

```excel
=SUM(A2:A5)
```

Output

```text
6500
```

### Diagram

```text
1200
1500
1800
2000
──────
6500
```

---

## 2️⃣ AVERAGE()

### Purpose

Finds the average value.

### Syntax

```excel
=AVERAGE(range)
```

Example

```excel
=AVERAGE(A2:A5)
```

Output

```text
1625
```

---

## Visual

```text
1200
1500
1800
2000
────────
Average

   ↓

1625
```

---

# 🟢 Conditional Functions

---

## 3️⃣ IF()

### Purpose

Returns different results based on a condition.

### Syntax

```excel
=IF(condition,value_if_true,value_if_false)
```

Example

```excel
=IF(B2>=60,"Pass","Fail")
```

Output

| Marks | Result |
| ----: | ------ |
|    85 | Pass   |
|    40 | Fail   |

---

### Logic Diagram

```text
        Marks >=60?
          │
     ┌────┴────┐
     │         │
   YES         NO
     │         │
  Pass       Fail
```

---

## 4️⃣ AND()

Returns TRUE only if **all conditions are TRUE**.

Example

```excel
=AND(B2>=60,C2>=75)
```

| Marks | Attendance | Result |
| ----: | ---------: | ------ |
|    80 |         90 | TRUE   |
|    80 |         60 | FALSE  |

---

## Diagram

```text
Condition 1 ✓

AND

Condition 2 ✓

↓

TRUE
```

---

## 5️⃣ OR()

Returns TRUE if **any one condition is TRUE**.

Example

```excel
=OR(B2>=60,C2>=75)
```

---

Diagram

```text
Condition 1 ❌

OR

Condition 2 ✓

↓

TRUE
```

---

## Nested IF Example

```excel
=IF(B2>=90,"A",
IF(B2>=75,"B",
IF(B2>=60,"C","Fail")))
```

Output

| Marks | Grade |
| ----: | ----- |
|    95 | A     |
|    80 | B     |
|    65 | C     |
|    45 | Fail  |

---

# 🔍 Lookup Functions

---

## 6️⃣ VLOOKUP()

Searches vertically.

```excel
=VLOOKUP(E2,A2:C10,3,FALSE)
```

---

Diagram

```text
ProductID

↓

Search Column

↓

Return Price
```

---

## 7️⃣ HLOOKUP()

Searches horizontally.

```excel
=HLOOKUP("Jan",A1:F2,2,FALSE)
```

---

## 8️⃣ XLOOKUP() ⭐ Recommended

Modern replacement for VLOOKUP.

```excel
=XLOOKUP(E2,A2:A10,C2:C10)
```

Advantages

✅ Faster

✅ Simpler

✅ Looks left & right

✅ Returns custom "Not Found" values

---

Diagram

```text
Search Value

↓

Search Column

↓

Return Column

↓

Answer
```

---

# 📍 INDEX() + MATCH()

Powerful alternative to VLOOKUP.

---

## INDEX()

Returns a value from a specified row/column.

```excel
=INDEX(C2:C10,4)
```

---

## MATCH()

Returns the position.

```excel
=MATCH("Laptop",A2:A10,0)
```

---

## Combined

```excel
=INDEX(C2:C10,MATCH(E2,A2:A10,0))
```

---

Diagram

```text
MATCH()

↓

Find Row

↓

INDEX()

↓

Return Value
```

---

# 🔢 Counting Functions

---

## COUNT()

Counts numbers only.

```excel
=COUNT(A2:A20)
```

---

## COUNTA()

Counts non-empty cells.

```excel
=COUNTA(A2:A20)
```

---

## COUNTIF()

Counts cells meeting a condition.

```excel
=COUNTIF(C2:C20,">1000")
```

---

Example

| Sales |
| ----: |
|   500 |
|   800 |
|  1500 |
|  2000 |

Formula

```excel
=COUNTIF(A2:A5,">1000")
```

Output

```text
2
```

---

Diagram

```text
500 ❌

800 ❌

1500 ✅

2000 ✅

↓

Count = 2
```

---

# 📋 Real Business Example

| Employee | Sales |
| -------- | ----: |
| Alice    |  1500 |
| Bob      |  2200 |
| Charlie  |  1800 |
| David    |  2700 |

Formula

```excel
=SUM(B2:B5)
```

↓

Revenue

```text
8200
```

Average

```excel
=AVERAGE(B2:B5)
```

↓

```text
2050
```

Highest Performer

```excel
=XLOOKUP(MAX(B2:B5),B2:B5,A2:A5)
```

↓

```text
David
```

---

# 📈 Summary Table

| Function | Purpose                  | Example                    |
| -------- | ------------------------ | -------------------------- |
| SUM      | Add numbers              | `=SUM(A2:A10)`             |
| AVERAGE  | Average value            | `=AVERAGE(A2:A10)`         |
| IF       | Conditional logic        | `=IF(B2>60,"Pass","Fail")` |
| AND      | Multiple conditions      | `=AND(A2>0,B2>0)`          |
| OR       | Any condition            | `=OR(A2>0,B2>0)`           |
| VLOOKUP  | Vertical lookup          | `=VLOOKUP()`               |
| HLOOKUP  | Horizontal lookup        | `=HLOOKUP()`               |
| XLOOKUP  | Modern lookup            | `=XLOOKUP()`               |
| INDEX    | Return value by position | `=INDEX()`                 |
| MATCH    | Find position            | `=MATCH()`                 |
| COUNT    | Count numbers            | `=COUNT()`                 |
| COUNTA   | Count non-empty cells    | `=COUNTA()`                |
| COUNTIF  | Count with criteria      | `=COUNTIF()`               |

---

# 💼 Interview Questions

### Q1. What is the difference between COUNT and COUNTA?

* **COUNT** counts only numeric values.
* **COUNTA** counts all non-empty cells (text, numbers, dates, etc.).

---

### Q2. Why is XLOOKUP preferred over VLOOKUP?

* Searches both left and right.
* No column index number required.
* Built-in handling for missing values.
* Easier to read and maintain.

---

### Q3. When would you use INDEX + MATCH instead of VLOOKUP?

* When the lookup column is not the first column.
* For more flexible and robust lookups across large datasets.

---

# 🎯 Practice Tasks

* ✅ Calculate total and average sales using `SUM()` and `AVERAGE()`.
* ✅ Assign grades with nested `IF()` statements.
* ✅ Validate multiple conditions using `AND()` and `OR()`.
* ✅ Compare `VLOOKUP()` and `XLOOKUP()` on the same dataset.
* ✅ Retrieve values using `INDEX()` + `MATCH()`.
* ✅ Count records with `COUNT()`, `COUNTA()`, and `COUNTIF()`.

---

## 📚 Quick Revision Mind Map

```text
                 FORMULAS & FUNCTIONS
                        │
     ┌──────────────────┼──────────────────┐
     ▼                  ▼                  ▼
 Aggregate         Conditional         Lookup
(SUM,AVERAGE)   (IF,AND,OR)   (VLOOKUP,XLOOKUP,
                                      INDEX,MATCH)
                        │
                        ▼
                Counting Functions
         (COUNT, COUNTA, COUNTIF)
                        │
                        ▼
               Reports • Dashboards • Automation
```

This structure is suitable for your **Google Sheets Data Analytics Bootcamp** repository and provides clear explanations, examples, diagrams, interview tips, and practice tasks in a visually organized format.


Comprehensive Excel Mastery: Design, Flowcharts, and Formulas

This study guide provides a structured review of professional spreadsheet design, the creation of visual workflows, and the technical application of Excel's most powerful functions and formulas. It is synthesized from expert methodologies and official documentation.

Part 1: Knowledge Quiz

Instructions: Provide 2–3 sentences for each short-answer question based on the provided source materials.

1. Why is it a best practice to separate "Input" sheets from "Output" sheets in a workbook?
2. What is the specific purpose of a "Control Sheet" in professional spreadsheet design?
3. How should color coding be utilized to improve the visual design of a worksheet?
4. What are "Connection Points" in the context of creating Excel flowcharts, and why are they useful?
5. Explain the difference between a "Relative Reference" and an "Absolute Reference" when copying formulas.
6. What is a "3-D Reference" and what are its requirements?
7. How does XLOOKUP handle exact matches differently than its predecessor, VLOOKUP?
8. What function does the fourth parameter (if_not_found) serve in an XLOOKUP formula?
9. Under what circumstances would an "Instruction Sheet" be necessary for an Excel workbook?
10. In a VLOOKUP formula, what does the col_index_num represent, and how is it calculated?

Part 2: Answer Key

1. Separation of Data: Keeping raw data separate from reports prevents accidental corruption of the data structure and allows for different levels of access protection. This structure ensures users can interact with the report results without risking the integrity of the underlying connective services or sensitive raw data.
2. Control Sheets: A Control Sheet serves as a documentation hub to record changes and updates made to the workbook as business requirements evolve. It helps the developer remember specific modifications over time, providing a historical record when memories of the initial build have faded.
3. Consistent Color Coding: Design principles suggest using only 2 to 3 muted colors to denote specific messaging, such as distinguishing between input cells and calculation cells. This "less is more" approach ensures the formatting is professional and that colors have consistent meanings, such as coding by department or region.
4. Connection Points: These are small handles that appear on the outline of a shape when hovering with an arrow tool. By attaching an arrow to these points, Excel "locks" the connection, ensuring the arrow stays attached to the shapes even if they are moved or rearranged on the sheet.
5. Reference Types: A Relative Reference (e.g., A1) is based on the relative position of the cell and automatically adjusts when a formula is copied to a new location. An Absolute Reference (e.g., A1) uses dollar signs to "lock" the reference, ensuring it always points to the exact same cell regardless of where the formula is moved.
6. 3-D References: A 3-D reference allows a user to analyze data in the same cell or range across multiple worksheets (e.g., Sheet1:Sheet4!A1). It requires a range of worksheet names followed by an exclamation point and the cell reference, but it cannot be used in array formulas.
7. Exact Match Defaults: XLOOKUP performs an exact match by default, making it more streamlined and less error-prone. In contrast, VLOOKUP requires the user to explicitly enter "FALSE" or "0" as the final parameter to ensure an exact match; otherwise, it defaults to an approximate match.
8. Error Handling with XLOOKUP: The if_not_found parameter allows the user to define a specific text string or value (such as "Value not found") to display if the lookup search fails. This built-in feature eliminates the need to wrap lookup formulas in separate IFERROR or IFNA functions.
9. Instruction Sheets: These are necessary to explain the workbook's purpose, the order of data input, calculation dependencies, and how data is refreshed. They are vital for helping new users or even the original developer understand the operational process after a significant amount of time has passed.
10. Column Index Number: In VLOOKUP, the col_index_num is the number of the column in the table array that contains the result you want to return. It is calculated by counting columns from the leftmost column of the range, which is always designated as 1.



Part 3: Essay Questions

The following questions are designed for in-depth analysis. Responses should incorporate multiple principles from the study materials.

1. The Evolution of Lookups: Compare and contrast VLOOKUP, INDEX+MATCH, and XLOOKUP. Discuss why XLOOKUP is considered a superior tool for data professionals while acknowledging its primary limitation regarding compatibility.
2. Principles of Durable Spreadsheet Design: Discuss how Workbook Structure and Visual Design work together to create a professional spreadsheet. Explain how documentation (Control Sheets and Instructions) and structural separation (Input vs. Output) contribute to long-term workbook viability.
3. Visualization and Workflow: Describe the step-by-step process of building a professional-looking flowchart in Excel. Include details on shape selection for specific functions, alignment techniques, and the use of hyperlinks to connect data to the visual process.
4. Cell Referencing Strategy: Analyze the strategic use of Relative, Absolute, and Mixed references. Provide a hypothetical scenario for each where using the wrong reference type would result in a business-critical error.
5. Risk Management in Excel: Based on the provided sources, evaluate the "Don’ts" of spreadsheet design. Focus on the risks of file corruption, the lack of backups, and the dangers of unorganized public-facing reports.




<img width="2752" height="1536" alt="BEST_Financial_Modelling_Framework (1)" src="https://github.com/user-attachments/assets/4f31932f-6072-41ed-be0a-a81307cf9740" />


Part 4: Glossary of Key Terms

Term	Definition
3-D Reference	A reference to a range that spans two or more worksheets in a workbook.
Absolute Reference	A cell reference in a formula that remains constant even if the formula is copied to another cell; indicated by dollar signs (e.g., $A$1).
A1 Reference Style	The default Excel style that identifies columns with letters (A-XFD) and rows with numbers (1-1,048,576).
Constants	Values in a formula that are not calculated and remain the same, such as numbers or text strings entered directly.
Control Sheet	A dedicated worksheet used to document updates, changes, and versions of an Excel workbook over time.
Flowchart	A visual representation of a process or workflow using connected shapes to illustrate steps and decision points.
Format Painter	A tool used to copy formatting (font, size, style) from one object or cell and apply it to another.
Lookup Array	In XLOOKUP, the range or column where Excel searches for the specified lookup value.
Mixed Reference	A reference that has either an absolute column and relative row (e.g., $A1) or an absolute row and relative column (e.g., A$1).
Operator	A symbol used in a formula to perform a mathematical or logical operation, such as +, -, *, or ^.
R1C1 Reference Style	An alternative referencing style where both rows and columns are numbered, often used in macros to compute positions.
Relative Reference	A cell reference that adjusts automatically based on its new position when copied or moved.
Return Array	In XLOOKUP, the range or column from which the data will be retrieved once a match is found.
Spill	A feature where a formula (like XLOOKUP returning multiple columns) automatically fills adjacent cells with results.
Table Array	The range of cells that VLOOKUP searches; the lookup value must be in the leftmost column of this range.
Wildcard Match	A search mode (Mode 2 in XLOOKUP) that uses symbols like * (any number of characters) or ? (one character) to find partial matches.
XLOOKUP	A modern lookup function that can search in any direction and provides built-in error handling and exact match defaults.
