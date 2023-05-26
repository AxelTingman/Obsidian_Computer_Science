#Kurs/Databasmetodik 

Klassdiagram | Relationsschema
:---|:---
Klass | Tabell
Envärd attribut | Kolumn
Flervärd attribut | Tabelll + främmande nyckel
0/1:1 association | Främmande nyckel/tabell
0/1:M association | Främmande nyckel/tabell
M:M | Tabell + främmande nycklar
Generalisering | Främmande nyckel/tabell
Regler | Nyckel, främmande nyckel
Regler | Domändef, triggers, etc.


# Översättningsprinciper
- Om multipliciteten på ett attribut är ``1..1`` blir det en kolumn i tabellen.
![[attribut-till-kolumn.PNG]]
- Om multipliviteten på ett attribut är ``0..1`` så blir [[Reifirering|reifireras]] behövs en relationsklass.
- 

Alla klassattribut som har 1 som maxvärde (envärda attribut) blir en kolumn i ett relationsschema, förutom om minvärdet är 0. Anledningen är att man vill undvika nullvärden i tabellen.

Varje flervärt attribut ger upphov till en ny tabell.

Primärnyckeln i den nya tabellen är sammansatt av det flervärda attributet tillsammans med den gamla primärnyckel-kolumnen.

Den nya tabellen har en främmande nyckel-kolumn som refererar till ... (se föreläsning)

