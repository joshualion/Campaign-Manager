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
  <a href="docs/installation.md"><img src="https://img.shields.io/badge/Installation-Guide-0A7F55?style=for-the-badge&logo=readthedocs&logoColor=white" alt="Installation Guide"></a>
  <a href="https://www.campaignmanager.ng"><img src="https://img.shields.io/badge/Official%20Website-Visit-006B45?style=for-the-badge" alt="Official Website"></a>
  <a href="https://www.campaignmanager.ng/order/campaign-manager?deployment=managed"><img src="https://img.shields.io/badge/Managed-Deployment-0A7F55?style=for-the-badge" alt="Managed Deployment"></a>
</p>

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

A live Super Admin product audit verified Campaign Manager capabilities including:

- **National campaign dashboards** combining political/geographic coverage, member readiness and election-operation metrics
- **Political structure drill-downs** from national operations into Regions and lower campaign geography
- **Member coverage views** by Region, State, LGA, Ward and Polling Unit
- **Voter-readiness indicators** including Eligible Voters and members Without Voter Card
- **Polling Unit Agent workflows** for Self Request, Leader Nomination, Admin Appointment and Super Admin Assignment
- **Agent status and identity stages** covering Pending, Approved, Rejected, Suspended and Revoked workflows
- **Campaign deployment override** for authorised agent deployment outside a person's registered Polling Unit
- **Election Situation Room** monitoring for result submissions, verified/disputed results, active/silent Polling Units and incidents/evidence
- **Election analytics** including Submission Coverage, Incident Evidence, Coverage by State and an Operational Activity Timeline
- **Internal Communication, Email Notifications and Announcements / Notice Board** workflows
- **Campaign-specific roles and permissions** spanning national through polling-unit responsibilities
- **Campaign branding** using campaign colours, logos and visible campaign identity
- campaign scope configuration and geography management
- free manual geography configuration
- optional QuickStart Geography Provisioning
- optional Campaign SMS integration

See the **[verified Product Overview](docs/product-overview.md)** for a fuller summary, plus dedicated guides for the **[Polling Unit Agent Workflow](docs/polling-unit-agent-workflow.md)**, **[Election Situation Room](docs/election-situation-room.md)** and **[Roles & Permissions](docs/roles-and-permissions.md)**.

## See Campaign Manager in Action

The screenshots below are verified Campaign Manager screens with meaningful demo data. Empty or privacy-sensitive screens are intentionally excluded.

### National Campaign Dashboard

![Campaign Manager National Dashboard](docs/images/screenshots/dashboard-overview.jpg)

Campaign leadership can see geographic coverage, regular members, coordinators/admins, Polling Unit Agents and voter-readiness indicators from one central dashboard.

### Member Coverage by Region

![Campaign Manager Members by Region](docs/images/screenshots/member-coverage-regions.jpg)

Member coverage can be reviewed across Nigeria's six geopolitical Regions, with direct drill-down into each Region dashboard.

### State Campaign Dashboard

![Campaign Manager State Dashboard](docs/images/screenshots/state-dashboard.jpg)

State-level dashboards show the campaign's coverage across Senatorial Districts, Federal Constituencies, LGAs, Wards and Polling Units alongside membership and voter-readiness metrics.

Additional screenshots for the Election Situation Room, Polling Unit Agent workflows and other operations will be added when the demo data is sufficiently meaningful and privacy-safe.

The current national dataset displayed by Campaign Manager contains **6 Regions, 37 States, 109 Senatorial Districts, 360 Federal Constituencies, 774 LGAs, 8,809 Wards and 176,846 Polling Units**. These are Campaign Manager dataset totals rather than an independent electoral-data certification.

## Supported campaign scopes

Campaign Manager can be configured for:

- **Presidential / National**
- **Governorship / State**
- **Senatorial**
- **Federal Constituency**
- **Local Government / Chairmanship**

The live product uses the package terminology **Presidential Campaign, Governorship Campaign, Senatorial District Campaign, Federal Constituency Campaign and Chairmanship Campaign**. The installer adjusts the relevant geography selection to the campaign scope. See **[Campaign Scopes](docs/campaign-scopes.md)** for the high-level model.

## Campaign branding

