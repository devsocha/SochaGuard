<p align="center">
  <img src="../../assets/branding/logo_wordmark_transparent.png" alt="SochaGuard" width="320">
</p>

<p align="center"><a href="../../README.md">English</a> · <a href="../pl/README.md">Polski</a> · <a href="../de/README.md">Deutsch</a> · <a href="../es/README.md">Español</a> · <b>Italiano</b> · <a href="../uk/README.md">Українська</a></p>

<p align="center">
  <b>Cassaforte offline con crittografia end-to-end per password, codici TOTP, note e file.</b><br>
  Nessun account. Nessun cloud. Nessun accesso alla rete.
</p>

<p align="center">
  <a href="https://github.com/devsocha/SochaGuard/releases"><img alt="release" src="https://img.shields.io/github/v/release/devsocha/SochaGuard?include_prereleases&label=release"></a>
  <img alt="platforms" src="https://img.shields.io/badge/platforms-Windows%20%7C%20Android-blue">
  <img alt="status" src="https://img.shields.io/badge/status-pre--release-orange">
</p>

> **Versione preliminare (0.x).** SochaGuard è in sviluppo attivo e non ha ancora avuto un audit di sicurezza indipendente. Conserva una copia di backup dei dati importanti.

## Funzionalità

- **Completamente offline** – nessun server, nessuna sincronizzazione, nessuna analisi. L’app non richiede una connessione di rete.
- **Crittografia robusta** – derivazione della chiave dalla password principale con Argon2id e crittografia autenticata (XChaCha20-Poly1305 / AES-256-GCM) per ogni oggetto salvato, compresi titoli e indirizzi.
- **Password, TOTP, note e file** in un’unica cassaforte; più casseforti supportate.
- **Chiave di recupero** ed esportazione / importazione cifrate (importazione KeePass `.kdbx`).
- **Android:** compilazione automatica di sistema (con l’opzione «suggerisci password sicura» nelle registrazioni), sblocco rapido biometrico.
- **Windows (portatile):** scorciatoia globale **auto-type** `Ctrl + Maiusc + Spazio` digita utente e password nella finestra attiva (senza appunti); resta nell’**area di notifica**, una sola istanza, **avvio con Windows** opzionale.
- Lingue: English, Polski, Deutsch, Español, Italiano, Українська.

## Download

Scarica l’ultima versione dalla pagina [Releases](https://github.com/devsocha/SochaGuard/releases).

### Windows (portatile)

1. Scarica `SochaGuard_Windows_portable_v<version>.zip` e `SHA256SUMS_v<version>.txt`.
2. Verifica il checksum (PowerShell):
   ```powershell
   Get-FileHash .\SochaGuard_Windows_portable_v<version>.zip -Algorithm SHA256
   ```
   Il valore deve coincidere con quello in `SHA256SUMS_v<version>.txt`.
3. Estrai lo zip dove preferisci (ad es. `C:\Tools\SochaGuard`) ed esegui `sochaguard.exe`. Non viene installato nulla; la tua cassaforte resta nel tuo profilo utente.

> Windows SmartScreen può avvisare di un «editore sconosciuto»: le build non sono ancora firmate (vedi [ROADMAP](ROADMAP.md)). Verificare il checksum SHA-256 conferma che il file è quello pubblicato qui.

### Android

Un APK verrà allegato alle release a partire dalla tappa indicata nella [roadmap](ROADMAP.md).

## Documentazione

[Getting started](../../docs/GETTING_STARTED.md) · [FAQ](../../docs/FAQ.md) · [Security model](../../docs/SECURITY_MODEL.md) · [Limitations](../../docs/LIMITATIONS.md) · [Privacy](../../docs/PRIVACY.md) (English)

## Sicurezza

Hai trovato una vulnerabilità? **Non** aprire una issue pubblica: vedi [SECURITY](SECURITY.md).

Vedi anche: [CHANGELOG](../../CHANGELOG.md) · [ROADMAP](ROADMAP.md)

## Versionamento

[Semantic Versioning](https://semver.org/). Finché la versione è `0.x`, il formato della cassaforte può ancora cambiare; ogni modifica è indicata nel [changelog](../../CHANGELOG.md).

## Licenza

Vedi [LICENSE](../../LICENSE).
