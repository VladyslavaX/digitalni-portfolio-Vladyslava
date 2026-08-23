# Cvičení 3 – Kontrola lokální sítě
## Zadání
- Zjistěte svou IP adresu a masku.
- Ověřte dostupnost routeru.
- Zkontrolujte ARP tabulku.
- Shrňte, zda je problém u vás nebo u poskytovatele.
---
## Řešení
Popis postupu řešení:
- Zjistila jsem IP adresu, masku a gateway pomocí ipconfig, poté jsem ověřil dostupnost routeru příkazem ping a zkontrolovala jsem ARP tabulku pomocí arp -a.
- Na základě výsledků jsem vyhodnotila, že IP konfigurace je správná, ale router není dosažitelný, což ukazuje na problém mimo můj počítač.
---
## Použité příkazy
```bash
ipconfig/ifconfig
ping <IP routeru>
arp -a
```
---
## Výstupy / Testy
Ukázkový výstup ipconfig
```bash
 Connection-specific DNS Suffix  . :
   IPv6 Address. . . . . . . . . . . : fdfd::1a4c:c67a
   Link-local IPv6 Address . . . . . : fe80::f5a:dd2d:e45d:1e24%10
   IPv4 Address. . . . . . . . . . . : 26.76.198.122
   Subnet Mask . . . . . . . . . . . : 255.0.0.0
   Default Gateway . . . . . . . . . : 26.0.0.1
```
Ukázkový výstup ping 26.0.0.1
```bash
Ping statistics for 26.0.0.1:
    Packets: Sent = 4, Received = 0, Lost = 4 (100% loss)
```
Ukázkový výstup 
```bash
Interface: 26.76.198.122 --- 0xa
  Internet Address      Physical Address      Type
  26.0.0.1              02-00-00-00-51-00     dynamic
  26.255.255.255        ff-ff-ff-ff-ff-ff     static
  224.0.0.22            01-00-5e-00-00-16     static
  224.0.0.251           01-00-5e-00-00-fb     static
  224.0.0.252           01-00-5e-00-00-fc     static
  239.255.255.250       01-00-5e-7f-ff-fa     static

Interface: 172.29.7.245 --- 0x13
  Internet Address      Physical Address      Type
  172.29.254.254        c4-c6-03-f7-63-e7     dynamic
  224.0.0.22            01-00-5e-00-00-16     static
  224.0.0.251           01-00-5e-00-00-fb     static
  224.0.0.252           01-00-5e-00-00-fc     static
  224.0.0.253           01-00-5e-00-00-fd     static
  239.255.255.250       01-00-5e-7f-ff-fa     static
  255.255.255.255       ff-ff-ff-ff-ff-ff     static

```

---
## Reflexe
- Diagnostika proběhla bez komplikací a jednotlivé příkazy poskytly jasné informace.
- Zjištění, že ARP funguje, ale ping ne, mi pomohlo určit, že chyba je pravděpodobně u poskytovatele nebo routeru.
