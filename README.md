# Lazarus

Lazarus is a Telegram-first signal intelligence platform for spotting early community takeover (CTO) activity on EVM tokens.

The product watches tokens that appear abandoned but recoverable, evaluates revival signals, publishes neatly formatted Telegram alerts, and gives approved users a guided way to monitor portfolios, configure alerts, and eventually route controlled trades from their own encrypted wallets.

This repository contains **public product and specification documentation only**. The application source code is private.

## What Lazarus Is Building

Lazarus is designed around three connected experiences:

1. **Public signal channel**
   - Posts concise CTO-starting alerts.
   - Shows contract address, chain, token age, holder data, liquidity, audit checks, and a score out of 100.
   - Links directly to DexScreener and a trade-tool bot.

2. **User Telegram bot**
   - Handles onboarding, trial access, wallet setup, portfolio views, PnL, detector settings, and trading preferences.
   - Supports guided presets for newer users and advanced controls for experienced users.
   - Keeps each user's configuration and activity under their own tenant/user record.

3. **Operator admin panel**
   - Gives the team visibility into users, paid status, revenue, referrals, payouts, signals, and worker health.
   - Supports operational review before expanding live access.

## Product Principles

- **Telegram-native first.** Users should not need a web dashboard for the main workflow.
- **Guided by default.** New users get presets instead of a wall of confusing parameters.
- **Advanced when needed.** Power users can tune sensitivity, liquidity, market cap, volume, holders, score, cooldowns, and limits.
- **Tenant-safe.** Wallets, trades, settings, subscriptions, and referral attribution are scoped to each user/tenant.
- **Risk-gated.** Live execution remains behind explicit controls, acknowledgement flows, allowlists, and operator rollout.
- **Readable alerts.** Every signal should be compact, useful, and formatted for fast mobile review.

## Documentation Map

Start here:

- [Product Overview](docs/product-overview.md)
- [Product Specification](docs/product-spec.md)
- [Telegram User Experience](docs/user-experience.md)
- [Signals and Scoring](docs/signals-scoring.md)
- [Wallets and Security](docs/wallets-security.md)
- [Subscriptions and Referrals](docs/subscriptions-referrals.md)
- [Admin and Operations](docs/admin-operations.md)
- [Roadmap](docs/roadmap.md)
- [FAQ](docs/faq.md)

## Important Notice

Lazarus deals with volatile on-chain markets. Public signal posts are informational and should not be treated as financial advice. Users are responsible for their own trading decisions, wallet security, and risk exposure.

