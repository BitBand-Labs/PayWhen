# Backend & Oracles Roadmap 🧠⚙️

This document tracks the backend infrastructure and Oracle condition engine for PayWhen.

---

## 🏗️ Phase 1: Core API & Indexing

### Issue #BK-1: Soroban Event Indexing
**Category:** `[DATA]`
**Status:** ❌ PENDING
**Priority:** Critical
**Description:** Index smart contract events to serve the frontend quickly.
- **Tasks:**
  - [ ] Setup Node.js indexing service.
  - [ ] Listen to `EscrowCreated` and `EscrowExecuted` events on Horizon/Soroban RPC.
  - [ ] Store escrow status in a local database (PostgreSQL/MongoDB).

### Issue #BK-2: API Layer
**Category:** `[API]`
**Status:** ❌ PENDING
**Priority:** High
**Description:** Serve escrow data to the frontend miniapp.
- **Tasks:**
  - [ ] Endpoint: `GET /escrows/{wallet_address}` (fetch sent/received escrows).
  - [ ] Endpoint: `GET /escrow/{escrow_id}` (fetch specific details).
  - [ ] Support filtering by active vs completed escrows.

---

## 🔮 Phase 2: External Condition Oracles

### Issue #BK-3: Oracle Node Setup
**Category:** `[ORACLE]`
**Status:** ❌ PENDING
**Priority:** High
**Description:** Create a trusted backend oracle to trigger off-chain conditions.
- **Tasks:**
  - [ ] Set up a secure Oracle server with its own Stellar keypair.
  - [ ] Whitelist the Oracle address in the `ConditionalPayment` smart contract for specific condition types.

### Issue #BK-4: Webhook Triggers
**Category:** `[ORACLE]`
**Status:** ❌ PENDING
**Priority:** Medium
**Description:** Trigger payments based on external API webhooks (e.g., Zapier, Shipping APIs).
- **Tasks:**
  - [ ] Endpoint: `POST /webhook/{escrow_id}`.
  - [ ] Verify the webhook payload securely.
  - [ ] The Oracle Node signs and submits the `execute` transaction to Soroban.

---

## ⚡ Phase 3: Notifications & Polish

### Issue #BK-5: Email / SMS Notifications
**Category:** `[NOTIFICATIONS]`
**Status:** ❌ PENDING
**Priority:** Low
**Description:** Notify users when conditions are met.
- **Tasks:**
  - [ ] Integrate SendGrid (Email) / Twilio (SMS).
  - [ ] Send alert to recipient when funds are locked.
  - [ ] Send alert when payment is executed or refunded.

### Issue #BK-6: Off-Ramp Integration (Future)
**Category:** `[INTEGRATION]`
**Status:** ❌ PENDING
**Priority:** Low
**Description:** Connect executed payments to fiat off-ramps.
- **Tasks:**
  - [ ] Mobile money integration.
  - [ ] Bank transfer integration.