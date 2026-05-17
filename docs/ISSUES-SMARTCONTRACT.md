# Smart Contract Issues - PayWhen 🔐

This document tracks the detailed development tasks for PayWhen Soroban smart contracts.

---

## 🏛️ Core Escrow Architecture

### Issue #SC-1: Conditional Payment Initialization
**Priority:** Critical
**Status:** ❌ PENDING
**Description:** Initialize the core escrow contract for conditional payments.
- **Tasks:**
  - [ ] Initialize `conditional_payment` project.
  - [ ] Define `DataKey` enum: `Sender`, `Recipient`, `Amount`, `ConditionType`, `ConditionData`, `DisputeTimeout`.
  - [ ] Implement `create_escrow(env, sender, recipient, amount, condition_type, condition_data)` function.

### Issue #SC-2: Deposit & Lock Logic
**Priority:** Critical
**Status:** ❌ PENDING
**Description:** Accept funds into the contract and lock them.
- **Tasks:**
  - [ ] Implement token transfer from `Sender` to the contract.
  - [ ] Store escrow state securely.
  - [ ] Emit `EscrowCreated` event.

### Issue #SC-3: Condition Execution
**Priority:** Critical
**Status:** ❌ PENDING
**Description:** Enforce execution only when conditions are met.
- **Tasks:**
  - [ ] Implement `execute(env, escrow_id)` function.
  - [ ] Check if `condition_type == Time` and `unlock_time` has passed.
  - [ ] Check if `condition_type == Manual` and the authorized party signed.
  - [ ] Transfer funds to `Recipient`.
  - [ ] Emit `EscrowExecuted` event.

---

## ⚙️ Fallback & Refunds

### Issue #SC-4: Dispute and Refund Timeout
**Priority:** High
**Status:** ❌ PENDING
**Description:** Ensure senders can retrieve funds if a condition is never met.
- **Tasks:**
  - [ ] Store `dispute_timeout` upon creation.
  - [ ] Implement `refund(env, escrow_id)`.
  - [ ] Time-check: refund only available after `dispute_timeout`.
  - [ ] Transfer funds back to `Sender`.

---

## 🔒 Access Control

### Issue #SC-5: Trigger Authorization
**Priority:** High
**Status:** ❌ PENDING
**Description:** Only authorized parties can trigger executions.
- **Tasks:**
  - [ ] Implement authorization check using Soroban Auth.
  - [ ] For `Manual` triggers, ensure caller matches the authorized recipient/arbiter.
  - [ ] Ensure `execute` can't be called twice.

---

## 🧪 Testing

### Issue #SC-6: Condition Logic Tests
**Priority:** High
**Status:** ❌ PENDING
**Description:** Verify escrow lock and release behavior.
- **Tasks:**
  - [ ] Test deposit and lock.
  - [ ] Test early execution fails.
  - [ ] Test successful execution after time passes.
  - [ ] Test refund after dispute timeout.