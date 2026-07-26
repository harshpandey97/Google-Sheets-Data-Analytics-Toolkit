# Google Sheets — Data Entry & Formatting Basics

> 💡 **Workflow at a glance:** Correct data entry → Cell formatting → Conditional formatting → Themes/banded rows → Report-ready sheet. Each stage builds on the last — skipping data entry correctness breaks conditional formatting rules downstream.

## 1. Entering Text, Numbers, and Dates Correctly

Google Sheets auto-detects data type based on how you type it. Getting this wrong is the #1 cause of broken formulas later (SUM returning 0, dates not sorting properly, etc.).

<img width="1440" height="680" alt="image" src="https://github.com/user-attachments/assets/cbb09ac0-fc80-4a9b-96e4-383862ea0c27" />

**Numbers**
- Type plainly: `1000`, not `1,000` or `Rs. 1000` — these become text.
- If you need a number stored as text (e.g., a Pincode starting with 0, or Phone number), prefix with an apostrophe: `'011234` → keeps leading zero, stored as text.
- Check alignment as a quick test: numbers auto-align **right**, text auto-aligns **left**. If a number is left-aligned, it's actually text — formulas like SUM will silently ignore it.

**Dates**
- Type in a recognizable format: `26/07/2026` or `07/26/2026` (depends on Sheet's locale setting under File → Settings).
- Dates auto-align right when entered correctly (Sheets stores them as serial numbers internally).
- Avoid typing dates as plain text like `26th July` — Sheets won't recognize it as a date, breaking `DATEDIF`, sorting, and filters.

**Common fix for text-formatted numbers**
- Select range → `Data` → `Data cleanup` → `Text to columns` (splits and often auto-corrects type)
- Or use `=VALUE(A1)` in a helper column to force conversion.

---

## 2. Cell Formatting: Bold, Font Color, Fill Color, Borders

Located in the toolbar or `Format` menu:

| Element | Toolbar Icon | Use Case |
|---|---|---|
| **Bold** | `B` | Headers, key totals, KPIs |
| **Font Color** | `A` with underline | Negative values in red, highlights |
| **Fill Color** | Paint bucket icon | Section headers, status backgrounds |
| **Borders** | Grid icon | Separating table sections, print-ready sheets |

<img width="1580" height="980" alt="image" src="https://github.com/user-attachments/assets/bead7a3c-3d4a-4753-b8e4-da34c593a2c2" />


**Best practice for dashboards/reports:**
- Bold + fill color for header row (e.g., dark blue fill, white bold text)
- Borders only where needed (all-borders on every cell looks cluttered — use outer border + header underline instead)
- Keep font color changes purposeful (red = negative/alert, green = positive/on-track) — don't overuse colors

---

## 3. Conditional Formatting

Path: `Format` → `Conditional formatting`

> 📊 **Usage note:** In most real dashboards, Single Color rules cover the majority of cases (status flags like "Delayed"/"Completed"), Color Scales are used for numeric heatmaps (sales, SLA%), and Custom Formula is reserved for cross-column logic (e.g., highlighting a full row based on another column's value).

**a) Single Color Rule**
- Apply to a range → choose condition (`Text is exactly`, `Greater than`, `Is not empty`, etc.) → set formatting style (fill/bold/font color) → Done
- Example: Highlight all cells in Status column where `Text is exactly` = `"Delayed"` → red fill

**b) Color Scale**
- Best for numeric ranges (sales figures, scores, SLA %)
- Sheets auto-applies a gradient (e.g., red → yellow → green) based on min/mid/max values
- Great for heatmap-style dashboards — no manual thresholds needed

**c) Custom Formula**
- Most powerful option — lets you reference other cells/columns
- Example: Highlight entire row if Column D (Delivery Status) = "Delayed":
  ```
  =$D1="Delayed"
  ```
  Apply this to range `A1:F100` (note the `$D1` — column locked, row relative — so it checks each row's own D value)

- Example: Highlight duplicate entries in column A:  
  ```
  =COUNTIF($A$1:$A100, A1) > 1
  ```

---

## 4. Themes & Alternating Row Colors (Readability)

**Alternating colors (banded rows):**
- Select range → `Format` → `Alternating colors`
- Choose a preset (or customize header/footer color separately)
- Improves readability for long datasets — eyes don't "lose the row" while scanning across many columns

**Themes:**
- `Format` → `Theme`
- Applies a consistent color palette + font pairing across the whole sheet (title, headers, body text)
- Useful for dashboards meant to be shared with stakeholders — gives a polished, non-default look without manual styling of every element

**Why this matters for analyst work:**
Clean formatting isn't cosmetic — in real jobs, a dashboard/report that's hard to scan gets ignored regardless of how correct the analysis is. Conditional formatting + banded rows are usually the fastest way to make raw data look review-ready.
