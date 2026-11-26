<p align="center">
  <img src="assets/branding/logo_wordmark_transparent.png" alt="SochaGuard" width="320">
</p>

<p align="center"><b>English</b> · <a href="translations/pl/README.md">Polski</a> · <a href="translations/de/README.md">Deutsch</a> · <a href="translations/es/README.md">Español</a> · <a href="translations/it/README.md">Italiano</a> · <a href="translations/uk/README.md">Українська</a></p>

<p align="center">
  <b>Offline, end-to-end encrypted vault for passwords, TOTP codes, notes and files.</b><br>
  No account. No cloud. No network access.
</p>

<p align="center">
  <a href="https://github.com/devsocha/SochaGuard/releases"><img alt="release" src="https://img.shields.io/github/v/release/devsocha/SochaGuard?include_prereleases&label=release"></a>
  <img alt="platforms" src="https://img.shields.io/badge/platforms-Windows%20%7C%20Android-blue">
  <img alt="status" src="https://img.shields.io/badge/status-pre--release-orange">
</p>

> **Pre-release (0.x).** SochaGuard is under active development and has not had an independent security audit yet. Keep a backup of anything important.

## Features

- **Fully offline** – no backend, no sync server, no analytics. The app does not need a network connection.
- **Strong encryption** – Argon2id key derivation from your Master Password, authenticated encryption (XChaCha20-Poly1305 / AES-256-GCM) for every stored object, including titles and addresses.
- **Passwords, TOTP, notes and files** in one vault; multiple vaults supported.
- **Recovery key** and encrypted export / import (KeePass `.kdbx` import supported).
- **Android:** system autofill (with a "suggest strong password" option on sign-up forms), biometric quick unlock.
- **Windows (portable):** global **auto-type** shortcut `Ctrl + Shift + Space` types the login and password into the window you are in (no clipboard); lives in the **system tray**, single instance, optional **start with Windows**.
- Languages: English, Polski, Deutsch, Español, Italiano, Українська.

## Download

Get the latest build from the [Releases](https://github.com/devsocha/SochaGuard/releases) page.

### Windows (portable)

1. Download `SochaGuard_Windows_portable_v<version>.zip` and `SHA256SUMS_v<version>.txt`.
2. Verify the checksum (PowerShell):
   ```powershell
   Get-FileHash .\SochaGuard_Windows_portable_v<version>.zip -Algorithm SHA256
   ```
   The value must match the one in `SHA256SUMS_v<version>.txt`.
3. Unpack the zip anywhere (e.g. `C:\Tools\SochaGuard`) and run `sochaguard.exe`. Nothing is installed; your vault stays in your user profile.

> Windows SmartScreen may warn about an "unknown publisher" – the builds are not code-signed yet (see [ROADMAP](ROADMAP.md)). Verifying the SHA-256 checksum confirms the file is the one published here.

### Android

Android: distributed through Google Play (link will be added here once published).

## Documentation

[Getting started](docs/GETTING_STARTED.md) · [FAQ](docs/FAQ.md) · [Security model](docs/SECURITY_MODEL.md) · [Limitations](docs/LIMITATIONS.md) · [Privacy](docs/PRIVACY.md) · [Privacy Policy](PRIVACY_POLICY.md) · [Terms of Use](TERMS.md)

## Security

Found a vulnerability? Please **do not** open a public issue – see [SECURITY](SECURITY.md).

See also: [CHANGELOG](CHANGELOG.md) · [ROADMAP](ROADMAP.md)

## Versioning

[Semantic Versioning](https://semver.org/). While the version is `0.x` the vault format may still change; every such change is called out in the [changelog](CHANGELOG.md).

## License

See [LICENSE](LICENSE).
