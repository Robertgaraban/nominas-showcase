# Public Scope

## Intent

This document defines what belongs in the public Nominas showcase and what must remain private.

## Safe to publish

- product narrative
- architecture summary
- workflow explanations
- sanitized screenshots
- selected UI descriptions
- implementation notes at a high level

## Keep private

- `.deploy.env`
- `api/config.php`
- `.env.production`
- setup/bootstrap endpoints
- deploy runbooks tied to the live environment
- real spreadsheets and operational files
- environment-specific troubleshooting notes
- private or sensitive seed paths

## Publishing rule

If a file helps explain the quality of the product, it may belong in the showcase.

If a file helps reproduce the live environment, business process, or deployment setup, it should remain private.

## Review-on-request rule

Full source review should be granted only in a real hiring, diligence, or collaboration context.
