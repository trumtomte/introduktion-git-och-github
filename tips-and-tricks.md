# Tips och tricks

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
