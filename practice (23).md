# 📊 Google Sheets Bootcamp – Module 3

# 🧮 Formulas & Functions (Complete Study Notes)

> **Status:** ⬜ Not Started
> **Difficulty:** ⭐⭐⭐☆☆ (Beginner → Intermediate)
> **Duration:** 2–3 Hours
>
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
