# Mit Dateien arbeiten

### Dateien wiederherstellen und zurücksetzen
* Änderungen bekannter Dateien zurücksetzen: `git restore [PFAD]`
* Aus Staging Bereich entfernen: `git restore -S [PFAD]`
* Beide oberen Arbeiten zusammen: `git restore -W -S [PFAD]`
* Änderungen auf bestimmten Commit zurücksetzen: `git restore -s [COMMIT] [PFAD]`

### Dateien im Index und Arbeitsbereich auflisten
* Gecachte Dateien: `git ls-files`
* Andere Datei Stati: `git ls-files -[CHAR]`
  * [CHAR]:
    * d = gelöschte Dateien
    * i = ignorierte Dateien 
    * m = geänderte Dateien
    * u = Dateien die nicht gemergt wurden
    * o = andere Dateien (z.B. neue Dateien)
* Einen Befehl auf jede einzelne Datei anwenden: `git ls-files -z | xargs -0 [BEFEHL]`

### Dateien löschen
* Beim löschen für die erste Ausführung besser mit Option `-n`!
* Datei aus dem Index und dem Arbeitsbereich löschen: `git rm [PFAD]`
* Datei nur aus dem Index löschen: `git rm --cached [PFAD]`
* Ganze Verzeichnisse löschen: `git rm -r [PFAD]`
