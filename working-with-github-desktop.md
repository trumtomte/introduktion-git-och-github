# Arbeta med GitHub Desktop

> En guide för att arbeta med [GitHub Desktop](https://desktop.github.com).

![GitHub Desktop](images/github-desktop-landing-page.png)

## Innehållsförteckning

* [Förord](#Förord)
* [Förberedelser](#Förberedelser)
* [Terminologi](#Terminologi)
* [Skapa ett repository](#Skapa-ett-repository)
  - [Lägg till användare](#Lägg-till-användare)
* [Arbeta lokalt med GitHub Desktop](#Arbeta-lokalt-med-GitHub-Desktop)
  - [Klona ett repository](#Klona-ett-repository)
  - [Arbetsvy](#Arbetsvy)
  - [Historik](#Historik)

## Förord

## Förberedelser

Till att börja med måste ni [registrera er på GitHub](https://github.com/join).

För att följa med i denna guiden krävs det att ni installerar:

* [GitHub Desktop](https://desktop.github.com) (versionshantering)
* [Atom](https://atom.io) (textredigerare)

Det finns givetvis fler alternativ till textredigerare men i denna guiden används [Atom](https://atom.io) då den har bra integration med både Git och GitHub. Ett alternativ är [Visual Studio Code](https://code.visualstudio.com) som har likvärdigt stöd för Git och GitHub.

Syftet med dessa textredigerare i denna guiden är huvudsakligen integrationen med Git och GitHub, till exempel hur dessa underlättar hantering av *merge konflikter*, inte att dom nödvändigtvis måste användas till programmering.

## Terminologi

Nedan finner ni en tabell över några vanliga termer och en kortare beskrivning.

Term          | Betydelse
------------- | -----------------
Repository    | Ert projekt, dvs. alla era filer.
`.gitignore`  | Innehåller sökvägar till filer som **inte** ska publiceras till GitHub.
`README.md`   | Det innehåll som visas när någon besöker projektsidan på GitHub. Skrivs i [Markdown](https://guides.github.com/features/mastering-markdown/).
Commit        | Att spara en eller flera ändringar med ett beskrivande meddelande.
Branch        | En version av ert projekt. Ni skapar en *branch* varje gång någon vill göra ändringar (*commits*).
Merge         | Sammanställ *commits* från en *branch* till en annan.
Working copy  | Den nuvarande *branch* (version) som ni redigerar.
Checkout      | Byta från en *branch* till en annan, dvs. er *working copy* ändras.
Remote        | Den plats där era ändringar sparas, GitHub i ert fall.
Pull          | Hämta *commits* från er *remote*.
Push          | Publicera *commits* till er *remote*.
Pull request  | Skapa ett förslag till en *commit* som sedan kan *mergas*, diskussion sker via GitHub.
Conflict      | TODO

## Skapa ett repository

När ni har registrerat er och loggat in på [GitHub](https://github.com) kan ni i huvudmenyn välja att skapa ett nytt repository. På sidan för att skapa ett nytt repository har ni sedan möjlighet att fylla i följande uppgifter:

1. Namnet på ert repository.
2. En kort beskrivning över ert projekt (valfritt).
3. Om ert repository ska vara publikt eller privat (**välj publikt**).
4. Om ert repository ska skapas med en `README.md` (**checka i denna**).
5. Om ert repository ska skapas med en `.gitignore`.
    * **Välj en** av följande: *Unity*, *VisualStudio*, *Java* eller *Python*. Vi kommer redigera detta i ett senare skede.
6. Om ert repository ska skapas med en licens (valfritt).  

**Skapa ett nytt repository:**

![Github: create a new repository](images/2-github-create-new-repo.png)

**Ert nya repository:**

![Github: new repository](images/4-github-repo-initial-commit.png)

### Lägg till användare

Innan vi går vidare med att skapa mer innehåll i vårt repository så ska vi börja med att lägga till fler användare. Så att vi har möjlighet att börja samarbeta.

![Github: invite collaborator](images/13-github-repo-settings.png)

## Arbeta lokalt med GitHub Desktop

Nästa steg är nu att kunna börja arbeta lokalt och detta kommer ge med hjälp av [GitHub Desktop](https://desktop.github.com). Första gången ni öppnar denna applikationen presenteras ni med följande:

![Github desktop: first glance](images/5-github-desktop-first-glance.png)

### Klona ett repository

Välj sedan att klona ett repository och börja med att logga in på ert GitHub konto, på så vis kommer ni få tillgång till alla era repositories.

![Github desktop: sign in](images/6-github-desktop-sign-in.png)

Därefter kommer ni i högerspalten se en lista över dessa **men** klicka istället på klona *igen* så ni kan välja till vilken mapp ni vill ha ert projekt i.

![Github desktop: clone](images/8-github-desktop-clone-repo.png)

### Arbetsvy

Nu kommer ni till den vy som ni kommer arbeta med.

![Github desktop: first use](images/9-github-desktop-first-use.png)

Om ni behöver ändra vilken textredigerare som ska gälla går ni in på *inställningar*.

![Github desktop: preferences](images/10-github-desktop-preferences.png)

### Historik

Nu kan ni välja att ta en titt på er historik för att se vad som skett.

![Github desktop: history](images/15-github-desktop-history.png)
