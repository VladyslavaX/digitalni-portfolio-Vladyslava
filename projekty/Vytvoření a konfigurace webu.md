# Dokumentace Webu 
datum 02.02.2026
- Tato dokumentace popisuje náš postup vytvoření a nastavení webu, který běží v kontejneru. Součástí je in nasazení WordPressu, zákldaní nastavneí serveru a využití Cloudflaru.
## Začátek projektu
V této fázi jsme připravili prostředí pro web.
### Co jsme udělali:
  + **Vytvoření kontejneru**
    Kontrejner slouží jako oddělené prostředí, ve ktrém běží celý web. Kvůli tomu je systém přehlednějsí, bezpečnější a lépe se spravuje.
  + **Nastvaneí kontejneru**
    Kontejner jsme nastavili tak, aby byl připravený na instalaci WordPressu.
## Nastavení sítě a WordPressu
V této části se kontejner připravil pro provoz webu.
### Postup:
**1. Nastavení síťových parametrů**
  + **DNS**, aby doména správně směrovala na sever
  + **IP adresa**, aby byl server v síti dostupný
  + **Brána**, aby mohl server komunikovat s internetem
**2. Přihlášení do kontejneru**
  + Ověření, že se do kontejneru můžeme přihlásit a spravovat ho
**3. Instalace a nastavení WordPressu**
  + Instalace WordPressu
  + Nastavení přihlašovacích údajů
  + Ověření, že se jde přihlásit
## Cloudflare
 Pro zpřístupnění serveru z privátní sítě do veřejného internetu jsme použili **Cloudflare**
   + Server běží v privátní síti a není přímo dostupný z internetu
   + Přes tento tunel jsou vytvořeny další podtunely, které zajišťují provoz na konkrétní kontejnery
### Postup nastavení
**1. Vytvoření hlavního Cloudflare tunelu**
  + Použili jsme **template (šablona)** pro Cloudflare tunel
  + Pomocí šablony byl vytvořen **hlavní tunel**, který zajišťuje spojení mezi privátní a veřejnou sítí
**2. Vytvoření podtunelů (napojení na kontejnery)**
Po vytvoření hlavního tunelu byly nastaveny další **podtunely**, které směřují na jednotlivé kontejnery.
  + Pro každý kontejner byl vytvořen **samostatný podtunel**
  + Každý podtunel:
      + je napojený na hlavní Cloudflare tunel
      + směřuje provoz na konkrétní kontejner
  + Pomocí podtunelů je možné:
      + oddělit jednoltivé služby
      + jednoduše spravovoat, který kontejner je dostupný z internetu
Celkem byly vytvořeny **tři podtunely** a každý byl připojen k jinému kontejneru.
## Parametry serveru
Tato část popisuje parametry serveru, na kterém běží kontejnery a Cloudflare tunely. 
### Použité parametry serveru:
  + **Operační paměť (RAM)**: 1 GiB
  + **Swap**: 512 miB
  + **Procesor (CPU)**: 1 jádro
### K čemu tyto parametry slouží:
  + **RAM**
    Slouží pro běh kontejnerů, WordPressu a Cloudflare tunelů. Tato velikost paměti je dostačující pro menší web.
  + **Swap**
    Swap funguje jako záložní paměť v případě, že dojde RAM. Pomáhá zabránit pádům systému při krátkodobém zvýšení zátěže.
  + **CPU**
    Zajišťuje běh systému a obsluhu webu. 
## Závěr
Během projektu se nám podařilo nastavit server s kontejnery, nainstalovat WordPress a zpřístupnit web z privátní sítě do veřejné pomocí Cloudflare tunelů. Měli jsme problémy s instalací WordPressu přes příkazy, takže jsme nakonec použili template. Ta sice instalaci zjednodušila, ale zpočátku byla špatně nakonfigurovaná (web nás přesměrovával na špatnou doménu). Po úpravě nastavení domény, tunelů a zabezpečení se podařilo vše zprovoznit.
