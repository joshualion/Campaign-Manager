# Security Policy

Campaign Manager can hold sensitive campaign, supporter, member, field-operation and election information. Please report security concerns responsibly and **do not expose sensitive information in public GitHub Issues**.

## Report vulnerabilities privately

For a security vulnerability, contact the Campaign Manager team privately using the official channel:

**Email:** `info@campaignmanager.ng`

**Website:** https://www.campaignmanager.ng

Use a subject such as:

```text
Security Report — Campaign Manager
```

Provide enough information to reproduce and assess the issue, but minimise real campaign/customer data.

## Do not publish these in a public issue

Never post:

- passwords
- API keys or access tokens
- application secrets / `APP_KEY`
- `.env` contents
- database passwords or connection strings
- server/SSH/cPanel credentials
- QuickStart Geography Provisioning Keys
- private URLs containing authentication tokens
- campaign personal data
- supporter/member records
- phone/email lists
- private political information or campaign strategy
- production database dumps
- unredacted logs containing any of the above

If evidence is required, redact secrets and personal information first.

## What to include in a private report

Where possible include:

- affected Campaign Manager version
- deployment type (self-hosted/managed, cPanel/VPS, etc.)
- affected route/module
- concise reproduction steps
- expected vs actual behaviour
- impact assessment
- sanitised request/response or log excerpts
- screenshots with secrets/personal information removed

Please avoid destructive testing against systems you do not own or have permission to test.

## Public bug reports vs security reports

Use a normal GitHub Bug Report for ordinary reproducible application problems that do not expose a vulnerability or sensitive data.

Use the private security contact above for authentication bypass, data exposure, privilege escalation, injection, secret leakage or other vulnerability classes.

## Supported versions

Security fixes are generally delivered through current Campaign Manager releases. Check the latest supported release and release notes before reporting a problem already fixed in a newer version:

https://github.com/joshualion/Campaign-Manager/releases

## Managed deployments

Customers using a Govware-managed deployment should use their agreed support/operations channel in addition to the security contact above when the issue affects an active managed environment.
