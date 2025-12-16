# Integration (Conceptual)

> This describes how PayWallX will integrate in the future.
> APIs and SDKs are not publicly available yet.

## High-level flow

Client → Request protected resource  
Server → `402 Payment Required`  
Client → On-chain payment  
Client → Retry request  
Server → `200 OK`

## Server responsibilities

- Define pricing per route or resource
- Return HTTP 402 with payment metadata
- Verify on-chain payment
- Grant access

## Client responsibilities

- Detect HTTP 402 responses
- Display paywall UI
- Trigger wallet payment
- Retry request after payment
