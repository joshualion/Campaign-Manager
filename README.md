<img align="right" src="docs/images/logo.png" alt="Campaign Manager Logo" width="56">

# Campaign Manager

**Free Self-Hosted Political Campaign & Election Management Software**

Campaign Manager is a Laravel-based platform for campaign organisations that need one structured system for supporters, members, volunteers, political structures, campaign teams, electoral geography, polling units, field operations, agents, mobilisation, internal communication, dashboards and election-day monitoring.

<p>
  <a href="https://github.com/joshualion/Campaign-Manager/releases/latest"><img src="https://img.shields.io/github/v/release/joshualion/Campaign-Manager?label=Latest%20Release&style=for-the-badge&color=008F5A" alt="Latest Release"></a>
  <a href="https://github.com/joshualion/Campaign-Manager/releases"><img src="https://img.shields.io/github/downloads/joshualion/Campaign-Manager/total?label=Total%20Downloads&style=for-the-badge&color=0A7F55" alt="Total Downloads"></a>
  <img src="https://img.shields.io/badge/Public%20Since-4%20Sep%202026-006B45?style=for-the-badge" alt="Public Since">
  <img src="https://img.shields.io/badge/Release%20Channel-Stable-008F5A?style=for-the-badge" alt="Release Channel">
</p>

<p>
  <a href="https://github.com/joshualion/Campaign-Manager/releases/latest"><img src="https://img.shields.io/github/release-date/joshualion/Campaign-Manager?display_date=published_at&label=Latest%20Update&style=for-the-badge&color=008F5A" alt="Latest Update"></a>
  <a href="https://github.com/joshualion/Campaign-Manager/releases/latest/download/campaign-manager.zip"><img src="https://img.shields.io/badge/Download-Free%20Download-008F5A?style=for-the-badge" alt="Free Download"></a>
  <a href="https://www.campaignmanager.ng"><img src="https://img.shields.io/badge/Official%20Website-Visit-006B45?style=for-the-badge" alt="Official Website"></a>
  <a href="https://www.campaignmanager.ng/order/campaign-manager?deployment=managed"><img src="https://img.shields.io/badge/Managed-Deployment-0A7F55?style=for-the-badge" alt="Managed Deployment"></a>
</p>

