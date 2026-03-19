# Notification Worker

## Overview

The notification worker handles asynchronous communications triggered by order and payment events. It is separated from the synchronous order path to keep customer checkout latency stable.

## Key Capabilities

- subscribe to messaging events from core workflows
- enrich outbound notifications with order and payment context
- deliver status updates for order confirmation and payment results

## Dependencies

- `orders-api`
- `payments-api`
- `rabbitmq-main`
- `k8s-prod-cluster`

## Operational Notes

This worker is managed by the operations team because it sits close to downstream fulfillment and customer communication timing.
