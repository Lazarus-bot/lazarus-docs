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

## Example Main Menu Structure

The exact wording can evolve, but the structure should stay stable:

```text
Lazarus

Account
- Plan: Trial / Premium / Locked
- Wallets: 1 of 5
- Mode: Paper

Signal Setup
- Detector: Balanced
- Trading: Starter
- Chains: Base

Tip: Start with paper mode until your settings feel right.
```

Recommended button layout:

```text
[Wallets] [Portfolio]
[PnL] [Detector]
[Trading] [Billing]
[Referrals] [Help]
```

## Example Detector Menu

```text
Detector

Profile
- Preset: Balanced
- Interface: Guided
- Chains: Base

Filters
- Score: 70/100 minimum
- Liquidity: $10K+
- Holders: 100+
- Cooldown: 60 minutes

Tip: Use Advanced only when you want to tune each filter yourself.
```

Recommended buttons:

```text
[Starter] [Balanced: On] [Aggressive]
[Advanced] [Chains: Base]
[Trading] [Menu]
```

## Empty States

Empty states should help users decide what to do next.

Examples:

- No wallets: "Add a wallet to start tracking portfolio and PnL."
- No portfolio snapshot: "Portfolio will appear after the next wallet scan."
- No referrals: "Share your code to start tracking referred users."
- Trial expired: "Your trial has ended. Upgrade to continue."

Avoid technical explanations in empty states.

## Confirmation Rules

Require confirmation for:

- Importing a private key.
- Enabling live mode.
- Acknowledging live trading risk.
- Removing or disabling a wallet.
- Requesting referral payout.
- Any destructive admin action.

Do not require confirmation for:

- Viewing menus.
- Switching guided presets.
- Opening external links.
- Viewing portfolio or PnL.

## Tone Rules

Use plain, confident language:

- "Your trial ends in 12 hours."
- "Live trading is locked until risk acknowledgement and operator approval."
- "Balanced is a practical default for most users."

Avoid hype:

- Do not say "guaranteed."
- Do not say "safe token."
- Do not say "easy profit."
- Do not imply Lazarus has certainty.
