# Ograniczenia

Warto wiedzieć, czego SochaGuard nie potrafi.

- **Zainfekowane urządzenie.** Malware, keyloggery, nagrywanie ekranu lub złośliwe rozszerzenie przeglądarki na komputerze albo telefonie mogą zobaczyć to, co wpisujesz lub widzisz. SochaGuard nie obroni przed tym.
- **Odblokowana sesja.** Każdy, kto może używać Twojego urządzenia przy odblokowanym sejfie, może go odczytać. Ustaw krótką blokadę automatyczną.
- **Słabe Master Password.** Argon2id spowalnia zgadywanie, ale nie naprawi „123456”. Użyj długiej frazy.
- **Brak odzyskiwania bez kluczy.** Jeśli zgubisz Master Password i Klucz odzyskiwania, dane przepadną. Nie ma tylnych drzwi ani resetu.
- **Auto-type (Windows).** Symuluje naciśnięcia klawiszy w aktywnym oknie. Program docelowy dostaje tekst, podobnie jak dostałby go keylogger. Nie działa w programach uruchomionych jako administrator (chyba że SochaGuard też) i może nie działać w niektórych oknach pulpitu zdalnego lub maszyn wirtualnych.
- **Schowek.** Czyszczony po czasie i przy blokadzie, ale menedżery schowka i historia schowka Windows mogą zachować kopie; synchronizacja schowka między urządzeniami jest poza kontrolą SochaGuard. Gdy się da, używaj auto-type lub autouzupełniania.
- **Pamięć.** Po odblokowaniu klucze znajdują się w pamięci aplikacji. Pamięć działającego procesu może odczytać uprzywilejowane malware.
- **Autouzupełnianie na Androidzie** zależy od klawiatury i budowy aplikacji lub strony; niektóre aplikacje w ogóle go nie dopuszczają.
- **Platformy.** Wspierane: Windows (portable) i Android 8.0 lub nowszy (zrzuty ekranu aplikacji są na Androidzie celowo blokowane). iOS, macOS i Linux nie są wydawane.
- **Format może się zmienić w 0.x.** Do wersji 1.0 aktualizacja może wymagać ponownego zaimportowania eksportu. Zawsze miej świeżą kopię zapasową.
- **Bez audytu.** Zobacz [SECURITY_MODEL.md](SECURITY_MODEL.md).
