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
vi sammanställt en liten tabell över dom vanligaste termerna med en kort
beskrivning.

| Term           | Beskrivning                                                                                       |
|:---------------|:--------------------------------------------------------------------------------------------------|
| repository     | Ert projekt (alla filer som ska versionshanteras)                                                 |
| clone          | Att hämta (eller ladda ner) ett repository från, t.ex., github.com                                |
| add            | Gruppera en eller flera filer (nya eller redigerade) för att sedan göra en *commit*               |
| commit         | Spara ändringar från en eller flera filer med ett beskrivande meddelande                          |
| branch         | En separat version av ert *repository* så att ni kan arbeta parallellt                            |
| working copy   | Den nuvarande *branch* som ni arbetar i                                                           |
| merge          | Slå samman *commits* från en *branch* till en annan (t.ex. från din egen till `main`)             |
| checkout       | Byta från en *branch* till en annan, dvs. er *working copy* ändras                                |
| remote         | Den plats där era ändringar sparas (GitHub i ert fall)                                            |
| fetch          | Hämta de senaste ändringarna (*commits*) från er *remote*                                         |
| pull           | Stoppa in de senaste ändringarna (*commits*) bland era filer                                      |
| push           | Publicera era *commits* och *merges* till er *remote*                                             |
| pull request   | Skapa ett förslag till en *merge* med en diskussion via GitHub innan den godkänns                 |
| merge conflict | När en *merge* från en *branch* till en annan har filändringar som kolliderar                     |
| `.gitignore`   | En fil som innehåller sökvägar till andra filer som **inte** ska publiceras till på er *remote*   |
| `README.md`    | Det innehåll som visas när någon besöker projektsidan på GitHub. Formateras enligt [Markdown][md] |

När ni känner er redo kan ni gå vidare med guiden.

1. [Kom igång](getting-started.md)
2. [Börja versionshantera](how-to-version-control.md)
3. [Vanliga situationer](common-situations.md)
