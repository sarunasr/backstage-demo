# Inventory Service

## Overview

The inventory service coordinates available stock for active orders and operational fulfillment workflows. It consumes order events and maintains a near-real-time view of reservation status.

## Key Capabilities

- reserve inventory for accepted orders
- coordinate fulfillment readiness across warehouse nodes
- detect stock pressure before dispatch
- consume order data from the `orders-api`

## Dependencies

- `orders-api`
- `postgres-orders`
- `rabbitmq-main`
- `k8s-prod-cluster`

## Operational Notes

Operational correctness is prioritized over throughput because this service feeds warehouse and dispatch decisions.
