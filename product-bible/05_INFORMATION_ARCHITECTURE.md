# KHARCHA

# 05_INFORMATION_ARCHITECTURE.md

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

This document defines the overall structure of the Kharcha application.

Its objective is to organize all features into logical sections, making navigation simple, intuitive, and scalable.

The architecture follows the principles defined in **00_PRODUCT_PRINCIPLES.md**, especially:

- Less Typing, More Tapping
- Five-Second Rule
- Simplicity Is a Feature
- Busy People Come First

---

# Navigation Philosophy

Kharcha should never feel overwhelming.

The most frequently used actions should always be one tap away.

Users should never need more than three taps to reach any important feature.

---

# Application Structure

```
Kharcha

├── Authentication
│
├── Home
│
├── Reports
│
├── Budget
│
├── Profile
│
└── Settings
```

---

# Module 1 — Authentication

Purpose:

Allow users to securely access their data.

### Screens

- Splash Screen
- Welcome Screen
- Login
- Register
- Google Sign In
- Forgot Password

---

# Module 2 — Home

Purpose:

Provide an instant overview of the user's financial status.

This is the primary screen users will visit every day.

## Sections

### Greeting

Examples:

Good Morning ☀️

Good Evening 🌙

---

### Monthly Summary

Displays:

- Today's Expense
- Monthly Expense
- Remaining Budget

---

### Quick Add Expense

One-tap access to expense entry.

---

### Frequently Used Categories

Examples:

🍔 Food

🚌 Travel

🛒 Grocery

☕

💊 Medical

🎬 Entertainment

---

### Recent Expenses

Shows the latest transactions.

Each item displays:

- Category
- Amount
- Date

---

### Money Story Preview

Example:

> "You've spent 15% less than last month."

Selecting this section opens the full Money Story page.

---

# Module 3 — Expense Management

Purpose:

Allow users to manage daily expenses quickly.

### Features

- Add Expense
- Edit Expense
- Delete Expense
- Search Expense
- Filter Expenses
- Notes
- Custom Categories

---

# Module 4 — Reports

Purpose:

Help users understand spending behavior.

## Sections

- Daily Report
- Monthly Report
- Category Analysis
- Spending Trends
- Money Story

Future:

- Yearly Report
- AI Insights

---

# Module 5 — Budget

Purpose:

Help users stay within spending limits.

### Features

- Monthly Budget
- Budget Remaining
- Budget Progress
- Category Budgets
- Budget Alerts

---

# Module 6 — Notifications

Purpose:

Encourage healthy financial habits.

### Types

- Daily Reminder
- Budget Warning
- Salary Day Reminder

---

# Module 7 — Profile

Purpose:

Store user information.

### Sections

- Profile Information
- Account Settings
- Logout

---

# Module 8 — Settings

Purpose:

Allow users to personalize the application.

### Options

- Dark Mode
- Light Mode
- Change Password
- Notification Preferences
- Privacy Settings
- About Kharcha

---

# Navigation Structure

## Bottom Navigation

The application uses five primary tabs.

```
Home

Reports

+

Budget

Profile
```

The center **+** button is dedicated to adding a new expense.

This action should always remain visible because adding expenses is the application's primary use case.

---

# Quick Add Flow

```
Dashboard

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
```

Target completion time:

**Less than 5 seconds**

---

# Information Hierarchy

Priority 1

- Add Expense
- Today's Expense
- Remaining Budget

Priority 2

- Recent Expenses
- Monthly Summary
- Budget Progress

Priority 3

- Reports
- Money Story
- Settings

---

# User Journey

First-Time User

```
Splash

↓

Welcome

↓

Register/Login

↓

Create Monthly Budget

↓

Choose Default Categories

↓

Home Dashboard

↓

Add First Expense

↓

Dashboard Updated

↓

Continue Daily Tracking
```

Returning User

```
Open App

↓

Home Dashboard

↓

Tap +

↓

Add Expense

↓

Dashboard Updates

↓

Close App
```

Weekly User

```
Home

↓

Reports

↓

Money Story

↓

Budget Review
```

---

# Future Expansion

The architecture allows future modules without changing the navigation.

Examples:

- Family Wallet
- Expense Split
- Subscription Tracker
- Savings Goals
- Investment Dashboard
- OCR Receipt Scanner
- Voice Expense Entry

---

# Architecture Principles

The information architecture follows these rules:

1. Every important action should be reachable within three taps.
2. Expense entry should take less than five seconds.
3. Frequently used features should remain visible.
4. Reports should explain spending instead of only displaying numbers.
5. The interface should remain clean and uncluttered.
6. Future features should integrate without disrupting the existing navigation.

---

# Success Criteria

The architecture is successful if users can:

- Open the app and immediately understand their financial status.
- Add an expense in under five seconds.
- Review spending without confusion.
- Find any important feature quickly.
- Build a habit of checking Kharcha daily.
