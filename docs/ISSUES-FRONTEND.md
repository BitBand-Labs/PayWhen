# Frontend Issues - PayWhen 🎨

This document tracks the detailed UI/UX and integration tasks for the PayWhen miniapp.

---

## 🚀 Phase 1: Foundation

### Issue #FE-1: Project Scaffold & Theme
**Category:** `[UI]`
**Status:** ❌ PENDING
**Priority:** Critical
**Description:** Initialize Next.js app with PayWhen branding.
- **Tasks:**
  - [ ] Configure `tailwind.config.ts`.
  - [ ] Setup `globals.css` colors.
  - [ ] Implement `Layout` with header and navigation.

### Issue #FE-2: Wallet Integration
**Category:** `[INTEGRATION]`
**Status:** ❌ PENDING
**Priority:** Critical
**Description:** Global wallet state management.
- **Tasks:**
  - [ ] Create wallet connection hooks.
  - [ ] Implement Freighter connection logic.
  - [ ] Auto-reconnect on refresh.
  - [ ] Display connected wallet address.

---

## 💸 Phase 2: Create Payment Flow

### Issue #FE-3: Escrow Setup
**Category:** `[UI]`
**Status:** ❌ PENDING
**Priority:** High
**Description:** Enter recipient, amount, and condition.
- **Tasks:**
  - [ ] Input field for recipient address.
  - [ ] Amount input (USDC or XLM).
  - [ ] Condition selector (Time-based, Manual, Oracle).
  - [ ] Dynamic fields based on condition type (e.g. Datepicker for Time-based).

### Issue #FE-4: Transaction Review
**Category:** `[UI]`
**Status:** ❌ PENDING
**Priority:** High
**Description:** Review and confirm the conditional payment.
- **Tasks:**
  - [ ] Summary of all escrow settings.
  - [ ] "Lock Funds" button with wallet confirmation.
  - [ ] Transaction toast notifications.

---

## 🔐 Phase 3: Escrow Management

### Issue #FE-5: Active Escrows Dashboard
**Category:** `[UI]`
**Status:** ❌ PENDING
**Priority:** High
**Description:** View payments created and payments received.
- **Tasks:**
  - [ ] Tabbed view: "Sent" and "Received".
  - [ ] List active, pending, completed, and refunded escrows.
  - [ ] Visual indicators for condition met/unmet.

### Issue #FE-6: Execution Triggers
**Category:** `[UI]`
**Status:** ❌ PENDING
**Priority:** High
**Description:** Allow triggering of the escrow if condition is met.
- **Tasks:**
  - [ ] "Execute Payment" button for met conditions.
  - [ ] "Request Refund" button if dispute timeout reached.
  - [ ] Wallet signature handling for manual trigger.

---

## 🧪 Phase 4: Testing & Polish

### Issue #FE-7: Error Handling
**Category:** `[ERROR]`
**Status:** ❌ PENDING
- **Tasks:**
  - [ ] Handle wallet not installed.
  - [ ] Handle invalid address.
  - [ ] Handle insufficient balance.
  - [ ] Handle smart contract simulation errors.

### Issue #FE-8: Responsive Design
**Category:** `[UI]`
**Status:** ❌ PENDING
- **Tasks:**
  - [ ] Test on mobile devices (miniapp focus).
  - [ ] Optimize for small screens.
  - [ ] PWA manifest setup.