# Blendy — Zero-Cost Borrowing Money Markets

Blendy is a money market that lets users borrow at (near) zero net cost.  
It routes collateral into yield strategies so the yield offsets borrowing costs. In favorable conditions, loans can self-repay over time.

- Current focus: Solana (Anchor/Rust)
- Goal: Simple, safe, capital-efficient borrowing with built-in risk controls
- Angle: Zero/low net cost via collateral yield

---

## Why Blendy

- Zero-Cost Borrowing: Collateral earns yield that subsidizes borrowing costs.
- Self-Repaying Loans: Direct yield to interest and/or principal automatically.
- Risk Controls Built-In:
  - Downside Guard (hedging) to soften volatility shocks.
  - Dynamic Throttling (LTV/limits/rates) to stabilize utilization.
- Simple UX: Deposit → Borrow → Monitor (auto-repayment handles the rest).

> Note: Zero or negative net cost depends on market yields and parameters. In low-yield or high-volatility regimes, an effective cost may still apply.

---

## How It Works

1. Deposit collateral (supported Solana assets).  
2. Protocol routes collateral to yield (lending, staking, or LP strategies).  
3. Borrow stable assets against the collateral.  
4. Yield offsets your cost; when yield is greater than or equal to cost, your loan trends toward zero.  
5. Risk modules hedge and throttle to maintain healthy markets.

---

## Core Features

- Interest Subsidy Engine: Matches collateral yield to borrow cost.
- Self-Repayment Toggle: Opt in to auto-apply yield to interest/principal.
- Adaptive Risk Modules:
  - Hedge module: buys protection when risk rises.
  - Throttle module: adjusts parameters to keep markets balanced.
- Oracle-Backed Pricing: Pyth / Switchboard on Solana.
- Programmatic Access: Interfaces for integrators and wallets.

---

## Tech Stack

- Smart Contracts: Rust, Anchor (Solana)  
- Frontend: React, Next.js, Tailwind  
- Backend/Indexing: Node.js with RPC/indexers  
- Infra/Oracles: Pyth, Switchboard; Vercel for web deploys

---

## Getting Started

Prerequisite: a supported Solana wallet (for example, Phantom).

1. Connect wallet and deposit supported collateral.  
2. Choose borrowing amount and (optional) self-repayment toggle.  
3. Confirm transaction; monitor LTV and health.  
4. Repay anytime or let yield reduce your debt over time.

Networks:
- Solana: Testnet/Mainnet (see app for current status)
- Other chains: on the roadmap

---

## Risk & Disclaimers

- Collateral can lose value; hedging reduces but does not remove risk.  
- Zero-cost outcome is not guaranteed; it depends on yield versus borrowing parameters.  
- Smart contract risk exists despite best practices and audits.

---

## Roadmap (High-Level)

- Solana MVP and strategy router  
- External audits  
- Mainnet hardening, more assets/strategies, integrator SDK  
- Cross-chain expansion (no announcements yet)

---

## Contributing

Pull requests and issues are welcome. Please open a discussion before large changes.

---

## License

© Blendy. All rights reserved. Licensing details to be finalized at mainnet.
