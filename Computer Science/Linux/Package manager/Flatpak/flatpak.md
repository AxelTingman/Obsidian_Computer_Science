#Operating_System/Linux/Packet_Manager 

## Problem
### Hittar inga applikationer
Om Flatpak inte hittar ngra applikationer så måst man lägga till rätt repository med följande kommando:
```
flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
```
[källa](https://itsfoss.com/no-remote-ref-found-flatpak/)