# Changelog

Format: [Semantic Versioning](https://semver.org/) — MAJOR.MINOR.PATCH+BUILD.
Version is set in `pubspec.yaml` and mirrored in `lib/core/app_version.dart`.

## [Unreleased]

## [0.8.0+21] — 2026-11-26

### Added
- Unsaved input in an Add/Edit password or note form is saved automatically as a NEW entry (titled "<title> (autosaved)" or "Untitled (autosaved)") right before the vault locks. Editing never overwrites the original entry.

## [0.7.1+20] — 2026-11-26

### Changed
- Android: autofill (filling and saving) stays off until the Terms and Privacy Policy have been accepted in the app.
- Terms and Privacy Policy: removed the website address (the current version is always available in the app) and the "to be confirmed" note about the INTERNET permission.

## [0.7.0+19] — 2026-11-26

### Added
- First-run screen: Terms of Use and Privacy Policy (read in the app) with two checkboxes that start unchecked — "I accept the Terms" and "I have read the Privacy Policy". Acceptance is stored only on the device and asked again when the documents change.
- Settings: Terms of Use, Privacy Policy and Open-source licenses (the licence list of all bundled libraries).
- After an auto-lock and unlock, the app reopens the same tab and the same open password/note (only the location is remembered, in memory, for 30 minutes; the content is decrypted again).

### Changed
- Terms and Privacy Policy rewritten: liability and warranty clauses now carve out intent, gross negligence, injury to life/body/health and consumer rights that cannot be excluded.

## [0.6.0+18] — 2026-11-26

### Added
- Password generator panel with preferences (length, uppercase, lowercase, digits, symbols) and a Copy button — in the app (add/edit password) and in the Android autofill dialog. Preferences are remembered and shared by both.
- Android: choose where autofill suggestions appear — on the keyboard or in a window under the field (Settings → Autofill suggestions).
- Android: on a sign-up form the "Suggest strong password" tile now opens the generator panel and fills both the password and the confirm field; you can copy the password before using it.
- Android: when no login is saved for a site (or from the account list) you can pick any other login from the vault; afterwards SochaGuard asks whether to also save it for the current site.

### Fixed
- Camera (TOTP scan): when permission is denied (including "Only this time") the screen stays and offers "Try again" — the system permission dialog is requested again every time; the vault no longer locks under the permission dialog.
- After copying a login or password and switching to another app (e.g. Chrome), the vault gets a 2-minute grace period before locking, so you return to the same screen instead of the vault list.
- Chrome instructions now match the real Chrome settings (Settings → Autofill services → Autofill using another service).

## [0.5.11+17] — 2026-11-21

### Fixed (Android)
- Autofill no longer shows a suggestion in ordinary text fields of other apps (search boxes in YouTube/X, notes). The password-field check compared single input-type bits that search and web fields also set; it now compares the exact input class and variation.

## [0.5.10+16] — 2026-11-21

### Security (Android)
- Release builds now explicitly remove the INTERNET permission that a dependency may add through manifest merging (new `android/app/src/release/AndroidManifest.xml`), so the app cannot access the network at all. Debug and profile builds are unchanged.

## [0.5.9+15] — 2026-11-15

### Changed (Android)
- Autofill no longer offers its tile on a field that already contains text, so the popup stops re-appearing while you type by hand (and no longer fights with the keyboard). The other field of the pair is not considered, so typing the login and filling only the password still works.

## [0.5.8+14] — 2026-11-15

### Changed (Android)
- Autofill suggestions are shown only as the dropdown under the field; the keyboard-strip (inline) variant is off, to avoid focus conflicts that closed the keyboard in password fields on some tablets.

## [0.5.7+13] — 2026-11-15

### Fixed
- The vault database handle is re-opened automatically if it was closed unexpectedly, so opening an entry no longer fails with "Something went wrong" after such an event.

## [0.5.6+12] — 2026-11-15

### Fixed
- Android: the autofill service no longer closes the vault database that the open app is using ("Something went wrong" after saving from autofill; lists not refreshing). The background engine now uses its own database connection.
- Android: fixed Kotlin build errors in the autofill code.

## [0.5.5+11] — 2026-11-15

### Fixed
- Logins saved through autofill now appear in the vault list as soon as you return to the app (the list refreshes on resume); before, they showed up only after restarting it.
- Site matching is stricter: the "update existing / save as new" choice and autofill matches only consider logins of the same site (same domain or its sub-domains); loose substring matching was removed.

## [0.5.4+10] — 2026-11-15

### Fixed (Android)
- Saving a second account for the same site (e.g. another Facebook login) now asks what to do: update an existing saved login or save as a new account. An identical login is reported as already saved.

## [0.5.3+9] — 2026-11-15

### Fixed (Android)
- Autofill save no longer fails silently: the user now sees "Saved in SochaGuard" or "Could not save", and failures are logged.
- Headless engine hardened: created from the application context (no leaked Activity), all calls on the main thread, a stale engine is discarded and restarted instead of crashing later fills.
- Pages with embedded frames (webmail portals such as wp.pl): the site is now taken from the frame holding the password field instead of whichever frame was seen last.
- Save after submit: the form is read from the newest autofill context that still contains the typed password (the last one is often already cleared).
- Logins saved on one sub-domain (profil.wp.pl) now match the same site on another (poczta.wp.pl).
- One unreadable record can no longer break saving or filling for the whole vault.

## [0.5.2+8] — 2026-11-15

### Fixed (Android)
- Autofill: a single, ambiguous password field now shows ONE suggestion instead of two ("fill" and "generate"). The taller two-row popup fought with the keyboard on some tablets (keyboard closing after one character). When nothing is saved for the site, tapping the suggestion offers "Suggest strong password".

## [0.5.1+7] — 2026-11-15

### Fixed (Android)
- Saving a password after a login no longer fails silently: if quick unlock is unavailable, cancelled or cached for another vault, SochaGuard now asks for the Master Password (same dialog as autofill) and then saves.
- The save prompt no longer depends on the username field being detected; only the password field is required.
- Master Password dialog: the keyboard opens together with the dialog and re-opens if the window loses focus (tablets closed it after the first typed character); the activity no longer restarts on keyboard / screen-layout changes.

## [0.5.0+6] — 2026-11-15

### Android
- Minimum supported version is now Android 8.0 (API 26), the first with the autofill framework; newer-only features stay guarded for older versions, target/compile SDK follow the installed Flutter (newest Android).
- Backups: explicit Android 12+ rules (`data_extraction_rules.xml`) exclude all app data from cloud backup and device transfer, in addition to `allowBackup=false`; cleartext traffic disabled.
- Screenshots / screen recording / recent-apps thumbnail are blocked on Android at all times, including the unlock screen and the autofill account and Master Password dialogs.
- Autofill: the e-mail field of web forms such as facebook.com is now recognised as the username (via Chrome's computed autofill hints).
- Autofill: reading the field ids passed between activities uses the non-deprecated API on Android 13+.
- Release signing is read from `android/key.properties` (see docs/ANDROID_SIGNING.md); added docs/ANDROID_RELEASE_CHECKLIST.md.

## [0.4.0+5] — 2026-11-15

### Security
- Import: archive entry names are validated, so a crafted `.vault` file can no longer write outside the temporary folder.
- Vault header is now written crash-safely (temp file + rename) with a `header.json.bak` backup; a damaged header falls back to the backup.
- Export files are written under a temporary name and renamed when complete.
- Auto-lock: after returning from the background the app now compares real elapsed time, so it locks even if the timer was frozen while suspended.
- Windows: the vault locks when Windows is locked (Win+L) or goes to sleep.
- Copied secrets are removed from the clipboard when the vault locks; the Recovery Key copy buttons now also clear the clipboard automatically.
- Argon2id calibration is capped at 256 MiB, so vaults stay unlockable on phones with little RAM.
- Vault header parsing rejects a missing or invalid format version cleanly.

### Added
- Automated tests: encryption (tamper / AAD / wrong key), Argon2id, Recovery Key, vault header, full vault lifecycle (create / unlock / recovery / change password), RFC 6238 TOTP vectors, and a format-stability test (`test/frozen_vault_test.dart`).
- User documentation: getting started, FAQ, security model, limitations, privacy.

### Removed
- Obsolete default `widget_test.dart` (it tested a counter app that does not exist).

## [0.3.1+4] — 2026-11-15

### Changed (Windows)
- The auto-type shortcut hint bar is now always visible and can no longer be dismissed.

## [0.3.0+3] — 2026-11-15

### Added (Windows)
- Single instance: starting SochaGuard again just brings the running window to the front.
- System tray icon (Open / Lock / Quit); closing the window hides it to the tray so the Ctrl+Shift+Space shortcut keeps working.
- Settings: "Close button hides to tray" toggle and "Start with Windows" (per-user, starts minimized to the tray).

## [0.2.0+2] — 2026-11-15

### Added
- Windows: auto-type by global shortcut (Ctrl + Shift + Space) — picks an entry and types
  login/password into the window that had focus (offline, no clipboard).
- Windows: hint bar about the shortcut at the bottom of the main screen.
- Android autofill: redesigned suggestion tile, account picker and Master Password dialog;
  suggestions can also appear on the keyboard strip (inline) where the keyboard supports it.
- Changelog and version rules (`lib/core/app_version.dart`).

### Changed
- Windows: window opens tall (600×800) in the bottom-right corner of the screen.
- Windows/desktop: quick unlock and system autofill options are hidden (phones/tablets only).
- New logo on the unlock, welcome and language screens.

### Fixed
- Android autofill: registration forms (e.g. facebook.com) now offer "Suggest strong password"
  instead of saved passwords.
- Android autofill: follows the vault that is active right now (including quick-unlock key).
- Android build error caused by mismatched `BiometricKeystoreChannel.kt`.
- Quick-unlock key on older Android versions (< 11).

## [0.1.0+1] — MVP
- First MVP: encrypted offline vault (passwords, TOTP, notes, files), Android autofill, Windows app.

[Unreleased]: https://github.com/devsocha/SochaGuard/compare/v0.8.0...HEAD
[0.8.0+21]: https://github.com/devsocha/SochaGuard/compare/v0.7.1...v0.8.0
[0.7.1+20]: https://github.com/devsocha/SochaGuard/compare/v0.7.0...v0.7.1
[0.7.0+19]: https://github.com/devsocha/SochaGuard/compare/v0.6.0...v0.7.0
[0.6.0+18]: https://github.com/devsocha/SochaGuard/compare/v0.5.11...v0.6.0
[0.5.11+17]: https://github.com/devsocha/SochaGuard/compare/v0.5.10...v0.5.11
[0.5.10+16]: https://github.com/devsocha/SochaGuard/compare/v0.5.9...v0.5.10
[0.5.9+15]: https://github.com/devsocha/SochaGuard/compare/v0.5.8...v0.5.9
[0.5.8+14]: https://github.com/devsocha/SochaGuard/compare/v0.5.7...v0.5.8
[0.5.7+13]: https://github.com/devsocha/SochaGuard/compare/v0.5.6...v0.5.7
[0.5.6+12]: https://github.com/devsocha/SochaGuard/compare/v0.5.5...v0.5.6
[0.5.5+11]: https://github.com/devsocha/SochaGuard/compare/v0.5.4...v0.5.5
[0.5.4+10]: https://github.com/devsocha/SochaGuard/compare/v0.5.3...v0.5.4
[0.5.3+9]: https://github.com/devsocha/SochaGuard/compare/v0.5.2...v0.5.3
[0.5.2+8]: https://github.com/devsocha/SochaGuard/compare/v0.5.1...v0.5.2
[0.5.1+7]: https://github.com/devsocha/SochaGuard/compare/v0.5.0...v0.5.1
[0.5.0+6]: https://github.com/devsocha/SochaGuard/compare/v0.4.0...v0.5.0
[0.4.0+5]: https://github.com/devsocha/SochaGuard/compare/v0.3.1...v0.4.0
[0.3.1+4]: https://github.com/devsocha/SochaGuard/compare/v0.3.0...v0.3.1
[0.3.0+3]: https://github.com/devsocha/SochaGuard/compare/v0.2.0...v0.3.0
[0.2.0+2]: https://github.com/devsocha/SochaGuard/compare/v0.1.0...v0.2.0
[0.1.0+1]: https://github.com/devsocha/SochaGuard/releases/tag/v0.1.0
