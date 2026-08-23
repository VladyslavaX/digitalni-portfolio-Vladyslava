# Cvičení 6 – Testování portu
## Zadání
- Použijte telnetna port 80 (např. telnet www.eduxo.cz 80).
- Pokud není možné spojení, uveďte možné důvody (firewall, server offline, blokace portu).
---
## Řešení
Popis postupu řešení:
- Nejprve jsem ve Windows zapnula funkci Telnet Client (Ovládací panely → Programy → Zapnout/vypnout funkce).
- Spustila jsem příkazový řádek.
- Zadala jsem příkaz: telnet www.eduxo.cz 80
- Telnet se úspěšně připojil – zobrazila se prázdná obrazovka, což znamená navázané spojení (výhledala jsem).
- Odeslala jsem HTTP požadavek: GET / HTTP/1.1 Host: www.eduxo.cz (dvakrát enter).
- Server odpověděl kódem 301 Moved Permanently, takže port 80 funguje a server přesměrovává na HTTPS.
- Co fungovalo / nefungovalo:
  - Fungovalo připojení přes Telnet na port 80.
  - Fungovalo odeslání HTTP požadavku.
  - Nebylo potřeba řešit žádné chyby ani blokace.
- Výsledek:
  - Port 80 je otevřený, telnet se připojuje, server odpovídá a směruje klienta na HTTPS.
---
## Použité příkazy

`telnet www.eduxo.cz 80
GET / HTTP/1.1
Host: www.eduxo.cz`

---
## Výstupy / Testy
```bash
HTTP/1.1 301 Moved Permanently
Content-Type: application/binary
Cache-Control: no-cache, no-store, max-age=0, must-revalidate
Pragma: no-cache
Expires: Mon, 01 Jan 1990 00:00:00 GMT
Date: Mon, 01 Dec 2025 11:14:03 GMT
Location: https://www.eduxo.cz/
Server: ESF
Content-Length: 0
X-XSS-Protection: 0
X-Frame-Options: SAMEORIGIN
X-Content-Type-Options: nosniff
```
---
## Reflexe
- Naučila jsem se testovat dostupnost síťového portu pomocí telnetu.
- Vyzkoušela jsem ruční odeslání HTTP požadavku.
- Trochu matoucí bylo, že telnet po připojení ukazuje jen prázdnou obrazovku, ale je to normální chování (výhledala jsem).
