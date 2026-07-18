# KHARCHA

# 11_UI_COMPONENT_LIBRARY.md

---

# Document Information

| Field | Value |
|--------|-------|
| Product | Kharcha |
| Version | 1.0 |
| Status | Approved |
| Owner | Souvik Ghosh |

---

# Purpose

This document defines all reusable UI components used throughout Kharcha.

Goals:

- Consistency
- Faster development
- Better maintainability
- Reusable Flutter widgets
- Design consistency

---

# Design Philosophy

Every component should be:

- Simple
- Reusable
- Accessible
- Responsive
- AI-ready

---

# Component Categories

1. Navigation Components
2. Cards
3. Buttons
4. Input Components
5. Lists
6. Charts
7. Feedback Components
8. AI Components
9. Loading Components
10. Empty States

---

# Navigation Components

## App Bar

Purpose

Provide screen title and navigation.

Properties

- Title
- Back Button
- Action Icons

Used In

- Insights
- Settings
- Profile
- Search

---

## Bottom Navigation Bar

Tabs

🏠 Home

📊 Insights

👤 Profile

Floating Button

💰 Add Expense

---

# Cards

## Financial Health Card

Purpose

Display overall financial score.

Contains

- Score
- Trend
- Status
- Recommendation

Used In

- Home
- Financial Health

---

## Budget Intelligence Card ⭐

Purpose

Replace the traditional budget progress bar.

Contains

- Budget Left
- Time Progress
- Budget Progress
- Safe Daily Spend
- AI Recommendation

Example

Time Progress

██████░░░░

Budget Progress

████░░░░░░

Safe Today

₹1,280

Status

✅ On Track

---

## Today's Snapshot Card

Contains

- Today's Spending
- Remaining Budget
- Monthly Expenses

---

## AI Insight Card

Contains

- Daily Insight
- Smart Tip
- Action Button

Example

💡

"Cooking twice this week could save ₹900."

Button

Learn More

---

## Expense Card

Contains

- Category Icon
- Merchant
- Amount
- Date
- Notes

Actions

Edit

Delete

---

# Buttons

## Primary Button

Purpose

Main call-to-action.

Examples

- Login
- Save Expense
- Continue

---

## Secondary Button

Examples

- Cancel
- Skip

---

## Floating Action Button

Purpose

Quick Add Expense

Icon

💰

Signature Animation

Coin Drop

---

# Input Components

## Amount Field

Properties

- Currency Prefix
- Numeric Keyboard
- Validation

---

## Category Selector

Type

Bottom Sheet

---

## Date Picker

Default

Today

---

## Notes Field

Optional

Maximum

250 Characters

---

# Charts

## Donut Chart

Purpose

Category Breakdown

---

## Line Chart

Purpose

Weekly Spending

---

## Bar Chart

Purpose

Monthly Comparison

---

# Search Components

Search Bar

Recent Searches

Filters

Search Results

---

# AI Components

## AI Daily Insight

Frequency

Daily

---

## Smart Recommendation Card

Contains

- Problem
- Recommendation
- Expected Saving

---

## Money Story Preview

Contains

- Monthly Summary
- Open Button

---

## AI Coach Chat Card

Contains

Question

Response

Suggested Actions

---

# Feedback Components

Success Snackbar

Expense Added

Coin Animation

---

Error Dialog

Validation Errors

---

Confirmation Dialog

Delete Expense

---

# Loading Components

Splash Loader

Skeleton Cards

Progress Indicator

---

# Empty States

No Expenses

No Budget

No Search Results

No Insights Yet

---

# Accessibility

Every component must support:

- Screen Readers
- Dynamic Text
- High Contrast
- Large Touch Targets
- Keyboard Navigation

---

# Flutter Mapping

Every component should have its own widget.

Example

FinancialHealthCard

BudgetIntelligenceCard

ExpenseCard

AIInsightCard

PrimaryButton

CategoryChip

SearchBar

BottomNavigation

FloatingExpenseButton

MoneyStoryCard

---

# Reusability Rules

Never duplicate components.

If a UI element appears more than once,

it becomes a reusable component.

---

# CEO Vision

We do not build screens.

We build reusable experiences.

Every reusable component reduces future development effort, improves consistency, and makes Kharcha easier to scale.
