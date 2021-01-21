# Git i terminalen

> En kort översikt över git-relaterade kommandon i terminalen.

* [Förberedelser](#Förberedelser)
* [Rekommenderad läsning](#Rekommenderad-läsning)
* [Nytt projekt](#Nytt-projekt)
* [Konfiguration](#Konfiguration)
* [Spara ändringar](#Spara-ändringar)
* [Ignorera ändringar i utvalda filer](#Ignorera-ändringar-i-utvalda-filer)
* [Skapa en release](#Skapa-en-release)
* [Vem har gjort vad?](#Vem-har-gjort-vad)
* [Ångra ändringar](#Ångra-ändringar)
* [Lämna textredigerarna Vim och Nano](#Lämna-textredigerarna-Vim-och-Nano)

## Förberedelser

Om ni sedan tidigare är ovana med att använda en terminal rekommenderar jag att
ni går igenom avsnittet [Terminalen][terminal].

För att kunna köra dessa Git-kommandon behöver vi givetvis [installera
Git][install].

## Rekommenderad läsning

* [Setting up a repository][setup]
* [Här hittar ni en väldigt utförlig lista över bra Git-tips][tips]

## Nytt projekt

Skapa ett nytt projekt (dvs. ett nytt *Git repository*).

``` bash
$ cd /path/to/project
$ git init
$ git add .         # Dessa kommandon (add + commit) innebär att vi
$ git commit        # sparar vårt projekt för första gången
```

Om det istället finns ett befintlig projekt (*repository*) kan vi istället klona
detta:

``` bash
$ git clone https://github.com/username/my-project.git
$ cd my-project
```

Sökvägen till ett projekt hittar ni på GitHub.

## Konfiguration

Spara och redigera inställningar kopplade till er Git.

``` bash
$ git config --global user.email # hämta
$ git config --global user.email "my_email@example.com" # skriva
$ git config --global core.editor "vim"
$ git config --global core.editor "'c:/program files/sublime text 3/sublimetext.exe' -w"
```

Vi kan även skapa förkortningar till kommandon som används ofta.

``` bash
$ git config --global alias.co checkout
$ git config --global alias.ci commit
```

## Spara ändringar

Att spara ändringar i Git sker i två steg. Först väljer vi vilka filer vi vill
spara (vi kan välja att ange en hel katalog). Sedan bestämmer vi att vi vill
spara ändringarna och anger ett meddelande till detta.

``` bash
$ git add index.html    # Vi vill spara ändringarna till denna filen
$ git commit            # Spara ändringarna, din förvalda `editor` öppnas

# Eller spara alla ändringar i den nuvarande katalogen (".")
$ git add .             
$ git commit -m "Fixed issues withing <body>" # Med ett meddelande
```

Spara alla ändringar (`-a` kör en `git add .`) med ett meddelande:

``` bash
$ git commit -am "commit message"
```

Ändra på din senaste *commit* (dvs. meddelandet):

``` bash
$ git commit --amend
```

Kontrollera statusen för ert projekt (*repository*), det vill säga vad som ska
sparas, det som ändrats, med mera:

``` bash
$ git status
```

## Ignorera ändringar i utvalda filer

Filer vars ändringar ni inte vill ska spåras placeras i filen `.gitignore`
(observera punkten i början av filnamnet).

I kodsnutten nedan anger vi att filen `debug.log` inte ska spåras, när vi lägger
till denna tömmer vi vår *cache* över de filer som inte spåras (för att
säkerhetsställa att ändringen sker).

``` bash
$ echo debug.log >> .gitignore  
$ git rm --cached debug.log
$ git commit -m "Start ignoring debug.log"
```

Ibland kan det vara enklare att bara tömma hela denna *cache* över filer som
inte ska sparas och sedan låta Git gå igenom alla filer igen så att allt
stämmer.

``` bash
$ git rm -r --cached .
$ git commit -am "git cache cleared"
$ git push
```

## Skapa en release

Skapa en release, det vill säga en Git *Tag*:

``` bash
$ git tag v1.0.1
```

Lista alla tags:

``` bash
$ git tag
```

Kolla vad en "tag" innehöll:

``` bash
$ git checkout v1.0.1
```

Radera en tag:

``` bash
$ git tag -d v1.0.1
```

## Vem har gjort vad?

Kontrollera vem som har gjort ändringar i en fil:

``` bash
$ git blame README.md
```

## Ångra ändringar

Ångra, men behåll, den senaste *commit* (gör en inverterad *commit*):

``` bash
$ git revert HEAD
```

Ångra (gå tillbaka till) en commit:

*dock problematiskt för remote repositories som ev. har kvar commits.*

``` bash
$ git log # Här ser ni respektive hash för varje commit
$ git reset --hard a1e85r9d # Ni anger vilken hash ni vill återgå till
```

## Lämna textredigerarna Vim och Nano

I vissa fall när ni gör *commits* eller det uppstår en *merge conflict* kan en
standard textredigerare öppnas, vanligen Vim eller Nano. I dessa fall kan det
vara svårt att stänga av eller lämnas dessa då dom inte har ett grafisk
gränssnitt. Nedan hittar ni hur detta görs för respektive textredigerare.

### Vim

Om ni inte har gjort ändringar och bara vill lämna skriver ni in `:q` (notera
kolonet först). Om ändringar har gjorts men ni vill bortse från dom skriver ni
in `:qa`. Sedan trycker ni `Enter`.

Om ni vill spara era ändringar och avsluta skriver ni in `:wq` och sedan trycker
ni `Enter`.

### Nano

Om ni inte har ändrat någonting eller vill slänga bort ändringar trycker ni
`CTRL + X` och sedan `N`.

Om ni vill spara ändringar trycker ni `CTRL + X` och sedan `Y`.

[terminal]: the-terminal.md
[install]: https://git-scm.com/downloads
[setup]: https://www.atlassian.com/git/tutorials/setting-up-a-repository
[tips]: https://github.com/git-tips/tips
