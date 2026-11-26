> Polish original. English and Ukrainian versions will follow.

# Polityka prywatności aplikacji SochaGuard

**Ostatnia aktualizacja:** 26.11.2026
**Wydawca aplikacji (dalej: „Wydawca”):** Konrad Socha, Nowy Dwór Mazowiecki, Polska
**Kontakt:** sochaguard@gmail.com

## 1. W skrócie

SochaGuard to aplikacja do przechowywania haseł, kodów jednorazowych (TOTP), notatek i plików, działająca **wyłącznie offline** na Twoim urządzeniu (Android, Windows). **Wydawca nie zbiera, nie odbiera, nie przechowuje ani nie udostępnia żadnych Twoich danych.** Aplikacja nie ma kont użytkowników, reklam, analityki, raportów awarii ani modułów śledzących.

## 2. Jakie dane przechowuje aplikacja

Wszystko, co zapiszesz w aplikacji (loginy, hasła, adresy stron, kody TOTP, notatki, pliki, nazwy sejfów oraz ustawienia aplikacji, w tym informacja o zaakceptowaniu Regulaminu), jest zapisywane **tylko lokalnie na Twoim urządzeniu**.

Dane sejfu są szyfrowane algorytmami XChaCha20-Poly1305, a klucz jest wyprowadzany z Twojego hasła głównego funkcją Argon2id. Hasło główne nie jest nigdzie zapisywane ani wysyłane. Wydawca nie ma ani dostępu do Twoich danych, ani żadnego sposobu ich odszyfrowania lub odzyskania.

## 3. Brak komunikacji sieciowej

Aplikacja nie łączy się z internetem w celu przesyłania Twoich danych i nie wysyła ich do Wydawcy ani do osób trzecich. Wersja na Androida nie zawiera uprawnienia INTERNET, więc technicznie nie może łączyć się z siecią.

## 4. Uprawnienia i funkcje systemowe

- **Usługa autouzupełniania (Android).** Gdy włączysz SochaGuard jako usługę autouzupełniania w ustawieniach systemu, Android przekazuje aplikacji strukturę ekranu z polami logowania (m.in. nazwę strony lub aplikacji), aby mogła zaproponować dane i zapisać nowe. Informacje te są przetwarzane wyłącznie w pamięci urządzenia na czas operacji, nie są wysyłane poza urządzenie i nie są zapisywane inaczej niż jako rekord w Twoim zaszyfrowanym sejfie, jeśli sam o to poprosisz.
- **Aparat.** Aplikacja korzysta z aparatu wyłącznie na Twoje żądanie, aby zeskanować kod QR z kluczem TOTP. Obraz jest przetwarzany na urządzeniu i nie jest zapisywany ani wysyłany.
- **Biometria / blokada ekranu.** Jeśli włączysz szybkie odblokowanie, aplikacja korzysta z systemowego mechanizmu biometrycznego (odcisk palca, twarz, PIN/wzór urządzenia). Dane biometryczne pozostają pod kontrolą systemu Android. Aplikacja ich nie widzi ani nie zapisuje.
- **Schowek.** Skopiowane hasła i kody mogą być automatycznie usuwane ze schowka po krótkim czasie i przy blokadzie sejfu.
- **Pliki.** Aplikacja odczytuje i zapisuje pliki tylko wtedy, gdy sam wybierzesz plik do dodania, eksportu lub importu (systemowy wybór plików).
- **Ochrona zrzutów ekranu.** Aplikacja może blokować zrzuty ekranu i podgląd w liście ostatnich aplikacji.

## 5. Kopie zapasowe i eksport

Kopie zapasowe w chmurze systemu Android są dla aplikacji wyłączone. Eksport i import sejfu wykonujesz samodzielnie do pliku, którego lokalizację wybierasz sam. Za bezpieczeństwo takiego pliku i miejsca jego zapisu odpowiadasz Ty.

## 6. Podmioty trzecie

Aplikację możesz pobrać z serwisów takich jak Google Play lub GitHub (wersja windowsowa). Te serwisy mogą zbierać własne dane o pobraniu, urządzeniu lub koncie zgodnie ze swoimi politykami prywatności. Wydawca nie ma na to wpływu ani dostępu do tych danych w zakresie wykraczającym poza zbiorcze statystyki udostępniane deweloperom.

## 7. Dzieci

Aplikacja nie jest kierowana do dzieci i nie zbiera żadnych danych, w tym danych dzieci.

## 8. Twoje prawa

Ponieważ Wydawca nie przetwarza Twoich danych osobowych zapisanych w aplikacji, nie ma w swoim posiadaniu danych, które mógłby udostępnić, sprostować lub usunąć. Dane w aplikacji możesz w każdej chwili edytować, wyeksportować lub usunąć samodzielnie (łącznie z usunięciem sejfu lub aplikacji).

Jeśli napiszesz do Wydawcy, Twój adres e-mail i treść wiadomości służą wyłącznie do odpowiedzi na nią i możesz poprosić o ich usunięcie. Przysługuje Ci także prawo wniesienia skargi do organu nadzorczego (w Polsce: Prezes Urzędu Ochrony Danych Osobowych, uodo.gov.pl).

## 9. Bezpieczeństwo

Bezpieczeństwo danych zależy także od Ciebie: od siły hasła głównego, ochrony urządzenia, aktualizacji systemu i unikania złośliwego oprogramowania. Szczegóły w Regulaminie.

## 10. Zmiany polityki

Polityka może być aktualizowana, np. przy dodaniu nowych funkcji. O istotnych zmianach poinformujemy w Aplikacji.

## 11. Kontakt

W sprawach dotyczących prywatności napisz na: sochaguard@gmail.com.
