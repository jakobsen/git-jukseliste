# git-jukseliste
En oversikt over de viktigste kommandoene til Git og Terminalen (bash, zsh og fish).
Det finnes veldig mange flere kommandoer det er verdt å lære seg (f.eks. [`git grep`](https://git-scm.com/docs/git-grep)), men du kommer langt med de under.
De fleste kommandoene har også flere versjoner, og kan modifiseres ved hjelp av argumenter som start med en eller to bindestreker.
En oversikt ligger [her](https://git-scm.com/docs).

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
* `git commit -m "melding"`: Lager en ny versjon av mappen og legger denne til i git. Meldingen burde kort beskrive endringene som er gjort, se under.*
* `git push origin [gren]`: Forsøker å dytte grenen du er på til [gren] på github.com.
* `git pull origin [gren]`: Henter endringer fra GitHub-branchen [gren] og forsøker å merge dem med din nåværende branch.
* `git branch`: Viser en liste over alle grenene som finnes på repoet.
* `git checkout [gren]`: Flytter deg til branchen [gren].
* `git checkout -b [gren]`: Oppretter og flytter deg til branchen [gren].
* `git log`: Gå gjennom historikken til den nåværende branchen, commit for commit.
* `git diff`: Se hva som er annerledes mellom filene i ditt Working Tree og filene i commiten du for øyeblikket befinner deg på.
* `git diff --staged`: Samme som over, men sammenligner filene i din Staging Area med filene i commiten du for øyeblikket befinner deg på.

#### *) Om commit-meldinger

Det finnes (overraskende) sterke meninger om hvordan commit-meldinger burde formateres. De kan også være på mer enn en linje, med flere avsnitt.
For å få til dette skriver du bare `git commit`.
Da vil det åpnes en tekstbehandler med informasjon om commiten, og du kan skrive en linje øverst som en kort beskrivelse og flere avsnitt under som utdyping.
Det finnes ikke bare én stil som er korrekt, men [denne ressursen](https://chris.beams.io/posts/git-commit/) kommer med forslag til 7 regler, hvor flere er blitt nesten standard i bransjen. De er:
1. Separer overskriften fra brødteksten med en blank linje.
2. Overskriften skal ikke være lenger enn 50 karakterer (flere tekstbehandlere og GitHub kjefter på deg om du prøver deg).
3. Overskriften skal starte med stor forbokstav.
4. Overskriften skal ikke ende med punktum.
5. Overskriften skal skrives i [imperativ](https://www.sprakradet.no/sprakhjelp/Praktisk-grammatikk/Imperativ/), som en kommando. Dette er konsekvent med hvordan git sine automatiske meldinger skrives.
6. Bruk linjeskift ved 72 karakterer.
7. Bruk brødteksten til å forklare _hva_ og _hvorfor_, ikke _hvordan_.

Det viktigste er at alle teammedlemmene er enige om hvordan commit-meldinger skal formateres, og at en holder seg til retningslinjene når de først er satt.
Om dette ikke skjer blir prosjektets historie fort veldig uoversiktlig.
