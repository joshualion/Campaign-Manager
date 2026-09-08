# Contributing to Campaign Manager

Thank you for helping improve Campaign Manager.

This repository is the public home for **Campaign Manager Community documentation and official release distribution**. The `campaign-manager.zip` published in GitHub Releases is the Campaign Manager application distributed to self-hosted users. Managed Deployment and other paid offerings use the same Campaign Manager product; they are service options for teams that want setup, infrastructure management, support or customisation rather than a separate software edition.

The main application source is not maintained here as an editable public source tree, so code changes to the application itself cannot be accepted directly through normal repository pull requests at this time. Product ideas, reproducible bug reports, documentation improvements and deployment knowledge are still very welcome.

## Useful contributions

We welcome improvements such as:

- documentation corrections
- installation guides
- cPanel/shared-hosting guidance
- VPS/server deployment knowledge
- troubleshooting improvements
- translations
- tutorials
- verified screenshots with sensitive data removed
- typo/grammar fixes
- clearer examples
- issue templates/community documentation
- feature ideas and workflow suggestions
- reproducible bug reports against the distributed application

## Before opening a pull request

1. Search existing issues and pull requests to avoid duplicates.
2. Keep the change focused.
3. Verify every command/link you add.
4. Do not invent product functionality.
5. Do not describe Campaign Manager as open source unless a formal licence has been published.
6. Keep Community/Self-Hosted wording accurate: the software is free to download/use and does not require a software licence key.
7. Describe QuickStart as optional automatic geography setup, not software activation/licensing.

## Never include sensitive information

Do not commit or paste:

- `.env` files
- passwords
- API tokens/keys
- database credentials
- server credentials
- QuickStart Provisioning Keys
- supporter/member records
- voter/campaign personal data
- internal political strategy or private campaign information
- production database dumps

Use sanitised examples only.

## Documentation style

Prefer:

- direct instructions
- short sections and meaningful headings
- commands that are safe to copy
- relative links inside repository docs
- clear distinction between required and optional steps
- warnings before destructive commands

Avoid:

- keyword stuffing
- fake social proof
- unverified performance/security claims
- insecure defaults such as recommending `chmod 777`
- instructions that expose the application root instead of Laravel's `/public` directory

## Screenshots

Screenshots must come from a verified Campaign Manager environment and must be reviewed for sensitive information before publication.

For the current documentation layout, use:

```text
docs/images/screenshots/
```

Prefer clear captures with meaningful demo data. Do not publish empty or misleading product screens simply to fill a screenshot slot.

## Pull request checklist

A good PR should explain:

- what was changed;
- why it improves the public repository/documentation;
- how the change was checked;
- whether screenshots are included;
- whether any links/commands require manual verification.

The repository pull request template will guide you through this.

## Application bugs and feature ideas

If a problem is reproducible in the distributed Campaign Manager application, open a Bug Report issue using sanitised details. If you have a product idea, open a Feature Suggestion. The maintainers will assess application-level changes against the maintained Campaign Manager codebase.

Security vulnerabilities should **not** be posted publicly. Follow [SECURITY.md](SECURITY.md).

## Licence

Contributing documentation does not change the application licence. See [docs/licensing.md](docs/licensing.md) for the current licence status.
