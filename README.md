# OnlyOptionsTrades — Business Finance

Internal finance dashboard for OnlyOptionsTrades. Single-file HTML app with localStorage persistence — no backend, no database, no install.

## Features

- Dashboard with revenue, expenses, net profit, cash on hand, and runway
- 12-month cash flow chart and category breakdown
- Bank/credit card CSV import with auto-categorization rules
- Stripe integration (live API + CSV import)
- Contractor (1099) and W-2 payroll tracking with $600 1099-NEC threshold flag
- Bills & recurring charge auto-detection
- Monthly budgets vs. actual with progress bars
- 12-month insights, month-over-month movement, and rule-based feedback
- End-of-month reminder banner (25th–2nd) for contractor payments and accountant statements
- Custom logo upload, JSON backup/restore

## Run it

Double-click `oot_finance.html` to open in any browser. That's it.

## Data storage

Everything lives in your browser's `localStorage`. Data is private to:
- The exact file path / URL it's opened from
- The specific browser (Chrome ≠ Safari ≠ Firefox)

**Back up regularly** via Settings → "Export Everything (JSON)".

## Stripe API setup

1. https://dashboard.stripe.com → Developers → API keys → **Create restricted key**
2. Grant **Read** access to: Charges, Balance transactions
3. Copy the `rk_live_...` key
4. Paste into the app: Revenue & Stripe → Save Key → Fetch Last 90 Days

## Privacy / security

This repo should be **private**. Even though no secrets are checked in by default, your local browser stores your Stripe key in localStorage on whatever device you open the file on.
