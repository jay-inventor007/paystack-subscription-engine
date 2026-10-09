# Paystack Subscription Engine: SaaS Billing & Lifecycle Platform

> **A resilient SaaS billing and subscription lifecycle engine integrated with Paystack, featuring webhook signature verification, tiered plan transitions, and append-only payment audits.**

[![TypeScript](https://img.shields.io/badge/TypeScript-5.0+-blue.svg)](https://www.typescriptlang.org/)
[![React](https://img.shields.io/badge/React-18+-61dafb.svg)](https://react.dev/)
[![Paystack](https://img.shields.io/badge/Paystack-Integrated-00c3f7.svg)](https://paystack.com/)
[![Supabase](https://img.shields.io/badge/Supabase-Edge%20Functions%20%26%20Postgres-3ecf8e.svg)](https://supabase.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

---

## Overview

A complete subscription management system built for high-reliability fintech workflows:
- **Plan Selection & Checkout:** Dynamic plan subscription with Paystack inline popup and server-side payment initialization.
- **Webhook Processing:** Cryptographic HMAC-SHA512 webhook signature validation and idempotency enforcement preventing replay attacks.
- **Lifecycle Transitions:** Prorated plan upgrades, downgrades, and cancellations with grace-period access retained until the current billing cycle expires.
- **Append-Only Financial Ledger:** Immutable payment transaction log ensuring auditability for every customer invoice.

👉 **Complete Architecture & Technical Specs:** See [`DOCUMENTATION.md`](./DOCUMENTATION.md) for data models, webhook event state machines, and reconciliation logic.

---

## Quick Start

```bash
# 1. Install dependencies
npm install

# 2. Configure environment
cp .env.example .env   # Set VITE_API_BASE_URL and Paystack public keys

# 3. Start local development server
npm run dev
```

Full setup, including linking the Supabase project, setting Paystack secret keys, and deploying webhook Edge Functions, is detailed in [`DOCUMENTATION.md`](./DOCUMENTATION.md).
