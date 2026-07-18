# KHARCHA

# 06_USER_FLOW.md

---

# Document Information

| Field | Value |
|--------|-------|
| Product | Kharcha |
| Tagline | Every Rupee Matters |
| Version | 1.0 |
| Status | Approved |
| Owner | Souvik Ghosh |
| Last Updated | 19-Jul-2026 |

---

# Purpose

This document defines how users interact with Kharcha to accomplish important tasks.

The goal of every user flow is to make financial management:

- Fast
- Simple
- Predictable
- Effortless

Every user journey should follow the product principles defined in **00_PRODUCT_PRINCIPLES.md**.

---

# User Flow Index

| Flow ID | User Flow | Priority | Frequency |
|----------|-----------|----------|-----------|
| UF-01 | First-Time User Onboarding | High | One Time |
| UF-02 | Returning User | Critical | Daily |
| UF-03 | Add Expense | Critical | Multiple Times Daily |
| UF-04 | Edit Expense | Medium | Occasionally |
| UF-05 | Delete Expense | Medium | Occasionally |
| UF-06 | View Insights | High | Weekly |
| UF-07 | Review Budget | High | Weekly / Monthly |
| UF-08 | Search Expenses | Medium | Occasionally |
| UF-09 | Manage Profile & Settings | Low | Rare |
| UF-10 | Forgot Password | Low | Rare |
| UF-11 | Logout | Low | Rare |

---

# UF-01 — First-Time User Onboarding

## Goal

Help a new user start tracking expenses in less than two minutes.

---

## Trigger

User opens Kharcha for the first time.

---

## Flow

```
Launch App

↓

Splash Screen

↓

Welcome Screen

↓

Sign Up / Google Login

↓

Set Monthly Budget

↓

Choose Default Categories

↓

Home Dashboard

↓

Contextual Tip

"Let's record your first expense."

↓

Add First Expense

↓

Success Message

↓

Continue Using Kharcha
```

---

## Postconditions

- Account created
- Budget saved
- Categories configured
- First expense recorded
- User reaches Home Dashboard

---

## Success Criteria

- Setup completed in under 2 minutes.
- User understands the app without reading a tutorial.

---

## Related Screens

- Splash
- Welcome
- Login
- Budget Setup
- Category Setup
- Home

---

# UF-02 — Returning User

## Goal

Allow users to quickly check their financial status.

---

## Trigger

User opens Kharcha.

---

## Flow

```
Open App

↓

Home Dashboard

↓

Review Today's Spending

↓

Review Budget

↓

Continue Using App
```

---

## Success Criteria

Users should understand their financial status within 5 seconds.

---

# UF-03 — Add Expense

## Goal

Record an expense in less than five seconds.

---

## Trigger

User taps the "+" button.

---

## Preconditions

- User is logged in.
- Categories exist.

---

## Flow

```
Home

↓

Tap +

↓

Select Category

↓

Enter Amount

↓

(Optional) Add Note

↓

Save

↓

Dashboard Updates

↓

Expense Added Successfully
```

---

## Postconditions

- Expense stored
- Budget recalculated
- Dashboard refreshed
- Recent Expenses updated
- Money Story updated

---

## Success Criteria

- Less than 5 seconds
- Maximum 3 user interactions
- Minimal typing

---

## Related Screens

- Home
- Add Expense
- Dashboard

---

# UF-04 — Edit Expense

## Goal

Correct previously entered expenses.

---

## Trigger

User selects an expense.

---

## Flow

```
Home

↓

Recent Expenses

↓

Select Expense

↓

Edit

↓

Update Information

↓

Save

↓

Dashboard Refresh
```

---

## Postconditions

- Expense updated
- Reports recalculated
- Budget updated

---

# UF-05 — Delete Expense

## Goal

Remove incorrect expenses safely.

---

## Trigger

User selects Delete.

---

## Flow

```
Home

↓

Recent Expenses

↓

Select Expense

↓

Delete

↓

Confirmation

↓

Expense Removed

↓

Dashboard Refresh
```

---

