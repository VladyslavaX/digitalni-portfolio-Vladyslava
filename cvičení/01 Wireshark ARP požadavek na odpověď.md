# Cvičení 1 – ARP požadavek na odpověď
## Zadání
- Otevřete v programu Wireshark soubor smallFlows.pcap.
- Použijte filtr arp.
- Sledujte, jak počítač zjišťuje MAC adresu cílového zařízení.
- Identifikujte všechny hosty (IP, MAC, ....).
- Popište rozdíl mezi ARP request a ARP reply.
---
## Řešení
Popis postupu řešení:
- Otevřela jsem soubor v Wiresharku, použila filtr arp a prohlédla ARP requesty a reply, abych našla IP a MAC adresy hostů.
- Fungovalo filtrování a čtení ARP rámců, nefungovalo rychlé nalezení správných paketů, protože jsem je musela chvíli hledat.
- Identifikace hostů
  - Odesílatel (Sender):
    - IP: 172.16.0.1
    - MAC: 00:1e:68:51:4f:a9
  - Cíl (Target):
    - IP: 172.16.255.1
    - MAC: 00:1a:8c:10:ad:30
- Rozdíl mezi ARP request a ARP reply
  - ARP Request: dotaz, kdo má danou MAC adresu s danou IP.
  - ARP Reply: odpověď se skutečnou MAC adresou.
---
## Použité příkazy
`arp`

---
## Výstupy / Testy
<img width="1917" height="1079" alt="image" src="https://github.com/user-attachments/assets/ca76aabe-3b59-4dbf-b909-e3097b5b403f" />
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/ddb8be0f-7f87-4a59-a10a-f1c8004c9766" />
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/7c78077b-fa6d-4832-a1bc-6b076e16e73a" />

---
## Reflexe
- Pochopila jsem, jak ARP funguje a jak zařízení v síti zjišťují MAC adresy.
- Bylo složoté najít správné rámce ve Wiresharku a pochopit strukturu ARP hlavičky.
- Příště bych si lépe propojila teorii s praxí a rovnou si zapisovala všechny hosty při analýze.
