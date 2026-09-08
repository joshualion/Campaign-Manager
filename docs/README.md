# Campaign Manager Documentation

This directory contains deployment, configuration and self-service documentation for the public Campaign Manager Community / Self-Hosted distribution.

Campaign Manager is free to download and use on infrastructure you control. Community operation does not require a software licence key. Optional paid services such as QuickStart Geography Provisioning, Professional Installation, Priority Support, Managed Deployment and Campaign SMS are separate convenience/support services.

## Start here

- [Product overview](product-overview.md) — verified live-demo capabilities and product strengths
- [Installation guide](installation.md) — complete release-to-install workflow
- [cPanel installation](cpanel-installation.md) — practical shared-hosting deployment
- [VPS / Linux installation](vps-installation.md) — Apache/Nginx-oriented server deployment
- [Upgrading](upgrading.md) — safer update planning and rollback preparation
- [Troubleshooting](troubleshooting.md) — common deployment/runtime diagnostics

## Campaign operations

- [Political campaign scopes](campaign-scopes.md)
- [Polling Unit Agent workflow](polling-unit-agent-workflow.md)
- [Election Situation Room](election-situation-room.md)
- [Roles and permissions](roles-and-permissions.md)

## Campaign configuration

- [Campaign scopes](campaign-scopes.md)
- [Geography setup](geography-setup.md)
- [QuickStart Geography Provisioning](quickstart.md)
- [Campaign SMS](sms.md)
- [Frequently asked questions](faq.md)
- [Licence status and decision notes](licensing.md)

## Screenshot assets

The first live-demo audit has been completed and verified screenshot candidates have been captured. A final screenshot refresh is still planned after privacy-safe election-demo data is populated, so the README keeps stable insertion slots rather than publishing empty election/agent states as final showcase images.

Screenshot assets belong under:

```text
docs/images/screenshots/
```

Reserved README filenames:

```text
dashboard-overview.webp
political-structure.webp
supporter-member-management.webp
electoral-geography.webp
field-agent-operations.webp
election-monitoring-results.webp
```

Recommended master size: **1600×900 (16:9)**, with sensitive/demo-identifying information reviewed before publication and interface text kept readable at GitHub README width.

See [the screenshot asset handoff file](images/screenshots/README.md) for the complete insertion plan.

## Important deployment note

The public distribution repository intentionally does not expose the private Campaign Manager application source/dependency manifest. Therefore this documentation does not invent a PHP version or extension list. Use the **Requirements** step of the installer and the requirements shipped with the release you are deploying as the authoritative compatibility check. If a future public release publishes a verified runtime matrix, this documentation should be updated to match it.
