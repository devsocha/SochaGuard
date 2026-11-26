<p align="center">
  <img src="../../assets/branding/logo_wordmark_transparent.png" alt="SochaGuard" width="320">
</p>

<p align="center"><a href="../../README.md">English</a> · <a href="../pl/README.md">Polski</a> · <a href="../de/README.md">Deutsch</a> · <a href="../es/README.md">Español</a> · <a href="../it/README.md">Italiano</a> · <b>Українська</b></p>

<p align="center">
  <b>Офлайн-сховище з наскрізним шифруванням для паролів, кодів TOTP, нотаток і файлів.</b><br>
  Без облікового запису. Без хмари. Без доступу до мережі.
</p>

<p align="center">
  <a href="https://github.com/devsocha/SochaGuard/releases"><img alt="release" src="https://img.shields.io/github/v/release/devsocha/SochaGuard?include_prereleases&label=release"></a>
  <img alt="platforms" src="https://img.shields.io/badge/platforms-Windows%20%7C%20Android-blue">
  <img alt="status" src="https://img.shields.io/badge/status-pre--release-orange">
</p>

> **Попередня версія (0.x).** SochaGuard активно розробляється й ще не пройшов незалежного аудиту безпеки. Зберігайте резервну копію важливих даних.

## Можливості

- **Повністю офлайн** – без сервера, синхронізації та аналітики. Застосунку не потрібне мережеве з’єднання.
- **Надійне шифрування** – виведення ключа з майстер-пароля через Argon2id, автентифіковане шифрування (XChaCha20-Poly1305 / AES-256-GCM) кожного збереженого об’єкта, зокрема назв і адрес.
- **Паролі, TOTP, нотатки та файли** в одному сховищі; підтримка кількох сховищ.
- **Ключ відновлення** та зашифрований експорт / імпорт (імпорт KeePass `.kdbx`).
- **Android:** системне автозаповнення (з опцією «запропонувати надійний пароль» під час реєстрації), швидке біометричне розблокування.
- **Windows (portable):** глобальне скорочення **auto-type** `Ctrl + Shift + Пробіл` вводить логін і пароль у активне вікно (без буфера обміну); працює в **системному треї**, один екземпляр, за бажанням **запуск разом із Windows**.
- Мови: English, Polski, Deutsch, Español, Italiano, Українська.

## Завантаження

Останню версію можна завантажити зі сторінки [Releases](https://github.com/devsocha/SochaGuard/releases).

### Windows (portable)

1. Завантажте `SochaGuard_Windows_portable_v<version>.zip` і `SHA256SUMS_v<version>.txt`.
2. Перевірте контрольну суму (PowerShell):
   ```powershell
   Get-FileHash .\SochaGuard_Windows_portable_v<version>.zip -Algorithm SHA256
   ```
   Значення має збігатися з указаним у `SHA256SUMS_v<version>.txt`.
3. Розпакуйте архів у будь-яке місце (наприклад, `C:\Tools\SochaGuard`) і запустіть `sochaguard.exe`. Нічого не встановлюється; ваше сховище залишається у профілі користувача.

> Windows SmartScreen може попередити про «невідомого видавця» – збірки ще не підписані (див. [ROADMAP](ROADMAP.md)). Перевірка суми SHA-256 підтверджує, що файл саме той, який опубліковано тут.

### Android

APK додаватиметься до релізів, починаючи з етапу з [дорожньої карти](ROADMAP.md).

## Документація

[Getting started](../../docs/GETTING_STARTED.md) · [FAQ](../../docs/FAQ.md) · [Security model](../../docs/SECURITY_MODEL.md) · [Limitations](../../docs/LIMITATIONS.md) · [Privacy](../../docs/PRIVACY.md) (English)

## Безпека

Знайшли вразливість? **Не** створюйте публічний issue – див. [SECURITY](SECURITY.md).

Див. також: [CHANGELOG](../../CHANGELOG.md) · [ROADMAP](ROADMAP.md)

## Версіонування

[Semantic Versioning](https://semver.org/). Поки версія `0.x`, формат сховища ще може змінюватися; кожну таку зміну зазначено в [changelog](../../CHANGELOG.md).

## Ліцензія

Див. [LICENSE](../../LICENSE).
