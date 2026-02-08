# SMS Parsing Strategy – Credlytic

## Overview
Credlytic uses a rule-based SMS parsing approach for detecting financial transactions from bank, UPI, and card messages.

## Phase 1: Rule-Based Parsing
- Keyword detection for debit/credit classification
- Regex-based amount extraction
- Pattern matching for account, date, and reference ID
- Noise filtering for non-transactional lines

## Message Classification
Messages are classified into:
- UPI Debit
- Bank Credit (IMPS/NEFT)
- Card Debit

## Phase 2: AI Enhancement (Future Scope)
- NLP-based merchant categorization
- Intelligent transaction labeling
- Spending behavior insights

## Reason for Approach
Rule-based parsing offers:
- High accuracy
- Low computational cost
- Easy debugging
- Better transparency for users