#Application 
En applikation för att installera .deb-filer på Archsystem.

## Installation
`yay -S debtap`

## Konvertera fil
1. Ändra sökvägen till mappen som filen finns. Exempel: `cd ~/Downloads`
2. Konverera filem med följande kommando: `debtap YOURFILE.deb`
   Debtap kommer att skapa en fil som heter `YOURFILE.zst`.
3. För att installera .zst-filen; kör: `sudo pacman -U YOURFILE.zst`