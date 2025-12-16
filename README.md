# PayWallX

**Pay once. Access instantly.**

PayWallX is a crypto-native paywall built on Solana that uses **HTTP 402 (Payment Required)**
as the access control mechanism.

Instead of subscriptions or accounts, PayWallX enables **pay-per-access**
using one-time on-chain payments.

---

## 🚀 What is PayWallX?

PayWallX turns payments into HTTP responses.

- Protected content or APIs return `HTTP 402 — Payment Required`
- The client completes a one-time on-chain payment (SOL / USDC)
- Access is immediately granted with `HTTP 200`

**Payment becomes authorization.**

---

## 🧪 Demo (MVP)

This repository contains the **PayWallX demo documentation + project scaffold**.

What the demo is meant to show:
- A locked resource returning HTTP 402
- A payment prompt (testnet or simulated)
- Instant unlock after payment
- Transition to HTTP 200

⚠️ **This is a demo / MVP. Not production-ready.**

---

## 🔁 HTTP 402 Flow (Concept)

```text
Client → GET /content
Server → 402 Payment Required

Client → On-chain payment (SOL / USDC)

Client → Retry request
Server → 200 OK (Access Granted)
```

---

## 🧩 Repo contents

- `demo/frontend/`  
  Placeholder folder for your demo UI (drop your existing frontend here)

- `demo/backend-mock/`  
  Notes and placeholder for mocked verification

- `docs/`  
  Documentation:
  - HTTP 402 concept
  - Conceptual integration flow
  - Roadmap and positioning

---

## 🛠️ Integration (Conceptual)

PayWallX is designed to integrate at the HTTP layer.

Future integrations will allow developers to:
- Define prices per route or resource
- Return HTTP 402 with payment metadata
- Verify on-chain payments
- Grant access via standard HTTP responses

📄 See: `docs/integration-concept.md`

---

## 🗺️ Roadmap

Planned milestones:
- Public HTTP 402 API
- Production-grade payment verification
- Developer SDK
- Tooling and dashboards

A protocol token is planned as part of the long-term roadmap
for usage, governance, and incentives.

---

## 📄 License

MIT — see `LICENSE`.
