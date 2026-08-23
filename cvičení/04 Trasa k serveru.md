# Cvičení 4 – Trasa k serveru
## Zadání
- Spusťte trasování.
- Poznamenejte si, kolik „hopů“ paketům trvá dosáhnout cíle.
- Zhodnoťte, zda je trasa efektivní nebo obsahuje problémy.
---
## Řešení
Popis postupu řešení:
- Otevřela jsem příkazový řádek a spustila příkaz tracert www.google.com.
- Poznamenala jsem si počet hopů – celkem 10.
- Výsledky:
  - Některé hopy odpovídaly rychle (např. 4–18 ms).
  - Některé hopy byly hvězdičky nebo timeouty, což znamená, že routery neodpovídaly na trasování.
- Závěr:
  - Trasa byla většinou efektivní, web Google je dostupný, ale některé hopy neodesílaly odpovědi.
---
## Použité příkazy

`tracert`

---
## Výstupy / Testy
```bash
Microsoft Windows [Version 10.0.26100.6899]
(c) Microsoft Corporation. Všechna práva vyhrazena.
C:\Users\vladi>tracert www.google.com
Tracing route to www.google.com [2a00:1450:4014:80a::2004]
over a maximum of 30 hops:
  1     4 ms     4 ms     4 ms  2a02:8308:b106:7400:5667:51ff:fee8:9c7d
  2     *        *        *     Request timed out.
  3    13 ms    14 ms    13 ms  2a02:8300:9::1
  4     *        *        *     Request timed out.
  5     *        *        *     Request timed out.
  6    18 ms    16 ms    16 ms  2a00:11b0:2:29::1
  7    17 ms    15 ms    15 ms  2a00:11b0:2:29::2
  8    16 ms    14 ms    15 ms  2001:4860:0:1::9829
  9    16 ms    14 ms    14 ms  2001:4860:0:1::389b
 10    16 ms    16 ms    13 ms  prg03s10-in-x04.1e100.net [2a00:1450:4014:80a::2004]
Trace complete.
C:\Users\vladi>
```
---
## Reflexe
- Naučila jsem se používat příkaz tracert a sledovat cestu paketů k serveru.
- Pochopila jsem, co znamenají jednotlivé časy a hvězdičky u hopů.
- Naučila jsem se vyhodnotit, zda je trasa efektivní nebo obsahuje problémy.
