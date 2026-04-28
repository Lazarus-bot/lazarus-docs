# Documentation Policy

The public docs should stay useful, current, and safe to publish.

## What Must Be Updated

Update the docs when any of these change:

- Public signal format.
- Scoring model explanation.
- Supported chains.
- Supported DEX coverage.
- Telegram onboarding flow.
- Wallet features.
- Security model.
- Billing plans or pricing.
- Referral rules.
- Live trading access policy.
- Admin/operator workflow.
- Launch status.

## Changelog Rules

Every meaningful public-facing change should update `CHANGELOG.md`.

Use these sections:

- Added.
- Changed.
- Fixed.
- Clarified.
- Deprecated.
- Removed.

Keep the changelog readable for non-engineers.

## GitBook Sync Rules

GitBook should use:

- `README.md` as the landing page.
- `SUMMARY.md` as navigation.
- `docs/` for long-form pages.
- `CHANGELOG.md` for update history.

When adding a page, update `SUMMARY.md` in the same change.

## Public Safety Rules

Do not publish:

- Source code from the private repo.
- Bot tokens.
- API keys.
- Wallet private keys.
- Server IPs that are not intentionally public.
- Internal passwords.
- Private deployment runbooks.
- Exploit details that reduce user safety.

Do publish:

- Product behavior.
- User flows.
- Safety principles.
- Public pricing.
- Public referral rules.
- Public launch state.
- Risk disclaimers.

## Writing Style

Write docs that are:

- Direct.
- Specific.
- Mobile-readable.
- Clear for users who are not engineers.
- Honest about risk.
- Detailed enough for GitBook readers to understand the product without seeing private code.

