# How to Build an Election Situation Room for Results and Incident Monitoring

An election Situation Room is a campaign's operational command centre for tracking what is happening across many Polling Units at the same time.

The useful question is not "Do we have a dashboard?" It is: **Can campaign leadership quickly identify missing reports, disputed results, incidents and silent locations that need attention?**

## Define what the Situation Room must answer

Before choosing charts or screens, define the operational questions:

- How many Polling Units are expected to report?
- How many have submitted?
- Which Polling Units are still pending?
- Which submissions have been verified?
- Which are disputed?
- Which Polling Units are active or silent?
- How many incidents have been reported?
- Which incidents include evidence?
- Which States or areas have low coverage?

Campaign Manager's verified [Election Situation Room](../election-situation-room.md) is organised around these types of indicators.

## Establish a clear reporting chain

A Situation Room is only as useful as the information reaching it. Campaign leadership should define:

1. who reports from each Polling Unit;
2. what information must be submitted;
3. which users can verify or dispute reports;
4. how incidents are escalated;
5. who reviews evidence;
6. how unresolved gaps are assigned for follow-up.

Polling Unit Agents and field teams should know this chain before election day.

## Separate result status from incident status

A Polling Unit can have a result submission and also have an incident. Treat these as related but distinct workflows.

For result monitoring, useful statuses may include submitted, pending, verified and disputed.

For incidents, the Situation Room should capture whether a report exists, whether evidence is attached and whether follow-up is required.

Combining everything into one generic "message" stream makes it difficult to see the real operational picture.

## Make coverage visible

Coverage is one of the most important metrics in election monitoring.

If 70% of Polling Units have submitted, leadership needs to know **which 30% have not**. Aggregate percentages are useful, but they should lead to geography-level detail.

Campaign Manager's verified interface includes Submission Coverage and Coverage by State, helping teams identify gaps rather than only displaying national totals.

## Highlight silent Polling Units

A silent Polling Unit may simply be delayed, or it may indicate a communication, staffing or operational problem. Either way, it deserves attention.

A good Situation Room should make silence visible instead of treating the absence of data as nothing.

Campaign Manager includes active/silent Polling Unit monitoring in the verified Situation Room workflow.

## Track disputes explicitly

When a result is disputed, it should not disappear into chat history. The campaign needs a clear status that distinguishes disputed reports from verified ones.

The workflow should allow authorised reviewers to see disputed submissions and decide what follow-up is necessary according to the campaign's legal and operational process.

## Require evidence where appropriate

Incident reports are more actionable when evidence can be attached and reviewed. The Situation Room should make it obvious which incidents have supporting evidence and which do not.

Campaign Manager's verified interface includes Incident Evidence indicators and counts for incidents with and without evidence.

## Use an activity timeline

An operational activity timeline helps leadership understand what is happening now, not only the final totals. It can surface new result submissions, incident reports and other significant activity in sequence.

This is especially useful during periods when many locations are reporting at once.

## Protect access and sensitive information

Election-day data can be politically sensitive. Situation Room access should follow least privilege. Not every campaign member needs access to every result, incident, evidence file or administrative action.

Use secure authentication, HTTPS, role-based permissions and careful handling of screenshots and exports. Never publish real incident evidence or identifiable campaign data in public repositories without a deliberate privacy review.

## Rehearse before election day

A Situation Room should be tested with demo data before the election. Rehearsal can reveal:

- missing Polling Unit assignments;
- users who cannot access the right screens;
- unclear verification responsibilities;
- slow escalation paths;
- reporting fields that are misunderstood;
- dashboards that appear useful but do not answer operational questions.

## Where Campaign Manager fits

Campaign Manager combines electoral geography, Polling Unit Agent operations, result-submission monitoring, verification/dispute states, incident evidence and geographic coverage in one self-hosted campaign platform.

See the [Polling Unit Agent Workflow](../polling-unit-agent-workflow.md), [Election Situation Room](../election-situation-room.md), and [Product Overview](../product-overview.md), or visit [campaignmanager.ng](https://www.campaignmanager.ng).
