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

## Threat Model

Lazarus must assume the following risks exist:

- Users may paste the wrong private key.
- Users may fund the wrong wallet.
- Users may misunderstand live trading.
- Telegram accounts can be compromised.
- Tokens can be malicious.
- RPCs can fail or return stale data.
- Payment transactions can be delayed.
- Referral payout wallets can be mistyped.

The product should reduce these risks with clear copy, validation, confirmations, and operator controls.

## Wallet Safety UX

Wallet screens should show:

- Address in a copyable format.
- Wallet type.
- Whether the wallet can sign.
- Whether it is the default trading wallet.
- Plan wallet limit.

Private keys should never be displayed back to the user after import. For generated wallets, any export or backup flow should be treated as a sensitive action and require explicit confirmation.

## Live Trading Safety Copy

Before live trading, the user should understand:

- Paper mode is the default.
- Live mode can lose real funds.
- Signals are not financial advice.
- The selected wallet signs transactions.
- Small test amounts are strongly recommended.
- The operator may restrict live access during beta.

## Security Documentation Boundaries

Public docs can explain principles:

- Encryption algorithm.
- Tenant scoping.
- Risk gates.
- Wallet types.
- Live access policy.

Public docs should not expose:

- Secrets.
- Private deployment details.
- Internal keys.
- Infrastructure credentials.
- Exploit paths.
