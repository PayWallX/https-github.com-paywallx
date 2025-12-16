# HTTP 402 as Access Control

HTTP 402 (Payment Required) was designed for future payment systems
but is rarely used in practice.

PayWallX uses HTTP 402 as a native access control mechanism.

## Core idea

- A protected resource responds with `HTTP 402`
- The response indicates a required payment
- Once payment is verified, the same request returns `HTTP 200`

This keeps access control simple, stateless, and HTTP-native.
