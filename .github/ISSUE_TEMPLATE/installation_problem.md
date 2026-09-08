---
name: Installation Problem
about: Report a reproducible installation or hosting problem
labels: installation
---

## Before posting

**Remove all sensitive information.** Do not post `.env`, passwords, API keys, database credentials, server credentials, QuickStart keys, campaign data or supporter/member records.

Please review:

- [Installation Guide](../../docs/installation.md)
- [Troubleshooting](../../docs/troubleshooting.md)

## Campaign Manager version

Example: `v1.0.9`

## Hosting type

- [ ] cPanel/shared hosting
- [ ] VPS/dedicated server
- [ ] Local/testing environment
- [ ] Other

## Environment

**PHP version:**  
**Database + version:**  
**Web server:** Apache / Nginx / LiteSpeed / Other  
**Operating system/hosting platform:**

## Installation stage

Where did the problem occur?

- [ ] Requirements
- [ ] Environment
- [ ] Database
- [ ] Mail / Storage
- [ ] Campaign Scope
- [ ] Campaign Geography
- [ ] Geography Setup
- [ ] Super Administrator
- [ ] Installation / Provisioning
- [ ] Post-install verification

## What happened?

Describe the problem clearly.

## Exact error text

```text
Paste the exact sanitised error here.
```

## What did you expect?

Describe the expected result.

## Sanitised logs

Paste only the smallest relevant section. **Redact secrets, personal information, absolute private URLs/tokens and campaign data.**

```text
Relevant log lines only.
```

## Checks already performed

- [ ] Document root points to `/public`
- [ ] Installer Requirements step has no critical failures
- [ ] Database credentials tested
- [ ] `storage/` and `bootstrap/cache/` writable
- [ ] `APP_URL` is correct
- [ ] `php artisan optimize:clear` tried where CLI access exists and is appropriate
