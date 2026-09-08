# Polling Unit Agent Workflow

Campaign Manager includes a structured Polling Unit Agent lifecycle for campaign field operations.

The functionality described here was verified in the live Super Admin demo.

## Entry paths

Polling Unit Agents can enter the workflow through:

- **Self Request**
- **Leader Nomination**
- **Admin Appointment**
- **Super Admin Assignment**

The application exposes dedicated surfaces for **Agent Request**, **My Agent Status**, **Polling Unit Agents**, **Nominate Agent** and **Direct Agent Assignment**.

## Request and status tracking

The Polling Unit Agent request register supports filtering by status, source and identity status.

Verified workflow fields include:

- User
- Polling Unit
- Source
- Status
- Identity
- Stage
- Action

Visible statuses include:

- Pending
- Approved
- Rejected
- Suspended
- Revoked

## Identity and readiness

The onboarding workflow can collect identity-document type/number, identity document, voter evidence or voter card, passport photo, current address and a willingness statement.

These are sensitive fields. Do not publish screenshots or GitHub issues containing real identity documents, contact details or voter information.

## Campaign deployment override

An authorised administrator can use the person's registered Polling Unit or assign another Polling Unit through the application's **campaign deployment override** workflow.

This allows operational deployment to differ from a user's normal voting geography where campaign leadership has authorised the assignment.

## Privacy guidance

For public documentation, prefer aggregate or empty-state agent screens. Do not publish Agent Request, Nominate Agent or Direct Agent Assignment screenshots containing names, emails, phone numbers, addresses, identity uploads or private geography information.
