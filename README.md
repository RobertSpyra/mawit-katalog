# MAWIT – katalog projektów: kanał aktualizacji wtyczki WordPressa

Stąd wtyczka **MAWIT – katalog projektów** na [mawit.com.pl](https://mawit.com.pl/projekty/) pobiera swoje nowe
wersje. Katalog projektów domów (wizualizacje, modele 3D) jedzie w środku wtyczki, a wtyczka publikuje go pod adresem
`/projekty/`.

- **`wersja.json`** — numer najnowszej wersji. WordPress zagląda tu dwa razy na dobę (nagłówek wtyczki
  `Update URI: https://github.com/RobertSpyra/mawit-katalog`), a gdy wersja jest nowsza od zainstalowanej, sam pobiera
  paczkę i ją instaluje; katalog na stronie podmienia się w tle. Po każdym wydaniu autor wysyła też stronie sygnał
  (`POST /?rest_route=/mawit-katalog/v1/odswiez`) — strona instaluje wtedy nową wersję od razu, bez czekania na
  zadania WordPressa w tle.
- **[Wydania](https://github.com/RobertSpyra/mawit-katalog/releases)** — paczka `mawit-katalog.zip` każdej wersji
  (`v<wersja>`). Wtyczka bierze paczkę wyłącznie spod
  `https://github.com/RobertSpyra/mawit-katalog/releases/download/v<wersja>/mawit-katalog.zip`.

## Pierwsza instalacja

Panel WordPressa → **Wtyczki → Dodaj nową → Wyślij wtyczkę na serwer** → `mawit-katalog.zip` z
[najnowszego wydania](https://github.com/RobertSpyra/mawit-katalog/releases/latest) → **Zainstaluj teraz** →
**Włącz**. Gdy jest już zainstalowana starsza wersja (bez samoaktualizacji): **Zastąp bieżącą wersję przesłaną**.
Kolejne wersje przychodzą same.

Bez czekania: **Kokpit → Aktualizacje → Sprawdź ponownie**, potem zaktualizuj wtyczkę.

Wyłączenie wtyczki zdejmuje katalog ze strony, włączenie publikuje go ponownie.

Paczki składa i wydaje autor wtyczki — tu niczego nie wgrywaj ręcznie.
