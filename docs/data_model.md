# Credlytic Data Model

## Transaction Entity
The Transaction entity represents a single financial event detected via SMS or manual entry.

### Core Fields
- amount
- type (DEBIT / CREDIT)
- account (masked)
- transactionDate
- mode (UPI / CARD / BANK)

### Deduplication Strategy
- Primary: referenceId
- Secondary: composite hash of amount, date, account, and type

### Design Principles
- Store only validated data
- Never store raw SMS
- Mask sensitive information