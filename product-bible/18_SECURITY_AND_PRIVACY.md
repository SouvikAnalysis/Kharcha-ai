# KHARCHA

# 18_SECURITY_AND_PRIVACY.md

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

This document defines the security and privacy standards for Kharcha.

As a personal finance application, Kharcha handles sensitive financial information. Every feature must be designed with security, privacy, and user trust as first-class principles.

This document establishes:

- Security standards
- Authentication strategy
- Data protection
- Privacy controls
- Incident response
- Compliance guidelines

---

# Security Principles

Kharcha follows six core security principles.

✓ Security by Design

✓ Privacy by Default

✓ Least Privilege Access

✓ Defense in Depth

✓ Secure Communication

✓ User Transparency

Security should never be an optional feature.

---

# Data Classification

All stored information is classified according to sensitivity.

| Classification | Examples | Protection Level |
|---------------|----------|------------------|
| Public | App version, help content | Low |
| Internal | Analytics events | Medium |
| Confidential | User profile, salary, budgets, expenses | High |
| Restricted | Password hash, authentication tokens | Critical |

---

# Authentication

Kharcha uses secure authentication.

Features

- Email & Password Login
- Google Sign-In
- JWT Access Token
- Refresh Token
- Secure Password Hashing
- Multi-device Support

Passwords are never stored in plain text.

---

# Authorization

Every request is verified before processing.

Access Rules

- Users can only access their own data.
- Every API validates user identity.
- Role-based permissions are enforced where applicable.

---

# Password Security

Requirements

Minimum Length

8 Characters

Recommended

12+ Characters

Must contain

- Uppercase letter
- Lowercase letter
- Number
- Special character

Passwords are hashed using a strong password hashing algorithm such as Argon2 or bcrypt before storage.

---

# Secure Communication

All communication uses HTTPS.

Requirements

- TLS Encryption
- Secure Headers
- HSTS Enabled
- Certificate Validation

HTTP requests are not allowed in production.

---

# Token Management

Access Token

Short Lifetime

Refresh Token

Long Lifetime

Rules

- Tokens expire automatically.
- Refresh tokens can be revoked.
- Invalid tokens are rejected immediately.

---

# Data Encryption

## Data in Transit

Protected using HTTPS (TLS).

---

## Data at Rest

Sensitive database fields are encrypted where appropriate.

Examples

- Salary
- Financial Goals
- AI Preferences

---

## Secrets

API keys and secrets are never stored in source code.

Environment variables or secret-management services must be used.

---

# Input Validation

Every request is validated.

Protection includes

- SQL Injection Prevention
- Cross-Site Scripting (XSS) Prevention
- Request Validation
- File Validation
- JSON Schema Validation

Never trust client-side validation alone.

---

# Rate Limiting

To protect against abuse:

| Endpoint | Limit |
|----------|-------|
| Login | 5 requests/minute |
| AI Chat | 30 requests/hour |
| Expense APIs | 100 requests/minute |
| Search | 100 requests/minute |

Excessive requests return:

HTTP 429 — Too Many Requests

---

# Session Management

Users can:

- View active sessions (future)
- Log out from current device
- Log out from all devices

Inactive sessions expire automatically.

---

# Privacy Principles

Kharcha follows these commitments:

- Collect only required data.
- Explain why data is collected.
- Never sell user data.
- Never use financial data for advertising.
- Respect user consent.

---

# User Privacy Controls

Users can:

- Download their data.
- Delete their account.
- Delete AI conversation history.
- Disable notifications.
- Disable AI features (future).

---

# Analytics Privacy

Analytics must never store:

- Passwords
- Card numbers
- Bank account numbers
- UPI PINs
- Authentication tokens

Analytics events use anonymized identifiers whenever possible.

---

# AI Privacy

The AI system only accesses information necessary to generate insights.

Examples

- Expenses
- Budget
- Categories
- Goals

The AI does not access unrelated personal information.

Users are informed when AI-generated content is displayed.

---

# Backup Security

Database backups are:

- Encrypted
- Access-controlled
- Verified regularly
- Stored separately from production systems

---

# Logging Policy

Logs should contain:

- Request ID
- Timestamp
- Endpoint
- Error Code

Logs should never contain:

- Passwords
- JWT Tokens
- Financial amounts tied to identifiable users
- Personal secrets

---

# Incident Response

In case of a security incident:

1. Detect
2. Isolate
3. Investigate
4. Fix
5. Recover
6. Notify affected users if required
7. Document lessons learned

---

# Compliance Goals

Kharcha aims to follow industry best practices for:

- Secure authentication
- Data protection
- Privacy
- Financial data handling

Future expansion may require compliance with regional privacy regulations depending on deployment.

---

# Security Checklist

Before every release:

☐ HTTPS enforced

☐ Authentication tested

☐ Authorization verified

☐ Input validation completed

☐ Rate limiting enabled

☐ Secrets secured

☐ Logs reviewed

☐ Backups verified

☐ Dependency vulnerabilities checked

☐ Penetration testing completed (where applicable)

---

# Related Documents

- 15_BACKEND_ARCHITECTURE.md
- 16_API_SPECIFICATION.md
- 17_DATABASE_SCHEMA.md
- 19_TESTING_STRATEGY.md

---

# CEO Vision

Users trust Kharcha with one of the most personal parts of their lives—their financial information.

That trust is earned through transparent privacy practices, secure engineering, and responsible data handling.

Every security decision should answer one question:

"Would I be comfortable protecting my own financial data this way?"

If the answer is no, the design must change.
