# Odkodowana kopia projektu

Ta kopia została przygotowana z zachowaniem oryginalnego projektu. Odkodowano wykryte warstwy obfuskacji tekstowej w:

- `ddd.js` — 2 dekodery, 334 podmienione wywołania
- `load.js` — 1 dekoder, 270 podmienionych wywołań
- `dupablada123.js` — 1 dekoder, 576 podmienionych wywołań
- `ps1.js` — 1 dekoder, 299 podmienionych wywołań
- `connectionManager.js` — 1 dekoder, 46 podmienionych wywołań

Odkodowane pliki zachowują również własne funkcje dekoderów/aliasów, żeby maksymalnie ograniczyć ryzyko zmiany zachowania programu. Wszystkie pięć plików przechodzi `node --check`.

`ps.js` używa osobnej, bardziej złożonej maszyny wirtualnej z bytecode'em. Nie zastępowałem jej kodu pozornym „dekoderem”; szczegóły są w `PS_JS_ANALYSIS.md`.

`keygen.js` i `keys.json` nie były modyfikowane. W analizowanych głównych plikach nie znaleziono bezpośrednich odwołań do `keygen.js`, `keys.json` ani funkcji `verifyKeyData`. Sam `keygen.js` zawiera generator i weryfikator CD-Key jako osobny moduł.

Raport techniczny znajduje się w `DEOBFUSCATION_REPORT.json`.
