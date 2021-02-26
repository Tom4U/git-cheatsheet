# Grundbefehle

### Git Dokumentation für einen Befehl
`git help [BEFEHL]`

### Erstellen eines Repository
* Mit Arbeitsbereich: `git init`
* Ohne Arbeitsbereich: `git init --bare`

### Dateien dem Staging Bereich hinzufügen
* Alle Dateien: `git add .`
* Alles, außer neue Dateien: `git add --update`
* Nur Dateien in einem bestimten Ordner: `git add ordner1`
* Mit Platzhaltern: 
  * `git add ordner1/**/*.txt` fügt alle Textdateien im Ordner _ordner1_ und dessen Unterordnern hinzu
  * `git add *.txt` fügt alle Textdateien hinzu

### Dateien dem Repository hinzufügen
* Mit Editor für die Commit Message: `git commit`
* Mit Editor und automatischem Staging aller Dateien, die nicht neu sind: `git commit -a`
* Direkt mit Commit Message: `git commit -m "Mein Commit"`
* Vorherigen Commit aktualisieren: `git commit --amend`

### Historie überprüfen
* Standard Ausgabe: `git log`
* Einzeilige Ausgabe: `git log --oneline`
* Detaillierte Ausgabe des letzten Commit: `git show`
* Ausgabe wer Zeilen einer Datei geändert hat und wann: `git blame --color-lines [PFAD_ZUR_DATEI]`
* Commits finden, die eine bestimmte Datei verändert haben: `git log --follow [PFAD_ZUR_DATEI]`
* Formatierte Ausgabe (Beispiel): `git log --pretty=format:"%h committed by %an %ar with title: %s"`
* Commits für bestimmten Zeitpunkt auflisten: 
  * Zeitangaben:
    * Relativ: `"2 days ago"` oder `"5 hours ago"`
    * Exaktes Datum: `2021-02-26`
    * Exaktes Datum und Zeit: `2021-02-26T13:00:00`
  * Nach einem bestimmten Zeitpunkt: `git log --since [ZEITANGABE]`
  * Bis zu einem bestimmten Zeitpunkt: `git log --until [ZEITANGABE]`
* Commits für einen bestimmten Ersteller auflisten: `git log --author "[NAME_ODER_TEIL_DES_NAMENS]"`
* Commits mit bestimmtem Suchbegriff in Commit Message auflisten: `git log --grep [SUCHBEGRIFF]`
* Commits auflisten, die bestimmten Begriff in Dateien hinzufügen oder entfernen: `git log -S [SUCHBEGRIFF]`

### Arbeitsbereich sichern und auf HEAD zurücksetzen
* Schnell sichern: `git stash`
* Neuesten (letzten) Stash wiederherstellen: `git stash pop`
* Neue Dateien berücksichtigen: `git stash push -u`
* Neue und ignorierte Dateien berücksichtigen: `git stash push -a`
* Mit eigener Message: `git stash push -m "WIP: Meine Sicherung"`
* Stashes anzeigen: `git stash list`
