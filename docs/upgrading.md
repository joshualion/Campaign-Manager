# Upgrading Campaign Manager

Campaign Manager application updates are distributed through GitHub Releases. Treat an upgrade as a production deployment change: back up first, read the release notes, preserve environment/user data, and verify after the update.

## Before upgrading

1. Read the release notes for the version you are moving to.
2. Confirm the new release is intended for your current deployment/profile.
3. Back up the application database.
4. Back up `.env`.
5. Back up user-generated/uploaded files and any storage content not reproducible from the release package.
6. Record the currently running version.
7. If the installation is mission-critical, rehearse the update on a staging copy first.

## Download the official package

Use the official release asset:

[GitHub Releases](https://github.com/joshualion/Campaign-Manager/releases)

The normal production package is:

```text
campaign-manager.zip
```

Do not substitute GitHub's automatically generated source-code archive for the release asset.

## Safe deployment pattern

Because releases can change over time, follow release-specific instructions first. A conservative Laravel deployment pattern is:

1. place the application in maintenance mode where appropriate;
2. deploy/extract the new release without overwriting your `.env` or user-generated data blindly;
3. restore/preserve the production `.env` values;
4. ensure `storage/` and `bootstrap/cache/` retain correct ownership/permissions;
5. run any database migration command explicitly required by the release;
6. clear stale framework caches;
7. restart long-running queue workers if asynchronous queues are in use;
8. return the application to service;
9. verify login, dashboards, campaign scope/geography, uploads, queues, scheduler and mail.

Common Laravel maintenance commands that may be used during a documented release deployment include:

```bash
php artisan down
php artisan migrate --force
php artisan optimize:clear
php artisan queue:restart
php artisan up
```

Do **not** run a command merely because it appears above. Use it when it applies to your deployment and the release notes. For example, `queue:restart` is relevant only if long-running queue workers are being used.

## Do not overwrite blindly

Be especially careful with:

```text
.env
storage/
publicly linked user-upload directories
server-specific web-server configuration
cron/process-manager configuration
```

The release package should replace application release files, not erase site-specific secrets or campaign data.

## Database migrations

Take a database backup before running migrations.

If a release requires migrations, execute them from the application directory using the release's documented command. On a production Laravel deployment this is commonly:

```bash
php artisan migrate --force
```

Never test an unfamiliar migration workflow first against the only production database copy.

## Rollback preparation

Before starting, keep:

- the previous working application release;
- the pre-upgrade database backup;
- the previous `.env` backup;
- user-upload/storage backups;
- a record of deployment commands used.

A rollback may require both restoring the prior application files and restoring the matching database backup if the newer release introduced incompatible schema changes.

## After upgrading

Verify:

- reported application version
- login and role access
- campaign scope and geography
- dashboards
- member/supporter workflows used by your team
- uploads/media
- queue processing where configured
- scheduler where configured
- mail/SMS integrations where enabled
- server logs for new errors

## Need assistance?

Migration/Upgrade Assistance and Priority Technical Support are optional paid Govware services. Community users can still manage their own updates independently.

[Campaign Manager website](https://www.campaignmanager.ng)
