<img width="8534" height="4572" alt="image" src="https://github.com/user-attachments/assets/785b4f20-e0d2-4b0b-8f5c-3405ef4e5293" />

# DMP-ART-Portable

Dystrybucyjne repozytorium pakietów portable dla DMP-ART.

To repo nie służy do rozwoju aplikacji. Zawiera dokumentację publikacji oraz artefakty przygotowane do wrzucenia do GitHub Releases.

## Dla użytkownika końcowego

Najprostszy sposób użycia aplikacji:

1. Otwórz zakładkę Releases.
2. Pobierz `DMP-ART-Portable.zip` z najnowszej wersji.
3. Rozpakuj archiwum do zwykłego folderu, np. na Pulpicie.
4. Uruchom `start_portable.bat`.
5. Pracuj w przeglądarce pod `http://localhost:5000`.

## Co jest ważne z perspektywy prywatności

- aplikacja działa lokalnie na komputerze użytkownika,
- pliki wejściowe, konfiguracja komentarzy i wyniki pozostają lokalnie,
- repozytorium dystrybucyjne nie powinno zawierać żadnych danych użytkowników ani lokalnych konfiguracji roboczych.

## Struktura repo

- `release-assets/` — lokalny staging artefaktów do wydania
- `PUBLISHING.md` — instrukcja przygotowania wydania na GitHubie

## Repo źródłowe

Kod źródłowy i proces budowania pakietu portable znajdują się w repo głównym DMP-ART https://github.com/gammaro85/DMP-ART .
Paczka jest budowana poleceniem `python build_portable.py`, a następnie publikowana tutaj jako asset release.
