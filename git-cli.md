# Git i terminalen

[Här hittar ni en väldigt utförlig lista över bra Git tips.](https://github.com/git-tips/tips)

## Init och Clone

Starta ett nytt git repository i den nuvarande mappen:

``` bash
$ cd /path/to/project
$ git init
$ git add .
$ git commit
```

Klona ett befintligt repository:

``` bash
$ git clone https://.../my-project.git
$ cd my-project
```

## Config

Ändra git konfiguration (hämta/skriva):

``` bash
$ git config --global user.email # hämta
$ git config --global user.email "my_email@example.com" # skriva
$ git config --global core.editor "vim"
$ git config --global core.editor "'c:/program files/sublime text 3/sublimetext.exe' -w"
$ git config --global alias.co checkout
$ git config --global alias.ci commit
```

## Add och Commit

Spara alla ändringar:

``` bash
$ git add .     # Lägg till filer som ska sparas
$ git commit    # Spara, din valda `editor` kommer öppnas
```

Spara ändringar från en fil:

``` bash
$ git add hello.py
$ git commit
```

Spara en ändring med ett meddelande:

``` bash
$ git commit -m "commit message"
```

Spara alla ändringar (`-a` kör en `git add .`) med ett meddalande:

``` bash
$ git commit -am "commit message"
```

Lägg till ändringar på senaste commit:en:

``` bash
$ git commit --amend
```

Se status för vad som är tillagt/modifierat:

``` bash
$ git status
```

## Stash

Spara undan dina ändringar (för att återkomma senare):

``` bash
$ git stash
```

Återkom till dina ändringar:

``` bash
$ git stash pop
$ git stash apply # återkom och låt stashen vara kvar som den var
```

Funkar inte på icke stage:ade filer (eller ignorerade), såfall:

``` bash
$ git stash -u # untracked
$ git stash -a # include ignored
```

Kolla vad som är stashat:

``` bash
$ git stash list
```

Stasha med ett meddelande:

``` bash
$ git stash save "stash message"
```

Återkom till specifik stash:

``` bash
$ git stash pop stash@{2}
```

## .gitignore

Ignorera en tillagd fil:

``` bash
$ echo debug.log >> .gitignore
$ git rm --cached debug.log
$ git commit -m "Start ignoring debug.log"
```

## Tag

Skapa en "tag":

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

## Blame

Kolla vem som ändrat vad i en fil:

``` bash
$ git blame README.md
```

## Undo

Ångra, men behåll, den senaste commit:en (gör en inverterad commit):

``` bash
$ git revert HEAD
```

Ångra (gå tillbaka till) en commit:

*dock problematiskt för remote repositories som ev. har kvar commits.*

``` bash
$ git reset --hard a1e85r9d
```

## Hur man lämnar Vim/Nano

Ifall ni inte bytar eran default code-editor så kommer ni komma in i Vim eller Nano (beroende på operativ system) när ni får en merge conflict eller försöker köra:

``` bash
$ git commit --amend
```

Vim / Nano är by default en väldigt simpel code-editor (som man kan modifiera nästan precis allt med), den är dock inte så användarvänlig. Detta har skapat väldigt mycket memes kring hur man lämnar Vim/Nano (på tex. /r/programmerhumor).

### Så hur lämnar man Vim/Nano?

#### Om du inte har ändrat någonting i Vim

``` bash
$ :q
```

Klicka sen på `Enter`.

#### För att slänga bort dina ändringar och avsluta Vim

``` bash
$ :qa
```

Klicka sen på `Enter`.

#### För att spara dina ändringar och avsluta Vim

``` bash
$ :wq
```

Klicka sen på `Enter`.

#### Om du inte ändrat någonting i Nano eller vill slänga bort dina ändringar

`CTRL + X` sen `N`.

#### För att spara dina ändringar i Nano och avsluta

`CTRL + X` sen `Y`.
