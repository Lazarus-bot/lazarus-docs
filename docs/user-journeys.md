# User Journeys

This page describes how people should actually use Lazarus.

## Journey 1: New User Joins From A Referral Link

1. User receives a Telegram link from a friend.
2. User opens the Lazarus bot.
3. Bot recognizes the referral code.
4. Bot creates the user account and starts the 48-hour trial.
5. User sees a simple main menu.
6. User adds a watch-only wallet or generates a new wallet.
7. User selects the Starter or Balanced preset.
8. User reviews public signal examples and waits for alerts.

The user should not need to understand liquidity thresholds, holder concentration, or LP burn percentages on day one.

## Journey 2: User Wants Alerts But No Trading

1. User joins the public signal channel.
2. User reads signal posts.
3. User opens DexScreener from a post.
4. User checks chart, liquidity, taxes, and community context independently.
5. User decides whether to act manually outside Lazarus.

This journey should remain available even before live trading is opened.

## Journey 3: User Sets Up A Portfolio

1. User opens the private bot.
2. User chooses Wallets.
3. User adds a watch-only wallet or generated wallet.
4. Bot shows wallet count and plan limit.
5. User opens Portfolio.
6. Bot shows wallet value, exposure, realized PnL, unrealized PnL, and latest snapshot time.

The portfolio view should be clear even when no trades exist yet.

## Journey 4: User Configures Detector Presets

1. User opens Detector.
2. Bot shows the active profile: Starter, Balanced, Aggressive, or Custom.
3. User taps a preset.
4. Bot saves the preset.
5. Bot updates the menu with summarized settings.

The preset should make the user's intent clear:

- Starter: fewer alerts, stricter quality.
- Balanced: practical default.
- Aggressive: more alerts, more noise, higher risk.

## Journey 5: Advanced User Tunes Detection

1. User opens Detector.
2. User turns Advanced on.
3. Bot reveals detailed controls.
4. User adjusts liquidity, market cap, volume, holders, DEXes, chains, score, cooldown, and open-position limits.
5. Bot saves the profile as Custom.

Advanced mode should feel powerful but not crowded.

## Journey 6: User Upgrades To Premium

1. Trial expires or user wants more wallets.
2. User opens Billing.
3. Bot shows plan status and payment instructions.
4. User pays the exact requested amount.
5. Payment monitor confirms the transfer.
6. Subscription becomes active.
7. Wallet limit increases to five.

The billing screen should always show whether the account is trialing, active, locked, or past due.

## Journey 7: Referral Partner Shares Lazarus

1. User opens Referrals.
2. Bot displays their referral code.
3. Bot provides a shareable Telegram link.
4. New users sign up with that link.
5. Referrer sees referred users and commission status.
6. Referrer sets a payout wallet.
7. Available commission can be claimed or paid according to operator rules.

Referral flows should be transparent and easy to explain.

## Journey 8: Controlled Live Beta User

1. Operator adds user to the live beta allowlist.
2. User confirms risk acknowledgement in Telegram.
3. User selects a funded generated/imported wallet.
4. User starts with tiny trade sizes.
5. System records all live trade intents, positions, trades, PnL, and risk outcomes.
6. Operator reviews results before increasing access.

This flow should be invite-only until live trading has enough operating history.

