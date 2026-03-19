# Web Frontend

## Overview

The web frontend provides the primary customer ordering experience for Fry Express Systems. It supports product discovery, cart management, checkout, and order tracking for web users.

## Key Capabilities

- render catalog and promotion content
- submit checkout requests to the Orders API
- initiate payment authorization through the Payments API
- surface real-time order state to customers

## Dependencies

- `orders-api`
- `payments-api`
- `k8s-prod-cluster`

## Operational Notes

The platform team owns release coordination, performance tuning, and customer-facing availability for this component.
