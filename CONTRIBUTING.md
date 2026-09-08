# Contributing to Campaign Manager

Thank you for helping improve Campaign Manager.

This public repository is primarily used for **Campaign Manager Community documentation and official release distribution**. The private Campaign Manager application core is not published here, so public contributions should focus on areas that can be reviewed safely in this repository.

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

## Before opening a pull request

1. Search existing issues and pull requests to avoid duplicates.
2. Keep the change focused.
3. Verify every command/link you add.
4. Do not invent product functionality.
5. Do not describe Campaign Manager as open source unless a formal licence has been published.
6. Keep Community/Self-Hosted wording accurate: the software is free to download/use and does not require a software licence key.
7. Describe QuickStart as optional geography provisioning, not software activation/licensing.

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
- private application source code

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

For the current documentation layout, use the reserved screenshot directory:

```text
docs/images/screenshots/
```

Preferred master format is 1600×900 (16:9), with WebP preferred where text remains sharp and readable.

## Pull request checklist

A good PR should explain:

- what was changed;
- why it improves the public repository/documentation;
- how the change was checked;
- whether screenshots are included;
- whether any links/commands require manual verification.

The repository pull request template will guide you through this.

## Application bugs

If a problem is reproducible in the distributed Campaign Manager application, open a Bug Report issue using sanitised details. Do not upload application source code, credentials or campaign data.

Security vulnerabilities should **not** be posted publicly. Follow [SECURITY.md](SECURITY.md).

## Licence

Contributing documentation does not change the application licence. See [docs/licensing.md](docs/licensing.md) for the current licence status.
