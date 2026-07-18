# KHARCHA

# 08_DATA_ARCHITECTURE.md

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

This document defines the complete data architecture of Kharcha.

It describes what information the application stores, why it is collected, and how it supports analytics, personalization, and future AI features.

The objective is to build a scalable data foundation rather than simply designing database tables.

---

# Data Strategy

Every piece of data collected must satisfy at least one objective.

• Operate the application

• Improve user experience

• Generate insights

• Train personalization models

• Enable AI-powered recommendations

If a field has no purpose, it should not be collected.

---

# Core Business Entities

## User

Purpose

Represents the account owner.

Key Attributes

- User ID
- Name
- Email
- Login Provider
- Currency
- Country
- City
- Salary Cycle
- Created Date

---

## Financial Profile

Purpose

Represents the user's financial background.

Attributes

- Monthly Salary
- Salary Date
- Occupation
- Employment Type
- Monthly Budget
- Savings Goal
- Emergency Fund Goal
- Preferred Budget Method

---

## Expense

Purpose

Stores every spending activity.

Attributes

- Expense ID
- Amount
- Category
- Payment Method
- Date
- Time
- Notes
- Merchant (optional)
- Location (optional)

---

## Category

Purpose

Organizes spending.

Attributes

- Category ID
- Name
- Icon
- Color
- Monthly Budget

---

## Budget

Purpose

Tracks spending limits.

Attributes

- Monthly Budget
- Category Budget
- Remaining Budget
- Percentage Used

---

## Insight

Purpose

Stores generated analytics.

Examples

- Monthly Spending
- Highest Category
- Weekly Trend
- Average Daily Expense

---

## Money Story

Purpose

Stores AI-generated monthly summaries.

Attributes

- Story ID
- Month
- Story Text
- Highlights
- Warnings
- Achievements

---

## Financial Health

Purpose

Measures financial wellness.

Attributes

- Overall Score
- Savings Score
- Budget Score
- Spending Score
- Trend

---

# Entity Relationships

User

↓

Financial Profile

↓

Budget

↓

Expenses

↓

Insights

↓

Money Story

↓

Financial Health

---

# Data Collection Strategy

## During Signup

Collect

- Name
- Email

Nothing else.

---

## After Login

Collect

- Salary
- Budget

---

## During Daily Usage

Collect

- Expenses
- Categories
- Notes

---

## After One Week

Generate

- Spending Insights

---

## After One Month

Generate

- Money Story

Financial Health

---

# AI Data Model

Future AI features require additional signals.

Examples

Lifestyle

- Rent
- Own House
- Student
- Married
- Dependents

Financial Goals

- Vacation
- Bike
- House
- Emergency Fund

Behavior

- Weekend Spending
- Recurring Expenses
- Spending Frequency
- Savings Consistency

---

# Privacy Principles

Kharcha should only collect data that creates value.

User trust is more important than data quantity.

Principles

- Privacy by Default
- User Ownership
- Transparent AI
- Explainable Recommendations
- Secure Storage

---

# Future Expansion

Version 2

- Recurring Bills
- Subscription Tracking

Version 3

- AI Financial Coach
- Smart Budget Planner
- Spending Prediction
- Savings Forecast

Version 4

- Family Finance
- Shared Wallets
- Investment Tracking

---

# CEO Principles

Data is not collected because we can.

Data is collected because it improves the user's financial life.

Every new field added to the database should answer one question:

"What better decision can Kharcha help the user make because of this information?"
