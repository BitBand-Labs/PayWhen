# PayWhen Smart Contracts 🧠

This directory contains the **Soroban** smart contracts for PayWhen — the Intent-Based Payment Protocol on Stellar.

## 📚 Documentation

- **[Smart Contract Issues Tracker](../docs/ISSUES-SMARTCONTRACT.md)**: Roadmap for factory and implementation contracts.
- **[Development Guide](../docs/SMARTCONTRACT_GUIDE.md)**: Setup, build, and deploy instructions.

## 🚀 Quick Start

```bash
cargo build --target wasm32-unknown-unknown --release
cargo test
```

## Architecture

The smart contracts handle:
- **PaymentFactory**: Creates and tracks conditional payment contracts on Stellar.
- **ConditionalPayment**: Core logic for escrow, triggers, and fund execution using Soroban.
- **Conditions**: Supports time-based locks and manual trigger logic.
- **Security**: Implements reentrancy protection and non-custodial safety patterns.

---

*Built with Soroban (Rust) for the Stellar network.*
