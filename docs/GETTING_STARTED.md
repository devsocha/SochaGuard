# Getting started

## 1. Install
- **Windows:** unpack the portable zip anywhere and run `sochaguard.exe` (see the [README](../README.md) for checksum verification).
- **Android:** install the APK from the Releases page.

## 2. Create your vault
1. Choose the app language.
2. Create a **Master Password**. It is the only key to your data: SochaGuard never stores it and cannot reset it. Use a long passphrase (12+ characters, several unrelated words). The strength bar helps.
3. Save your **Recovery Key** (`XXXX-XXXX-XXXX-XXXX-XXXX-XXXX`). It is shown once. Write it on paper and keep it somewhere safe, separate from the device. Without the Master Password **and** the Recovery Key, nobody – including the developer – can open your vault.

## 3. Add data
Use the **+** button: passwords (with optional one-time codes), standalone TOTP codes (scan a QR code or type the secret), secure notes and encrypted files. You can import from KeePass (`.kdbx`), Aegis and CSV files (Settings → Import).

## 4. Use it
- **Copy** a password: it is cleared from the clipboard after the time set in Settings (default 20 s) and when the vault locks.
- **Windows:** press `Ctrl + Shift + Space` in any window to type a login and password into it (no clipboard). Closing the window keeps SochaGuard in the system tray; right-click the tray icon for Open / Lock / Quit.
- **Android:** enable *Settings → Autofill* to fill passwords in other apps and browsers; enable *Quick unlock* for fingerprint / face.

## 5. Back up
Settings → **Export vault** creates an encrypted `.vault` file. Make one regularly and keep copies on a different device or drive. Test restoring it (Settings → Import vault) at least once.

## 6. Lock
The vault locks automatically (Settings → Auto-lock: immediately, 1, 5, 15 or 30 minutes after you leave the app), when Windows is locked or goes to sleep, and from the tray menu.
