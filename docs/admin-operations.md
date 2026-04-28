# Admin and Operations

The admin panel is the internal control surface for Lazarus operators.

## Admin Goals

Operators need to answer:

- Who signed up?
- What is their Telegram username?
- Who is trialing, active, past due, locked, or cancelled?
- Who has paid?
- How much revenue is active?
- Which referral codes are driving users?
- Which referral payouts are pending?
- Are workers healthy?
- Are signal posts being sent?

## Core Admin Views

### Overview

High-level metrics:

- Total users.
- Active users.
- Trialing users.
- Locked users.
- Active subscriptions.
- Revenue.
- Pending invoices.
- Signal and trade activity.

### Users

User table:

- Telegram ID.
- Telegram username.
- Tenant ID.
- Plan.
- Status.
- Wallet count.
- Created date.
- Last seen date.

### Revenue

Revenue view:

- Paid invoices.
- Pending invoices.
- Expired invoices.
- Monthly recurring revenue estimate.
- Payment provider.
- Payment chain.

### Referrals

Referral view:

- Code.
- Owner.
- Referred users.
- Pending commission.
- Available commission.
- Paid commission.
- Payout wallet.

### Payouts

Payout review:

- Requested payout.
- Destination wallet.
- Amount.
- Status.
- Transaction hash when paid.

## Operational Guardrails

Before public live trading, operators should verify:

- Migrations applied.
- Worker health stable.
- Public notifier posts cleanly.
- Paper trade path produces expected trade intents.
- Portfolio/PnL snapshots are updating.
- Risk gates work.
- Kill switch and halt controls work.
- Fork tests pass.
- Tiny-funded live dry run succeeds.

## Incident Controls

Lazarus should support:

- Manual halt.
- Manual kill switch.
- Worker restart.
- Failed payment review.
- Referral payout review.
- Signal channel pause.
- Live trading disablement without disabling paper mode.

