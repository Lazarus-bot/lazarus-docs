# Telegram User Experience

Lazarus is designed to feel like a polished Telegram product, not a command-line bot.

## Message Style

Messages should be:

- Short enough to read on mobile.
- Structured with bold underlined headings.
- Lightly decorated with useful emoji.
- Written in plain language.
- Actionable without over-explaining.
- Finished with one small tip line.

Buttons should:

- Use short labels.
- Stack cleanly.
- Avoid long descriptions.
- Put destructive or risky actions behind confirmation.
- Use guided menus before advanced settings.

## Main Menu

The main menu should give users a clear route to:

- Wallets.
- Portfolio.
- PnL.
- Trading.
- Detector.
- Billing.
- Referrals.
- Help.

The menu should summarize the user's current state:

- Trial or subscription status.
- Active wallet count.
- Trading mode.
- Detector profile.
- Whether live trading is locked.

## Wallet Flow

Users need three wallet actions:

- Generate a new EVM wallet.
- Import an existing private key.
- Add a watch-only wallet.

Generated and imported wallets are encrypted before storage. Watch-only wallets can be used for portfolio tracking but cannot sign trades.

The wallet menu should clearly show:

- Address.
- Label.
- Type.
- Default wallet status.
- Wallet limit based on plan.

## Trading Flow

The trading menu should start with guided controls:

- Starter.
- Balanced.
- Aggressive.
- Advanced toggle.
- Chain selector.
- Paper/live status.
- Auto-trading status.

Advanced mode can expose:

- Per-trade size.
- Global budget.
- Per-token cap.
- Daily loss limit.
- Score threshold.
- Slippage.
- Allowed signal types.

Live mode should always explain what is required before activation:

- Funded wallet.
- Risk acknowledgement.
- Operator allowlist during beta.
- Subscription access.
- Kill switch availability.

## Detector Flow

The detector menu should explain what kind of tokens the user is asking Lazarus to find.

Guided profiles:

- Starter: strict, fewer alerts.
- Balanced: practical default.
- Aggressive: more alerts, higher risk.

Advanced filters:

- Liquidity.
- Market cap.
- Volume.
- Holders.
- Top-holder concentration.
- LP locked/burned.
- Honeypot strictness.
- Renounced ownership.
- Cooldown.
- Daily signal cap.

## Referral Flow

The referral menu should make sharing easy:

- Show the user's referral code.
- Show a Telegram share link.
- Show attributed signups.
- Show pending/available/paid commissions.
- Let users set a payout wallet.
- Let eligible users request payout.

Referral copy should be direct and easy to forward.

