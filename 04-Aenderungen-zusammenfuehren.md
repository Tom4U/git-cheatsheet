# Änderungen zusammenführen

## Aktuellen Stand eines anderen Branch zusammenführen
* Den aktuellen Stand eines Branch in den aktuellen Branch holen: `git merge [ANDERER_BRANCH]`
* Einen Merge mit Commit erzwingen: `git merge --no-ff [ANDERER_BRANCH]`
* Merge auf einen Working Tree anwenden, der nicht committete Dateien enthält: `git merge --autostash [ANDERER_BRANCH]`
* Einen Branch mergen, der keine gemeinsame Historie mit aktuellem Branch hat: `git merge --allow-unrelated-histories [ANDERER_BRANCH]`
* Einen Merge Vorgang bei Konflikten abbrechen: `git merge --abort [ANDERER_BRANCH]`

## Alle Commit eines Branches zusammenführen/nachspielen
* In einem (üblicherweise Feature) Branch: `git rebase [MASTER_BRANCH]`
* Ohne in einen Branch zu wechseln: `git rebase [MASTER_BRANCH] [FEATURE_BRANCH]`
* Einen Feature Branch auf den Stand eines Master Branch, statt eines Development Branch setzen: <br />`git rebase --onto [MASTER_BRANCH] [DEV_BRANCH] [FEAT_BRANCH]`
* Commits innerhalb eines Branch entfernen: <br />`git rebase --onto [BRANCH]~[AELTESTER_COMMIT] [BRANCH]~[NAECHSTER_GUELTIGER_COMMIT] [BRANCH]`
* Vorab entscheiden was zusammengeführt werden soll: `git rebase --interactive [BRANCH]`

## Bestimmten Commit in aktuellen Branch holen
* Ein oder mehrere Commits in Branch holen: `git cherry-pick [COMMIT(S)]`
* Den aktuellsten Commit eines Branch holen: `git cherry-pick [BRANCH]`
* Alle Änderungen anwenden, die mit einem Branch (DO) verwandt sind, aber nicht mit einem anderen (DONT): <br />`git cherry-pick ^[DONT_BRANCH] [DO_BRANCH]`
* Änderungen im Working Tree anwenden aber keine(n) Commit(s) erstellen: `git cherry-pick -n [...]`
* Commit(s) im Working Tree anwenden, die eine bestimmte Datei geändert haben: <br />`git rev-list --reverse [BRANCH] -- [DATEI] | git cherry-pick -n --stdin`
