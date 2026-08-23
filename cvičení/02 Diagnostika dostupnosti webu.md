# Cvičení 2 –  Diagnostika dostupnosti webu
## Zadání
- Zjistěte IP adresu serveru.
- Ověřte dostupnost serveru.
- Sledujte cestu paketů.
- Napište krátkou zprávu s výsledky a možnými příčinami problému.
---
## Řešení
Popis postupu řešení:
- Otevřela jsem příkazový řádek.
- Pomocí příkazu nslookup www.eduxo.cz jsem zjistila IP adresu webu, fungovalo to, IP adresa se zobrazila.
- Příkazem ping www.eduxo.cz jsem ověřila dostupnost serveru, odpovídal, web byl tedy dostupný.
- Pomocí tracert www.eduxo.cz jsem sledovala cestu paketů, přenos se po několika krocích zastavil, objevily se tři hvězdičky a hláška o vypršení časového limitu.
## Použité příkazy
`nslookup`
`ping`
`tracert`

---
## Výstupy / Testy
```bash
Microsoft Windows [Version 10.0.26100.6899]
(c) Microsoft Corporation. Všechna práva vyhrazena.
C:\Users\vladi>nslookup www.eduxo.cz
Server:  czntp.vodafone.cz
Address:  2a00:11b4:4110::a
Non-authoritative answer:
Name:    ghs.googlehosted.com
Addresses:  2a00:1450:4014:800::2013
          142.251.38.147
Aliases:  www.eduxo.cz
C:\Users\vladi>ping www.eduxo.cz
Pinging ghs.googlehosted.com [2a00:1450:4014:800::2013] with 32 bytes of data:
Reply from 2a00:1450:4014:800::2013: time=18ms
Reply from 2a00:1450:4014:800::2013: time=19ms
Reply from 2a00:1450:4014:800::2013: time=15ms
Reply from 2a00:1450:4014:800::2013: time=16ms
Ping statistics for 2a00:1450:4014:800::2013:
    Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
Approximate round trip times in milli-seconds:
    Minimum = 15ms, Maximum = 19ms, Average = 17ms
C:\Users\vladi>tracert www.eduxo.cz
Tracing route to ghs.googlehosted.com [2a00:1450:4014:800::2013]
over a maximum of 30 hops:
  1     6 ms     4 ms     4 ms  2a02:8308:b106:7400:5667:51ff:fee8:9c7d
  2     *        *        *     Request timed out.
  3    17 ms    23 ms    18 ms  2a02:8300:9::1
  4     *        *        *     Request timed out.
  5     *        *        *     Request timed out.
  6    18 ms    19 ms    15 ms  2a00:11b0:2:29::1
  7    16 ms    18 ms    19 ms  2a00:11b0:2:29::2
  8    18 ms    17 ms    17 ms  2001:4860:0:1::982f
  9    16 ms    16 ms    15 ms  2001:4860:0:1::4e4d
 10    18 ms    17 ms    15 ms  lcprga-af-in-x13.1e100.net [2a00:1450:4014:800::2013]
Trace complete.
```
---
## Reflexe
- Naučila jsem se používat příkazy nslookup, ping a tracert.
- Potíže mi dělalo správně pochopit výsledky, hlavně u tracert.
- Příště bych více sledovala detaily ve výsledcích a zkusila test z jiné sítě.
