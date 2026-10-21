# Repair an older Campaign Manager updater

Use the official v1.1.8 recovery bootstrap when the updater on an existing supported installation cannot start. A full release download alone does not repair an older updater. Manual software downloads remain free.

1. Download `campaign-manager-updater-bootstrap.zip` and its `.sha256` file from the official v1.1.8 release after publication. Use only `joshualion/Campaign-Manager` on GitHub. Do not use a test candidate.
2. Verify the ZIP checksum against the official checksum file. Upload it using cPanel File Manager and extract it into a private folder **outside the web document root**.
3. Open cPanel Terminal. Run `php /absolute/private/bootstrap/bootstrap-install.php /absolute/path/to/existing/core`. Use the existing application directory, not its public web directory. The installer verifies the signed bundle before installing it. The hosting PHP CLI must be compatible with the existing application.
4. If a faulty bootstrap already exists, first ensure that no update is running or awaiting recovery. Add `--replace-bootstrap` to the same command. The old bootstrap is archived privately; application data, `.env`, identity and installed Core version are preserved. Do not bypass a refusal caused by an active update.
5. Sign in to Campaign Manager as Super Admin and open `/campaign-update-bootstrap.php` on your installation. For a subdirectory installation, include that same subdirectory in the address. Check for updates and choose **Update Automatically**.
6. If asked to pay, use the Portal account for the registered administrator email. Complete any genuinely missing one-time email ownership verification. Pending bank transfers cannot update until approved. After returning, confirm installation. Keep the progress page open; a dropped connection does not cancel the server's update.

No PHP file editing is required. Installing or visiting the bootstrap does not install a Core update. A browser visit alone cannot install the bootstrap: installation requires access to the server's private files and PHP CLI. If cPanel Terminal/process execution is unavailable, ask the hosting operator or an authorized support engineer to perform the command, or use the free manual upgrade guide. Do not upload a public browser command runner.

After a verified successful update, an operator may remove `public/campaign-update-bootstrap.php` and the active `storage/app/updates/bootstrap` directory. Keep private bootstrap history and recoverable update backups until the owner confirms acceptance. Never delete a backup that is still needed for recovery.

## Failure and rollback

If the updater reports failure, keep its private backups and logs. Do not retry while an update or recovery is running. A normal recoverable failure restores the verified application/database backups automatically. Verify the original version, sign-in, uploads and representative campaign data afterward.

If recovery requires assistance, keep maintenance enabled and use the job's generated private recovery script with the hosting operator. For the actual failed job, run `php storage/app/updates/jobs/<job-uuid>/recover.php --confirm=<same-job-uuid>` from the Core directory. Add `--restore-database` when its journal says migrations started. The script verifies the job, backup and recovery state and refuses a database rollback after an update has passed final verification. Do not invent a job ID or use another installation's backup. Never run `migrate:fresh`, seeders, a database reset or an unverified archive extraction over the live installation.

For an independent hosting backup restore, restore application files and database from the **same pre-update snapshot**, preserving the matching `.env`/application key, registration identity and uploads. Verify health and the previous installed version before restoring normal access. Bootstrap replacement history restores only the updater bridge, not a Core/database upgrade.
