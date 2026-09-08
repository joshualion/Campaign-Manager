# Campaign SMS

Campaign Manager supports an optional managed SMS service for deployments that need campaign messaging through the platform.

## Community use does not require SMS

Campaign Manager Community / Self-Hosted can be downloaded, installed and operated without purchasing SMS.

SMS is a separate optional service. Activation, availability and credits are handled independently from the free application download.

## Managed SMS model

Where Campaign SMS is available:

- SMS activation/credits are purchased separately;
- Community users do not need to expose upstream provider credentials through the public distribution repository;
- usage is subject to available credits and the configured messaging service;
- pricing/availability can change, so use the Campaign Manager Portal for current information.

## Before relying on SMS

Verify:

- the SMS service is activated for your deployment;
- adequate credits are available;
- sender/recipient formatting is correct for your target network/country;
- the application can reach the required service endpoint;
- any queue worker required by your selected messaging workflow is running;
- test messages are delivered before a major campaign broadcast.

## Protect campaign data

Phone numbers and message content can be sensitive campaign data.

Do not publish:

- supporter/member phone lists;
- SMS credentials/tokens;
- private campaign messaging;
- delivery logs containing personal information

in GitHub Issues or other public support channels.

## Need help?

For current Campaign SMS availability or paid technical support, use the official Campaign Manager website:

[www.campaignmanager.ng](https://www.campaignmanager.ng)
