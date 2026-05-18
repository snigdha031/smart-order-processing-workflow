# System Architecture

## Workflow Overview

The system processes incoming orders through multiple validation and resilience layers.

## Processing Flow

Webhook API
→ Email Validation
→ Duplicate Order Detection
→ Order Creation
→ Payment Processing
→ Retry Handling
→ Execution Logging
→ API Response

## Key Components

### Validation Layer
Checks whether required fields such as email exist before processing.

### Duplicate Protection
Prevents duplicate order creation using Supabase lookup validation.

### Payment Processing
Simulates external payment gateway behavior with random failures.

### Retry Mechanism
Automatically retries failed payment processing attempts.

### Execution Logging
Stores workflow events and failures inside Supabase for monitoring and observability.

## Tech Stack

- n8n
- Supabase
- Docker
- Postman