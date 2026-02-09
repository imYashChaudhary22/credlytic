# Credlytic System Architecture

## Overview
Credlytic is an event-driven personal finance application that automatically tracks transactions from SMS notifications.

## Core Flow
SMS Receiver → Message Classifier → Transaction Parser → Validation → Deduplication → Database → Analytics → UI

## Module Responsibilities
- Parser: Transaction detection and extraction
- Data Layer: Storage and retrieval
- Analytics: Insight generation
- UI: Data presentation

## Design Principles
- Separation of concerns
- Defensive parsing
- Privacy-first data handling
- Modular and extensible architecture