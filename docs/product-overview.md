# Product Overview

Lazarus is a Telegram-first platform for discovering and monitoring early CTO activity in EVM token markets.

Community takeover opportunities often start when a token looks inactive, abandoned, or distressed, then begins showing signs of renewed attention: new holders, liquidity changes, stronger volume, wallet accumulation, refreshed social activity, or chart recovery. Lazarus is built to detect those patterns earlier, score them clearly, and deliver the result where crypto users already spend time: Telegram.

## Target Users

### Signal Followers

Users who want a high-signal Telegram channel that summarizes potential token revival opportunities without requiring them to inspect every chart manually.

### Active Traders

Users who want wallet-aware monitoring, portfolio visibility, configurable detector settings, and eventually controlled trading from their own wallet.

### Operators

Internal admins who need to see who has joined, who has paid, which users were referred, what revenue is active, and whether workers/signals/payments are healthy.

## Core Surfaces

### Public Signal Bot

The notifier bot posts into a Telegram channel. Each post is compact and formatted for mobile:

- Token name/symbol and contract address.
- Chain and age.
- Strength score out of 100.
- Audit score out of 100 when available.
- Holder count and top-holder concentration.
- Liquidity and DEX context.
- Ownership, honeypot, and LP checks.
- DexScreener and trading-tool links.

### User Bot

The main Telegram bot handles the private user workflow:

- Signup and 48-hour trial.
- Wallet generation, import, and watch-only wallet support.
- Encrypted private key storage for generated/imported wallets.
- Portfolio and PnL views.
- Billing and payment status.
- Referral code creation and sharing.
- Trading settings.
- Detector settings.
- Guided presets and advanced mode.

### Admin Panel

The admin panel gives the operator a plain view of the business and system:

- Users and Telegram usernames.
- Subscription status and trial locks.
- Revenue and invoices.
- Referral codes, attribution, commissions, and payouts.
- Worker status and operational health.

## Product Boundaries

Lazarus is not trying to be a generic exchange, a social trading app, or a broad portfolio manager. The first product focus is narrow:

- Detect CTO-style token revival patterns.
- Present them clearly.
- Let users configure how strict the detector should be.
- Keep wallet/trade accounting tenant-safe.
- Add live routing only through controlled, risk-gated rollout.

## What Makes Lazarus Different

Most crypto alert products either send raw noise or require users to stare at dashboards. Lazarus is designed for a narrower problem:

- Find possible token revival moments.
- Package the evidence clearly.
- Let users choose how strict the detector should be.
- Keep the workflow in Telegram.
- Keep wallet and subscription accounting clean from the start.

The product is intentionally opinionated. It should not post every movement. It should post signals that are strong enough to deserve review.

## The Lazarus Loop

The product loop is:

1. Lazarus watches token activity.
2. A comeback pattern appears.
3. The token is scored.
4. A public alert is posted if it passes threshold.
5. Users review the alert.
6. Private bot users can track wallets, tune settings, and monitor outcomes.
7. Operators review quality and adjust thresholds.

This loop should continuously improve signal quality.

## Launch Philosophy

The safest launch path is:

- Public signal channel first.
- Private bot trial second.
- Paper trading validation third.
- Live trading beta last.

This sequence lets Lazarus prove value before user funds are placed at risk.
