# 🤖 Automation in Google Sheets

<p align="center">

<img src="https://img.shields.io/badge/Google%20Sheets-Automation-34A853?style=for-the-badge&logo=googlesheets&logoColor=white"/>

<img src="https://img.shields.io/badge/Apps%20Script-JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black"/>

<img src="https://img.shields.io/badge/Macros-No%20Code-blue?style=for-the-badge"/>

<img src="https://img.shields.io/badge/Status-Completed-success?style=for-the-badge"/>

</p>

---

# 📚 Table of Contents

- 📖 Introduction
- ⚙️ What is Automation?
- 🖱️ Google Sheets Macros
- 💻 Google Apps Script
- 🔄 Triggers
- 🧩 Custom Functions
- 📊 Automation Workflow
- 🛠️ Real-World Examples
- 📈 Best Practices
- ❓ Interview Questions
- 🚀 Mini Projects
- 📂 Resources

---

# 📖 Introduction

Automation allows you to eliminate repetitive tasks and improve productivity by letting Google Sheets perform operations automatically.

Instead of manually formatting data, creating reports, sending emails, or updating dashboards, automation enables these tasks to run with a single click or on a scheduled basis.

Google Sheets supports automation through:

- 🖱️ Macros (No Coding)
- 💻 Google Apps Script (JavaScript)
- ⏰ Triggers
- 🧩 Custom Functions

---

# 🎯 Learning Objectives

After completing this module, you will be able to:

- ✅ Record Macros
- ✅ Edit Macro Scripts
- ✅ Understand Google Apps Script
- ✅ Create Custom Functions
- ✅ Automate Reports
- ✅ Schedule Tasks using Triggers
- ✅ Send Emails Automatically
- ✅ Build Smart Dashboards

---

# ⚙️ What is Automation?

Automation means performing repetitive work without manual intervention.

```text
Before Automation

Receive Data
      │
      ▼
Clean Data
      │
      ▼
Create Report
      │
      ▼
Format Report
      │
      ▼
Share Report
```

↓

```text
After Automation

Receive Data
      │
      ▼
Run Script
      │
      ▼
Everything Done Automatically ✅
```

---

# 🖱️ Google Sheets Macros

## What are Macros?

Macros record your actions and replay them whenever needed.

Think of them as a "Record → Stop → Replay" feature.

Perfect for:

- Formatting reports
- Cleaning datasets
- Applying filters
- Creating templates
- Repeating calculations

---

## Workflow

```text
Tools
    │
    ▼
Macros
    │
    ▼
Record Macro
    │
    ▼
Perform Actions
    │
    ▼
Save Macro
    │
    ▼
Run Anytime
```

---

## Example

Suppose every day you:

- Bold headers
- Change background color
- Apply currency formatting
- Freeze first row

Instead of doing it manually every day...

Simply run your Macro.

Done in seconds.

---

# 💻 Google Apps Script

## What is Apps Script?

Google Apps Script is Google's cloud-based JavaScript platform for automating Google Workspace.

It can interact with:

- Google Sheets
- Google Docs
- Gmail
- Google Drive
- Google Forms
- Google Calendar

---

## Architecture

```text
Google Sheets

       │

       ▼

Apps Script (JavaScript)

       │

       ▼

Automation

       │

       ├── Send Emails

       ├── Create Reports

       ├── Generate PDFs

       ├── Update Dashboard

       ├── Import Data

       └── Schedule Tasks
```

---

# 🚀 Opening Apps Script

Inside Google Sheets

```
Extensions

↓

Apps Script
```

Google automatically creates:

```javascript
function myFunction() {

}
```

---

# ✨ Example 1 — Hello World

```javascript
function helloWorld(){

SpreadsheetApp.getUi()

.alert("Hello Harsh!");

}
```

Output

```
Hello Harsh!
```

---

# 📊 Example 2 — Add Current Date

```javascript
function addDate(){

var sheet = SpreadsheetApp.getActiveSheet();

sheet.getRange("A1").setValue(new Date());

}
```

Output

```
07/28/2026
```

(Current date when executed.)

---

# 📧 Example 3 — Send Email

```javascript
function sendMail(){

MailApp.sendEmail(

"example@gmail.com",

"Monthly Report",

"Report Generated Successfully"

);

}
```

---

# 📄 Example 4 — Create Custom Menu

```javascript
function onOpen(){

SpreadsheetApp.getUi()

.createMenu("Automation")

.addItem("Run Report","runReport")

.addToUi();

}
```

