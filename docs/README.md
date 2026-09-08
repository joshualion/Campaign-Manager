# Campaign Manager Documentation

This directory contains deployment, configuration, operations and self-service documentation for the public Campaign Manager Community / Self-Hosted distribution.

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

## Practical campaign technology guides

- [How to Organise a Political Campaign in Nigeria from State to Polling Unit](guides/organising-political-campaign-nigeria.md)
- [Political Campaign Management Software: What a Modern Campaign Actually Needs](guides/political-campaign-management-software.md)
- [How to Manage Campaign Supporters and Volunteers Without Spreadsheets](guides/campaign-supporters-without-spreadsheets.md)
- [How Polling Unit Agent Management Works on Election Day](guides/polling-unit-agent-management.md)
- [Nigeria's Electoral Geography Explained for Political Campaign Teams](guides/nigeria-electoral-geography.md)
- [How to Build an Election Situation Room for Results and Incident Monitoring](guides/election-situation-room-guide.md)
- [Self-Hosted Political Campaign Software vs Cloud SaaS Platforms](guides/self-hosted-vs-saas-campaign-software.md)
- [Political Campaign CRM vs a General CRM: What's the Difference?](guides/political-campaign-crm.md)

These guides are educational resources for campaign teams and technical operators. They explain the underlying operational problem first and link back to Campaign Manager only where the product directly supports the workflow being discussed.

## Campaign configuration

- [Campaign scopes](campaign-scopes.md)
- [Geography setup](geography-setup.md)
- [QuickStart Geography Provisioning](quickstart.md)
- [Campaign SMS](sms.md)
- [Frequently asked questions](faq.md)
- [Licence status and decision notes](licensing.md)

## Community

- [Support](../SUPPORT.md)
- [Contributing](../CONTRIBUTING.md)
- [Code of Conduct](../CODE_OF_CONDUCT.md)
- [Public Roadmap](../ROADMAP.md)
- [Security](../SECURITY.md)

## Screenshot assets

A verified, privacy-safe national dashboard screenshot is published in the README. Additional election/Situation Room and field-operation screenshots should only be added when they contain meaningful demo data and have been reviewed for privacy.

Screenshot assets belong under:

```text
docs/images/screenshots/
```

The current published dashboard image is:

```text
campaign-manager-dashboard-readme.jpg
```

Reserved future screenshot slots remain documented in [the screenshot asset handoff file](images/screenshots/README.md).

## Important deployment note

This public repository distributes the official Campaign Manager release package and documentation rather than maintaining the application as a public editable source tree. Therefore the documentation does not invent a PHP version or extension list that cannot be verified here. Use the **Requirements** step of the installer and the requirements shipped with the release you are deploying as the authoritative compatibility check. If a future public release publishes a verified runtime matrix, this documentation should be updated to match it.
