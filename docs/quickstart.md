# QuickStart Geography Provisioning

QuickStart Geography Provisioning is an **optional paid convenience service** for Campaign Manager Community / Self-Hosted deployments.

In plain language, it automatically installs the electoral geography needed for the campaign scope you purchased instead of requiring your team to create that structure manually.

Depending on the campaign scope, that geography can include the required:

- Regions
- States
- Senatorial Districts
- Federal Constituencies
- LGAs
- Wards
- Polling Units

The exact set depends on the campaign boundary being installed.

## Why QuickStart exists

Without QuickStart, Campaign Manager still works normally. The installer prepares the core campaign boundary, then your team builds out the remaining geography manually.

For example:

- a Presidential / National campaign starts with the national context and Regions, then the remaining States and lower geography can be added manually;
- a Governorship campaign starts with the selected State, then the relevant Senatorial Districts, Federal Constituencies, LGAs, Wards and Polling Units can be added manually;
- smaller campaign scopes start with their selected boundary and require the relevant lower geography to be completed.

QuickStart removes most of that repetitive setup work by provisioning the supported geography automatically.

## Supported high-level campaign scopes

- Presidential / National
- Governorship / State
- Senatorial
- Federal Constituency
- Local Government / Chairmanship

The exact geography returned depends on the purchased scope.

## What QuickStart is not

A QuickStart Geography Provisioning Key is **not a software licence key**.

Campaign Manager Community:

- remains free to download and use;
- does not require a software licence key;
- does not require QuickStart;
- can be configured manually for free.

QuickStart pays for **automatic geography setup and convenience**, not permission to run the application.

## Getting a QuickStart key

During installation, if you choose QuickStart, Campaign Manager provides a route to the Campaign Manager Portal where you can order provisioning for the selected campaign scope/geography.

Current service information is available at:

[Campaign Manager](https://www.campaignmanager.ng)

## Scope matching

The provisioning service validates the requested campaign context against the geography/scope purchased.

A key purchased for one scope/boundary cannot be used to provision another. For example, a State-scoped QuickStart cannot be used to provision a Presidential / National installation.

## One successful provisioning

QuickStart is intended for one successful geography provisioning for the purchased entitlement.

After successful completion, the entitlement is treated as consumed for another independent installation/provisioning session.

If a provisioning attempt is interrupted before successful completion, resume the existing installer/session flow rather than starting a separate independent provisioning attempt.

## If provisioning cannot continue

Check:

- internet connectivity from the server to the Campaign Manager Portal;
- that the selected installation scope/geography matches the purchased QuickStart entitlement;
- that you are using the correct provisioning key;
- server/application logs for the exact error;
- whether an existing provisioning session should be resumed.

Do not publish the key in GitHub Issues, screenshots or logs shared publicly.

## Manual alternative

If you do not want QuickStart, return to **Manual Geography Configuration**. Manual geography setup remains free.

See [Geography Setup](geography-setup.md).
