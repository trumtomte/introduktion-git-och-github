# Terminalen

> En kort introduktion till terminalen

* [Förberedelser](#Förberedelser)
* [Kom igång](#Kom-igång)
* [Exekvera kommandon](#Exekvera-kommandon)
* [Vanliga kommandon](#Vanliga-kommandon)
    - [Navigera filsystemet](#Navigera-filsystemet)
    - [Skapa kataloger](#Skapa-kataloger)
    - [Skapa filer](#Skapa-filer)
    - [Se innehåll](#Se-innehåll)
    - [Skriv ut text](#Skriv-ut-text)
    - [Kopiera](#Kopiera)
    - [Flytta](#Flytta)
    - [Radera](#Radera)
    - [Manualen](#Manualen)
* [Summering över kommadon](#Summering-över-kommandon)
* [Kommandotolken på Windows](#Kommandotolken-på-Windows)

## Förberedelser

Börja med att [installera Git][install].

Beroende på vilket operativsystem ni använder så finns det en del alternativa
terminalprogram:

* **Mac OS**: Terminal (installerad från början), [iTerm 2][iterm2]
* **Windows**: Git BASH (installeras tillsammans med Git), [Putty][putty]
* **Linux**: Terminal (installerad från början), KDE Konsole, XTerm

:exclamation: Skulle ni råka öppna upp något program i terminalen som ni inte
lyckas stänga av kan ni pröva att båda trycka `CTRL + c` eller `q`.

## Kom igån

När ni öppnar er terminal för första gången presenteras ni oftast med något
liknande:

``` bash
sebastian@sebbesDator:~$
```

Vilket kan översättas till:

* `sebastian`: Detta är användarnamnet (*username*) av den inloggade användaren.
* `sebbesDator`: Detta är värdnamet (*hostname*) av server, i mitt fall min egen dator.
* `~`: Detta är den nuvarande katalogen (*current directory*). Tildetecknet är synonymt med din hemkatalog (*home directory*), i mitt fall `/Users/sebastian`.
* `$`: Denna symbol visar vart våra kommandon kommer att börja skrivas ifrån.

För att pröva ett första kommando kan vi ta reda på vilken katalog (mapp) som vi
befinner oss i med kommandot `pwd` (*print working directory*). Skriv in
följande och tryck `Enter`:

``` bash
sebastian@sebbesDator:~$ pwd
```

I mitt fall får jag svaret:

``` bash
/Users/sebastian
```

Kommande kommando kommer vi att skriva utan `sebastian@sebbesDator:~` för att
göra det mer kortfattat. Det vill säga ovanstående kommandoexempel hade vi
skrivit som:

``` bash
$ pwd
/Users/sebastian
```

Rader som börjar **utan** `$` visar oss vad vi fick för svar från kommandot.

## Exekvera kommandon

När vi kör kommandon kan vi göra detta genom att skicka med ett eller flera
argument. Det kan vara allt från att skapa en fil med ett namn (ett argument)
till att söka efter ett ord i alla filer i en katalog (två argument, ordet och
vilken katalog). Viktigt att notera är att alla kommandon är skiftlägeskänsliga,
det vill säga dom gör skillnad på gemener och versaler.

För att pröva ange argument till ett kommando ska vi börja med kommandot `ls`
(*list*) som visar allt innehåll i den katalog vi befinner oss i.

``` bash
$ ls
Desktop     Downloads   Library     Movies      Public
Documents   GitHub      Mail        Music       Work
```

Vi kan med detta kommando även bestämma vilken katalog vi vill titta i med ett
argument.

``` bash
$ ls Desktop
```

Här är `Desktop` vårt första argument. Vi kan även inkludera argument med namn
(eng. *options*, *flags*, *switches*). Vi kan till exempel be om att få allt
innehåll i en lång lista med `-l` (*long listing*). Dessa argument med namn
börjar antingen med ett eller två bindestreck baserat på om det ska vara
förkortat eller inte, till exempel `-f` eller `--filename`.

``` bash
$ ls -l Desktop
```

Vi kan givetvis inkludera flera argument med namn, vi börjar med att lägga till
`-a` (*all*) som gör att vi kan se dolda filer.

``` bash
$ ls -l -a Desktop
```

Flera argument med namn kan förkortas till:

``` bash
$ ls -la Desktop
```

Notera att ovanstående kommando ger oss alla dolda filer och kataloger. Två
speciella kataloger ni kan notera är `.` och `..`, den första representerar den
katalog vi befinner oss i och `..` katalogen ovanför.

Pröva lägga till argumentet `-h` (*human readable*) så får ni filstorlekar på
ett mer läsvänligt sätt.

## Vanliga kommandon

Nedan kommer vi gå igenom ett urval av de vanligare kommandon som behövs för att
kunna navigera runt i filsystemet och kunna skapa/flytta/radera filer och
kataloger.

### Navigera filsystemet

Kommando: `cd` (*change directory*)

Ändra den nuvarande katalogen till `Desktop`.

``` bash
$ cd Desktop
```

Nu kan ni till exempel köra kommandon som `ls -ahl` för att se vad som finns i
denna katalogen.

Om ni skulle vilja navigera tillbaka till hemkatalogen räcker det med att ni
skriver `cd` utan några argument. Skulle ni däremot vilja navigera upp en nivå
(vilket skulle bli tillbaka till er hemkatalog) så kan ni skriva `cd ..`, kom
ihåg att `..` representerade en nivå upp (precis som sökvägar till filer
generellt).

### Skapa kataloger

Kommando: `mkdir` (*make directory*)

För att skapa en katalog använder vi `mkdir`. Om vi befinner oss på skrivbordet
(*Desktop*) så kan vi till exempel skapa katalogen `assets` genom:

``` bash
$ mkdir assets
```

Skulle vi däremot vilja skapa flera kataloger i ett djup direkt får vi använda
oss av argumentet `-p` (*path*).

``` bash
$ mkdir -p project_name/assets/images
```

Detta hade skapat katalogerna `project_name` och i denna `assets` och slutligen
`images`.

### Skapa filer

Kommando: `touch`

För att skapa en fil används kommandot `touch`. Observer att filen skapas utan
innehåll.

``` bash
$ touch index.html
```

### Se innehåll

Kommando: `cat` (*concatenate and print files*)

Kommandot `cat` används för att både skriva ut innehåll från en fil och för att
konkatenera flera filer till en ny (ungefär som att slå ihop flera strängar till
en). Vanligtvis brukar den användas för att se vad en fil innehåller. Låt oss
säga att vi har filen `index.html` med lite HTML inuti, då hade vi kunnat få en
utskrift liknande detta:

``` bash
$ cat index.html
<!doctype html>
<html>
  <head>
    ...
  </head>
  <body>
    ...
  </body>
</html>
```

### Skriv ut text 

Kommando: `echo` (*write arguments to standard output*)

Kommandot `echo` används för att skriva ut saker, så som
miljövariabler<sup>2</sup> på ert operativsystem eller att skriva ut en bit text
och spara den i en fil. På många operativsystem finns en miljövariabel med
namnet `$PATH` som innehåller sökvägar till diverse program och filer.

<sup>2</sup> Miljövariabler kan liknas vid "globala" variabler, fast för ert
operativsystem.

``` bash
$ echo $PATH
```

Vi kan också skriva ut text som ska sparas till en fil.

``` bash
$ touch usernames.txt               # Skapa filen usernames.txt
$ echo "sebastian" > usernames.txt  # Skriv ut "sebastian" till filen
$ cat usernames.txt                 # Skriv ut innehållet i filen
sebastian
```

Här kan vi se operatorn `>` som kan översättas till skicka innehållet från
*vänstra* sidan till *högra* sidan (och skriv över det som redan finns).

``` bash
$ echo "kristina" > usernames.txt
$ cat usernames.txt
kristina
```

I ovanstående fall lade vi till ett namn men använde oss av `>` vilket också
skriver över nuvarande innehåll, om vi vill lägga till (*append*) skriver vi
istället `>>`.

``` bash
$ echo "sebastian" >> usernames.txt
$ cat usernames.txt
kristina
sebastian
```

### Kopiera

Kommando: `cp` (*copy*)

Kommandot `cp` används för att kopiera filer och kataloger.

``` bash
$ mkdir username_project            # Skapa katalogen `username_project`
$ touch usernames.txt               # Skapa filen `usernames.txt`
$ echo "sebastian" > usernames.txt
$ cp usernames.txt username_project # Kopiera filen username.txt till katalogen username_project
$ ls username_project
usernames.txt
```

Låt oss säga att vi befinner oss i katalogen `unknown_project` och vill kopiera
filen `index.html` till katalogen `another_project`, så att den finns i båda
kataloger.

``` bash
$ mkdir unknown_project             # Notera att båda dessa finns i samma katalog
$ mkdir another_project
$ cd unknown_project
$ touch index.html
$ cp index.html ../another_project  # Här nyttjar vi `..` för att gå upp ett steg 
```

### Flytta

Kommando: `mv` (*move*)

Kommandot `mv` används för att flytta en fil från en plats till en annan, det
vill säga inte kopiera den som med `cp`. Skulle vi därför utgå från föregående
exempel hade vi flyttat filen `index.html` istället för att kopiera den så den
finns i båda kataloger.

``` bash
$ mkdir unknown_project
$ mkdir another_project
$ cd unknown_project
$ touch index.html
$ mv index.html ../another_project 
```

Detta hade inneburit att filen `index.html` **inte** finns kvar i
`unknown_project` utan numera i `another_project`.

### Radera

Kommando: `rm` (*remove*)

Kommandot `rm` används för att radera filer och kataloger, observera att detta
är en **permanent** förändring.

``` bash
$ ls
index.html  styles.css
$ rm index.html
$ ls
styles.css
$ rm styles.css
$ ls
```

Skulle vi däremot vilja radera en katalog behöver vi lägga till argumentet `-r`
(*recursive*).

:exclamation: Var **väldigt nogranna** med detta kommando eftersom allting
raderas **permanent**.

``` bash
$ ls                            # Här har vi katalogen `assets` som vi vill radera
index.html  styles.css  assets
$ ls assets
logo.png    profile.jpg
$ rm -r assets
$ ls
index.html  styles.css
```

### Läsa manualer för kommandon

Kommando: `man` (*manual pages*

Kommandot `man` används för att hämta manualer för de olika kommandon (som har
en sådan). Ni trycker på `q` (*quit*) när ni vill stänga ner sidan. Använd
piltangenterna för att navigera upp och ner.

``` bash
$ man ls
```

Detta är ett supernyttigt kommando som snabbt kan ge er insikt hur ni ska
använda ett visst kommando och vilka argument som finns tillgängliga.

## Summering över kommandon

Kommando    | Funktion
----------- | --------
`pwd`       | Visa vilken katalog ni befinner er i
`ls`        | Visa innehållet i en katalog
`mkdir`     | Skapa en ny katalog
`touch`     | Skapa en ny fil
`cat`       | Skriv ut innehållet i en fil
`echo`      | Skriv ut text från variabler eller till en fil
`cp`        | Kopiera en fil från en plats till en annan
`mv`        | Förflytta en fil från en plats till en annan
`rm`        | Radera en fil eller en katalog
`man`       | Manualen för ett givet kommando

## Kommandotolken på Windows

Ytterligare ett alternativ till terminalen på Windows är kommandotolken
(`cmd.exe`), anledningen till att vi inte presenterat det tidigare är för att
denna har sina egna varianter på kommandon. Så för att försöka få
instruktionerna enhetliga föreslog vi både Git BASH och Putty, som emulerar
terminaler på Unix (Mac OS, Linux). Dessutom kommer många sökningar på Google ge
svar där det ofta förutsätts att en Unix-baserad terminal används.

[Här hittar ni en tabell][windows2unix] som översätter kommandon från Windows
till Unix.

[install]: https://git-scm.com/downloads
[iterm2]: https://www.iterm2.com
[putty]: https://www.putty.org
[window2unix]: https://www.lemoda.net/windows/windows2unix/windows2unix.html
