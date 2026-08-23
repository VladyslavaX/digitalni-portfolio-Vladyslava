# Cvičení 1 – Zjištění IP adresy
## Zadání
- Zjistěte, jakou IP adresu, masku podsítě a výchozí bránu má váš počitač.
---
## Řešení
Popis postupu řešení:
- Otevřít příkazový řádek.
- Vložit ipconfig/all.
- Výsledek: IPv4 Address. . . . . . . . . . . : 192.168.56.1
---

## Použité příkazy

`ipconfig/all`

---
## Výstupy / Testy
```
Microsoft Windows [Version 10.0.26100.2314]
(c) Microsoft Corporation. Všechna práva vyhrazena.
C:\Users\CL1-06>ipconfig/all

Windows IP Configuration

   Host Name . . . . . . . . . . . . : VDI11-CL1020
   Primary Dns Suffix  . . . . . . . : jcekb.cz
   Node Type . . . . . . . . . . . . : Hybrid
   IP Routing Enabled. . . . . . . . : No
   WINS Proxy Enabled. . . . . . . . : No
   DNS Suffix Search List. . . . . . : jcekb.cz

Ethernet adapter Ethernet0:

   Connection-specific DNS Suffix  . : jcekb.cz
   Description . . . . . . . . . . . : vmxnet3 Ethernet Adapter
   Physical Address. . . . . . . . . : 00-50-56-B9-84-9E
   DHCP Enabled. . . . . . . . . . . : Yes
   Autoconfiguration Enabled . . . . : Yes
   IPv4 Address. . . . . . . . . . . : 172.25.105.24(Preferred)
   Subnet Mask . . . . . . . . . . . : 255.255.255.0
   Lease Obtained. . . . . . . . . . : středa 24. září 2025 16:20:48
   Lease Expires . . . . . . . . . . : pátek 26. září 2025 10:20:48
   Default Gateway . . . . . . . . . : 172.25.105.254
   DHCP Server . . . . . . . . . . . : 172.30.104.1
   DNS Servers . . . . . . . . . . . : 172.30.104.2
                                       172.30.104.1
   NetBIOS over Tcpip. . . . . . . . : Enabled

Ethernet adapter Ethernet:

   Connection-specific DNS Suffix  . :
   Description . . . . . . . . . . . : VirtualBox Host-Only Ethernet Adapter
   Physical Address. . . . . . . . . : 0A-00-27-00-00-05
   DHCP Enabled. . . . . . . . . . . : No
   Autoconfiguration Enabled . . . . : Yes
   IPv4 Address. . . . . . . . . . . : 192.168.56.1(Preferred)
   Subnet Mask . . . . . . . . . . . : 255.255.255.0
   Default Gateway . . . . . . . . . :
   NetBIOS over Tcpip. . . . . . . . : Enabled
```

---
## Reflexe
- Umím zjistit IP adresu počitače.
