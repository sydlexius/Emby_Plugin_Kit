# Security Policy

## Supported Versions

| Version | Supported |
| ------- | --------- |
| latest  | Yes       |

This project is pre-release and does not yet contain shipping code.

## Reporting a Vulnerability

**Please do not report security vulnerabilities through public GitHub issues.**

Use [GitHub Security Advisories](https://github.com/sydlexius/Emby_Plugin_Kit/security/advisories/new)
to report vulnerabilities privately. This ensures the issue can be triaged and a
fix prepared before public disclosure.

When reporting, please include:

- A description of the vulnerability and its potential impact
- Steps to reproduce or a proof-of-concept
- The affected version(s) or commit(s)
- A suggested fix, if you have one

You should receive an initial acknowledgment within 72 hours. Critical issues
will be addressed as quickly as practical.

## Scope

In scope:

- The workflows in `.github/workflows/`
- Any code added to this repository in future

Out of scope:

- Vulnerabilities in Emby itself (report those to Emby)
- Vulnerabilities in upstream dependencies (report those upstream)

## Security Measures

- **Pinned actions:** all GitHub Actions are pinned to a commit SHA
- **Least-privilege tokens:** workflow permissions are declared at job level
- **No persisted credentials:** checkouts use `persist-credentials: false`
- **Secret scanning** with push protection is enabled