**[Download Latest Release](https://github.com/joshualion/Campaign-Manager/releases/latest)** · **[Installation Guide](docs/installation.md)** · **[Documentation](docs/README.md)** · **[Official Website](https://www.campaignmanager.ng)** · **[Professional Installation](https://www.campaignmanager.ng)** · **[Managed Deployment](https://www.campaignmanager.ng/order/campaign-manager?deployment=managed)**

<br clear="right">

---

![Campaign Manager](docs/images/banner.jpg)

## What Campaign Manager does

Political campaigns often coordinate supporters, volunteers, ward/LGA structures, polling units, agents and election-day activity across disconnected spreadsheets, WhatsApp groups and paper records. Campaign Manager brings those operations into one structured campaign management system that can be hosted on infrastructure controlled by the campaign.

Built around Nigerian electoral geography and campaign operations, Campaign Manager is relevant to political-tech and civic-tech teams evaluating self-hosted campaign management software, political campaign CRM workflows, supporter management, polling-unit operations and election monitoring.

The **Community / Self-Hosted Edition is free to download and use**. It does **not** require a software licence key or remote software activation. Your team can configure campaign geography manually for free and operate the deployment independently.

Optional Govware services are available for teams that want convenience, speed or professional technical support: **QuickStart Geography Provisioning, Professional Installation, Migration/Upgrade Assistance, Priority Support, Custom Development/Integration, Managed Deployment and Campaign SMS**.

## Why Campaign Manager?

Campaign operations become difficult to control when organisational structure, supporter data, electoral geography, field teams and election reporting live in separate tools. Campaign Manager is designed to give political organisations a common operating platform from campaign setup through field coordination and election-day reporting.

## Feature overview

Campaign Manager includes tools for:

- campaign dashboards and operational visibility
- political structure and campaign-team coordination
- supporter and member management
- volunteer and field-team organisation
- campaign geography management
- polling-unit and agent management
- notices, announcements and internal communication
- election monitoring and field reporting workflows
- election reporting/results workflows
- role-based access and campaign-level permissions
- campaign scope configuration
- free manual geography configuration
- optional QuickStart Geography Provisioning
- optional Campaign SMS integration

Descriptions here are intentionally conservative. A verified live-demo feature inventory and updated product screenshots will be incorporated in Phase 2.

## See Campaign Manager in Action

Verified screenshots from the live Campaign Manager demo are being prepared. Generic stock images and fabricated product screens are intentionally not used.

Phase 2 screenshot slots are reserved for:

1. **Dashboard** — campaign overview and operational visibility
2. **Political Structure** — campaign hierarchy and structure management
3. **Supporter / Member Management** — people and organisation records
4. **Electoral Geography** — state/LGA/ward/polling-unit structure
5. **Field / Agent Operations** — field-team and polling-unit operations
6. **Election Monitoring / Results** — election-day reporting and results workflows

<!--
PHASE 2 SCREENSHOT INSERTION PLAN
1. docs/images/screenshots/dashboard-overview.webp
2. docs/images/screenshots/political-structure.webp
3. docs/images/screenshots/supporter-member-management.webp
4. docs/images/screenshots/electoral-geography.webp
5. docs/images/screenshots/field-agent-operations.webp
6. docs/images/screenshots/election-monitoring-results.webp
Recommended master size: 1600x900 (16:9), WebP preferred; keep text readable at GitHub README width.
Optional later assets: communications.webp, reports-analytics.webp, roles-access.webp, campaign-configuration.webp.
-->

## Supported campaign scopes

Campaign Manager can be configured for:

- **Presidential / National**
- **Governorship / State**
- **Senatorial**
- **Federal Constituency**
- **Local Government / Chairmanship**

The installer adjusts the relevant geography selection to the campaign scope. See **[Campaign Scopes](docs/campaign-scopes.md)** for the high-level model.

## Free self-hosted model

Community / Self-Hosted Campaign Manager is distributed through official GitHub Releases as:

```text
campaign-manager.zip
```

The release package contains the production dependencies and compiled assets needed for deployment.

**Community use does not require a software licence key.** Your technical team supplies and manages its own server, database, domain, SSL, storage and operational environment.

## Quick installation

1. **[Download the latest stable release](https://github.com/joshualion/Campaign-Manager/releases/latest)**.
2. Upload and extract `campaign-manager.zip` on your server.
3. Point the website document root to the application's `/public` directory.
4. Create the application database and database user.
5. Create/configure `.env` from `.env.example` where required by your deployment workflow.
6. Ensure `storage/` and `bootstrap/cache/` are writable by the web-server user.
7. Open `https://your-domain.com/install` and follow the installer.
8. Verify login, campaign scope, storage/media, mail and any enabled background services after installation.

For proper deployment guidance, use the full **[Installation Guide](docs/installation.md)** rather than relying only on this summary.

## Documentation

- [Documentation index](docs/README.md)
- [Installation guide](docs/installation.md)
- [cPanel / shared-hosting installation](docs/cpanel-installation.md)
- [VPS / Linux installation](docs/vps-installation.md)
- [Upgrading](docs/upgrading.md)
- [Troubleshooting](docs/troubleshooting.md)
- [Campaign scopes](docs/campaign-scopes.md)
- [Geography setup](docs/geography-setup.md)
- [QuickStart Geography Provisioning](docs/quickstart.md)
- [Campaign SMS](docs/sms.md)
- [FAQ](docs/faq.md)

## Geography setup

### Manual Geography Configuration — Free

You can create and manage the geography required for your campaign scope yourself without purchasing an additional geography service. See **[Geography Setup](docs/geography-setup.md)**.

### QuickStart Geography Provisioning — Optional

QuickStart is an optional paid convenience service that provisions supported electoral geography for the campaign scope/geography purchased through the Campaign Manager Portal.

A **QuickStart Geography Provisioning Key authorises geography provisioning only**. It is **not a software licence key** and Community Campaign Manager does not require it to run. See **[QuickStart](docs/quickstart.md)**.

## Optional professional services

You can self-host and operate Campaign Manager independently for free. If you prefer professional assistance, Govware Solutions can provide:

- **QuickStart Geography Provisioning** — prepared geography provisioning for the purchased scope
- **Professional Installation** — one-time deployment and configuration on customer infrastructure
- **Migration / Upgrade Assistance** — technical help moving or upgrading an installation
- **Priority Technical Support** — paid support beyond self-service documentation
- **Custom Development / Integration** — agreed project-specific work
- **Managed Deployment** — Govware-operated infrastructure, monitoring, maintenance and technical support for an agreed campaign cycle
- **Campaign SMS** — optional managed messaging activation/credits where available

**[Visit Campaign Manager](https://www.campaignmanager.ng)** for current service information.

## Updates

New application versions are published through **[GitHub Releases](https://github.com/joshualion/Campaign-Manager/releases)**. Review release notes before upgrading and keep verified backups of your database, `.env` configuration and user-uploaded files.

## Community and contributions

This public repository is primarily the Community documentation and official release-distribution home for Campaign Manager. Useful public contributions are welcome for documentation, installation guidance, hosting knowledge, translations, tutorials, screenshots and typo corrections.

See **[CONTRIBUTING.md](CONTRIBUTING.md)** before opening a pull request. Please use GitHub Issues for reproducible installation, documentation and repository problems; do not publish credentials, QuickStart keys or campaign data.

## Security

Please do **not** report vulnerabilities containing passwords, API tokens, server credentials, database passwords, QuickStart keys, campaign personal data or political records in a public issue.

Read **[SECURITY.md](SECURITY.md)** for the responsible private reporting route.

## Licence status

Campaign Manager Community Edition is free to download and use. However, **free-to-use does not by itself grant open-source redistribution or modification rights**.

A final public redistribution/source licence has not yet been declared in this repository. Until a formal licence is published, do not assume MIT, GPL, Apache or other open-source rights. See the **[licence status and decision note](docs/licensing.md)** before redistributing or modifying the application package.

---

<div align="center">

## ❤️ Support Campaign Manager Development

Campaign Manager is free to download and use. If it is useful to you or your organisation, voluntary support can help continued development, maintenance, testing, security improvements and documentation.

<p>
  <a href="https://www.campaignmanager.ng/support-development?amount=20"><img src="https://img.shields.io/badge/Support-%2420-008F5A?style=for-the-badge&logo=githubsponsors&logoColor=white" alt="Support $20"></a>
  <a href="https://www.campaignmanager.ng/support-development?amount=50"><img src="https://img.shields.io/badge/Support-%2450-0A7F55?style=for-the-badge&logo=githubsponsors&logoColor=white" alt="Support $50"></a>
  <a href="https://www.campaignmanager.ng/support-development?amount=100"><img src="https://img.shields.io/badge/Support-%24100-006B45?style=for-the-badge&logo=githubsponsors&logoColor=white" alt="Support $100"></a>
  <a href="https://www.campaignmanager.ng/support-development?amount=500"><img src="https://img.shields.io/badge/Support-%24500-008F5A?style=for-the-badge&logo=githubsponsors&logoColor=white" alt="Support $500"></a>
  <a href="https://www.campaignmanager.ng/support-development?amount=custom"><img src="https://img.shields.io/badge/Support-Custom-0A7F55?style=for-the-badge&logo=githubsponsors&logoColor=white" alt="Custom Support"></a>
</p>

<sub>Support is voluntary and does not purchase a software licence, campaign service, political influence or preferential treatment.</sub>

</div>

---

<div align="center">

**Campaign Manager**  
Political Campaign Technology  
[www.campaignmanager.ng](https://www.campaignmanager.ng)

</div>
