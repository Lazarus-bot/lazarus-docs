# Signals and Scoring

Lazarus evaluates tokens through multiple lenses and converts the result into user-readable scores.

## Signal Types

### Composite

A combined signal that blends several revival indicators. This is the preferred signal type for cautious users.

### Accumulation

Indicates buying or transfer behavior that may suggest renewed interest.

### Holder Inflection

Indicates holder count growth or meaningful changes in holder behavior.

### Volume Inflection

Indicates a notable increase in volume compared with baseline activity.

### LP Add

Indicates liquidity changes that may matter for revival quality.

## Signal Post Fields

Each public signal should include:

- Token name/symbol.
- Chain.
- Contract address.
- Strength score out of 100.
- Audit score out of 100 when available.
- Token age.
- Holder count.
- Top 10 holder concentration.
- Liquidity.
- DEX.
- Renounced ownership status.
- Honeypot status.
- LP locked/burned status.
- DexScreener link.
- Trading-tool bot link.

## Strength Score

The strength score answers:

> How strong is the detected comeback signal right now?

It can consider:

- Signal type.
- Magnitude of the activity change.
- Freshness.
- Supporting market data.
- Liquidity quality.
- Holder quality.
- Risk filters.

Scores should be shown as `N/100`.

## Audit Score

The audit score answers:

> How clean is the token from a basic risk perspective?

It can consider:

- Ownership renounced.
- Honeypot result.
- LP lock or burn status.
- Liquidity level.
- Holder concentration.
- Known metadata quality.

The audit score is not a guarantee. It is a quick triage indicator.

## Suggested Score Bands

| Score | Meaning |
|---|---|
| 90-100 | Very strong signal, still requires manual review |
| 80-89 | Strong and worth reviewing |
| 70-79 | Moderate, useful for balanced users |
| 60-69 | Speculative, aggressive users only |
| Below 60 | Usually too noisy for public posting |

## Public Channel Policy

The public channel should avoid spam. Defaults should favor:

- Composite signals.
- Higher minimum score.
- Cooldowns per token.
- No duplicate posts for the same signal/channel.
- Clear links for independent verification.

