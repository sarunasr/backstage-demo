# Orders Service

## Overview

The orders service is the transactional backbone for Fry Express checkout. It accepts order submissions, persists state, and coordinates downstream activities with payments and fulfillment systems.

## Key Capabilities

- validate carts and create order records
- expose the `orders-api`
- orchestrate payment checks before order confirmation
- emit events for inventory reservation and notifications

## Dependencies

- `payments-api`
- `postgres-orders`
- `rabbitmq-main`
- `k8s-prod-cluster`

## Operational Notes

This service is monitored as a business-critical workload because checkout conversion depends on its availability and latency.
