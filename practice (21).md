# Data Entry & Formatting — Practice Notes

Module: Data Entry & Formatting (Google Sheets)

---

## Exercise 1: Format a sample table (bold headers, borders, alternating row colors)

**Sample table structure:**

| Employee ID | Name | Department | Sales Amount ($) |
|---|---|---|---|
| 101 | Rohan Sharma | Sales | 45000 |
| 102 | Priya Singh | Marketing | 62000 |
| 103 | Amit Kumar | IT | 28000 |

**Steps in Google Sheets:**

1. **Bold headers** — Select header row → `Ctrl+B` (or Format → Bold). Optionally add a fill color: select row → click the paint-bucket icon → pick a dark color → set text color to white for contrast.
2. **Borders** — Select the full table range → click the Borders icon in the toolbar → choose "All borders." Use a light gray thin border so it doesn't overpower the data.
3. **Alternating row colors** — Select the data range (excluding header, or including it) → `Format → Alternating colors` → pick a built-in theme or "Custom colors" → set header style and two alternating band colors → Done.

**Why it matters:** this is the baseline "readable sheet" look — recruiters and reviewers judge data hygiene by this first.

---

## Exercise 2: Conditional formatting — highlight values above/below a threshold

**Steps:**

1. Select the numeric column (e.g., `Sales Amount`, range `D2:D16`).
2. `Format → Conditional formatting` → in the side panel, under "Format rules," choose **"Greater than"** → enter `50000` → set fill color (green) → Done.
3. Click **"+ Add another rule"** → choose **"Less than"** → enter `20000` → set fill color (red) → Done.

**Result:** any Sales Amount above 50000 turns green, below 20000 turns red — a quick visual scan for outliers, without touching the raw numbers.

---

## Exercise 3: Custom formula in conditional formatting — highlight duplicate rows

Google Sheets' built-in duplicate check only works well on a single column. To flag **whole duplicate rows** (all columns match), you need a custom formula rule.

**Steps:**

1. Select the full data range, e.g. `A2:D16`.
2. `Format → Conditional formatting` → under "Format rules," choose **"Custom formula is."**
3. Enter this formula:
   ```
   =COUNTIFS($A$2:$A$16,$A2,$B$2:$B$16,$B2,$C$2:$C$16,$C2,$D$2:$D$16,$D2)>1
   ```
4. Set fill color (amber/yellow works well) → Done.

**How the formula works:**
- `COUNTIFS` checks all four columns (ID, Name, Department, Sales Amount) together for each row.
- If a row's exact combination appears **more than once** anywhere in the range, `COUNTIFS(...)>1` returns `TRUE`, and the whole row gets highlighted.
- The `$` locks the range so it doesn't shift as the rule is applied row by row, while `$A2` (no `$` on the row number) lets the check move down with each row.

**Simpler variant** — if you only want to flag duplicate IDs (single column), just use:
```
=COUNTIF($A$2:$A$16,A2)>1
```
applied to range `A2:A16`.

---

## Quick reference — menu paths used

| Task | Menu path |
|---|---|
| Bold / fill color | `Format → Bold` or paint-bucket icon |
| Borders | Toolbar → Borders icon |
| Alternating colors | `Format → Alternating colors` |
| Threshold highlight | `Format → Conditional formatting → Greater than / Less than` |
| Custom formula highlight | `Format → Conditional formatting → Custom formula is` |

---

## Sheet link
`(paste your Google Sheet link here once created)`
