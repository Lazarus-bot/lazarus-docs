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

## Holder Revenue Sharing Direction

The referral model should stay referrer-first. A holder rewards program can sit beside it, but it should be a separate treasury/rewards ledger rather than being mixed into referral accounting.

Recommended draft policy:

- Referral share: 25% of eligible subscription revenue and eligible bot transaction fees attributed to the referral code.
- Holder rewards pool: up to 50% of net platform revenue after infrastructure, RPC, API, treasury, and operating reserves.
- Eligibility: wallets holding at least 0.5% of the qualifying Lazarus holder supply at snapshot time.
- Distribution: monthly claim window or batched treasury payout, not automatic until treasury controls and payout caps exist.
- Anti-abuse: minimum holding period, wash-transfer checks, excluded team/treasury wallets, and clear public terms.

This needs legal and tax review before being marketed as a live holder yield program.

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

## Subscription States

| State | Meaning | User Experience |
|---|---|---|
| Trialing | User is inside the 48-hour trial | Access is open, expiry is shown |
| Active | Payment is confirmed | Premium access is open |
| Past due | A renewal period ended | User is prompted to pay |
| Locked | Access is blocked | User must pay to continue |
| Cancelled | Subscription is no longer active | User can restart by paying |

The bot should always explain the state in plain English.

## Payment UX Requirements

Payment screens should show:

- Plan.
- Amount.
- Chain.
- Payment address.
- Expiry time if invoice-based.
- Current status.
- What happens after payment.

Users should not need to contact support to understand whether they are locked, trialing, or paid.

## Referral Commission Lifecycle

1. User creates or receives a referral code.
2. New user signs up with that code.
3. Attribution is stored.
4. Referred user pays or generates eligible platform fees.
5. Commission is created.
6. Commission becomes available after any hold/review period.
7. Referrer requests payout or payout is processed automatically later.
8. Payout is marked paid with transaction reference when available.

## Referral Messaging

Referral copy should be easy to share:

```text
I am using Lazarus to track early CTO token signals on Base and Ethereum.

Use my code: ABC123
Start here: https://t.me/example_bot?start=ABC123
```

The final bot copy can be shorter, but it should preserve the code and start link clearly.
