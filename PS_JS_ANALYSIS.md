# Analiza `ps.js`

`ps.js` nie korzysta z tej samej prostej warstwy RC4/Base64 co pozostałe pliki. Jest to samodzielny interpreter/VM, który przechowuje instrukcje w zakodowanych ciągach Base64 i wykonuje je przez własny zestaw opcode'ów.

W pliku wykryto 184 elementy w tablicy bytecode. Po prostym dekodowaniu Base64 widać m.in. nazwy API JavaScript, selektory DOM, teksty interfejsu i fragmenty kodu CSS, ale nie jest to jeszcze równoważne odzyskaniu oryginalnego kodu źródłowego.

Dla `ps.js` nie zmieniałem kodu wykonawczego. Dzięki temu paczka zachowuje jego oryginalne zachowanie. W pozostałych obfuskowanych plikach podmieniono wywołania wykrytych dekoderów na ich rzeczywiste wartości tekstowe.
