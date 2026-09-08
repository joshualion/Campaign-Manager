# Campaign Manager Troubleshooting

Use this guide for common installation and runtime problems on Community / Self-Hosted deployments.

Before changing anything, take note of:

- Campaign Manager version
- hosting type (cPanel/shared/VPS)
- PHP version
- web server (Apache/Nginx/LiteSpeed/etc.)
- database engine/version
- exact error text
- the installer/runtime stage where it happens

Never paste passwords, `.env`, API keys, database credentials, QuickStart keys or campaign personal data into a public issue.

## HTTP 500 / Internal Server Error

Check in this order:

1. web-server/PHP error log;
2. Laravel application log under `storage/logs/`;
3. `APP_KEY` exists;
4. database credentials are valid;
5. `storage/` and `bootstrap/cache/` are writable;
6. PHP version/extensions satisfy the installer's Requirements step;
7. stale caches are cleared after configuration changes.

Where CLI access exists:

```bash
php artisan optimize:clear
```

If `APP_DEBUG` is enabled temporarily for diagnostics, disable it again before production use. Do not expose stack traces containing secrets to the public web.

## HTTP 403 / Forbidden

Common causes include:

- incorrect web-server permissions/ownership;
- domain pointed at the wrong directory;
- hosting security rule blocking a request;
- web-server configuration denying access;
- an authenticated user attempting a route outside their allowed role/scope.

First confirm the domain document root is exactly the application's `public/` directory. Then inspect server/application logs for the route being rejected.

Do not resolve 403 errors by making the entire application world-writable.

## Blank page

A blank response is often a hidden PHP/server error.

Check:

- PHP error log;
- Laravel log;
- correct PHP runtime;
- required extensions;
- file permissions;
- application caches;
- whether production error display is hiding the real exception.

Use server-side logs rather than enabling verbose public error output on a live campaign site.

## Incorrect document root

Symptoms can include 403/404 errors, exposed directories, missing assets, broken routing or accidental exposure of sensitive application files.

The website root must point to:

```text
/path/to/campaign-manager/public
```

not:

```text
/path/to/campaign-manager
```

On cPanel, change the domain/subdomain document root. On Apache/Nginx, change `DocumentRoot`/`root` in the virtual host/server block.

## Missing APP_KEY

Symptoms commonly include encryption/session failures.

If the installer has not already generated it and shell access is available:

```bash
php artisan key:generate
```

Do not change `APP_KEY` on an established production installation casually: values encrypted with the old key may become unreadable.

## Database connection failure

Verify:

```text
DB_HOST
DB_PORT
DB_DATABASE
DB_USERNAME
DB_PASSWORD
```

Also check:

- database exists;
- database user has access to it;
- cPanel prefixes are included where applicable;
- remote database hosts allow the connection;
- firewall/security groups permit database traffic if DB is remote;
- the database service is running.

Avoid using a database root/superuser account for normal application access.

## PHP extension / requirements failure

The release installer Requirements step is authoritative for the installed version.

If a requirement fails:

- enable the extension in cPanel/PHP Selector; or
- install/enable the matching package on your VPS; or
- ask the hosting provider to enable it.

Confirm both web PHP and CLI PHP if you run Artisan or cron jobs: they can be different versions.

## Storage permission errors

Laravel needs write access to:

```text
storage/
bootstrap/cache/
```

Fix ownership/group permissions appropriate to the hosting model. Avoid `chmod 777` as the default fix.

After fixing permissions, clear stale caches if necessary:

```bash
php artisan optimize:clear
```

## Cache/config appears stale

After changing `.env`, deployment files or configuration, clear cached framework state:

```bash
php artisan optimize:clear
```

If your production deployment deliberately rebuilds caches, do so only after confirming the environment values are correct.

## Storage link / media problems

If uploaded media is expected to be public but URLs fail:

- complete the application's storage setup step;
- verify the expected public storage link exists;
- verify target directories are readable/writable as required;
- check `APP_URL`;
- confirm HTTPS/domain configuration;
- inspect filesystem disk configuration if customised.

Do not expose the whole `storage/` tree publicly.

## Queue jobs do not run

If your installation uses an asynchronous queue driver, a worker must be running.

Check:

```text
QUEUE_CONNECTION
```

Then verify the corresponding worker/service/process manager is active.

A generic diagnostic command is:

```bash
php artisan queue:work
```

Do not leave a production worker tied to an interactive SSH session; use the hosting/process-management method appropriate to your server.

If you are using the synchronous queue connection, there is no persistent worker to run.

## Scheduler / cron is not running

If an enabled feature depends on Laravel scheduled tasks, verify cron calls the scheduler every minute from the application directory:

```cron
* * * * * cd /path/to/campaign-manager && php artisan schedule:run >> /dev/null 2>&1
```

Confirm cron uses the correct PHP CLI binary and that the cron user can access the application.

## Mail does not send

Verify:

- mail driver/mailer;
- SMTP host/port;
- encryption mode;
- username/password;
- sender address;
- provider firewall/network restrictions;
- queue worker if mail is queued;
- application logs for transport errors.

Do not post SMTP credentials in GitHub Issues.

## Incorrect APP_URL

Set `APP_URL` to the final public URL, including HTTPS:

```text
APP_URL=https://campaign.example.org
```

An incorrect value may produce wrong links, redirects, callbacks or asset/media URLs.

After changing it:

```bash
php artisan optimize:clear
```

## QuickStart provisioning problem

Confirm:

- you selected the same campaign scope/geography for which QuickStart was purchased;
- you are entering a **QuickStart Geography Provisioning Key**, not treating it as a software licence;
- the server can reach the Campaign Manager Portal;
- an interrupted provisioning attempt is resumed rather than starting a separate independent provisioning session.

QuickStart is optional. If you are not using it, choose Manual Geography Configuration and continue without a key.

## Before opening an issue

Collect sanitised information:

- version
- hosting type
- PHP version
- database engine
- web server
- error text
- installation stage
- relevant log lines with secrets removed

Then use the appropriate GitHub issue template.
