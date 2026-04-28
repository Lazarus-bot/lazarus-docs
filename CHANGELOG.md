# Changelog

This changelog tracks public documentation and product-spec updates for Lazarus.

The private code repository has its own engineering changelog. This public changelog is for users, partners, operators, and anyone reading the GitBook docs.

## 2026-04-28

### Added

- Created the public Lazarus documentation repository.
- Added GitBook navigation through `SUMMARY.md`.
- Added a stronger landing README explaining the product, surfaces, principles, and public/private repository split.
- Added detailed docs for product overview, product specification, Telegram UX, signals/scoring, wallets/security, subscriptions/referrals, admin operations, launch readiness, system model, user journeys, glossary, FAQ, and documentation policy.
- Documented the alert bot watchlist feed as a separate informational post category from executor-grade signal posts.
- Clarified that watchlist ideas can come from strict CTO-able rows or recent indexed pools/tokens that pass basic safety scoring.
- Added strict watchlist gate requirements for DexScreener market data and GoPlus EVM security checks.
- Added the token scan tracking model for first/current/max market data and multiplier measurement.
- Added a draft holder revenue-sharing direction separate from referral accounting.

### Changed

- Expanded the public docs into a fuller GitBook handbook with concrete user journeys, launch stages, operator checklists, example Telegram menus, example signal posts, scoring caveats, payment states, referral lifecycle, and acceptance criteria.
- Reworked navigation into clearer sections: Product, Telegram Experience, Trust And Operations, and Reference.
- Updated signal/scoring docs with the `Lazarus Watchlist` format and explicit guidance that watchlist ideas do not trigger automatic execution.

### Clarified

- Public docs describe product behavior and operating principles without exposing source code or private deployment details.
- Live trading is described as a controlled beta capability that requires operational gates before broader access.
- Referral economics are documented as planned product behavior.

### Documentation Policy

- Every meaningful product, pricing, scoring, wallet, subscription, referral, or launch-flow change should update this changelog.
- GitBook navigation changes should update `SUMMARY.md`.
- New public-facing behavior should have a page or section in `docs/`.
