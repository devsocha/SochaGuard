# Security model

SochaGuard is an **offline** vault: no server, no account, no network access. Everything stays on your device.

## How your data is protected
- **Master Password → key.** A key is derived from the Master Password with **Argon2id** (memory-hard, tuned per device, parameters stored in the vault header – they are not secret). The password itself is never stored.
- **Key hierarchy.** A random **Vault Key** encrypts everything. It is stored only in encrypted ("wrapped") form: once under the key from your Master Password and, if you set it up, once under the Recovery Key. Changing the Master Password re-wraps only that key, no data has to be re-encrypted.
- **Per-item keys.** Every record and file has its own random key, wrapped by the Vault Key.
- **Authenticated encryption.** Each stored object uses **XChaCha20-Poly1305**. Any modification of the ciphertext, or moving an object into a different slot, is detected and rejected. Titles, usernames, URLs, notes and file names are encrypted together with the content.
- **Randomness.** All keys, salts and nonces come from the operating system's secure random generator.
- **Recovery Key.** 120 random bits, shown once. It is an independent way to open the same vault.
- **Export files** are encrypted; importing validates their structure and rejects unsafe archives.
- **Header safety.** The vault header is written crash-safely with a backup copy.
- **Screen capture** is blocked (Android: always, including the recent-apps thumbnail; Windows: while the vault is unlocked).
- **No backups to the cloud:** on Android all app data is excluded from Google backup and device transfer.
- **Clipboard** copies are cleared after a timeout and when the vault locks.
- **Auto-lock** after you leave the app, when Windows locks or sleeps, and from the tray menu.

## What is *not* protected
See [LIMITATIONS.md](LIMITATIONS.md). In short: malware or keyloggers on your device, someone using your unlocked session, and weak Master Passwords.

## Independent review
SochaGuard has **not** been independently audited yet. A review of the cryptography and code is on the [roadmap](../ROADMAP.md) before 1.0. Until then, treat it as pre-release software and keep backups.
