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

This document defines how users move through Kharcha to accomplish important tasks.

Every user flow should be:

- Simple
- Fast
- Predictable
- Require minimal typing

Following the product principles, every important task should require as few steps as possible.

---

# User Journey Overview

```
Open App
      │
      ▼
Authentication
      │
      ▼
Home Dashboard
      │
      ├───────────────┐
      ▼               ▼
Add Expense      View Insights
      │               │
      ▼               ▼
Dashboard Updates  Reports
      │
      ▼
Close App
```

---

# Flow 1 — First-Time User

Goal:

Allow a new user to start tracking expenses in less than two minutes.

```
Open App

↓

Splash Screen

↓

Welcome Screen

↓

Sign Up

↓

Google / Email Login

↓

Create Monthly Budget

↓

Select Default Categories

↓

Home Dashboard

↓

Add First Expense

↓

Success Message

↓

Continue Using Kharcha
```

Expected completion time:

**Less than 2 minutes**

---

# Flow 2 — Returning User

Goal:

Allow users to record expenses as quickly as possible.

```
Open App

↓

Home Dashboard

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

Continue Using App
```

Expected completion time:

**Less than 5 seconds**

---

# Flow 3 — Edit an Expense

```
Home

↓

Recent Expenses

↓

Select Expense

↓

Edit

↓

Update Amount / Category / Note

↓

Save

↓

Dashboard Updates
```

---

# Flow 4 — Delete an Expense

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

Dashboard Updates
```

---

# Flow 5 — View Insights

Goal:

Help users understand their spending.

```
Home

↓

Insights

↓

Monthly Overview

↓

Category Analysis

↓

Money Story

↓

Return Home
```

---

# Flow 6 — Review Budget

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

# Flow 7 — Search Expenses

```
Home

↓

Search

↓

Enter Keyword

↓

Results

↓

Select Expense

↓

View Details
```

---

# Flow 8 — Change Settings

```
Profile

↓

Settings

↓

Choose Option

↓

Save Changes

↓

Return
```

---

# Flow 9 — Forgot Password

```
Login

↓

Forgot Password

↓

Enter Email

↓

Receive Reset Link

↓

Create New Password

↓

Login

↓

Home
```

---

# Flow 10 — Logout

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

# Daily User Flow

Most users will follow this journey several times each day.

```
Open App

↓

View Dashboard

↓

Tap +

↓

Food

↓

₹120

↓

Save

↓

Dashboard Updates

↓

Close App
```

Target time:

**Under 5 seconds**

---

# Weekly User Flow

```
Open App

↓

Home

↓

Insights

↓

Money Story

↓

Budget Review

↓

Close App
```

---

# Monthly User Flow

```
Open App

↓

Home

↓

Budget Review

↓

Insights

↓

Monthly Money Story

↓

Adjust Budget

↓

Close App
```

---

# Navigation Rules

Every flow should follow these principles:

- Maximum three taps to reach an important feature.
- Expense entry should require minimal typing.
- Frequently used actions remain easily accessible.
- Users should never feel lost.
- Every completed action should provide immediate feedback.

---

# Success Criteria

A successful user flow means users can:

- Add an expense in under five seconds.
- Find any important feature quickly.
- Understand their spending without confusion.
- Stay engaged with the app over time.
- Build a consistent expense tracking habit.

---

# Future User Flows

The architecture supports future additions without changing existing flows.

Examples:

- Family Wallet
- Split Expenses
- Voice Entry
- OCR Receipt Scanning
- AI Financial Coach
- Subscription Tracking
- Savings Goals

These flows will be documented separately when they become part of the product roadmap.
