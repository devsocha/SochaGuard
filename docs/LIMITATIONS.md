# Limitations

Please know what SochaGuard cannot do.

- **A compromised device.** Malware, keyloggers, screen recorders or a malicious browser extension on your computer or phone can see what you type or see. SochaGuard cannot defend against that.
- **An unlocked session.** Anyone who can use your device while the vault is unlocked can read it. Keep auto-lock short.
- **Weak Master Passwords.** Argon2id slows guessing, it cannot fix "123456". Use a long passphrase.
- **No recovery without keys.** If you lose both the Master Password and the Recovery Key, the data is gone. There is no backdoor and no reset.
- **Auto-type (Windows).** It simulates key presses into the focused window. The target program receives the text, and so would a keylogger. It does not work in programs running as administrator (unless SochaGuard is too) and may not work in some remote-desktop or virtual-machine windows.
- **Clipboard.** Cleared after a timeout and on lock, but clipboard managers and Windows clipboard history may keep copies; clipboard sync across devices is outside SochaGuard's control. Prefer auto-type or autofill where possible.
- **Memory.** While unlocked, keys exist in the app's memory. Memory of a running process can be read by privileged malware.
- **Android autofill** depends on the keyboard and on how each app/website is built; some apps do not allow autofill at all.
- **Platforms.** Supported: Windows (portable) and Android 8.0 or newer (screenshots of the app are blocked on Android by design). iOS, macOS and Linux are not released.
- **Format may change in 0.x.** Until 1.0, an update may require re-importing an export. Always keep a recent backup.
- **Not audited.** See [SECURITY_MODEL.md](SECURITY_MODEL.md).
