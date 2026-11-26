# Pierwsze kroki

## 1. Instalacja
- **Windows:** rozpakuj archiwum portable w dowolnym miejscu i uruchom `sochaguard.exe` (sprawdzanie sumy kontrolnej opisano w [README](../README.md)).
- **Android:** zainstaluj plik APK ze strony Releases.

## 2. Utwórz sejf
1. Wybierz język aplikacji.
2. Utwórz **Master Password**. To jedyny klucz do Twoich danych: SochaGuard nigdy go nie zapisuje i nie potrafi go zresetować. Użyj długiej frazy (12+ znaków, kilka niepowiązanych słów). Pasek siły hasła pomaga.
3. Zapisz **Klucz odzyskiwania** (`XXXX-XXXX-XXXX-XXXX-XXXX-XXXX`). Jest pokazywany jeden raz. Zapisz go na papierze i trzymaj w bezpiecznym miejscu, osobno od urządzenia. Bez Master Password **i** Klucza odzyskiwania nikt – także autor – nie otworzy Twojego sejfu.

## 3. Dodawanie danych
Przycisk **+**: hasła (z opcjonalnym kodem jednorazowym), samodzielne kody TOTP (zeskanuj kod QR lub wpisz sekret), bezpieczne notatki i szyfrowane pliki. Możesz zaimportować dane z KeePass (`.kdbx`), Aegis i plików CSV (Ustawienia → Import).

## 4. Używanie
- **Kopiowanie** hasła: schowek jest czyszczony po czasie ustawionym w Ustawieniach (domyślnie 20 s) oraz przy blokadzie sejfu.
- **Windows:** naciśnij `Ctrl + Shift + Spacja` w dowolnym oknie, aby wpisać w nie login i hasło (bez schowka). Zamknięcie okna zostawia SochaGuard w zasobniku systemowym; prawy klik na ikonie: Otwórz / Zablokuj / Zakończ.
- **Android:** włącz *Ustawienia → Autouzupełnianie*, aby wypełniać hasła w innych aplikacjach i przeglądarkach; włącz *Szybkie odblokowanie* dla odcisku palca / twarzy.

## 5. Kopia zapasowa
Ustawienia → **Eksportuj sejf** tworzy zaszyfrowany plik `.vault`. Rób go regularnie i trzymaj kopie na innym urządzeniu lub dysku. Przetestuj przywracanie (Ustawienia → Importuj sejf) przynajmniej raz.

## 6. Blokada
Sejf blokuje się automatycznie (Ustawienia → Blokada automatyczna: od razu, po 1, 5, 15 lub 30 minutach od opuszczenia aplikacji), po zablokowaniu Windows lub przejściu w stan uśpienia oraz z menu zasobnika.
