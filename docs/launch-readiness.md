# Launch Readiness

Lazarus should launch in stages. The product touches wallets, markets, payments, and user trust, so the safest path is deliberate.

## Stage 1: Documentation And Positioning

Goal: make the product understandable before inviting users.

Required:

- Public docs repo live.
- Clear explanation of what Lazarus does.
- Clear risk notice.
- Public channel format documented.
- Telegram bot flows documented.
- Referral economics documented.
- Changelog started.

## Stage 2: Public Signal Channel

Goal: prove Lazarus can post useful alerts without user funds at risk.

Required:

- Notifier bot separated from main user bot.
- Signal post format reviewed on mobile.
- Minimum score threshold configured.
- Duplicate post prevention.
- DexScreener links validated.
- Trading-tool links validated.
- Channel admin permissions configured.

Success criteria:

- Alerts are readable.
- Alerts are not spammy.
- Each alert contains enough context to review independently.

## Stage 3: Private User Bot Trial

Goal: validate onboarding, wallets, presets, billing, referrals, and portfolio views.

Required:

- 48-hour trial working.
- Wallet generation/import/watch-only flows working.
- Wallet limit enforced.
- Starter/Balanced/Aggressive profiles saved.
- Advanced settings saved as Custom.
- Billing status visible.
- Referral link generation working.
- Portfolio/PnL screens populated.

Success criteria:

- A new user can understand the bot without support.
- Settings are saved correctly.
- No private key or wallet data leaks into logs or public outputs.

## Stage 4: Paper Trading Trial

Goal: validate trading logic without moving funds.

Required:

- Paper mode default.
- Trade intents recorded under the correct tenant/user/wallet.
- Risk gates checked.
- Positions and trades recorded.
- PnL snapshots generated.
- Admin panel shows activity.

Success criteria:

- Signal to trade-intent to position flow is traceable.
- No cross-tenant accounting issue.
- Risk and budget limits are explainable.

## Stage 5: Live Trading Beta

Goal: validate tiny-funded real trades with strict controls.

Required:

- Operator live flag.
- User allowlist.
- Risk acknowledgement.
- Funded beta wallet.
- Tiny trade size.
- Kill switch tested.
- Halt tested.
- Entry and exit reconciliation.

Success criteria:

- One live entry and exit complete with the intended wallet.
- Trade records match chain activity.
- PnL and fees reconcile.
- Operator can pause or stop the system.

## Stage 6: Premium Launch

Goal: open paid access with responsible limits.

Required:

- Payment monitor stable.
- Premium wallet limits working.
- Referral commissions tracked.
- Payout process defined.
- Support process ready.
- Monitoring and backups ready.

Success criteria:

- Users can upgrade without manual intervention.
- Operators can see revenue and referral state.
- Users understand plan limits and risks.