Output

```
Automation

↓

Run Report
```

---

# 🧩 Custom Functions

Apps Script allows you to create your own spreadsheet formulas.

Example

```javascript
function DISCOUNT(price){

return price*0.9;

}
```

Inside Sheets

```excel
=DISCOUNT(A2)
```

Output

```
10% Discount Applied
```

---

# ⏰ Triggers

Triggers execute scripts automatically.

Types

| Trigger | Purpose |
|----------|----------|
| On Open | Run when spreadsheet opens |
| On Edit | Run after editing |
| On Change | Run after structure changes |
| Time-driven | Hourly / Daily / Weekly |
| Form Submit | After Google Form submission |

---

## Workflow

```text
Trigger

      │

      ▼

Apps Script

      │

      ▼

Task Executes Automatically
```

---

# 📈 Real-World Automation Examples

## 📊 Daily Sales Report

Every morning

↓

Import latest sales

↓

Update Dashboard

↓

Generate Charts

↓

Send Email

---

## 📦 Inventory Automation

When stock falls below threshold

↓

Highlight Row

↓

Send Email Alert

↓

Notify Manager

---

## 📋 HR Dashboard

Employee joins

↓

Update Sheet

↓

Create ID

↓

Send Welcome Email

---

## 📧 Automated Reporting

```text
Database

↓

Google Sheets

↓

Apps Script

↓

Dashboard

↓

Email PDF

↓

Management
```

---

# 📊 Automation vs Manual Work

| Manual | Automated |
|---------|-----------|
| Slow | Fast ⚡ |
| Error-Prone | Accurate ✅ |
| Repetitive | One Click |
| Time Consuming | Scheduled |
| Human Dependency | Automatic |

---

# 🚀 Mini Projects

## Beginner

- Auto Timestamp
- Attendance Tracker
- Expense Calculator

---

## Intermediate

- Email Report Generator
- Inventory Manager
- Sales Dashboard Automation
- Invoice Generator

---

## Advanced

- CRM Automation
- HR Dashboard
- Employee Tracker
- Google Form Automation
- AI Report Generator

---

# 💡 Best Practices

✅ Write reusable scripts

✅ Add comments

✅ Test before deployment

✅ Handle errors

✅ Use meaningful function names

✅ Avoid duplicate code

✅ Keep scripts modular

---

# 🎯 Common Use Cases

- 📊 Business Reporting
- 💰 Financial Analysis
- 📦 Inventory Management
- 👥 HR Analytics
- 📈 Sales Dashboards
- 📧 Automated Emails
- 📄 PDF Report Generation
- 📅 Scheduling Tasks
- 🤖 Workflow Automation

---

# ❓ Interview Questions

### Q1. What is a Macro?

A recorded sequence of actions that can be replayed to automate repetitive tasks.

---

### Q2. What language does Apps Script use?

JavaScript.

---

### Q3. What is a Trigger?

A mechanism that automatically executes a script based on an event or schedule.

---

### Q4. Difference between Macro and Apps Script?

| Macro | Apps Script |
|---------|-------------|
| No Coding | JavaScript Coding |
| Limited Features | Highly Flexible |
| UI Recording | Custom Automation |
| Simple Tasks | Advanced Workflows |

---

### Q5. Can Apps Script interact with Gmail?

✅ Yes.

It can send emails, attachments, reminders, and notifications.

---

# 📂 Practice Exercises

- [ ] Record a Macro for formatting a sales report.
- [ ] Create a custom function to calculate discounts.
- [ ] Write a script to insert today's date into a cell.
- [ ] Create a custom menu with Apps Script.
- [ ] Set up a time-driven trigger to run daily.
- [ ] Send an automated email after generating a report.
- [ ] Build a simple attendance automation sheet.

---

# 📚 Resources

- 🌐 Google Sheets
- 🌐 Google Apps Script
- 🌐 JavaScript
- 🌐 Google Workspace Documentation

---

# 🎓 Module Summary

| Feature | Covered |
|----------|----------|
| Macros | ✅ |
| Apps Script | ✅ |
| JavaScript Basics | ✅ |
| Custom Functions | ✅ |
| Triggers | ✅ |
| Automation Workflow | ✅ |
| Real-World Projects | ✅ |

---

<div align="center">

## ⭐ Automation saves time, reduces errors, and turns Google Sheets into a powerful productivity platform.

### If this repository helped you, consider giving it a ⭐ on GitHub!

**Made with ❤️ by Harsh Pandey**

</div>
