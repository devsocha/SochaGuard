<p align="center">
  <img src="../../assets/branding/logo_wordmark_transparent.png" alt="SochaGuard" width="320">
</p>

<p align="center"><a href="../../README.md">English</a> · <a href="../pl/README.md">Polski</a> · <b>Deutsch</b> · <a href="../es/README.md">Español</a> · <a href="../it/README.md">Italiano</a> · <a href="../uk/README.md">Українська</a></p>

<p align="center">
  <b>Offline-Tresor mit Ende-zu-Ende-Verschlüsselung für Passwörter, TOTP-Codes, Notizen und Dateien.</b><br>
  Kein Konto. Keine Cloud. Kein Netzwerkzugriff.
</p>

<p align="center">
  <a href="https://github.com/devsocha/SochaGuard/releases"><img alt="release" src="https://img.shields.io/github/v/release/devsocha/SochaGuard?include_prereleases&label=release"></a>
  <img alt="platforms" src="https://img.shields.io/badge/platforms-Windows%20%7C%20Android-blue">
  <img alt="status" src="https://img.shields.io/badge/status-pre--release-orange">
</p>

> **Vorabversion (0.x).** SochaGuard wird aktiv entwickelt und wurde noch nicht unabhängig sicherheitsgeprüft. Bewahre von wichtigen Daten eine Sicherung auf.

## Funktionen

- **Komplett offline** – kein Server, keine Synchronisierung, keine Analyse. Die App braucht keine Netzwerkverbindung.
- **Starke Verschlüsselung** – Schlüsselableitung aus dem Master-Passwort mit Argon2id, authentifizierte Verschlüsselung (XChaCha20-Poly1305 / AES-256-GCM) für jedes gespeicherte Objekt, auch Titel und Adressen.
- **Passwörter, TOTP, Notizen und Dateien** in einem Tresor; mehrere Tresore möglich.
- **Wiederherstellungsschlüssel** sowie verschlüsselter Export / Import (KeePass-`.kdbx`-Import).
- **Android:** System-Autofill (mit „Starkes Passwort vorschlagen“ bei Registrierungen), biometrisches Schnellentsperren.
- **Windows (portabel):** globale **Auto-Type**-Tastenkombination `Strg + Umschalt + Leertaste` tippt Benutzername und Passwort in das aktive Fenster (ohne Zwischenablage); läuft im **Infobereich**, nur eine Instanz, optional **Start mit Windows**.
- Sprachen: English, Polski, Deutsch, Español, Italiano, Українська.

## Download

Die neueste Version findest du auf der Seite [Releases](https://github.com/devsocha/SochaGuard/releases).

### Windows (portabel)

1. Lade `SochaGuard_Windows_portable_v<version>.zip` und `SHA256SUMS_v<version>.txt` herunter.
2. Prüfsumme kontrollieren (PowerShell):
   ```powershell
   Get-FileHash .\SochaGuard_Windows_portable_v<version>.zip -Algorithm SHA256
   ```
   Der Wert muss mit dem in `SHA256SUMS_v<version>.txt` übereinstimmen.
3. Entpacke das Archiv an beliebiger Stelle (z. B. `C:\Tools\SochaGuard`) und starte `sochaguard.exe`. Es wird nichts installiert; dein Tresor bleibt in deinem Benutzerprofil.

> Windows SmartScreen kann vor einem „unbekannten Herausgeber“ warnen – die Builds sind noch nicht signiert (siehe [ROADMAP](ROADMAP.md)). Die SHA-256-Prüfsumme bestätigt, dass die Datei die hier veröffentlichte ist.

### Android

Eine APK wird ab dem in der [Roadmap](ROADMAP.md) genannten Meilenstein den Releases beigefügt.

## Dokumentation

[Getting started](../../docs/GETTING_STARTED.md) · [FAQ](../../docs/FAQ.md) · [Security model](../../docs/SECURITY_MODEL.md) · [Limitations](../../docs/LIMITATIONS.md) · [Privacy](../../docs/PRIVACY.md) (English)

## Sicherheit

Sicherheitslücke gefunden? Bitte **kein** öffentliches Issue eröffnen – siehe [SECURITY](SECURITY.md).

Siehe auch: [CHANGELOG](../../CHANGELOG.md) · [ROADMAP](ROADMAP.md)

## Versionierung

[Semantic Versioning](https://semver.org/). Solange die Version `0.x` ist, kann sich das Tresorformat noch ändern; jede solche Änderung steht im [Changelog](../../CHANGELOG.md).

## Lizenz

Siehe [LICENSE](../../LICENSE).
