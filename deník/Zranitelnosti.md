# Zranitelnosti
## Typy zranitelnosti
- Podle hardware
  - dle vlhkosti
  - dle prašnosti
  - dle znečištění
- Podle software
  - resetování
  - audit
## Sítová rizika
- nedostatečná ochrana komunikační linky
- nedostatečné zabezpečení sítové architektury
## Personální rizika
- neadekvátní proces přijímání
- neadekvatní znalost bezpečnosti
## Lokační rizika
- okolí s původním rizikem 
- nespolehlivý zdroj energie
- organizační riziko
- nepravidelnost auditu
- chybějící kontinualní plan
- nedostateční zabezpečni
## Hodnocni zranitelnosti
- CERT/CC
  - numerické skore od 1 po 180, hodnotí faktory jako např. riziko infrastruktury a jaké podmínky jsou potřeba k zneužití zraniteknosti
- SANS
  - bere do úvahy existenci slabiny i ve výchozí konfiguraci u klienta či serverového systému
- MSPSS
  - od microsoft, snaží se odrážet realní dopad každé zranitelnosti a její náročnost na zneužití
- CVSS
  - otevřený rámec metrik hodnocení a adresování zranitelnosti
## Priciny výskytu
  - komplexita velké rozsáhlé systémy mají větší pravděpodobnost výskytu chyb
- Obeznamovot 
  - použivání běžného známého kodu, SW, OS, HW zvyšuje pravděpodobnost, že utočník zná nebo může najít způsob nebo nástroj na realizaci daného utoku
- Konektivita
  - zvyšené množství fyzických propojených portů nebo protokolů představuje další možnosti nežádoucícho přístupu do systému
## Sprava hesel
- Fundametalní chyby v OS
  - nekteré OS povoluje v základu všem programům a všem uživatelům kompletní přístup k počitači, tím pádem i virům a malwarům povolují spustit příkaz jako admin
- Prohlížení webových stránek
  - některé stránky obsahují spiwary a adwary, které se automatický nainstalují do PC a může pak posílat osobní infotmace 3. straně
- Softwarový BUG
  - programator nevědomě nechá v programu chybu
## Důslednky zranitrlnosti
- musíme:
  - inplementovat
  - předejít zneužití 
  - detekovat a zabranit utoku
  - najít a dopadnout utočniky
## Sítové utoky
- Pasivní – utok s cílem zjístit a využit informace ze systému bez zásahu do jeho prostředků
- Aktivní – pokus o změnu, poškození nebo omezení provozu, případně zcizit či upravit data
