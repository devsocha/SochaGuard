# Security Policy

<p align="center"><b>English</b> · <a href="translations/pl/SECURITY.md">Polski</a> · <a href="translations/de/SECURITY.md">Deutsch</a> · <a href="translations/es/SECURITY.md">Español</a> · <a href="translations/it/SECURITY.md">Italiano</a> · <a href="translations/uk/SECURITY.md">Українська</a></p>

## Reporting a vulnerability

Please report vulnerabilities **privately**:

- Use GitHub's **"Report a vulnerability"** (Security → Advisories) on this repository.

Please do not open public issues or pull requests for security problems, and do not include real vaults or passwords in a report.

Helpful details: affected version, platform (Windows / Android), steps to reproduce, impact.

## What to expect

- Acknowledgement of the report within **7 days**.
- A fix or a mitigation plan as soon as the issue is confirmed; you will be kept informed.
- Credit in the release notes if you wish.

## Supported versions

SochaGuard is pre-release (0.x). Only the **latest release** receives security fixes.

## Scope

In scope: cryptography and key handling, vault format, unlock / lock logic, autofill and auto-type behaviour, data leaks (logs, temp files, clipboard), release artifacts.

Out of scope: a device already compromised by malware or a keylogger, physical access to an unlocked device, weak Master Passwords, social engineering.
