# Del 2: Börja versionshantera

> Del 2 av 3 i guiden [Arbeta med GitHub Desktop](working-with-github-desktop.md)

I denna del ska ni börja med att **en** person redigerar filen `.gitignore`.
Detta moment är **väldigt viktigt** att ni gör först. Filen `.gitignore`
innehåller nämligen sökvägar till alla de filer som ni inte vill ska
versionshanteras. Det kan vara allt från filer ert operativsystem skapar till de
filer som er textredigerare konstant redigerar i bakgrunden, t.ex. för era
inställningar. Ni vill ju bara versionshantera filer som har med er kodbas att
göra (dvs. källkoden).

När ovanstående är på plats ska ni som grupp pröva på att versionshantera. Ni
kommer alla att skapa varsin *branch*, så att alla arbetar i sin egen version av
kodbasen. Efter ni gjort lite småändringar (skapa någon fil och sedan redigera
den) ska ni testa att ändra till någon annan projektmedlems branch för att se
vad dom har gjort. Slutligen kommer ni att *merga* era ändringar till `main`
(dvs. huvudversionen) och sedan radera era - nu utdaterade - branches.

I mina videos använder jag textredigeraren [Visual Studio
Code](https://code.visualstudio.com/) för att skapa och redigera filer. Ni kan
använda er av vilken textredigerare ni vill.

## Steg 1: Redigera `.gitignore`

❕Detta görs av **en** projektmedlem.

Använd tjänsten [gitignore.io](https://www.toptal.com/developers/gitignore) för
att generera innehållet till er `.gitignore` fil. Här har ni möjlighet att fylla
i saker som operativsystem, programmeringsspråk, textredigerare och så vidare.
Till exempel kanske ett Java-projekt hade fyllt i "MacOS, Windows, Java,
JetBrains eller IntelliJ, Maven". Det beror så klart på er grupp. Kopiera nu den
text som genererades in till er `.gitignore`.

Nu ska ni göra er första *commit* (version), vilket innebär är att kommentera (ett
kort meddelande) vad ni precis gjort (och vad ändringen innebar). Därefter ska ni
publicera (*push*) detta till GitHub så alla andra i gruppen kan hämta dessa
ändringar (*fetch* och *pull*).

**Innan** ni går vidare till Steg 2 är det **viktigt** att alla i gruppen nu kan
se att deras `.gitignore` innehåller dessa nya ändringar.

*Är ni osäkra på om er `.gitignore` innehåller vettiga saker så fråga!*

[Skärminspelning: redigera gitignore](assets/V04-update-gitignore.mp4)

## Steg 2: Versionshantera (omgång 1)

❕Detta görs av **alla** projektmedlemar.

I detta steg kommer ni få pröva på den arbetsprocess som ni sedan framöver
kommer använda er av kontinuerligt under projektet. Kort så innebär det att
varje gång någon ska programmera något (skapa en ny klass, redigera en funktion,
osv.) så ska ni börja med att skapa en *branch*, göra era ändringar, sedan
*commita* dessa och slutligen *merga* er kod till `main`. Detta är i huvudsak en
rutin ni behöver vänja er vid - som dessutom ses som en viktig kompetens att ha
i industrin.

Det är **viktigt** att ni nu följer instruktionerna noga (låt bli att trycka på
den fina blåa knappen i GitHub Desktop om jag inte säger åt er att göra det).
Varje projektmedlem ska:

1. skapa en egen *branch* (valfritt namn, i framtiden **ska namnet vara något vettigt**)
   - tryck på den fina blåa knappen där det står "Publish branch"
2. skapa en fil och döp den till `förnamn.txt` (men med ert eget förnamn)
   - gör nu en *commit* med ett meddelande som berättar vad du precis gjorde
3. lägg till lite text i filen ni precis skapade (det behöver inte vara något speciellt)
   - gör nu ännu en *commit*
4. nu kan ni trycka på den fina blåa knappen där det står "Push origin"
5. **PAUS:** invänta nu så att alla andra har hunnit göra detta
6. i den övre menyn finner ni knappen "Current Branch", välj nu någon annan
   projektmedlems *branch* och se så att ni kan se deras fil och innehåll
   (**observera** att du nu inte ser din egen fil) 
7. välj nu *branch* `main`
   - klicka på samma knapp ("Current Branch") en gång till och längst ner finner
     ni knappen "Choose a branch to merge into **main**", klicka på den och välj
     sedan er egen *branch* och slutligen klicka på "Commit [...]"
8. **PAUS:** invänta nu så att alla andra hunnit göra detta
9. i den övre menyn finner ni knappen "Fetch origin", klicka på den
   - nu bör ni kunna se alla andras filer och deras innehåll
8. färdig!
   - det är dock vanligt att när vi *mergat* våra ändringar till `main` så kan
     vi städa upp våra gamla *branches*, klicka på "Current Branch" igen,
     högerklicka sedan på er *branch* och välj "Delete" (får ni frågan om att
     radera från er *remote* så bocka i "Yes")

[Skärminspelning: versionshantera](assets/V05-how-to-version-control.mp4)

[Skärminspelning: radera en branch](assets/V06-delete-a-branch.mp4)

### Tips

1. Innan ni skapar en ny *branch*, klicka på "Fetch origin" (och sedan *Pull*),
   så att ni har de senaste ändringarna.
2. Om det finns nya ändringar i `main` som ni kan dra nytta av i er egen
   *branch* kan ni givetvis göra en *merge* från `main` till er egen *branch*
   också.

## Steg 3: Kom igång med er egen källkod

❕Detta görs av **en** projektmedlem (den med er mest aktuella kodbas).

Nu vill ni säkert påbörja ert riktiga arbete igen. Utse en person som raderar
alla dessa onödiga filer ni precis skapat. Gör en *commit* av detta och *pusha*
det till `main`. Sedan ska alla kunna *fetcha* (och *pull*) för att se att det
faktiskt fungerade.

Nu kan ni kopiera in hela er kodbas i ert repository. **Observera** dock att ni
inte ska klistra in en mapp, utan mappens innehåll så att ert repository är den
sk. "rotmappen". Gör en *commit* av detta och *pusha* till `main`. Sedan ska
alla kunna *fetcha* för att se att det faktiskt fungerade.

**Observera** att ni från och med nu arbetar utifrån er versionshanterade mapp
(dvs. öppnar den i er textredigerare/IDE).

## Steg 4: Versionshantera (omgång 2)

❕Detta görs av **alla** projektmedlemar.

I detta steg ska ni, i princip, göra samma sak som ni gjorde i Steg 2. Men,
innan ni börjar göra detta måste ni först bestämma er för vem som ska göra vad.
Till exempel kanske ni skriver varsin tom klass, kanske ni skapar varsin metod
i en befintlig klass eller skapar några tomma HTML-filer, det är upp till er.
Men det ska vara någonting som har relevans för ert projekt.

Detta ska sedan genomföras genom att:

1. skapa en *branch* (med ett vettigt namn)
2. göra de ändringar som ni planerade och sedan göra en *commit* av detta (med
ett vettigt meddelande)
3. göra en *merge* av detta till `main`

## Färdig

Nu är ni färdiga med alla övningar. Vi har dock skapat en sista del med ett par
[vanliga situationer inom versionshantering](common-situations.md), som varmt
rekommenderas att ni läser. Jag skulle personligen rekommendera att ni tillämpar
"GitHub Flow" i ert projektarbete, det är både en bra övning och något som
faktiskt används i industrin. 