## Postconditions

- Expense deleted
- Budget updated
- Reports updated

---

# UF-06 — View Insights

## Goal

Help users understand spending habits.

---

## Trigger

User taps "Insights".

---

## Flow

```
Home

↓

Insights

↓

Monthly Summary

↓

Category Analysis

↓

Budget Status

↓

Money Story

↓

Return Home
```

---

## Success Criteria

Users should immediately understand:

- Total spending
- Highest spending category
- Budget status
- Spending trend

---

# UF-07 — Review Budget

## Goal

Help users stay within budget.

---

## Trigger

User taps Budget Card.

---

## Flow

```
Home

↓

Budget Card

↓

Budget Details

↓

Monthly Budget

↓

Category Budgets

↓

Budget Progress

↓

Return Home
```

---

## Success Criteria

Users immediately know:

- Budget remaining
- Budget percentage used
- Categories exceeding budget

---

# UF-08 — Search Expenses

## Goal

Quickly locate previous expenses.

---

## Trigger

User taps Search.

---

## Flow

```
Home

↓

Search

↓

Enter Keyword

↓

Results

↓

Expense Details
```

---

## Search Filters

- Category
- Amount
- Date

---

# UF-09 — Manage Profile & Settings

## Goal

Allow users to personalize Kharcha.

---

## Flow

```
Profile

↓

Settings

↓

Select Option

↓

Save

↓

Return
```

---

## Available Settings

- Dark Mode
- Notifications
- Change Password
- Logout

---

# UF-10 — Forgot Password

## Goal

Recover account access.

---

## Flow

```
Login

↓

Forgot Password

↓

Enter Email

↓

Receive Reset Link

↓

Create Password

↓

Login
```

---

# UF-11 — Logout

## Goal

Securely sign out.

---

## Flow

```
Profile

↓

Logout

↓

Confirmation

↓

Login Screen
```

---

# User Education Flow (UEF)

Kharcha teaches users progressively instead of showing long tutorials.

---

## UEF-01 — Welcome

Trigger:

First Login

Message:

> Welcome to Kharcha 👋
>
> Let's set up your budget in under a minute.

---

## UEF-02 — First Expense

Trigger:

First expense recorded.

Message:

> 🎉 Great start!
>
> Every expense helps you understand where your money goes.

---

## UEF-03 — Fifth Expense

Trigger:

After five expenses.

Message:

> You're building a great habit.
>
> Visit Insights to discover your spending patterns.

---

## UEF-04 — First Money Story

Trigger:

After seven days of usage.

Message:

> 📖 Your first Money Story is ready.
>
> Discover where every rupee went this week.

---

## UEF-05 — Budget Warning

Trigger:

80% budget used.

Message:

> ⚠️ You've used 80% of your monthly budget.
>
> Review your spending before the month ends.

---

# Navigation Rules

- Every important feature should be reachable within three taps.
- Expense entry should take less than five seconds.
- Frequently used actions should always remain visible.
- The interface should minimize typing.
- Users should never feel lost.
- Every completed action should provide immediate feedback.

---

# User Flow Dependency Diagram

```
Launch App
     │
     ▼
UF-01 First-Time User
     │
     ▼
UF-02 Returning User
     │
     ├──────────────┐
     ▼              ▼
UF-03          UF-06
Add Expense    View Insights
     │              │
     ▼              ▼
UF-07        UF-08
Review Budget Search
     │
     ▼
UF-09 Profile
     │
     ├──────┐
     ▼      ▼
UF-10    UF-11
Forgot   Logout
Password
```

---

# Success Criteria

The user flow is considered successful if users can:

- Complete onboarding in under 2 minutes.
- Add an expense in under 5 seconds.
- Understand their financial status immediately.
- Stay within budget using timely reminders.
- Build a daily expense tracking habit.
- Understand their spending through Insights and Money Story.

---

# Guiding Principle

Every user journey should answer one question:

> **"How can we help the user achieve their goal with the fewest possible steps?"**

If a flow feels complicated, it should be redesigned until it becomes simple.
