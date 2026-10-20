# Restore free update checking and upgrade safely

Campaign Manager 1.1.3 and later automatically configure the trusted release public key during installation. It also handles the incorrect missing-key path from older distribution templates after its corrected code is installed. No AWS account, external key download or manual key setup is needed for a normal new installation.

## Existing installations showing the verification error

If an older installation shows **“The update check could not be completed or verified. Check server connectivity and the trusted release key.”**, the environment template may point to a key file that was not distributed. Publishing a release cannot change that already-installed configuration remotely.

Ask your hosting administrator to apply this one-time correction. This is free and does not install a paid update, change the database, or reset the application:

1. Open the existing application's root directory, containing `artisan` and its private `.env` file. Back up `.env` privately before editing it.
2. Confirm that `config/release-public.pem` exists. Keep the official bundled key; do not generate a replacement or copy a key from an untrusted source.
3. If `CAMPAIGN_RELEASE_PUBLIC_KEY_PATH` points to the **missing** `storage/app/release-keys/campaign_release_public.pem`, replace that setting with the following. For an ordinary installation, leave the optional inline key empty:

   ```dotenv
   CAMPAIGN_RELEASE_PUBLIC_KEY_PATH=config/release-public.pem
   RELEASE_SIGNING_PUBLIC_KEY=
   ```

4. From that application directory, run:

   ```sh
   php artisan config:clear
   php artisan campaign:updates-check
   ```

5. Sign in as Super Admin and retry **Check for updates**.

Keep `APP_KEY`, database settings, Portal registration credentials, uploads and installation identity unchanged. An intentionally configured custom trust key should be reviewed by its administrator instead of overwritten. Never disable signature verification or TLS verification. If the bundled file is missing, or the error persists, contact support with the installed version and error text; do not share `.env`, passwords or private backups.

## Choose an upgrade method

**Checking for updates and manual downloads are free.** The optional automatic-update service requires active paid coverage for that registered installation and campaign scope. The default coverage period is 12 months; the purchased period shown in the Portal applies. It covers eligible releases during that period and does not renew or charge automatically.

- **Paid automatic update:** follow the [1.1.5 automatic-update guide](automatic-updates.md). Existing installations through 1.1.4 need the new signed `campaign-manager-updater-bootstrap.zip` once to replace the older updater flow. It checks readiness and coverage before downloading the application archive, then backs up and updates after consent. The bootstrap itself preserves Core, environment, uploads and database. Active coverage does not require another payment.
- **Free manual update:** download `campaign-manager.zip` from the [latest official release](https://github.com/joshualion/Campaign-Manager/releases/latest), verify its SHA-256 against the published checksum, and follow the steps below. Restoring update checking does not require buying the automatic-update service.

## Manual upgrade checklist for the hosting administrator

1. Back up the **entire existing application and database** privately, including `.env`, uploads and installation/registration identity. Verify that the backup is readable and can be restored. Rehearse the upgrade on a separate copy first, especially if code or migrations were customized.
2. Extract the official application ZIP to a separate private directory. Do not run its browser installer over the existing installation. Review the release notes and any pending migrations against the existing migration history.
3. Put the existing installation in maintenance mode (`php artisan down`), stop scheduled/queue workers, and prevent new writes while replacing application files.
4. Replace the distributed application code, `vendor` and built assets from the verified release. Include its new `release-manifest.json`. Preserve the existing `.env`, `APP_KEY`, database, `storage` data, uploads, hosting-specific rules and existing installation registration. Retain required new storage directory placeholders without replacing existing private data. Avoid merging old dependency files into the new `vendor` tree.
5. Using the new application code and the existing database settings, clear generated caches (`php artisan optimize:clear`), review `php artisan migrate:status` and `php artisan migrate --pretend`, then run only the reviewed pending migrations with `php artisan migrate --force`. If an unexpected migration appears or schema compatibility is uncertain, stop and have an administrator review it. Never use `migrate:fresh`, `migrate:refresh`, `db:wipe`, installer reset or database seeders on the live installation.
6. Verify login, version, existing records, registration, uploads and update checking while maintenance remains active. Restore normal worker/cron operation and use `php artisan up` only when checks pass. Keep the private backup until the installation is confirmed healthy. If the upgrade fails, keep writes stopped and restore the matching pre-upgrade files and database together.

Versions outside the reviewed list, customized schemas and hosts without required PHP/backup capabilities need individual review. Neither method promises a safe blind overwrite of an arbitrary installation.
