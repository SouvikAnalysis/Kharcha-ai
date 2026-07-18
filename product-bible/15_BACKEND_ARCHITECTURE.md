# KHARCHA

# 15_BACKEND_ARCHITECTURE.md

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

This document defines the backend architecture of Kharcha.

It explains how the mobile application, backend services, database, AI engine, authentication, notifications, and analytics work together.

The architecture should be:

- Scalable
- Secure
- Modular
- Cloud-native
- API-first
- AI-ready

---

# Architecture Principles

Every architectural decision should support:

✓ Security

✓ Reliability

✓ Scalability

✓ Performance

✓ Simplicity

✓ Maintainability

---

# High-Level Architecture

```

```
                    +----------------------+
                    |   Flutter Mobile App |
                    +----------+-----------+
                               |
                               |
                         HTTPS / REST
                               |
                               |
                 +-------------+--------------+
                 |         API Gateway         |
                 +------+------+------+--------+
                        |      |      |
                        |      |      |
         +--------------+      |      +---------------+
         |                     |                      |
         |                     |                      |
+--------+--------+   +--------+--------+   +---------+--------+
| Authentication  |   | Expense Service |   | Budget Service   |
+--------+--------+   +--------+--------+   +---------+--------+
         |                     |                      |
         |                     |                      |
         +---------------------+----------------------+
                               |
                               |
                      +--------+--------+
                      | PostgreSQL DB   |
                      +--------+--------+
                               |
                +--------------+--------------+
                |                             |
        +-------+-------+             +-------+-------+
        | AI Service    |             | Notification  |
        +-------+-------+             +-------+-------+
                |                             |
        +-------+-------+             +-------+-------+
        | Analytics     |             | Firebase FCM  |
        +---------------+             +---------------+

```

---

# Technology Stack

## Mobile

Flutter

---

## Backend

FastAPI (Python)

---

## Database

PostgreSQL

---

## Cache

Redis

---

## Authentication

Firebase Authentication

---

## Storage

Cloud Storage

---

## Notifications

Firebase Cloud Messaging (FCM)

---

## AI Layer

LLM API

Prompt Engine

Recommendation Engine

---

## Analytics

Firebase Analytics

Crashlytics

Custom Events

---

# Backend Services

---

## Authentication Service

Responsibilities

- Login
- Signup
- JWT Validation
- Password Reset
- Session Management

Endpoints

/login

/signup

/logout

/refresh-token

---

## User Service

Responsibilities

- Profile
- Salary
- Preferences
- Financial Goals

---

## Expense Service

Responsibilities

- Add Expense
- Update Expense
- Delete Expense
- Search Expense
- Expense History

---

## Budget Service

Responsibilities

- Monthly Budget
- Budget Status
- Safe Daily Spend
- Budget Intelligence

---

## Category Service

Responsibilities

- Default Categories
- Custom Categories

---

## Insight Service

Responsibilities

- Charts
- Reports
- Monthly Statistics

---

## Financial Health Service

Responsibilities

- Calculate Score
- Trend Analysis
- Recommendations

---

## AI Service

Responsibilities

Daily Insights

Money Story

Budget Recommendations

Financial Coach

Pattern Detection

Prediction

---

## Notification Service

Responsibilities

Budget Alerts

Money Story Ready

Reminder Notifications

Achievement Notifications

---

## Analytics Service

Responsibilities

Track

Product Events

AI Usage

Performance

Retention

Funnels

---

# Database Layer

Core Tables

Users

Expenses

Budgets

Categories

Goals

Notifications

Financial Health

Money Stories

Analytics Events

---

# Data Flow

Expense Added

↓

API Request

↓

Expense Service

↓

Database

↓

Budget Service Updates

↓

Financial Health Updates

↓

Analytics Event

↓

Dashboard Refresh

↓

AI Recommendation Refresh

---

# AI Processing Flow

Expense Added

↓

Store Expense

↓

Update Budget

↓

Recalculate Financial Health

↓

Pattern Detection

↓

Generate Insight

↓

Return Updated Dashboard

---

# Notification Flow

Budget reaches 80%

↓

Budget Service

↓

Notification Service

↓

FCM

↓

User Receives Alert

---

# Security Architecture

Authentication

JWT

Authorization

Role Based Access

HTTPS Only

Encrypted Database Connection

Rate Limiting

API Validation

Secure Headers

Input Sanitization

---

# Caching Strategy

Redis Stores

Frequently Used Dashboard

Categories

Budget Summary

Financial Health

Session Data

---

# Performance Targets

Dashboard API

<300ms

Expense Save

<200ms

Budget Calculation

<150ms

Search

<500ms

AI Recommendation

<3 seconds

---

# Logging

Application Logs

API Logs

Error Logs

Audit Logs

AI Logs

Performance Logs

---

# Error Handling

Standard Response

{
  "success": false,
  "message": "Budget not found",
  "errorCode": "BUDGET_404"
}

---

# Scalability Strategy

Stateless APIs

Horizontal Scaling

Database Indexing

Redis Cache

Background Workers

Async Processing

CDN for Assets

---

# Deployment Architecture

Flutter App

↓

Cloud Load Balancer

↓

FastAPI Containers

↓

PostgreSQL

↓

Redis

↓

Firebase

↓

Monitoring

---

# Monitoring

API Health

Database Health

Server CPU

Memory Usage

Crash Reports

AI Latency

Notification Delivery

---

# Backup Strategy

Daily Database Backup

Weekly Full Backup

Point-in-Time Recovery

Encrypted Storage

---

# Disaster Recovery

Database Restore

Server Failover

Health Checks

Automatic Restart

Backup Verification

---

# Development Environment

Local

Docker

Development

Staging

Production

Separate Databases

Separate Environment Variables

---

# Folder Structure

backend/

app/

api/

services/

models/

schemas/

repositories/

middleware/

utils/

config/

tests/

main.py

---

# Future Expansion

Web Application

Admin Dashboard

Family Accounts

Multi-Currency

Offline Sync

Receipt OCR

Voice Expense Entry

Investment Module

---

# CEO Vision

The backend should be invisible to users.

Users never praise a backend directly.

They praise:

• Fast loading

• Reliable syncing

• Accurate insights

• Secure data

• Instant updates

If users never think about the backend,

then the backend is doing its job.
