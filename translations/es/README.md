<p align="center">
  <img src="../../assets/branding/logo_wordmark_transparent.png" alt="SochaGuard" width="320">
</p>

<p align="center"><a href="../../README.md">English</a> · <a href="../pl/README.md">Polski</a> · <a href="../de/README.md">Deutsch</a> · <b>Español</b> · <a href="../it/README.md">Italiano</a> · <a href="../uk/README.md">Українська</a></p>

<p align="center">
  <b>Bóveda sin conexión con cifrado de extremo a extremo para contraseñas, códigos TOTP, notas y archivos.</b><br>
  Sin cuenta. Sin nube. Sin acceso a la red.
</p>

<p align="center">
  <a href="https://github.com/devsocha/SochaGuard/releases"><img alt="release" src="https://img.shields.io/github/v/release/devsocha/SochaGuard?include_prereleases&label=release"></a>
  <img alt="platforms" src="https://img.shields.io/badge/platforms-Windows%20%7C%20Android-blue">
  <img alt="status" src="https://img.shields.io/badge/status-pre--release-orange">
</p>

> **Versión preliminar (0.x).** SochaGuard está en desarrollo activo y aún no ha tenido una auditoría de seguridad independiente. Guarda una copia de seguridad de lo importante.

## Características

- **Totalmente sin conexión** – sin servidor, sin sincronización, sin analítica. La app no necesita conexión de red.
- **Cifrado robusto** – derivación de clave de tu contraseña maestra con Argon2id y cifrado autenticado (XChaCha20-Poly1305 / AES-256-GCM) de cada objeto almacenado, incluidos títulos y direcciones.
- **Contraseñas, TOTP, notas y archivos** en una misma bóveda; varias bóvedas compatibles.
- **Clave de recuperación** y exportación / importación cifradas (importación de KeePass `.kdbx`).
- **Android:** autocompletado del sistema (con la opción «sugerir contraseña segura» en registros), desbloqueo rápido biométrico.
- **Windows (portable):** atajo global de **auto-type** `Ctrl + Mayús + Espacio` escribe el usuario y la contraseña en la ventana activa (sin portapapeles); vive en la **bandeja del sistema**, una sola instancia, **inicio con Windows** opcional.
- Idiomas: English, Polski, Deutsch, Español, Italiano, Українська.

## Descarga

Descarga la última versión en la página de [Releases](https://github.com/devsocha/SochaGuard/releases).

### Windows (portable)

1. Descarga `SochaGuard_Windows_portable_v<version>.zip` y `SHA256SUMS_v<version>.txt`.
2. Verifica la suma de comprobación (PowerShell):
   ```powershell
   Get-FileHash .\SochaGuard_Windows_portable_v<version>.zip -Algorithm SHA256
   ```
   El valor debe coincidir con el de `SHA256SUMS_v<version>.txt`.
3. Descomprime el zip donde quieras (p. ej. `C:\Tools\SochaGuard`) y ejecuta `sochaguard.exe`. No se instala nada; tu bóveda permanece en tu perfil de usuario.

> Windows SmartScreen puede avisar de un «editor desconocido»: las compilaciones aún no están firmadas (ver [ROADMAP](ROADMAP.md)). Comprobar la suma SHA-256 confirma que el archivo es el publicado aquí.

### Android

Se adjuntará un APK a las versiones a partir del hito indicado en la [hoja de ruta](ROADMAP.md).

## Documentación

[Getting started](../../docs/GETTING_STARTED.md) · [FAQ](../../docs/FAQ.md) · [Security model](../../docs/SECURITY_MODEL.md) · [Limitations](../../docs/LIMITATIONS.md) · [Privacy](../../docs/PRIVACY.md) (English)

## Seguridad

¿Has encontrado una vulnerabilidad? **No** abras un issue público; consulta [SECURITY](SECURITY.md).

Véase también: [CHANGELOG](../../CHANGELOG.md) · [ROADMAP](ROADMAP.md)

## Versionado

[Semantic Versioning](https://semver.org/). Mientras la versión sea `0.x`, el formato de la bóveda aún puede cambiar; cada cambio se indica en el [changelog](../../CHANGELOG.md).

## Licencia

Consulta [LICENSE](../../LICENSE).
