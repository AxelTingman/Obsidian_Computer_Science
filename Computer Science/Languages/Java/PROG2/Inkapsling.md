Genom att dölja implementationsdetaljer från användaren av en [[Klass|klass]] krävs abstraktion.

- Skiljer den interna vyn (instansvariabler) från den externa vyn.
- "Skyddar" objektets data


![[Screenshot from 2022-03-22 12-39-30.png]]


#### Fördelar med inkapsling
- Abstraktion mellan objekt och användare.
- Skyddar intern data från att användas utan "lov"
- Vi kan ändra implementation men ha kvar den externa vyn
- Vi kan kontrollera att ett objekt uppfyller vissa villkor. Tex: en `TextBox` får ha max 142 tecken.