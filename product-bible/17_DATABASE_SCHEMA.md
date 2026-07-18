# KHARCHA

# 17_DATABASE_SCHEMA.md

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

This document defines the database schema used by Kharcha.

It specifies:

- Database structure
- Tables
- Relationships
- Constraints
- Indexes
- Data integrity rules

The goal is to ensure a scalable, secure, and maintainable database architecture.

---

# Database Overview

Database Engine

PostgreSQL

Architecture

Relational Database

Primary Key

UUID

Timezone

UTC

Soft Delete

Supported

Created / Updated Tracking

Supported

---

# Design Principles

The schema should be:

- Normalized
- Consistent
- Extensible
- Secure
- Performant
- AI-ready

---

# Entity Relationship Overview

Core Entities

Users

↓

Categories

↓

Expenses

↓

Budgets

↓

Financial Health

↓

Money Stories

↓

Notifications

↓

Goals

---

# Database Tables

1. users
2. categories
3. expenses
4. budgets
5. financial_health
6. money_stories
7. goals
8. notifications
9. ai_conversations
10. analytics_events

---

# users

Purpose

Store user information.

| Column | Type | Constraint |
|---------|------|------------|
| id | UUID | PK |
| full_name | VARCHAR(100) | NOT NULL |
| email | VARCHAR(255) | UNIQUE |
| password_hash | TEXT | NOT NULL |
| monthly_income | DECIMAL(12,2) | NULL |
| preferred_currency | VARCHAR(10) | DEFAULT 'INR' |
| timezone | VARCHAR(50) | DEFAULT 'Asia/Kolkata' |
| created_at | TIMESTAMP | NOT NULL |
| updated_at | TIMESTAMP | NOT NULL |
| deleted_at | TIMESTAMP | NULL |

Indexes

- email
- created_at

---

# categories

Purpose

Store default and custom categories.

| Column | Type |
|---------|------|
| id | UUID |
| user_id | UUID |
| name | VARCHAR(100) |
| icon | VARCHAR(50) |
| color | VARCHAR(20) |
| is_default | BOOLEAN |
| created_at | TIMESTAMP |

Relationship

One User → Many Categories

---

# expenses

Purpose

Store every expense.

| Column | Type |
|---------|------|
| id | UUID |
| user_id | UUID |
| category_id | UUID |
| amount | DECIMAL(12,2) |
| merchant | VARCHAR(100) |
| expense_date | DATE |
| notes | TEXT |
| created_at | TIMESTAMP |
| updated_at | TIMESTAMP |

Indexes

- user_id
- expense_date
- category_id

Relationship

One User → Many Expenses

One Category → Many Expenses

---

# budgets

Purpose

Store monthly budgets.

| Column | Type |
|---------|------|
| id | UUID |
| user_id | UUID |
| month | INTEGER |
| year | INTEGER |
| budget_amount | DECIMAL(12,2) |
| spent_amount | DECIMAL(12,2) |
| remaining_amount | DECIMAL(12,2) |
| created_at | TIMESTAMP |

Relationship

One User → Many Budgets

---

# financial_health

Purpose

Store Financial Health history.

| Column | Type |
|---------|------|
| id | UUID |
| user_id | UUID |
| score | INTEGER |
| budget_score | INTEGER |
| savings_score | INTEGER |
| consistency_score | INTEGER |
| calculated_at | TIMESTAMP |

---

# money_stories

Purpose

Store monthly AI summaries.

| Column | Type |
|---------|------|
| id | UUID |
| user_id | UUID |
| month | INTEGER |
| year | INTEGER |
| story | TEXT |
| recommendations | JSONB |
| created_at | TIMESTAMP |

---

# goals

Purpose

Store financial goals.

Examples

Emergency Fund

Vacation

Laptop

Bike

---

Columns

| Column | Type |
|---------|------|
| id | UUID |
| user_id | UUID |
| title | VARCHAR(100) |
| target_amount | DECIMAL |
| saved_amount | DECIMAL |
| target_date | DATE |

---

# notifications

Purpose

Store in-app notifications.

| Column | Type |
|---------|------|
| id | UUID |
| user_id | UUID |
| title | VARCHAR(150) |
| message | TEXT |
| is_read | BOOLEAN |
| created_at | TIMESTAMP |

---

# ai_conversations

Purpose

Store AI Coach conversations.

| Column | Type |
|---------|------|
| id | UUID |
| user_id | UUID |
| question | TEXT |
| response | TEXT |
| created_at | TIMESTAMP |

---

# analytics_events

Purpose

Store product analytics.

| Column | Type |
|---------|------|
| id | UUID |
| user_id | UUID |
| event_name | VARCHAR(100) |
| screen_name | VARCHAR(100) |
| occurred_at | TIMESTAMP |

---

# Relationships

Users

├── Categories

├── Expenses

├── Budgets

├── Goals

├── Financial Health

├── Money Stories

├── Notifications

├── AI Conversations

└── Analytics Events

---

# Constraints

Email

Unique

Expense Amount

Greater than zero

Budget

Greater than zero

Foreign Keys

Required

Soft Delete

Enabled

---

# Indexing Strategy

Indexes

- email
- user_id
- category_id
- expense_date
- month
- year
- created_at

Composite Indexes

(user_id, expense_date)

(user_id, month, year)

---

# Audit Fields

Every table contains:

created_at

updated_at

deleted_at

---

# Backup Strategy

Daily Incremental Backup

Weekly Full Backup

Point-in-Time Recovery

---

# Data Retention

Analytics

12 Months

AI Conversations

24 Months

Expenses

Retained unless deleted by the user

---

# Future Tables

subscriptions

recurring_expenses

family_members

receipt_uploads

bank_accounts

transactions

investment_portfolio

voice_expenses

---

# Related Documents

15_BACKEND_ARCHITECTURE.md

16_API_SPECIFICATION.md

18_SECURITY_AND_PRIVACY.md

---

# CEO Vision

A database is more than storage.

It is the foundation of every feature.

A well-designed schema should allow Kharcha to grow from a simple expense tracker into a complete AI-powered personal finance platform without major redesigns.
