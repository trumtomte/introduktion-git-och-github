# Tips och tricks

> Här samlar vi lite allt möjligt

## Terminalen och Git

Skulle ni versionshantera via terminalen och något inte funkar som det ska kan
ni alltid ta en titt på [Oh Shit, Git!?!](https://ohshitgit.com/).

## Vår `.gitignore` ignorerar inte nya filer

Internt har `.gitignore` en egen cache över vad som inte ska versionshanteras. Redigerar vi denna filen kan det hända att den inte upptäcker våra ändringar (utan att gå in på varför). För att lösa detta behöver ni dock köra ett par kommandon i en terminal (det finns ännu inget stöd för detta i GitHub Desktop).

Nedan anger vi att filen `debug.log` inte ska spåras (dvs. lägger till den i vår `.gitignore`), sedan tömmer vi Gits cache för denna fil och gör en commit för vår ändring i `.gitignore`. Sedan kan vi fortsätta arbeta som vanligt.

```bash
$ echo debug.log >> .gitignore  
$ git rm --cached debug.log
$ git commit -m "Start ignoring debug.log"
```

Ibland kan det vara enklare att bara tömma hela Gits cache och sedan låta Git gå igenom alla filer igen så att allt stämmer.

```bash
$ git rm -r --cached .                 # The single dot is our root folder
$ git commit -am "Git cache cleared"
$ git push
```

## Unity

1. Var noga med att `.gitignore` filen ska placeras i er rotmapp (där ni har
   assets, Library, ProjectSettings osv.), för att den innehåller relativa
   sökvägar.

2. Arbeta **aldrig** i samma *Scene* samtidigt. Scenfilerna kan inte sammanfogas
   mellan *branches* vilket leder till att någons arbete kommer att skrivas
   över. Om det krävs att flera personer jobbar med samma scen samtidigt så gör
   först en kopia av scenen, sen görs respektive arbete i vars en kopia.
   Slutligen för den som inte jobbade med orginal scenen, samla alla ändringar i
   ett tomt objekt och gör en prefab av detta master-objektet, se till att detta
   objekt har en noll-transform. Efter att orginal scenen är klar med dess
   ändringar så kan prefaben av master-objektet sättas in där. Slutligen packa
   upp master-objekt prefaben och flytta ut dess direkta barn till sceen
   hierarkin.
