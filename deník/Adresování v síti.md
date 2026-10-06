# Adresování v síti
- nesmíme vynechat na žádné úrovní
## MAC adresa
- pouze v lokální síti
- 48bitová (6 bajtů, 12 hex čísel), přírazaná výrobcem = první část (3) označuje výrobce, druhá část konkrétní zařízení
- nemůže být unikátní ve světě, ale musí být aspon v nějaké oblasti
### Typ doručení
- Unicast - konkrétní adresa - jedno zařízení
- Broadcast - FF-FF-FF-FF-FF-FF - všechna zařízení v LAN
- Multicast - 01-00-SE-xx-xx-xx - skupina zařízení
### ARP
- na lokální síti, 2. vrstva
- překládá IP adresu na MAC adresu
- bez ARP by zařízení neznalo fyz. adresu sítě
- ARP Request (broadcast), ARP Rrply (unicast)
## Adresace IPv4
- 4 oktety
- od 0 do 225
- sítová část a hostitelská (konkrétní zařízení), hranice určuje maska
- může být v binární podobě
### Maska podsítě a CIDR notace
- Jedničky - sít, nuly - hosté
### Typy IP adres
- sítová adresa - 1. adresa - identifikuje sit
- broadcast - poslední adresa - pro broadcastové vysílání
  - 1-126 /8
  - 128-191 /16
  - 192-223 / 24
  - 127.0.0.1 - loopback (já)
  - 0.0.0.0 - zástupná adresa (jakákoliv adresa, všechny)
  - 169.254.x.x - APIPA (bez DHCP)
## Subneting
