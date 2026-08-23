# Referenční sítové modely 
- Vzor / šablona, podle které se navrhují a vysvětlují skutečné systémy.
- Reference - odkaz nebo doporučení.
  - Výhoda - pokud se dodržují pravidla, můžeme propojit jakékoliv zařízení s jakýmkoliv zařízením.
  - Učel - popis principu komunikace.
## ISO/OSI 
- Starší, vychází z telefonní komunikace.
- ISO - název organizace.
- OSI – 7 vrstev.
  - 7 aplikační
  - 6 prezentační
  - 5 relační  
  - 4 transportní 
  - 3 sitová
  - 2 linková 
  - 1 fyzická 
## TCP/IP 
- Praktické protokoly (konkretní software např. HTTP (HyperText Transfer Protocol) je síťový protokol, který slouží k přenosu webových stránek a dat mezi klientem a serverem.).
- TCP - 4 vrstvy.
  - 4 aplikační (OSI - 7,6)
  - 3 transportní (rychlost, obsah atd.)
  - 2 sítová vrstva (adresace, směrování) 
  - 1 linková (rozhraní mezi fyzickou (1, 0, kabely) a linkovou vrstvou (připravuje to fyzické pro to logické a naopak))
- Komunikace probíhá tak, že vyšší vrstva využívá protokoly nižší a nižší poskytuje služby vyšší - zapouzdření.
- V 1. vrstvě vznikají data, postupně propadávají dolů, nižší vrstva pak přidá svojí hlavičku atd., poslední pak přidá i zápatí.
- Celkově data v jedné vrstvě se jmenují PDU segmenty.
## Vrstvy
- Na každé vrstvě vznikají PDU:
  - Datová jednotka používaná pro přenos informací v určité vrstvě síťového modelu.
    - Aplikační vrstva - data.
    - Transportní vrstva - segmenty.  
    - Sítová vrstva - pakety.
    - Vrstva sítového přístupu - rámce (+ zápatí - hledání chyb na fyzické urovni).
- V hlavičce se nachazi kdo kam posíla
## CRC (Cyclic Redundancy Check)
- je kontrolní mechanismus pro odhalení chyb při přenosu dat.
- Jak CRC funguje:
  - Odesílatel spočítá CRC kód z dat a připojí ho k nim.
  - Příjemce znovu spočítá CRC z přijatých dat.
  - Pokud se hodnoty shodují → data jsou v pořádku.
  - Pokud ne → došlo k chybě.
## Způsob odesílání dat
- Broadcast → ARP dotaz: „Kdo má IP 192.168.1.1?“ (jeden → všem v síti).
- Unicast → otevření webu (PC ↔ server, jeden → jednomu ).
- Multicast → IPTV stream (jeden → vybrané skupině).
- Anycast → dotaz na DNS (jeden → nejbližšímu zařízení).
## Server
- Je počítač nebo program, který poskytuje služby jiným počítačům (klientům) v síti.
- Server = poskytovatel služeb, klient = ten, kdo je využívá.

