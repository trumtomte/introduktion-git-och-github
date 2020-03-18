# Arbeta med GitHub Desktop

> En guide för att arbeta med [GitHub Desktop](https://desktop.github.com).

![GitHub Desktop](images/github-desktop-landing-page.png)

## Innehållsförteckning

* [Förberedelser](#Förberedelser)

## Förberedelser

Till att börja med måste ni [registrera er på GitHub](https://github.com/join).

För att följa med i denna guiden krävs det att ni installerar:

* [GitHub Desktop](https://desktop.github.com) (versionshantering)
* [Atom](https://atom.io) (textredigerare)

Det finns givetvis fler alternativ till textredigerare men i denna guiden används [Atom](https://atom.io) då den har bra integration med både Git och GitHub. Ett alternativ är [Visual Studio Code](https://code.visualstudio.com) som har likvärdigt stöd för Git och GitHub.

Syftet med dessa textredigerare i denna guiden är huvudsakligen integrationen med Git och GitHub, till exempel hur dessa underlättar hantering av *merge konflikter*, inte att dom nödvändigtvis måste användas till programmering.

## Terminologi

Term          | Betydelse
------------- | -----------------
Repository    | Ert projekt, dvs. alla era filer.
`.gitignore`  | TODO
`README.md`   | TODO
Branch        | En version (gren) av ert projekt.
Add           | TODO
Commit        | Att spara en eller flera ändringar.
Merge         | Sammanställ ändringar från en *branch* till en annan.
Conflict      | TODO
Checkout      | TODO
Tag           | TODO
Fetch         | TODO
Pull          | TODO
Staged        | TODO
Unstaged      | TODO
Pull request  | TODO
HEAD          | TODO

## Skapa ett repository

När ni har registrerat er och loggat in på [GitHub](https://github.com) kan ni i huvudmenyn välja att skapa ett nytt repository. På sidan för att skapa ett nytt repository har ni möjlighet att fylla i följande uppgifter:

1. Namnet på ert repository.
2. En kort beskrivning över ert projekt (valfritt).
3. Om ert repository ska vara publikt eller privat (**välj publikt**).
4. Om ert repository ska skapas med en `README.md` (**checka i denna**).
5. Om ert repository ska skapas med en `.gitignore`. **Välj** en av följande: Unity, VisualStudio, Java eller Python. Vi kommer redigera detta i ett senare skede.
6. Om ert repository ska skapas med en licens (valfritt).

    

![Github create new repository](images/2-github-create-new-repo.png)
