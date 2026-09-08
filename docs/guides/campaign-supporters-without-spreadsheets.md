# How to Manage Campaign Supporters and Volunteers Without Spreadsheets

Spreadsheets are useful when a campaign is small. They become fragile when the organisation starts tracking thousands of supporters, volunteers, coordinators and field operatives across many locations.

The problem is not that spreadsheets are bad. The problem is that they are not designed to be the operating system of a political campaign.

## Where spreadsheets begin to break down

Common warning signs include:

- multiple copies of the same file circulating in WhatsApp groups;
- duplicate supporters with slightly different names or phone numbers;
- unclear ownership of data entry;
- no reliable way to restrict who can see sensitive records;
- geography stored as inconsistent free text;
- separate sheets for volunteers, agents and coordinators that do not agree;
- difficulty answering simple questions by Ward, LGA or Polling Unit;
- accidental deletion or overwriting of records;
- no dependable audit trail of operational status changes.

A spreadsheet can still be useful for exports and one-off analysis, but it should not have to carry every campaign workflow.

## Build one structured supporter record

A better approach is to maintain a structured record for each supporter or member, then connect that record to the campaign's geography and operational roles.

This lets the campaign distinguish between:

- a supporter;
- a volunteer;
- a coordinator;
- a Polling Unit Agent candidate;
- an approved field operative.

One person may have more than one relationship to the campaign, but those relationships should be explicit rather than inferred from whichever spreadsheet tab contains the person's name.

## Use geography consistently

Campaign supporter data becomes far more useful when every record is connected to standard geography.

For a Nigerian campaign, that may mean State, LGA, Ward and Polling Unit, depending on the campaign scope. Once geography is structured, campaign leadership can compare coverage across areas instead of manually cleaning location names every time a report is needed.

Campaign Manager documents its geography model in [Geography Setup](../geography-setup.md).

## Separate mobilisation from administration

Not every volunteer should have administrative access. A campaign system should support different responsibilities so local organisers can work within the areas they manage without automatically gaining access to the full national or state database.

Role-based access reduces accidental exposure and makes it easier to delegate work. See [Roles and Permissions](../roles-and-permissions.md).

## Track operational status explicitly

For field roles, a simple "yes/no" column is often not enough. Campaigns may need to know whether someone has been requested, nominated, reviewed, approved, rejected, suspended or revoked.

Structured statuses make it possible to see bottlenecks and incomplete onboarding. Campaign Manager's [Polling Unit Agent Workflow](../polling-unit-agent-workflow.md) is one example of this approach.

## Measure coverage

A structured campaign database should answer questions such as:

- How many members are in each Region or State?
- Which LGAs have the weakest supporter coverage?
- Which Wards need more volunteers?
- Which Polling Units have no approved agents?
- How many supporters are election-ready according to the campaign's chosen indicators?

The point is not to collect data for its own sake. The point is to turn data into operational decisions.

## Keep data quality rules simple

A campaign does not need a complicated data-governance manual to improve quality. Start with a few rules:

1. use one authoritative system for active supporter records;
2. standardise geography rather than storing location names freely;
3. define who is allowed to create and update records;
4. avoid storing unnecessary sensitive information;
5. back up the database regularly;
6. document how duplicates are handled;
7. treat exports as copies, not the source of truth.

## Protect political data

Supporter lists can reveal political preference and organisational relationships. They should be treated as sensitive operational data.

Use HTTPS, strong authentication, least-privilege access, secure backups and careful export handling. Do not post real supporter information in public GitHub issues or screenshots.

## Where Campaign Manager fits

Campaign Manager is a self-hosted political campaign management platform designed to connect supporter/member records with political structure, electoral geography, roles, field operations and election monitoring.

It does not eliminate every spreadsheet. It reduces the need to use spreadsheets as the campaign's primary operating system.

See the [Product Overview](../product-overview.md), [Installation Guide](../installation.md), or visit [campaignmanager.ng](https://www.campaignmanager.ng).
