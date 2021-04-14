# En inledande övning till Git och GitHub

Denna övning är indelad i 5 steg och det är viktigt att ni följer denna ordning.
Läs igenom instruktioner noggrant innan ni påbörjar något arbete.

1. [Steg 1](#steg-1)
2. [Steg 2](#steg-2)
3. [Steg 3: Övningsinstruktioner](#steg-3-övningsinstruktioner)
4. [Steg 4: Guide](#steg-4-guide)
5. [Steg 5: Självstudier](#steg-5-självstudier)

## Steg 1

Läs [denna korta översikt av Git och GitHub](what-are-git-and-github.md).

## Steg 2

Registrera er [på GitHub][join] och ladda sedan ner [GitHub
Desktop][desktop].

## Steg 3: Övningsinstruktioner

Efter dagens övning ska ni ha:

1. Registrerat er på GitHub.
2. Skapat ett repository att arbeta med.
3. Lagt till en `.gitignore` med något innehåll.
4. Lagt till erat projekts (repository) första filer.
    - Återanvänd det material ni har från *Uppgift 1*.
5. Gjort ändringar till filen `README.md` (vad ni gör för ändringar är upp till
   er själva).
6. Utöver detta ska ni även (på egen hand) ha gjort följande:
    - Skapat minst en *branch*, så att ändringar kan göras (vad ni gör för
       ändringar är upp till er själva).
    - Gjort minst en *commit* med sina ändringar till sin *branch*.
    - Gjort minst en *merge* från sin *branch* till `main`.

## Steg 4: Guide

### Förberedelser

I denna guiden används textredigeraren [Atom][atom] för att den har en enkel
integration med både Git och GitHub. Det finns så klart många bra alternativ
till denna som [Visual Studio Code][vsc]. Många textredigerare och IDE:er (t.ex.
IntelliJ, Eclipse, m.m.) har antingen inbyggt stöd eller plugins som kan
integrera med Git och GitHub.

### Terminologi

Nedan finner ni en tabell över några vanliga termer och en kortare beskrivning.

Term           | Betydelse
-------------- | -----------------
Repository     | Ert projekt, dvs. alla era filer.
`.gitignore`   | Innehåller sökvägar till filer som **inte** ska publiceras till GitHub.
`README.md`    | Det innehåll som visas när någon besöker projektsidan på GitHub. Formateras enligt [Markdown][md].
Add            | Lägg till de filer och mappar som redigerats för att sedan spara dom (*commit*).
Commit         | Att spara en eller flera ändringar med ett beskrivande meddelande.
Branch         | En version av ert projekt. Ni skapar en *branch* varje gång någon vill göra ändringar (*commits*).
Merge          | Sammanställ *commits* från en *branch* till en annan.
Working copy   | Den nuvarande *branch* (version) som ni redigerar.
Checkout       | Byta från en *branch* till en annan, dvs. er *working copy* ändras.
Remote         | Den plats där era ändringar sparas, GitHub i ert fall.
Pull           | Hämta *commits* från er *remote*.
Push           | Publicera *commits* till er *remote*.

### Skapa ett repository

När ni har registrerat er och loggat in på [GitHub][gh] kan ni i huvudmenyn
välja att skapa ett nytt repository. På sidan för att skapa ett nytt repository
har ni sedan möjlighet att fylla i följande uppgifter:

1. Namnet på ert repository.
2. En kort beskrivning över ert projekt (t.ex. "Dagens övning").
3. Om ert repository ska vara publikt eller privat (**välj publikt**).
4. Om ert repository ska skapas med en `README.md` (**checka i denna**).
5. Om ert repository ska skapas med en `.gitignore` (**välj** `node`).
6. Om ert repository ska skapas med en licens (valfritt).

**Skapa ett nytt repository:**

![Github: create a new repository](images/2-github-create-new-repo.png)

**Ert nya repository:**

![Github: new repository](images/4-github-repo-initial-commit.png)

### Arbeta lokalt med GitHub Desktop

Nästa steg är nu att kunna börja arbeta lokalt och detta kommer ske med hjälp av
[GitHub Desktop][desktop]. Första gången ni öppnar denna applikationen
presenteras ni med följande:

![Github desktop: first glance](images/5-github-desktop-first-glance.png)

#### Klona ett repository

Efter ni startat applikationen första gången ska ni sedan hämta ert repository
från GitHub, detta kallas för att *klona* ett repository. För att göra detta
klickar ni på "Clone a Repository [...]" och där ni kan ni sedan välja att logga
in med ert GitHub-konto (då får ni tillgång till alla repositories ni har).

![Github desktop: sign in](images/6-github-desktop-sign-in.png)

Därefter kommer ni i högerspalten se en lista över dessa **men** klicka istället
på klona igen så ni kan välja till vilken mapp ni vill ha ert projekt i.

:exclamation: Vi kommer att fortsätta göra ändringar i detta repository **innan
ni går vidare** med att lägga till alla era egna filer och kan börja arbeta på
riktigt.

![Github desktop: clone](images/8-github-desktop-clone-repo.png)

#### Arbetsvy

När ni klonat ert första repository kommer ni till *arbetsvyn* och det är denna
som ni sedan huvudsakligen kommer arbeta med. Denna är indelad i två sektioner,
till vänster hittar ni de filer ni gjort ändringar i och till höger hittar ni
vilka ändringar som gjorts (baserat på den fil ni markerat i vänsterspalten).

![Github desktop: first use](images/9-github-desktop-first-use.png)

Om ni behöver ändra vilken textredigerare som ska gälla går ni in under
inställningar. Välj "Preferences" -> "Integrations" och sedan kan ni byta
textredigerare (t.ex. som i mitt fall, till Atom). **Detta är valfritt**.

![Github desktop: preferences](images/10-github-desktop-preferences.png)

#### Historik

I vänsterspalten kan vi välja *History* istället för *Changes* vilket ger oss
*historikvyn* som helt enkelt visar all historik över ändringar som gjorts.

![Github desktop: history](images/15-github-desktop-history.png)

### Att versionshantera

Innan ni nu börjar arbeta med att versionshantera behöver ni ha en
textredigerare igång (t.ex. Visual Studio Code) samt GitHub Desktop. När ni har
detta behöver ni sedan öppna projektmappen (den finns någonstans på er dator
efter att ni *klonade* erat respository, oftast finner ni denna under "dokument"
och "github") i er textredigare så ni kan göra ändringar.

För att ni ska pröva på processen att versionshantera ska vi redigera vår fil
`README.md` (den ska finnas i er projektmapp). Vi börjar med att skapa en
*branch* för denna ändring.
 
![Github desktop: create branch readme](images/32-github-desktop-create-branch-project-description.png)

Sedan publicerar vi denna.

![Github desktop: publish branch readme](images/33-github-desktop-branch-project-description.png)

Därefter börjar jag göra mina ändringar.

![Atom: readme changes](images/34-atom-update-readme.png)

Sedan gör vi en *commit* av dessa ändringar och därefter publicerar vi detta,
"Publish branch" eller "Push origin".

![Github desktop: commit readme](images/35-github-desktop-commit-project-description.png)

Vi kan nu kontrollera att våra ändringar kommit upp till GitHub.

![Github: check readme changes](images/37-github-check-project-description.png)

Nu är nästa steg att utföra vår *merge*. När vi gör en *merge* måste vi byta
*branch* (dvs. en *checkout*) till **den branch vi vill merga till**, i vårt
fall är detta vår `main`.

![Github desktop: switch to main](images/38-github-desktop-switch-to-master.png)

Sen väljer vi att vi ska *merga* `update-project-description` till `main`.

![Github desktop: merge to main](images/39-github-desktop-merge-into-master.png)

Där efter har ni möjlighet att klicka på *Push* så att alla era ändringar nu
laddas upp till er *remote* (dvs. GitHubs hemsida).

## Steg 5: Självstudier

Det som precis gjordes i steg 4 ska ni nu upprepa på egen hand men det måste ske
i en ny *branch* och i en annan fil än `README.md`.

**Börja med** att skapa en *branch*. Kopiera sedan in alla era filer (t.ex. från
Uppgift 1). Sedan i GitHub Desktop gör ni en *commit* med meddelandet "Added
project files".

**Därefter** ska ni göra någon redigering i en fil (t.ex. lägga till en
kommentar i en JavaScript-fil). Sedan gör ni ännu en *commit*.

**Avsluta** sedan med att göra en *merge* till `main`.

Ni bör nu kunna besöka erat repository på GitHubs hemsida och se alla filer och
den lilla ändring ni precis gjort.

Lycka till!

[desktop]: https://desktop.github.com
[join]: https://github.com/join
[atom]: https://atom.io
[vsc]: https://code.visualstudio.com
[md]: https://guides.github.com/features/mastering-markdown/
[gh]: https://github.com
