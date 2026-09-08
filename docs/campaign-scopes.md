# Campaign Scopes

Campaign Manager supports multiple campaign scopes so the installation can be aligned with the electoral geography relevant to the campaign.

Supported scopes:

- Presidential / National
- Governorship / State
- Senatorial
- Federal Constituency
- Local Government / Chairmanship

## Presidential / National

Used for nationwide campaign operations. The relevant geography can extend through national/state structures and the lower electoral geography required by the campaign.

## Governorship / State

Used for a campaign centred on one state. Geography and downstream campaign structures are limited to the selected state context.

## Senatorial

Used for a senatorial-district campaign. The installer identifies the relevant state and senatorial-district context, after which the campaign operates within that selected scope.

## Federal Constituency

Used for a House of Representatives / federal-constituency campaign. The selected constituency defines the relevant campaign geography context.

## Local Government / Chairmanship

Used for a local-government/area-council style campaign scope supported by Campaign Manager. The selected LGA defines the campaign context, with downstream ward/polling-unit geography managed as applicable.

## How scope affects geography

The selected campaign scope determines which parent geography must be identified during installation and which lower-level geography is relevant afterward.

At a high level:

| Campaign scope | Campaign boundary selected during setup | Lower geography managed within that boundary |
| --- | --- | --- |
| Presidential / National | Nigeria / national | National electoral geography |
| Governorship / State | State | Districts/constituencies/LGAs/wards/polling units as applicable |
| Senatorial | Senatorial District | LGAs/wards/polling units within the district as applicable |
| Federal Constituency | Federal Constituency | LGAs/wards/polling units within the constituency as applicable |
| LGA / Chairmanship | LGA | Wards/polling units within the selected LGA |

This table is intentionally high-level. Exact live-demo terminology and dashboard drill-down behaviour will be refined after the verified Phase 2 feature audit.

## Geography setup options

Every supported scope can use the normal geography workflow available to that installation:

- **Manual Geography Configuration** — free, managed by your administrator.
- **QuickStart Geography Provisioning** — optional paid provisioning for the purchased campaign scope/geography.

A QuickStart provisioning key is not a software licence key.

See:

- [Geography setup](geography-setup.md)
- [QuickStart](quickstart.md)
