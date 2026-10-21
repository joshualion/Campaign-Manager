# Automatic updates from v1.1.8

Checking for updates and manual downloads are free. Automatic installation requires active coverage for the registered installation and campaign scope. Prices and coverage periods come from CampaignManager.ng.

## Update your installation

1. Sign in as Super Admin and open **Official Updates**.
2. Select **Check for Updates**. If a newer release is available, select **Update Automatically** or **Manual Update**.
3. With active coverage, Campaign Manager checks whether the installation can update safely and asks you to confirm installation.
4. Without coverage, it opens secure Portal checkout. Use the Portal account for the installation's registered administrator email, review the price and coverage period, and choose a payment method.
5. After genuinely confirmed payment, return to your own installation. Campaign Manager checks coverage and the signed release again. Select **Confirm and Install Update** when ready.
6. Keep the progress page open. The updater backs up the application/database, briefly pauses access, applies approved changes and checks application health before reporting success.

A page visit, refresh, payment return or update check never installs an update by itself. A pending bank transfer does not provide active coverage until approved. Retrying checkout reuses the existing purchase rather than intentionally creating another charge. A failed or cancelled payment does not change the installed version.

## Repair an older updater once

An older installed updater cannot repair itself merely by discovering a newer full release. If it fails to open, redirects to a malformed login address, or exposes the old update controls, use the **official signed v1.1.8 recovery bootstrap**.

Follow [the recovery instructions](updater-recovery-v1.1.8.md). The supported process uses cPanel File Manager to upload/extract privately and cPanel Terminal to run one installer command; no PHP source editing is needed. Hosts without Terminal/process execution need assistance from their hosting operator or the free manual upgrade method. There is no promised one-click browser recovery.

Installing or opening the bootstrap preserves the current Core version, environment, uploads, registered identity and database. The real application update requires separate explicit confirmation. An existing faulty bootstrap can be archived/replaced only when no update or recovery is active.

The release gates rehearse actual official v1.1.3, v1.1.4, v1.1.5 and v1.1.6 installations against the packaged bootstrap and signed update. Older supported source versions and compatibility are checked by the installer and signed release policy; unsupported paths stop safely.

## Registration and ownership

A registered installation shows its domain, administrator email and active registration status. Existing verified ownership is not repeatedly confirmed. If ownership proof is genuinely missing, complete the one-time email verification already sent during installation, or follow the guided recovery link.

Sensitive domain/contact changes remain under **Manage Registration Details**. Editing a local administrator's email does not transfer Portal ownership. Another authorized Super Admin can use coverage that is already active, but purchasing requires the verified registered contact's Portal account.

## Backups and recovery

The updater verifies signed metadata, package integrity and the supported source version, then checks hosting/database capabilities before installation. It creates private recoverable backups and preserves environment configuration, installation identity, uploads and existing campaign/user data. Only approved pending migrations may run; no reset or seed is part of an update.

Supported MySQL/MariaDB backup paths preserve table engines and use a native export or a verified streaming fallback. Separate supervision handles interrupted workers. Recoverable failures restore verified application/database backups. If recovery cannot be verified, keep maintenance enabled and contact support before retrying. Never delete recovery backups or expose private logs, database exports or environment snapshots publicly.

See [recovery and rollback instructions](updater-recovery-v1.1.8.md#failure-and-rollback) for the job-specific recovery command. A database snapshot must not be blindly restored after the updated application has reopened to new writes.

## Free manual updates

**Manual Update** opens the official GitHub release. Download `campaign-manager.zip` and follow the [manual upgrade guide](upgrading.md). Do not substitute GitHub's source-code ZIP for the application package.

## What release tests prove

Release checks cover PHP 8.2/8.3, MySQL 8.0, MariaDB 10.11/11.4, signatures/checksums, packaged bootstrap HTTP behavior and older-archive upgrades. Isolated upgrade rehearsals stub entitlement calls and do not involve real payments or a customer's production database. A real payment followed by a successful customer-production upgrade is a separate acceptance test; do not infer it from CI alone.
