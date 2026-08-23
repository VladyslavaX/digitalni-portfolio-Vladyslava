# Aktualizace systému (eduxo_dmp)
## Postup aktualizace
1. Otevřit terminál.
2. Spustit aktualizaci systému:
 `sudo apt update`
    - Načte seznam dostupných aktualizací balíčků.
3. Proveď samotný upgrade:
`sudo apt upgrade`
    - Nainstaluje dostupné aktualizace.
## Vyčištění systému
- Po aktualizaci je vhodné odstranit nepotřebné balíčky:
`sudo apt autoremove `
    - Odstraní staré závislosti a uvolní místo (doporučeno dělat pravidelně).
## Odhlášení z terminálu
- Ctrl + D 
  - Ukončí aktuální shell / odhlásí uživatele z relace
