# Wallets and Security

Wallet security is central to Lazarus.

## Wallet Types

### Generated Wallet

Lazarus creates a new EVM wallet for the user. The private key is encrypted before storage.

### Imported Wallet

The user imports an existing private key. The private key is normalized, validated, and encrypted before storage.

### Watch-Only Wallet

The user adds an address for tracking. Watch-only wallets cannot sign transactions.

## Encryption Model

Private keys should be stored using AES-256-GCM with:

- A 32-byte encryption key.
- Random IV per secret.
- Authentication tag.
- Key version.
- Tenant/user/address context as additional authenticated data.

This means encrypted key material is scoped to the expected wallet owner context.

## Tenant Boundaries

Every sensitive object should be scoped to the tenant/user:

- Wallet rows.
- Default trading wallet.
- Trading settings.
- Detector settings.
- Trade intents.
- Positions.
- Trades.
- Portfolio snapshots.
- PnL snapshots.

Live signing must check that the selected wallet belongs to the tenant/user context of the trade intent.

## Live Trading Gates

Live trading should require:

- Operator feature flag.
- Tenant/user allowlist during beta.
- User risk acknowledgement.
- Active subscription.
- Active generated/imported wallet.
- Per-wallet execution lock.
- Risk gate approval.

Watch-only wallets cannot sign live trades.

## User Guidance

Users should be told:

- Only fund wallets with money they can afford to lose.
- Start with paper mode.
- Start live mode with tiny amounts.
- Verify every token independently.
- Never paste private keys outside the bot flow.
- The team will never ask for seed phrases.

