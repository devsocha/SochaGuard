# Model bezpieczeństwa

SochaGuard to sejf **offline**: bez serwera, konta i dostępu do sieci. Wszystko zostaje na Twoim urządzeniu.

## Jak chronione są dane
- **Master Password → klucz.** Klucz jest wyprowadzany z Master Password przez **Argon2id** (odporny na sprzęt, dobierany do urządzenia, parametry zapisane w nagłówku sejfu – nie są tajne). Samo hasło nie jest nigdzie zapisywane.
- **Hierarchia kluczy.** Losowy **Klucz sejfu** szyfruje wszystko. Jest zapisany tylko w postaci zaszyfrowanej („owiniętej”): raz kluczem z Master Password i, jeśli go ustawisz, raz Kluczem odzyskiwania. Zmiana Master Password owija ponownie tylko ten klucz; dane nie muszą być szyfrowane od nowa.
- **Klucze elementów.** Każdy rekord i plik ma własny losowy klucz, owinięty Kluczem sejfu.
- **Szyfrowanie uwierzytelnione.** Każdy zapisany obiekt używa **XChaCha20-Poly1305**. Każda modyfikacja szyfrogramu lub przeniesienie obiektu w inne miejsce jest wykrywane i odrzucane. Tytuły, loginy, adresy, notatki i nazwy plików są szyfrowane razem z treścią.
- **Losowość.** Wszystkie klucze, sole i nonce pochodzą z systemowego bezpiecznego generatora losowego.
- **Klucz odzyskiwania.** 120 losowych bitów, pokazywany raz. To niezależny sposób otwarcia tego samego sejfu.
- **Pliki eksportu** są zaszyfrowane; import sprawdza ich strukturę i odrzuca niebezpieczne archiwa.
- **Bezpieczny nagłówek.** Nagłówek sejfu jest zapisywany odpornie na awarie, z kopią zapasową.
- **Zrzuty ekranu** są blokowane (Android: zawsze, także miniatura w ostatnich aplikacjach; Windows: gdy sejf jest odblokowany).
- **Brak kopii w chmurze:** na Androidzie wszystkie dane aplikacji są wyłączone z kopii Google i przenoszenia między urządzeniami.
- **Schowek** jest czyszczony po czasie oraz przy blokadzie sejfu.
- **Blokada automatyczna** po opuszczeniu aplikacji, po zablokowaniu lub uśpieniu Windows i z menu zasobnika.

## Czego *nie* chroni
Zobacz [LIMITATIONS.md](LIMITATIONS.md). W skrócie: malware lub keyloggery na urządzeniu, ktoś korzystający z Twojej odblokowanej sesji oraz słabe Master Password.

## Niezależny przegląd
SochaGuard **nie** przeszedł jeszcze niezależnego audytu. Przegląd kryptografii i kodu jest w [roadmapie](../ROADMAP.md) przed 1.0. Do tego czasu traktuj go jako oprogramowanie przedpremierowe i rób kopie zapasowe.
