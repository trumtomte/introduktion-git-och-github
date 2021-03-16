# Tips och tricks

## Unity

1. Var noggran var .gitignore filen placeras eftersom den har relativa sökvägar
   i sig. Standard ignore filen ska ligga på samma nivå som assets, Library,
   ProjectSettings osv. Detta kommer på workshopen.

2. Arbeta **aldrig** i samma sceen samtidigt. Scenfilerna kan inte sammanfogas
   mellan grenar vilket leder till att någons arbete kommer skrivas över.  Om
   det krävs att flera personer jobbar med samma sceen samtidigt.  Gör först en
   kopia av sceenen, sen gör respektive arbete i vars en kopia.  Slutligen för
   den som inte jobbade med orginal sceenen, samla alla ändringar i ett tomt
   objekt och gör en prefab av detta master-objektet, se till att detta objekt
   har en noll-transform.  Efter att orginal scenen är klar med dess ändringar
   så kan prefaben av master-objektet sättas in där.  Slutligen packa upp
   master-objekt prefaben och flytta ut dess direkta barn till sceen hierarkin.
