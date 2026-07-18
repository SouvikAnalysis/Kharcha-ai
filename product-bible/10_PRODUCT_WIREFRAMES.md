# KHARCHA

# 10_PRODUCT_WIREFRAMES.md

---

# Document Information

| Field | Value |
|--------|-------|
| Product | Kharcha |
| Tagline | Every Rupee Matters |
| Version | 1.0 |
| Status | Approved |
| Owner | Souvik Ghosh |

---

# Purpose

This document defines the structural layout of every major screen in Kharcha.

Wireframes focus on:

- Information hierarchy
- User actions
- Navigation
- Content placement

Visual styling is defined separately in the Design System.

---

# Wireframing Principles

Every wireframe must answer:

1. What does the user need first?
2. What is the primary action?
3. What information is most important?
4. Can the user complete their task quickly?

---

# Screen Priority

| Priority | Screen |
|----------|--------|
| P1 | Home Dashboard |
| P1 | Add Expense |
| P1 | Insights |
| P1 | Budget |
| P2 | Expense Details |
| P2 | Search |
| P2 | Profile |
| P2 | Settings |
| P3 | AI Money Story |
| P3 | AI Coach |

---

# WF-01 — Splash Screen

Purpose

Create a memorable first impression.

Layout

```
+------------------------+
|                        |
|        LOGO            |
|                        |
|     Every Rupee        |
|       Matters          |
|                        |
+------------------------+
```

---

# WF-02 — Welcome Screen

```
+------------------------+
|      Illustration      |
|                        |
| Welcome to Kharcha     |
|                        |
| Track smarter.         |
| Spend wisely.          |
|                        |
|  Continue with Google  |
|                        |
|  Continue with Email   |
+------------------------+
```

---

# WF-03 — Home Dashboard (Most Important)

Purpose

Users should understand their financial situation in under five seconds.

```
+--------------------------------+
| 👋 Good Evening, Souvik        |
|-------------------------------|
| Financial Health     86/100    |
|-------------------------------|
| Salary        ₹37,500          |
| Spent         ₹22,100          |
| Remaining     ₹15,400          |
|-------------------------------|
| Today's Spending              |
| ₹820                          |
|-------------------------------|
| Budget Progress               |
| ███████░░░                    |
|-------------------------------|
| AI Daily Insight              |
| "Food spending is lower..."   |
|-------------------------------|
| Recent Expenses               |
| • Swiggy       ₹320           |
| • Uber         ₹250           |
| • Grocery      ₹480           |
|-------------------------------|
|        💰 Add Expense         |
|-------------------------------|
| Home Insights Profile         |
+--------------------------------+
```

---

# WF-04 — Add Expense

```
+----------------------------+
| Add Expense               |
|---------------------------|
| Amount                    |
| ₹________                 |
|---------------------------|
| Category                  |
| 🍔 Food                   |
|---------------------------|
| Date                      |
| Today                     |
|---------------------------|
| Notes (Optional)          |
|___________________________|
|                           |
|       Save Expense        |
+----------------------------+
```

Signature Interaction

After tapping **Save Expense**:

💰 Coin animation

↓

Wallet animation

↓

Dashboard updates

↓

Expense Added

---

# WF-05 — Insights

```
+------------------------------+
| Monthly Spending            |
|-----------------------------|
| Donut Chart                 |
|                             |
| Food       35%              |
| Travel     18%              |
| Shopping   14%              |
|-----------------------------|
| Weekly Trend                |
| Line Chart                  |
|-----------------------------|
| AI Summary                  |
|-----------------------------|
| Money Story                 |
+------------------------------+
```

---

# WF-06 — Budget

```
+---------------------------+
| Monthly Budget           |
|--------------------------|
| ₹40,000                 |
|--------------------------|
| Used                    |
| ₹26,000                 |
|--------------------------|
| Remaining               |
| ₹14,000                 |
|--------------------------|
| Progress Ring           |
|--------------------------|
| Category Budgets        |
+--------------------------+
```

---

# WF-07 — Money Story (Signature Screen)

Purpose

This should become Kharcha's most memorable experience.

```
+----------------------------------+
| 📖 July Money Story             |
|---------------------------------|
| Salary       ₹37,500            |
| Expenses     ₹30,200            |
| Savings      ₹7,300             |
|---------------------------------|
| Biggest Win                    |
| Food spending down 18%          |
|---------------------------------|
| Biggest Risk                   |
| Shopping up 24%                 |
|---------------------------------|
| AI Recommendation               |
| Save ₹1,500 next month by...    |
|---------------------------------|
| Financial Health               |
| 86 / 100                       |
+----------------------------------+
```

---

# WF-08 — AI Financial Coach

```
+--------------------------------+
| 🤖 Kharcha AI                 |
|-------------------------------|
| Good evening 👋              |
|-------------------------------|
| Today's Advice               |
|-------------------------------|
| Budget Alert                 |
|-------------------------------|
| Suggested Action             |
|-------------------------------|
| Ask Kharcha AI               |
|______________________________|
+--------------------------------+
```

---

# Navigation Flow

Splash

↓

Welcome

↓

Login

↓

Home

├── Add Expense

├── Insights

├── Budget

├── Profile

└── Search

---

# Wireframe Principles

Every screen should:

- Have one primary action.
- Minimize typing.
- Prioritize financial clarity.
- Use consistent layouts.
- Follow the Design System.

---

# Future Wireframes

Version 2

- Financial Health
- Recurring Bills
- Money Story

Version 3

- AI Coach
- Smart Budget Planner
- Savings Planner
- Predictive Spending

---

# CEO Vision

Every wireframe should answer one question:

"What is the fastest way to help users make a better financial decision?"
