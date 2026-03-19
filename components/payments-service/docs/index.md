# Payments Service

## Overview

The payments service encapsulates the payment domain for Fry Express. It provides APIs for authorization, capture, and refund operations while keeping payment records isolated from order data.

## Key Capabilities

- expose the `payments-api`
- persist payment events in a dedicated database
- emit settlement and reconciliation events
- provide audit-friendly transaction state

## Dependencies

- `postgres-payments`
- `rabbitmq-main`
- `k8s-prod-cluster`

## Operational Notes

This component is owned by the payments team and follows stricter change controls due to its financial impact.
