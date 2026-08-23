# Cvičení 2 – Ping (ICMP) analýza
## Zadání
- Otevřete v programu Wireshark soubor smallFlows.pcap.
- Použijte filtr icmp.
- Sledujte požadavek a odpověď (Echo Request / Echo Reply).
- Zaznamenejte časy odezvy paketů.
- Jaké hodnoty TTL jsou u paketů nastaveny?
- Popište co je TTL a k čemu slouží.
---
## Řešení
Popis postupu řešení:
- Otevřela jsem Wireshark a v něm soubor smallFlows.pcap.
- Použila jsem filtr icmp.
- Rozkliknutím konkretního reply zjístim čas odezvy paketů, což je cca 115 ms.
- Čas odezvy paketů, ping nebo latence - doba, kterou trvá, než se datový balíček (malý kousek informace) odešle z mého zařízení na server a potvrdím jeho přijetí (nebo se vrátím).
- TTL u reply 32, u request 50.
- TTL (Time to Live) - je údaj, který v systému DNS určuje, jak dlouho si mohou DNS servery nebo koncová zařízení (například počítače, routery nebo prohlížeče) uchovávat informace do méně v mezipaměti (cache), než si znovu uvěřit aktuální stav u autoritativního DNS serveru.
---
## Použité příkazy

`icmp`

---
## Výstupy / Testy
<img width="1165" height="863" alt="image" src="https://github.com/user-attachments/assets/2f4ddbf0-3def-4a5a-9d8e-81dc64403e49" />

---
## Reflexe
- Vím co je TTL a k čemu slouží.
- Myslela jsem si, že čas odezvy budu muset počítat ručně, ale rozkliknutím ICMP viděla jsem response time.
