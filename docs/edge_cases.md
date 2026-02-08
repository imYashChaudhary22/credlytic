# Credlytic – SMS Parsing Edge Cases

## Duplicate Messages
- Same transaction received twice
- Same amount but different timestamps

## Failed / Reversed Transactions
- Messages containing "failed", "declined", "reversed"

## Partial Refunds
- Refund amount less than original transaction

## Non-Financial SMS
- Promotional messages from banks
- Balance-only alerts

## Multi-Line Amount Placement
- Amount in first line vs middle line

## Merchant Noise
- Prefixes like null*, RSP*, PYU*

## Guard Rules
- Ignore messages containing keywords: failed, declined, unsuccessful
- Use reference ID as primary unique key
- Fallback to (amount + date + account) if ref ID missing
- Never store balance-only messages

## Deduplication Strategy
- Primary key: Reference ID
- Secondary key: Hash of amount + date + account
- Ignore duplicates detected within same day