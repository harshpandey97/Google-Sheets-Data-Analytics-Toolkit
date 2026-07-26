📖 Automation Module Notes & Practice Guide
Exercise 1: Record a Macro for Automated Formatting
Concept: A Macro records your repetitive actions (formatting, alignment, font changes) into reusable code without requiring you to write any Apps Script manually.

Step-by-Step Instructions:
Prepare Raw Data Dump:

In cells A1:C4, enter raw data:

A1:C1: Item | Quantity | Price

A2:C2: Keyboard | 15 | 45

A3:C3: Mouse | 30 | 20

A4:C4: Monitor | 10 | 150

Start Recording:

Go to Extensions → Macros → Record macro.

Select Use relative references (this allows you to apply the macro to any range, not just A1:C4).

Perform Formatting Actions:

Highlight A1:C1 → set fill color to Dark Blue, text color to White, and make text Bold.

Highlight C2:C4 → set format to Currency (Format > Number > Currency).

Highlight A1:C4 → apply All Borders.

Save Macro:

Click Save in the bottom Macro panel.

Name the macro: FormatDataDump.

Assign a shortcut if prompted (e.g., Ctrl + Alt + Shift + 1) and click Save.

Exercise 2: Write a Custom Apps Script Function (=DISCOUNT)
Concept: Custom functions allow you to extend Google Sheets' built-in formulas using JavaScript in Google Apps Script.

Step-by-Step Instructions:
Open Apps Script Editor:

In the top menu, click Extensions → Apps Script.

Delete any default code in the editor (Code.gs).

Paste Custom Function Code:

JavaScript
/**
 * Calculates the discounted price given a base price and discount percentage.
 * 
 * @param {number} price The original price of the item.
 * @param {number} pct The discount percentage (e.g., 10 for 10% or 0.10).
 * @return The final discounted price.
 * @customfunction
 */
function DISCOUNT(price, pct) {
  if (typeof price !== 'number' || typeof pct !== 'number') {
    return "Invalid Input";
  }

  // Convert percentage if entered as a whole number (e.g., 10 instead of 0.10)
  var discountDecimal = pct > 1 ? pct / 100 : pct;

  return price - (price * discountDecimal);
}
Save Script:

Click the Save icon (floppy disk) at the top or press Ctrl + S.

Test Function in Sheet:

Return to your Automation tab.

In cell E1, type Original Price → in E2, enter 100.

In cell F1, type Discount % → in F2, enter 15.

In cell G1, type Final Price → in cell G2, enter the custom formula:

Excel
=DISCOUNT(E2, F2)
Result: Cell G2 displays 85.

Exercise 3: Set Up a Time-Driven Trigger (Daily Execution)
Concept: Triggers allow Apps Script to execute automatically on a scheduled basis (e.g., daily, hourly) without manual intervention.

Step-by-Step Instructions:
Add Daily Task Code to Apps Script:

Reopen the Apps Script editor (Extensions > Apps Script).

Add the following function below your =DISCOUNT function:

JavaScript
function dailyAutomatedTask() {
  var sheet = SpreadsheetApp.getActiveSpreadsheet().getSheetByName("Automation");
  if (sheet) {
    sheet.getRange("I1").setValue("Last Automated Run: " + new Date().toLocaleString());
  }
}
Save the script (Ctrl + S).

Configure Time-Driven Trigger:

On the left sidebar of the Apps Script editor, click the Triggers icon (looks like an alarm clock Θ).

Click + Add Trigger (bottom-right corner).

Configure options:

Choose which function to run: dailyAutomatedTask

Select event source: Time-driven

Select type of time based trigger: Day timer

Select time of day: Choose preferred hour interval (e.g., Midnight to 1am or 8am to 9am).

Click Save (you may be prompted to grant authorization permissions for your Google account).

Final Check & Submission
Ensure the Automation tab contains:

Formatted sales data table (Macro output).

Working =DISCOUNT() custom formula.

Running/configured Apps Script trigger.

Click Share (top-right corner) → Set access to Anyone with the link.

Click Copy link and submit your link!
