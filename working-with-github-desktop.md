# Arbeta med GitHub Desktop

Denna guide består av tre delar och ska genomföras i den ordning som presenteras
nedan. För att göra detta måste ni ha [registrerat er på
GitHub](https://github.com/join) och installerat [GitHub
Desktop](https://desktop.github.com).

Det är viktigt att ni följer instruktionerna noga för att minska risken för
problem nu och i framtiden. Observera att vissa moment kan endast genomföras av
en projektmedlem. Detta kommer markeras tydligt och ni som grupp får själva utse
vem som gemomför dessa.

Eftersom versionshantering kommer med sitt egna ordförråd av diverse begrepp har
vi sammanställt en liten tabell nedan över dom vanligaste termerna med en kort
beskrivning.

När ni känner er redo kan ni gå vidare med att börja versionshantera.

1. [Kom igång](getting-started.md)
2. [Börja versionshantera](how-to-version-control.md)
3. [Vanliga situationer](common-situations.md)

## Terminologi

| Term           | Beskrivning                                                                                       |
|:---------------|:--------------------------------------------------------------------------------------------------|
| repository     | Ert projekt (alla filer som ska versionshanteras)                                                 |
| clone          | Att hämta (eller ladda ner) ett repository från, t.ex., github.com                                |
| add            | Lägg till en eller flera filer (med ändringar) som ska ingå i nästa *commit* (version)            |
| commit         | Skapa en ny version tillsammans med ett beskrivande meddelande                                    |
| branch         | En parallell version (gren)                                                                       |
| working copy   | Den nuvarande *branch* som ni arbetar i                                                           |
| merge          | Slå ihop *commits* från en *branch* till en annan (t.ex. från din egen till `main`)               |
| checkout       | Byta från en *branch* till en annan, dvs. er *working copy* ändras                                |
| remote         | Den plats där era ändringar sparas (t.ex. GitHub i ert fall)                                      |
| fetch          | Hämta de senaste ändringarna (*commits*) från er *remote*                                         |
| pull           | Detsamma som *fetch* men gör även en *merge* till `main`                                          |
| push           | Publicera era *commits* (dvs. era ändringar) till er *remote*                                     |
| pull request   | Skapa ett förslag till en *merge* med en diskussion via GitHub innan den godkänns                 |
| conflict       | När en *merge* från en *branch* till en annan har filändringar som kolliderar                     |
| `.gitignore`   | En fil som innehåller sökvägar till andra filer som **inte** ska versionshanteras                 |