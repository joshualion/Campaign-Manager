# Automatic updates from version 1.1.6

Checking for updates is free. Manual application downloads are free on GitHub. The in-app automatic-update service requires active coverage for the registered installation and campaign scope.

## The customer experience

1. Sign in as Super Admin and open **Official Updates → Update automatically**.
2. Campaign Manager checks the release, hosting capabilities and database backup/recovery support before offering payment.
3. If coverage is missing, select **Continue to secure payment** and complete the Portal checkout. Return to the same screen and select **I have paid — check coverage**.
4. If coverage is active, no additional payment is needed. Confirm the short maintenance period and select **Back up and update**.
5. The application downloads and verifies the package, creates private database/file backups, installs reviewed changes and checks the result.

An uncovered installation cannot use the revised in-app service to download the application update archive. Clients choosing the free manual method download it directly from GitHub.

## Existing 1.1.3, 1.1.4 and 1.1.5 installations

Those versions contain older updater code. Discovering a release cannot replace the installed updater or correct its existing screens. Version 1.1.3/1.1.4 also predates the engine-aware backup support. Apply the **signed 1.1.6 updater bootstrap once** to obtain the new flow before starting the application update.

Download these two files from the [official 1.1.6 release](https://github.com/joshualion/Campaign-Manager/releases/tag/v1.1.6):

- campaign-manager-updater-bootstrap.zip
- campaign-manager-updater-bootstrap.zip.sha256

Place them together in a private directory outside the web document root, verify the archive, and extract it:

```sh
sha256sum --check campaign-manager-updater-bootstrap.zip.sha256
unzip campaign-manager-updater-bootstrap.zip -d campaign-updater-1.1.6
cd campaign-updater-1.1.6
php bootstrap-install.php /absolute/path/to/existing/core
```

Replace the example path with the existing Core directory containing artisan and .env. Use the installation's PHP 8.2+ CLI executable. The installer verifies the signed bootstrap and all its files against the established release key. It preserves the installed application, database, environment and uploads.

If a previous bootstrap exists and no update/recovery is active, archive and replace it using:

```sh
php bootstrap-install.php /absolute/path/to/existing/core --replace-bootstrap
```

Sign in to the existing application as Super Admin and open **/campaign-update-bootstrap.php** on its own domain. Select **Check for updates** to load the latest release, then use that screen for the coverage-first automatic update. The bridge is removed after success. The bootstrap supports reviewed installed versions 1.0.8 through 1.1.5. Direct upgrades from 1.1.3, 1.1.4 and 1.1.5 to 1.1.6 are rehearsed before publication; intermediate installation is unnecessary for those paths.

A package downloaded earlier by the old screen is only staged; it is not installed. The new screen refreshes latest-release metadata and can reuse a matching verified package after checking coverage. An older unused package is replaced automatically when you start the covered update. Packages associated with active updates or pending recovery and all private recovery backups stay protected. If the release changes after review, review the new target before proceeding.

## Database backups and recovery

Version 1.1.6 preserves existing table engines. It uses a transaction snapshot for InnoDB or read locks for supported mixed local engines, including MyISAM, MEMORY and MariaDB Aria. It also supports CSV/ARCHIVE where available. Missing or unsuccessful native database export tools automatically select a streaming PHP/PDO backup. Incomplete exports are discarded and retried from a fresh snapshot.

Failed installation steps attempt automatic restoration of the verified pre-update database and managed application files. A separate supervisor handles interrupted workers and waits for surviving migration commands. An old database snapshot is never restored after the updated application may have reopened to new writes.

Backups remain in private storage under storage/app/updates/jobs. Never expose or send database exports, environment snapshots, connection files or private logs publicly.

The updater cannot bypass denied hosting permissions, exhausted storage or corruption. Unsupported connection topologies, active database events and independent/forced writers require a verified pause strategy. Readiness detects known incompatibilities before checkout; resources and permissions can still change later. If recovery cannot be verified, the application stays protected in maintenance and keeps its backups. Existing update coverage remains available for retry.

## Release validation

The 1.1.6 workflow gates publication on application checks for PHP 8.2/8.3, real native/PDO backup-and-restore tests for MySQL 8.0 and MariaDB 10.11/11.4, and signed-bootstrap upgrades from the official 1.1.3, 1.1.4 and 1.1.5 archives.

Isolated upgrade rehearsals replace entitlement calls with test stubs. They do not constitute a live payment or customer-production-server test.
