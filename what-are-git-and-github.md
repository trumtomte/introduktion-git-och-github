# Vad är Git och GitHub?

> En kort översikt över Versionskontrollsystem (VCS), Git och GitHub

## Versionskontrollsystem (VCS)

Ett versionskontrollsystem (VCS) är ett program (eller en uppsättning program)
som spårar ändringar i en samling filer (så som källkod och dokumentation).
Detta innebär att vi kan enkelt se tidigare versioner av enskilda filer eller
hela vårt projekt. Det vill säga att vi får en spårbar historik över alla
ändringar som gjorts. Med ett VCS så kan flera personer i ett team arbeta med
ett projekt, även samma fil, utan att påverka varandra.

En annan term som vanligtvis dyker upp i samband med versionskontrollsystem är
Software Configuration Management (SCM) och används ibland som en synonym till
VCS. Ett SCM-system innefattar mer processer än versionshantering, så som
kravhantering, granskning, releaser, med mera. Så tekniskt sätt är ett VCS bara
en del av ett SCM-system. Däremot kan ett VCS användas till mer än projekt för
programvara. Idag används det bland annat till att skriva böcker eller för
material till onlinebaserade självstudier.

## Git

[Git][scm] är ett versionskontrollsystem och dessutom ett distribuerat sådant
(DVCS), vilket innebär att ett projekts fullständiga historik finns både hos
klienten och på servern. Till skillnad mot centraliserade versionskontrollsystem
som Subversion (SVN) och Perforce där allting lagras på en central server.
Skulle denna server av någon anledning försvinna så gör all historik det också.

Med ett distribuerat VCS kan vi redigera filer utan en nätverksanslutning och
arbeta lokalt tills dess att vi vill synkronisera<sup>1</sup> våra filer eller
när en anslutning blir tillgänglig. Skulle dessutom vår server krasha så har vi
fortfarande hela projektet lokalt och kan snabbt komma på fötterna igen.

Git är idag också det mest använda VCS och har använts sedan 2005, då det
skapades av [Linus Torvalds][linus], personen som skapade operativsystemet
[Linux][linux].

<sup>1</sup>I vårat fall innebär detta att ladda upp våra ändringar på
GitHub.

## GitHub

[GitHub][github] är en plattform för Git och erbjuder mer än bara en plats för
att lagra våra projekt. Vi kan bland annat utforska andras projekt och där kan
vi se allt från statistik till deras fullständiga historik (och därmed dra
vettiga lärdomar om hur andra samarbetar).

Två vanliga funktioner introducerat av GitHub är att kunna skapa [Forks][forks]
(en kopia av någons repository) för att sedan göra en [Pull Request][pull] (ett
förslag till ändring som först ska granskas). Detta har gjort det enkelt att
samarbeta på stora projekt för utomstående som frilansare eller personer som
utvecklar på sin fritid.

Som på andra sociala nätverk kan vi även följa andra utvecklare och ta del av
vilka projekt dom i sin tur arbetar med eller bara följer. På så vis kan vi
också enkelt skapa oss ett kontaktnätverk och i vissa fall starta nya projekt
med personer som vi annars inte träffat.

Utöver att kunna utforska andras projekt och samarbeta med andra personer har
GitHub också ett starkt stöd för integration med olika tjänster. Det kan vara
allt från att testning ska köras på ett projekt innan det publiceras på en
server till att projektledare enkelt kan se vad som gjorts och vad som behöver
göras.

## Fortsatt läsning

För att sätta sig in mer om just versionshantering med Git så rekommenderas det
att läsa [What is version control][vcs]. Denna guide går igenom grundläggande
koncept som versionskontrollsystem till praktiska Git-kommandon för att kunna
versionhantera.

[scm]: https://git-scm.com
[linus]: https://sv.wikipedia.org/wiki/Linus_Torvalds
[linux]: https://github.com/torvalds/linux
[github]: https://github.com
[forks]: https://guides.github.com/activities/forking/
[pull]: https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request
[vcs]: https://www.atlassian.com/git/tutorials/what-is-version-control
