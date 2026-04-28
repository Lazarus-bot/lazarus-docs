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

## Example Public Signal Post

This is the shape of a good public post:

```text
Lazarus Signal

ABC on Base
0x1234...abcd

Score
- Strength: 84/100
- Audit: 91/100
- Age: 42d

Market
- Holders: 1,248
- Top 10: 21.4%
- Liquidity: $48.2K
- DEX: Aerodrome

Checks
- Renounced: yes
- Honeypot clear: yes
- LP locked/burned: 94.0%

DexScreener | Trade Tool

Tip: Verify liquidity, tax, ownership, and chart behavior before trading.
```

The post should be short, but it should not be vague. Users should know why the token appeared and what to verify next.

## Scoring Inputs By Category

### Market Activity

Signals can become stronger when:

- Volume increases versus baseline.
- Buy pressure appears after inactivity.
- Liquidity is added or becomes healthier.
- The token begins appearing across more holder wallets.

### Holder Quality

Signals can become weaker when:

- Holder count is too low.
- Top holders are too concentrated.
- Holder growth looks artificial.
- New holders appear only in tiny dust amounts.

### Liquidity Quality

Signals can become stronger when:

- Liquidity is meaningful enough for trading.
- LP is locked or burned.
- Liquidity is on a supported DEX.

Signals can become weaker when:

- Liquidity is too thin.
- LP state is unclear.
- Routing is unreliable.

### Contract Risk

Signals can become weaker when:

- Ownership is not renounced.
- Honeypot checks are negative or inconclusive.
- Token metadata is suspicious.
- Transfer behavior is abnormal.

## User Preset Relationship

Preset choice affects how many signals a user sees:

| Preset | Signal Behavior |
|---|---|
| Starter | Fewer alerts, stricter filters, composite-first |
| Balanced | More opportunities while keeping quality controls |
| Aggressive | More experimental signals and more noise |
| Custom | User-defined filters |

The public channel should usually behave closer to Starter than Aggressive.

## Scoring Caveats

Scores are decision support, not certainty.

A token can score highly and still fail because of:

- Bad timing.
- Hidden contract risk.
- Poor community follow-through.
- Liquidity removal.
- Market-wide volatility.
- Social manipulation.

Every score should be treated as a prompt for review, not a command to trade.
