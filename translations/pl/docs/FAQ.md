# FAQ

**Zapomniałem Master Password.** Użyj Klucza odzyskiwania (ekran odblokowania → odzyskiwanie) i ustaw nowe Master Password. Jeśli nie masz żadnego z nich, danych nie da się odzyskać – tak jest zaprojektowana ochrona.

**Czy SochaGuard łączy się z internetem?** Nie. Nie ma konta, serwera, synchronizacji ani analityki. Nic nie opuszcza Twojego urządzenia. Zobacz [PRIVACY.md](PRIVACY.md).

**Jak przenieść sejf na inne urządzenie?** Wyeksportuj go na starym urządzeniu (Ustawienia → Eksportuj sejf), skopiuj plik `.vault` i zaimportuj na nowym. Plik pozostaje zaszyfrowany; do otwarcia potrzebne jest Master Password (lub Klucz odzyskiwania).

**Czy jest synchronizacja z chmurą?** Jeszcze nie. Eksporty możesz kopiować ręcznie. Ręczna synchronizacja jest w [roadmapie](../ROADMAP.md).

**Czy można kopiować plik sejfu lub trzymać kopię w chmurze?** Zawartość jest zaszyfrowana, więc kopia bez Master Password jest bezużyteczna. Chroni Cię silne Master Password; słabe da się odgadnąć offline.

**Czy mogę używać na kilku komputerach?** Tak, ale każdy ma własny sejf; zmiany nie scalają się automatycznie. Do przenoszenia danych użyj eksportu/importu.

**Dlaczego Windows pokazuje „nieznany wydawca”?** Wersje nie są jeszcze podpisane certyfikatem. Sprawdź sumę SHA-256 ze strony Releases. Podpisywanie planowane jest przed 1.0.

**Auto-type wpisał dane w złe okno.** Wpisuje w okno, które miało fokus w chwili naciśnięcia skrótu. Sprawdź najpierw to okno. Nie wpisze do programów uruchomionych jako administrator, chyba że SochaGuard też tak działa.

**Dlaczego na Androidzie podpowiedź nie pojawia się nad klawiaturą?** To zależy od klawiatury. Gboard to obsługuje; niektóre klawiatury (np. Samsunga) nie, wtedy aplikacja używa zwykłej listy.

**Jak zmienić skrót?** Jeszcze nie da się go skonfigurować (planowane).

**Dlaczego na Androidzie nie mogę zrobić zrzutu ekranu?** Zrzuty ekranu i nagrywanie ekranu są celowo zablokowane, żeby hasła nie mogły w ten sposób wyciec.

**Czy kod źródłowy jest dostępny?** To repozytorium zawiera tylko wydania i dokumentację.

**Znalazłem problem z bezpieczeństwem.** Przeczytaj [SECURITY.md](../SECURITY.md) i zgłoś go prywatnie.
