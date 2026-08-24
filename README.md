# LedgerBook

A Tally-style, double-entry accounting ledger — a single self-contained HTML file, no backend, no build step.

## Features

- Chart of accounts modeled on Tally's standard groups (Capital, Current Assets/Liabilities, Sales/Purchase Accounts, Direct/Indirect Income/Expense, etc.), with custom sub-groups
- Ledgers with opening balances, GST rate, state, and GSTIN
- Vouchers: Payment, Receipt, Contra, Journal, Sales, Purchase, Credit Note, Debit Note — auto-numbered, enforced Dr = Cr balancing
- GST auto-split into CGST+SGST (same state) or IGST (different state) via a quick-fill helper, fully editable afterward
- Reports: Day Book, Ledger Statement, Trial Balance, Profit & Loss, Balance Sheet, GST Summary — all date-filterable, with CSV export
- Local-only persistence via `localStorage`, with JSON export/import for backups

## Usage

Open `ledger.html` directly in a browser, or serve it locally:

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000/ledger.html`.

All data stays in your browser's local storage — nothing is sent anywhere. Export a backup from Settings regularly.

## Status

Prototype — not a substitute for certified accounting software.
