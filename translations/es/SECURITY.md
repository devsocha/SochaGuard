# Política de seguridad

<p align="center"><a href="../../SECURITY.md">English</a> · <a href="../pl/SECURITY.md">Polski</a> · <a href="../de/SECURITY.md">Deutsch</a> · <b>Español</b> · <a href="../it/SECURITY.md">Italiano</a> · <a href="../uk/SECURITY.md">Українська</a></p>

## Cómo informar de una vulnerabilidad

Informa de las vulnerabilidades **de forma privada**:

- Usa la función de GitHub **«Report a vulnerability»** (Security → Advisories) en este repositorio.

No abras issues ni pull requests públicos por problemas de seguridad, y no incluyas bóvedas ni contraseñas reales en el informe.

Datos útiles: versión afectada, plataforma (Windows / Android), pasos para reproducirlo, impacto.

## Qué puedes esperar

- Confirmación de recepción en un plazo de **7 días**.
- Una corrección o plan de mitigación en cuanto se confirme el problema; se te mantendrá informado.
- Mención en las notas de la versión, si lo deseas.

## Versiones compatibles

SochaGuard es una versión preliminar (0.x). Solo la **última versión** recibe correcciones de seguridad.

## Alcance

Dentro del alcance: criptografía y manejo de claves, formato de la bóveda, lógica de desbloqueo / bloqueo, comportamiento de autocompletado y auto-type, fugas de datos (registros, archivos temporales, portapapeles), artefactos de las versiones.

Fuera del alcance: un dispositivo ya comprometido por malware o keylogger, acceso físico a un dispositivo desbloqueado, contraseñas maestras débiles, ingeniería social.
