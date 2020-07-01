# git-jukseliste
En oversikt over de viktigste kommandoene til Git og Terminalen (bash, zsh og fish).
Det finnes veldig mange flere kommandoer det er verdt å lære seg (f.eks. [`git grep`](https://git-scm.com/docs/git-grep)), men du kommer langt med de under.

---
## Bash (kommandolinjen)

* `pwd`: Vis hvilken mappe du befinner deg i.
* `cd [mappe]`: Gå til \[mappe].
* `cd ..`: Gå en mappe opp.
* `cd ~`: Gå til hjem-mappen
* `cd /`: Gå til systemes rotmappe
* `ls`: Vis en liste over filer og mapper som befinner seg i gjeldende mappe
* `ls -a`: Samme som over, men inkluderer også skjulte filer og mapper
* `touch fil.txt`: Lag filen fil.txt i gjeldende mappe
* `rm [fil]`: Fjern fil fra systemet. Denne slettes for godt, og kan ikke gjenopprettes.
* `rm -r [mappe]`: Samme som over, men for en mappe. `-r` står for _recursive_.

## Git
* `git init`: Initialiser en mappe på datamaskinen din som et git-repository (en git-mappe).
* `git clone [url]`: Lager en lokal kopi av repoet som ligger på den gitte url-en. For eksempel kan du bruke  `git clone https://github.com/erikaja/git-jukseliste.git` for å laste ned denne filen. Oppretter en mappe med samme navn som repoet i mappen kommandoen kjøres fra.
* `git status`: Viser om du har noen lokale endringer som ikke er lagt inn i git sin versjon av mappen. Sier ingenting om andre sine endringer.
* `git add [fil]`: Legger valgte fil til i _staging area_, slik at du kan legge den til i en ny _commit_.
* `git commit -m "melding"`: Lager en ny versjon av mappen og legger denne til i git. Meldingen burde kort beskrive endringene som er gjort.
* `git push origin [gren]`: Forsøker å dytte grenen du er på til [gren] på github.com.
* `git pull origin [gren]`: Henter endringer fra GitHub-branchen [gren] og forsøker å merge dem med din nåværende branch.
* `git branch`: Viser en liste over alle grenene som finnes på repoet.
* `git checkout [gren]`: Flytter deg til branchen [gren].
* `git checkout -b [gren]`: Oppretter og flytter deg til branchen [gren].
* `git log`: Gå gjennom historikken til den nåværende branchen, commit for commit.
* `git diff`: Se hva som er annerledes mellom filene i ditt Working Tree og filene i commiten du for øyeblikket befinner deg på.
* `git diff --staged`: Samme som over, men sammenligner filene i din Staging Area med filene i commiten du for øyeblikket befinner deg på.
