# Publishing Guide

## Cel repozytorium

To repozytorium jest przeznaczone wyłącznie do dystrybucji gotowych paczek portable przez GitHub Releases.
Nie commituj tutaj danych użytkowników ani lokalnych plików roboczych.

## Co publikować

- `DMP-ART-Portable.zip` jako asset release
- `SHA256SUMS.txt` jako asset release lub plik śledzony w repo
- krótki changelog dla użytkownika końcowego

## Czego nie publikować

- `uploads/`
- `outputs/`
- cache użytkownika
- kluczy API
- prywatnych komentarzy lub konfiguracji instytucjonalnych, jeśli nie są przeznaczone do publicznej dystrybucji

## Procedura wydania

1. W repo źródłowym uruchom `python build_portable.py`.
2. Sprawdź, że powstał plik `dist/DMP-ART-Portable.zip`.
3. Skopiuj ZIP do `release-assets/` w tym repo.
4. Zaktualizuj `release-assets/SHA256SUMS.txt`.
5. Zacommituj dokumentację i checksumy, ale nie commituj samego ZIP-a.
6. Utwórz nowy GitHub Release, np. `v0.9.1`.
7. Dodaj `DMP-ART-Portable.zip` jako release asset.
8. Dodaj `SHA256SUMS.txt` jako drugi asset lub wklej sumę do opisu release.

## Minimalny szablon opisu release

```text
DMP-ART Portable vX.Y.Z

Zmiany:
- krótki opis 1
- krótki opis 2

Uruchomienie:
1. Pobierz DMP-ART-Portable.zip
2. Rozpakuj archiwum
3. Uruchom start_portable.bat

Uwaga:
- OCR dla skanowanych PDF nadal wymaga osobnej instalacji Tesseract OCR.
```

## Rekomendacja operacyjna

Jeśli odbiorcami są wyłącznie pracownicy jednej instytucji, ustaw repo jako prywatne.
Jeśli dystrybucja ma być publiczna, upewnij się wcześniej, że domyślne pliki konfiguracyjne nie zawierają żadnych danych wewnętrznych.