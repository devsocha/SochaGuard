# FAQ

**I forgot my Master Password.** Use the Recovery Key (unlock screen → recovery) and set a new Master Password. If you have neither, the data cannot be recovered – this is by design.

**Does SochaGuard connect to the internet?** No. There is no account, server, sync or analytics. Nothing leaves your device. See [PRIVACY.md](PRIVACY.md).

**How do I move my vault to another device?** Export on the old device (Settings → Export vault), copy the `.vault` file, then Import on the new one. The file stays encrypted; you need the Master Password (or Recovery Key) to open it.

**Is there cloud sync?** Not yet. You can copy exports manually. Manual sync is on the [roadmap](../ROADMAP.md).

**Is it safe to copy the vault file around or store a backup in the cloud?** The contents are encrypted, so a copy is useless without the Master Password. A strong Master Password is what protects you; weak ones can be guessed offline.

**Can I use it on several computers?** Yes, but each keeps its own vault; changes do not merge automatically. Use export/import to move data.

**Why does Windows say "unknown publisher"?** The builds are not code-signed yet. Verify the SHA-256 checksum from the Releases page. Signing is planned before 1.0.

**Auto-type typed into the wrong window.** It types into the window that had focus when you pressed the shortcut. Check that window first. It cannot type into programs running as administrator unless SochaGuard does too.

**Why doesn't the Android suggestion appear above the keyboard?** It depends on the keyboard. Gboard supports it; some keyboards (e.g. Samsung's) do not and the app falls back to a normal dropdown.

**How do I change the shortcut?** Not configurable yet (planned).

**Why can't I take a screenshot on Android?** Screenshots and screen recording are blocked on purpose, so passwords cannot leak that way.

**Is the source code available?** This repository contains releases and documentation only.

**I found a security problem.** Please read [SECURITY.md](../SECURITY.md) and report it privately.
