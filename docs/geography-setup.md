# Geography Setup

Campaign Manager supports two geography-setup paths:

1. **Manual Geography Configuration — Free**
2. **QuickStart Geography Provisioning — Optional paid convenience service**

In simple terms, campaign geography is the electoral structure Campaign Manager needs in order to organise people and operations correctly: **Regions, States, Senatorial Districts, Federal Constituencies, LGAs, Wards and Polling Units**, depending on the campaign scope.

## Manual Geography Configuration — Free

Manual geography configuration is part of normal Community / Self-Hosted use and requires no software licence key.

The installer creates the core campaign boundary selected during setup, then your team can build out the remaining geography yourselves.

Examples:

- **Presidential / National campaign:** the national campaign context and Regions are prepared, while your team adds the States and the lower electoral structure under them.
- **Governorship / State campaign:** the selected State is prepared, while your team adds the remaining geography required inside that State, such as Senatorial Districts, Federal Constituencies, LGAs, Wards and Polling Units.
- **Senatorial, Federal Constituency and LGA / Chairmanship campaigns:** the selected campaign boundary is prepared and your team completes the relevant lower-level geography needed for campaign operations.

The exact lower levels depend on the selected campaign scope.

Manual setup is appropriate when:

- your team already has structured geography data;
- your campaign scope is small enough to configure directly;
- you prefer to control the data-entry/import process yourself;
- you do not want to purchase automatic geography setup.

### Imports and mapping

Where the application exposes import tools, review the template and relationship requirements carefully before importing production data. Imported records should be validated for correct parent relationships before campaign users depend on dashboard/drill-down counts.

If an import path does not automatically build every electoral relationship needed by your reporting structure, use the application's manual mapping workflow or the optional QuickStart service.

## QuickStart Geography Provisioning — Optional

**QuickStart is the automatic setup option.** Instead of sitting down to create the required States, Senatorial Districts, Federal Constituencies, LGAs, Wards and Polling Units one by one, Campaign Manager provisions the supported electoral geography for the campaign scope you purchased.

For example:

- a Presidential QuickStart can prepare the supported national geography structure needed by the campaign;
- a Governorship QuickStart can prepare the supported geography for the selected State;
- Senatorial, Federal Constituency and LGA / Chairmanship QuickStart orders provision the supported geography relevant to those purchased boundaries.

This is why QuickStart is useful for large campaign scopes: it removes a substantial amount of repetitive geography data entry during installation.

Typical reasons to use it:

- avoid lengthy manual creation of electoral boundaries;
- start with a prepared geography structure;
- reduce installation/setup time;
- reduce avoidable hierarchy/mapping mistakes;
- get the supported dataset for the purchased campaign boundary automatically.

### What the key means

A **QuickStart Geography Provisioning Key** authorises this automatic geography setup only.

It is **not**:

- a software licence key;
- a Community activation key;
- a requirement for running Campaign Manager;
- permission to provision a different campaign scope/geography from the one purchased.

Community Campaign Manager continues to run without a software licence key.

### Scope and one-time-use protection

QuickStart is tied to the exact campaign scope/geography purchased. The provisioning service validates that the requested installation context matches that entitlement.

A successfully completed QuickStart entitlement is consumed for another independent installation. If a provisioning session is interrupted before successful completion, resume that existing session through the normal installer/session flow rather than trying to create another independent provisioning session.

See [QuickStart Geography Provisioning](quickstart.md).

## Validate after setup

Whether you use Manual or QuickStart, verify before onboarding real campaign operations:

- expected parent geography exists;
- LGAs belong to the intended state/district/constituency context;
- wards belong to the correct LGA;
- polling units resolve through the expected ward/LGA structure;
- dashboard counts and drill-down views reflect the campaign boundary.

## The commercial distinction

QuickStart sells **speed and automatic geography setup**, not access to the Campaign Manager software.

You can run Campaign Manager yourself for free and configure geography manually. If you prefer the system to prepare the supported electoral structure automatically, QuickStart is available as a paid convenience service.

[Visit Campaign Manager](https://www.campaignmanager.ng)
