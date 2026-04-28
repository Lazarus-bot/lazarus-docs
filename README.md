# Lazarus

Lazarus is a Telegram-first signal intelligence platform for finding early community takeover activity in EVM token markets.

The product is built for the moment when a forgotten token starts showing signs of life again: holder growth, renewed volume, liquidity changes, stronger wallet behavior, and cleaner risk signals. Lazarus turns those raw on-chain movements into clear Telegram alerts, user-friendly detector settings, portfolio monitoring, and controlled trading workflows.

This repository is the **public documentation home** for Lazarus. It is designed to sync cleanly with GitBook. The application source code, trading logic, worker implementation, deployment files, and private operational details live in a separate private repository.

## The Product In One Line

Lazarus watches for tokens that look dead, scores signs that they may be coming back, and delivers the result through Telegram in a format traders can understand quickly.

## What Lazarus Includes

### Public Signal Channel

The public notifier is a Telegram channel for high-signal CTO alerts. Each post is designed for fast mobile review:

- Token name and symbol.
- Chain.
- Contract address.
- Strength score out of 100.
- Audit score out of 100 when available.
- Token age.
- Holder count and top-holder concentration.
- Liquidity and DEX context.
- Ownership, honeypot, and LP checks.
- DexScreener and trading-tool links.
- One concise tip reminding users to verify before acting.

### Private User Bot

The main Telegram bot is the user control surface:

- Signup and 48-hour trial.
- Wallet generation, import, and watch-only wallet tracking.
- AES-256-GCM encrypted private key storage for generated/imported wallets.
- Portfolio and PnL summaries.
- Detector profile controls.
- Trading settings.
- Billing and payment status.
- Referral code creation, tracking, and payout wallet setup.

The bot is designed around guided presets first, then advanced controls for users who want deeper tuning.

### Operator Admin Panel

The admin panel is for the Lazarus team:

- Users and Telegram usernames.
- Trial and subscription status.
- Revenue and invoice tracking.
- Referral codes, commissions, and payout states.
- Worker and signal health.
- Operational readiness before enabling live trading more broadly.

## Product Principles

| Principle | Meaning |
|---|---|
| Telegram-native | The core product should work from Telegram without requiring a web dashboard. |
| Guided by default | New users should not need to understand every market parameter before starting. |
| Advanced when needed | Experienced users can tune sensitivity, liquidity, market cap, volume, holders, cooldowns, DEXes, and chains. |
| Tenant-safe | User settings, wallets, trades, subscriptions, and referrals are scoped to the right user/tenant. |
| Risk-gated | Live execution must remain controlled until operational validation is complete. |
| Mobile-readable | Signal posts and menus should be compact, structured, and easy to scan. |
| Public-safe | Public docs explain the product clearly without exposing private source code or operational secrets. |

## How To Read These Docs

If you are new to Lazarus:

1. Start with [Product Overview](docs/product-overview.md).
2. Read the [User Journeys](docs/user-journeys.md) to understand how people actually use the bot.
3. Read [Signals and Scoring](docs/signals-scoring.md) to understand the alert format.
4. Read [Wallets and Security](docs/wallets-security.md) before any wallet or trading workflow.
5. Read [Launch Readiness](docs/launch-readiness.md) to understand what must happen before broader live access.

If you are syncing to GitBook:

- `README.md` is the landing page.
- `SUMMARY.md` defines the left navigation.
- `CHANGELOG.md` tracks public documentation and product-spec changes.
- All long-form pages live under `docs/`.

## Documentation Map

### Start Here

- [Product Overview](docs/product-overview.md)
- [Product Specification](docs/product-spec.md)
- [System Model](docs/system-model.md)
- [User Journeys](docs/user-journeys.md)

### Telegram Product

- [Telegram User Experience](docs/user-experience.md)
- [Signals and Scoring](docs/signals-scoring.md)
- [Subscriptions and Referrals](docs/subscriptions-referrals.md)

### Trust And Operations

- [Wallets and Security](docs/wallets-security.md)
- [Admin and Operations](docs/admin-operations.md)
- [Launch Readiness](docs/launch-readiness.md)
- [Roadmap](docs/roadmap.md)

### Reference

- [Glossary](docs/glossary.md)
- [FAQ](docs/faq.md)
- [Documentation Policy](docs/documentation-policy.md)
- [Changelog](CHANGELOG.md)

## Current Public Status

Lazarus is in production-readiness buildout:

- Public docs are available.
- The public signal channel design is specified.
- The Telegram user bot flow is specified.
- The billing and referral model is specified.
- Live trading is treated as a controlled beta capability, not a public default.

## Important Notice

Lazarus deals with volatile on-chain markets. Public signal posts are informational and are not financial advice. Users are responsible for their own wallet security, risk exposure, and trading decisions.

