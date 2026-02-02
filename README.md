# PixGo

PixGo is a hackathon project built at ETHGlobal exploring how stablecoins can be used to simulate PIX-style payments in Brazil.

## What it does
PixGo demonstrates a PIX-like user experience where a user initiates a payment using stablecoins and receives a near-instant confirmation, mimicking local payment rails.

## Problem
Global stablecoin users and protocols cannot easily pay Brazilian users or merchants using PIX-like experiences without local banking integrations.

## Solution
PixGo showcases a proof-of-concept flow that bridges stablecoin transfers with a PIX-style confirmation experience, validating the UX and technical feasibility for local payouts.

## Architecture Intent (Arc + Circle)

PixGo is designed as a chain-abstracted USDC payout system using Arc as a liquidity coordination layer.

While this hackathon MVP uses mocked or testnet flows, the intended production architecture leverages:
- Arc as the settlement and liquidity hub
- Circle Gateway for crosschain USDC routing
- Circle Wallets for user and app-controlled wallets
- PIX as the final local payment rail (offchain)

The system treats multiple chains as a single liquidity surface, abstracting crosschain complexity from the end user.

## Scope (Hackathon MVP)
- Single user payment flow
- Stablecoin transfer on-chain
- Mocked or sandboxed PIX-style confirmation
- Focus on UX + technical validation, not production readiness

## Disclaimer
PixGo is a proof-of-concept built for a hackathon.  
It does not process real PIX payments and is not a regulated financial product.

## Tech (tentative)
- Frontend: TBD
- Blockchain: TBD
- Payments: PIX-style flow (mocked or sandbox)

## Status
Work in progress

## Future Work
PixGo can evolve into an agent-driven payment layer where user intents (e.g. “pay rent”, “split dinner”, “send allowance”) are executed automatically via stablecoins and local payment rails.