Campaign Manager can be adapted to the campaign's visual identity, including campaign colours, logos and visible branding. A self-hosted or managed deployment can therefore present the campaign organisation's own identity rather than a generic shared portal.

## Free self-hosted model

Community / Self-Hosted Campaign Manager is distributed through official GitHub Releases as:

```text
campaign-manager.zip
```

The release package contains the production dependencies and compiled assets needed for deployment.

**Community use does not require a software licence key.** Your technical team supplies and manages its own server, database, domain, SSL, storage and operational environment.

The application published here is the Campaign Manager product used for self-hosted deployments. **Managed Deployment is a service model, not a separate hidden software edition.** It is for campaign teams that want Govware Solutions to handle infrastructure, installation, maintenance, monitoring and technical support around the same Campaign Manager application.

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
- [Product overview](docs/product-overview.md)
- [Installation guide](docs/installation.md)
- [cPanel / shared-hosting installation](docs/cpanel-installation.md)
- [VPS / Linux installation](docs/vps-installation.md)
- [Upgrading](docs/upgrading.md)
- [Troubleshooting](docs/troubleshooting.md)
- [Campaign scopes](docs/campaign-scopes.md)
- [Geography setup](docs/geography-setup.md)
- [Polling Unit Agent workflow](docs/polling-unit-agent-workflow.md)
- [Election Situation Room](docs/election-situation-room.md)
- [Roles & permissions](docs/roles-and-permissions.md)
- [QuickStart Geography Provisioning](docs/quickstart.md)
- [Campaign SMS](docs/sms.md)
- [FAQ](docs/faq.md)

## Geography setup

### Manual Geography Configuration — Free

Campaign Manager can be configured manually at no additional software cost. The installer prepares the core campaign boundary, then your team adds the remaining electoral structure needed for that scope.

For example, a Governorship installation prepares the selected State and your team can then add the required Senatorial Districts, Federal Constituencies, LGAs, Wards and Polling Units. A Presidential installation prepares the national context and Regions, while the remaining State and lower geography can be added manually.

See **[Geography Setup](docs/geography-setup.md)** for the full explanation.

### QuickStart Geography Provisioning — Optional automatic setup

QuickStart is the faster alternative. Instead of manually creating the required electoral boundaries one by one, it automatically provisions the supported **Regions, States, Senatorial Districts, Federal Constituencies, LGAs, Wards and Polling Units** relevant to the campaign scope purchased.

A **QuickStart Geography Provisioning Key authorises that automatic geography setup only**. It is **not a software licence key** and Community Campaign Manager does not require it to run.

See **[QuickStart](docs/quickstart.md)**.

## Optional professional services

You can self-host and operate Campaign Manager independently for free. If your campaign team wants assistance, Govware Solutions can provide only the services you need:

- **QuickStart Geography Provisioning** — automatic setup of the supported electoral geography for the purchased campaign scope
- **Professional Installation** — one-time deployment and configuration on customer infrastructure
- **Migration / Upgrade Assistance** — technical help moving or upgrading an installation
- **Priority Technical Support** — paid support beyond self-service documentation
- **Custom Development / Integration** — agreed project-specific work
- **Managed Deployment** — full technical operation of infrastructure, monitoring, maintenance and support for an agreed campaign cycle
- **Campaign SMS** — optional managed messaging activation/credits where available

**[Visit Campaign Manager](https://www.campaignmanager.ng)** for current service information.

## Updates

New application versions are published through **[GitHub Releases](https://github.com/joshualion/Campaign-Manager/releases)**. Review release notes before upgrading and keep verified backups of your database, `.env` configuration and user-uploaded files.

## Community and contributions

This repository is the public documentation and official release-distribution home for Campaign Manager. Useful public contributions are welcome for documentation, installation guidance, hosting knowledge, translations, tutorials, screenshots, typo corrections, feature ideas and reproducible bug reports.

The application source itself is not maintained here as an editable public source tree, so application-level code changes are assessed by the maintainers rather than accepted as direct source-code pull requests from this repository.

See **[CONTRIBUTING.md](CONTRIBUTING.md)** before opening a pull request. Please do not publish credentials, QuickStart keys or campaign data.

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
