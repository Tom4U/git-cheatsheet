# Tags und Branches

### Tags
* Tag für letzten Commit erstellen: `git tag [TAGNAME]`
* Tag für bestimmten Commit erstellen: `git tag [TAGNAME] [COMMIT]`
* Tag mit vollständigen Meta Informationen: 
  * Anlegen: `git tag -a [TAGNAME]`
  * Anzeigen: `git show [TAGNAME]`
* Tag löschen: `git tag -d [TAGNAME]`
* Bestehenden Tag auf anderen Commit verweisen: `git tag -f [TAGNAME] [COMMIT]`
* Alle Tags auflisten: `git tag`
* Bestimmte Tags auflisten: `git tag v1.*`

### Branches
* Branch erstellen: `git branch [BRANCHNAME]`
* Branch in Arbeitsbereich laden: `git switch [BRANCHNAME]`
* Branch erstellen und in Arbeitsbereich laden: `git switch -c [BRANCHNAME]`
* Neuen Branch mit anderem Commit, als HEAD starten und in Arbeitsbereich laden: `git switch -c [BRANCHNAME] [COMMIT]
* Branch ohne Historie erstellen: `git switch --orphan [BRANCHNAME]`
* Branches anzeigen, die bestimmten Commit enthalten: `git branch --contains [COMMIT]`
* Lokale und entfernte Branches anzeigen: `git branch -a`
* Aktuellen Branch umbenennen: `git branch -m [NEUER_NAME]`
* Beliebigen Branch umbenennen: `git branch -m [ALTER_NAME] [NEUER_NAME]`
* Branches und deren Heads anzeigen: `git show-branch`
* Branch löschen: `git branch -d [BRANCH_NAME]`
