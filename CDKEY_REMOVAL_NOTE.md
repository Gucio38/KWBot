# CD-Key verification removal

W tej kopii projektu usunięto mechanizm `checkAccessAndRun()` z `ps1.js` i pozostawiono bezpośrednie uruchamianie właściwego kodu.

Przed zmianą funkcja:
- pobierała zewnętrzną listę dostępu,
- obliczała SHA-256 identyfikatora z `GAME`,
- uruchamiała główny kod tylko dla identyfikatorów znajdujących się na liście.

Po zmianie główny kod uruchamia się bezpośrednio, bez zdalnej weryfikacji.

`keygen.js` i `keys.json` pozostawiono bez zmian, ponieważ są narzędziem generatora kluczy, a nie elementem wykonywania bota.

Dodatkowo usunięto nieużywany po zmianie helper SHA-256 oraz konstruktor `ACCESS_URL`.
