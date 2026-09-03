# Setup-Prüfliste

Diese Liste arbeitet dein Agent für dich ab. Du kannst sie natürlich auch selbst durchgehen.

## 1 · Git

```bash
git --version
```

Erwartet: eine Versionsnummer, 2.x oder höher.

## 2 · Repo-Zugang

Du liest diese Datei — dann hat das Klonen funktioniert und Punkt 2 ist erledigt.

```bash
git remote -v
git status
```

Erwartet: `origin` zeigt auf dieses Repo, Arbeitsverzeichnis ist sauber.

## 3 · Node.js und npm

```bash
node --version
npm --version
```

Erwartet: Node 20 oder höher.

**Zusatzprüfung Firmenproxy** — der eigentliche Grund für diesen Punkt:

```bash
npm ping
```

Erwartet: eine Antwort von der Registry. Bleibt es hängen oder kommt ein Zertifikatsfehler, liegt es am Proxy. Das ist der häufigste Stolperstein, und er fällt nie bei der Installation auf, sondern immer beim ersten Download.

## 4 · Coding-Agent

Du redest gerade mit ihm — dann ist er installiert, angemeldet und lizenziert. Punkt 4 ist erledigt.

Falls du diese Liste von Hand durchgehst: Es reicht nicht, den Agenten installiert zu haben. Er muss einmal gestartet und eine Frage beantwortet haben. Login und Lizenz fallen erst dabei auf.

## 5 · VS Code

```bash
code --version
```

Erwartet: eine Versionsnummer. Kommt „command not found", ist VS Code entweder nicht installiert oder der `code`-Befehl nicht im Pfad — in VS Code über die Befehlspalette „Shell Command: Install 'code' command in PATH" nachrüsten.

VS Code brauchen wir, um Änderungen am Code zu lesen. Das ist in der Session wichtiger, als es jetzt klingt.

## 6 · Schreibprobe

```bash
echo "test" > spielwiese/probe.txt
git status
```

Erwartet: Git zeigt die neue Datei als unversioniert an. Danach wieder löschen.

Das prüft, dass du im Ordner tatsächlich schreiben darfst — bei manchen Konfigurationen von synchronisierten Laufwerken ist das nicht so.

---

## Was der Agent am Ende liefern soll

Eine Tabelle mit sechs Zeilen, je Punkt **erledigt** oder **fehlt**, bei „fehlt" mit der konkreten Fehlermeldung. Keine Vermutungen, keine Reparaturversuche ohne Rückfrage.
