# Product Specification

This document describes the public-facing product requirements for Lazarus.

## Objectives

Lazarus should:

- Detect early CTO comeback signals on supported EVM chains.
- Score every evaluated token in a way users can understand.
- Publish high-quality signal posts to a Telegram channel.
- Provide a private Telegram bot for onboarding, wallets, settings, portfolio, PnL, billing, and referrals.
- Support guided presets for newer users and advanced settings for experienced users.
- Keep all user data scoped by tenant/user identity.
- Keep live trading locked until operational gates are passed.

## Supported Chains

Initial chain scope:

- Base.
- Ethereum mainnet.

Base is the priority chain for launch because lower fees make small-wallet testing and user workflows more practical.

## Supported DEX Coverage

Initial DEX scope:

- Uniswap V2-style pools where supported.
- Uniswap V3 pools.
- Aerodrome V2 and Slipstream on Base.
- BaseSwap-style pools where indexed.

The platform should show which DEX context was used for a signal when available.

## User Account Model

Each Telegram user maps to a tenant-owned account record. All user-owned objects should be stored under that tenant/user boundary:

- Wallets.
- Settings.
- Subscriptions.
- Payment invoices.
- Referral attribution.
- Portfolio snapshots.
- PnL snapshots.
- Trade intents.
- Positions.
- Trades.
- Signal decisions.

Market data can be global. User actions and balances cannot be global.

## Signup Flow

The signup flow should be short:

1. User starts the Telegram bot.
2. Bot creates or loads the user account.
3. User receives trial status.
4. User is shown the main menu.
5. User can create/import/watch a wallet.
6. User can choose a guided profile.
7. User can review detector/trading settings.
8. After trial, payment is required to unlock premium features.

## Subscription Model

Initial model:

- 48-hour free trial.
- Standard plan: one wallet.
- Premium plan: five wallets.
- Premium price: 0.05 ETH per month.
- Trial locks when expired unless payment is confirmed.

Payment can start with an internal on-chain payment monitor. External payment providers can be added later if they materially reduce support burden.

## Trading Modes

### Paper Mode

Default mode. The system records hypothetical trades from live quotes without submitting transactions.

### Live Mode

Live mode should require:

- Explicit operator enablement.
- User risk acknowledgement.
- Tenant/user allowlisting during early rollout.
- Valid encrypted user wallet.
- Per-wallet execution locks.
- Risk gates.
- Tiny-funded validation before broader launch.

Live trading must never use a global wallet for tenant user trades.

## Preset Settings

### Starter

For cautious users:

- Higher minimum score.
- Composite signals only.
- Lower budget.
- Lower slippage.
- Base-first.

### Balanced

For typical active users:

- Moderate score threshold.
- More signal types.
- Larger but still bounded budget.
- Base-first.

### Aggressive

For advanced users:

- Lower score threshold.
- More chains and signal types.
- Higher signal frequency.
- Higher slippage tolerance.
- Requires clear warnings.

### Advanced Mode

Advanced mode exposes detailed filters:

- Sensitivity.
- Minimum liquidity.
- Minimum/maximum market cap.
- Minimum volume.
- Minimum holders.
- Top-holder concentration.
- LP burned/locked threshold.
- Renounced ownership requirement.
- Honeypot strictness.
- Chains.
- DEXes.
- Signal types.
- Minimum composite score.
- Cooldown.
- Daily signal cap.
- Maximum open positions.

Any manual advanced change should be stored as a custom profile.

