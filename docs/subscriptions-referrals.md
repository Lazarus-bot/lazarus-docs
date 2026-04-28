# Subscriptions and Referrals

Lazarus combines subscription access with a referral program.

## Trial

Every new user receives a 48-hour trial.

During the trial, the user can explore the bot, set up a wallet, review detector settings, and understand the product before paying.

When the trial expires, access should lock until payment is received.

## Plans

### Standard

- One wallet.
- Good for users who want a simple setup.

### Premium

- Five wallets.
- 0.05 ETH per month.
- Designed for active users who manage multiple wallets or strategies.

## Payment Approach

The initial payment system can use internal on-chain payment monitoring:

- User receives payment instructions.
- Payment amount uses a unique exact amount where needed.
- Payment monitor confirms matching inbound transfer.
- Subscription extends after confirmation.

External providers can be added later if they reduce support and accounting complexity.

## Referral Economics

Referral model:

- Referrer earns 25% of subscription revenue attributed to their code.
- Referrer earns 25% of the platform's 1% transaction fee from referred user volume.
- Users can configure a payout wallet.
- Earnings can be claimed or paid out based on operator rules.

## Referral UX

The bot should make referrals easy:

- Generate a code automatically.
- Show the code clearly.
- Provide a Telegram share link.
- Track referred users.
- Track pending, available, and paid rewards.
- Let users set or update payout wallet.

## Referral Safety

Referral accounting should be ledger-based:

- Attribution should be stored once per referred tenant.
- Commissions should reference their source event.
- Payouts should be traceable.
- Manual adjustments should be recorded.
- Duplicate commission events should be prevented.

