# Cvičení 5 – Ověření DNS záznamů
## Zadání
- Používejte nslookup nebo dig.
- Ověřte, zda se IP adresy shodují s očekávanými.
- Zjistěte informace o tom, k čemu slouží DNS.
---
## Řešení
Popis postupu řešení:
- Otevřela jsem příkazový řádek a zadala nslookup www.seznam.cz.
- Zjistila jsem IP adresy webu, jedna se shodovala s očekávanou, další jsou jen jiné servery stejného webu.
- Očekávanou IP adresu jsem našla na internetu, ve veřejně dostupných informacích o seznam.cz.
- Ověřila jsem, že DNS funguje, protože název webu se přeložil na IP adresu.
---
## Použité příkazy
`nslookup`

---
## Výstupy / Testy
```bash
Microsoft Windows [Version 10.0.26100.6899]
(c) Microsoft Corporation. Všechna práva vyhrazena.
C:\Users\vladi>nslookup www.seznam.cz
Server:  czntp.vodafone.cz
Address:  2a00:11b4:4110::a
Non-authoritative answer:
Name:    www.seznam.cz
Addresses:  2a02:598:2::1222
          2a02:598:a::79:222
          77.75.79.222
          77.75.77.222
C:\Users\vladi>
```
---
## Reflexe
- Naučila jsem se používat nslookup, abych zjistila IP adresu webu.
- Pochopila jsem, že web může mít více IP adres kvůli rozdělení návštěvnosti.
- Naučila jsem se zkontrolovat, jestli DNS správně překládá název webu na IP.
