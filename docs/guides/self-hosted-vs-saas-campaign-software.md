# Self-Hosted Political Campaign Software vs Cloud SaaS Platforms

Political campaign teams choosing software often face a basic infrastructure decision: use a vendor-hosted SaaS platform or run a self-hosted application on infrastructure controlled by the campaign.

Neither model is automatically better. The right choice depends on technical capability, data-governance requirements, budget, customisation needs and how much operational responsibility the campaign wants to carry.

## What self-hosted means

With self-hosted campaign software, the campaign controls the server or hosting account where the application runs.

That usually means the campaign or its technical provider is responsible for:

- domain and DNS;
- HTTPS/SSL;
- server and database configuration;
- backups;
- software updates;
- monitoring;
- storage;
- email/SMS integration where applicable;
- access control and incident response.

Campaign Manager Community / Self-Hosted follows this model. The application can be downloaded and operated independently without a software licence fee.

## What SaaS means

With a cloud SaaS platform, the vendor normally operates the application infrastructure and gives campaign users accounts on the vendor's hosted system.

The campaign typically avoids most server administration, but it also depends more heavily on the provider's hosting model, data policies, product roadmap, service availability and commercial terms.

## Data control

Self-hosting gives the campaign more direct control over where its database and uploaded files live. This can be valuable when the organisation has specific data-governance or infrastructure requirements.

That control also creates responsibility. A badly secured self-hosted server can be riskier than a well-run SaaS platform. Self-hosting is not a security shortcut; it is an operational choice.

## Customisation and integration

Self-hosted software can be attractive when a campaign needs its own domain, branding, infrastructure policy or agreed custom integration.

SaaS products may offer configuration and APIs, but deeper changes depend on what the provider permits.

Campaign Manager supports campaign colours, logos and visible identity, with optional custom development/integration services available separately.

## Cost structure

SaaS platforms often charge subscriptions based on users, contacts, usage, modules or election cycles.

Self-hosted software shifts more of the cost toward infrastructure and technical operations. Even when the software itself is free, the campaign still pays for hosting, domains, backups, email/SMS usage and technical labour where required.

Campaign Manager Community / Self-Hosted is free to download and use. Optional paid services include QuickStart Geography Provisioning, Professional Installation, Priority Support, Managed Deployment and Campaign SMS.

## Technical capability

A campaign with a capable technical team may prefer self-hosting because it can manage its own environment.

A campaign without that capability may prefer SaaS or may use the same self-hosted application with professional management.

Campaign Manager's **Managed Deployment** is designed for that second case: the campaign uses Campaign Manager, while Govware Solutions handles agreed infrastructure, deployment, maintenance, monitoring and support.

Managed Deployment is a service model around the same application, not a separate software edition.

## Updates and maintenance

SaaS users usually receive updates automatically because the vendor controls the platform.

Self-hosted teams decide when to update and should review release notes, take backups and test changes before production deployment.

See Campaign Manager's [Upgrading Guide](../upgrading.md).

## Availability and resilience

Whichever model is used, campaigns should plan for:

- backups;
- server failure;
- internet connectivity;
- account recovery;
- monitoring;
- election-day traffic;
- operational support.

Election-day systems deserve more preparation than ordinary campaign websites because failure can occur at the exact moment the organisation most needs them.

## A simple decision framework

Choose self-hosting when your campaign values direct infrastructure control and has the technical capacity to operate it safely.

Choose SaaS when reducing infrastructure responsibility is more important than direct control.

Choose professionally managed self-hosting when you want the control and branding of a dedicated deployment but do not want your internal team to handle every technical task.

For Campaign Manager deployment options, see the [Installation Guide](../installation.md), [VPS Guide](../vps-installation.md), [cPanel Guide](../cpanel-installation.md) and [Support Guide](../../SUPPORT.md), or visit [campaignmanager.ng](https://www.campaignmanager.ng).
