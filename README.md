# Git-Workshop Aufgabe-2

**GGit Workshop: Kooperative Erstellung eines fiktiven Abspanns**

#### Aufgabenstellung

1. **Repository Initialisierung:**
   - Ein Teilnehmer erstellt ein neues privates Git-Repository auf GitHub und fügt eine Datei namens `abspann.txt` hinzu
   - Der Teilnehmer soll andere Mitglieder als Collaborators hinzufügen
     
2. **Klonen des Repositories:**
   - Jeder Teilnehmer klont das Repository auf seine lokale Maschine:
     ```bash
     git clone <repository-url>
     ```

#### Regeln und Ablauf

1. **Eigenständige Arbeit:**
   - Jeder Teilnehmer arbeitet ausschließlich auf seinem eigenen Klon des Repositories. Änderungen werden lokal vorgenommen.

2. **Startsignal:**
   - Sobald alle Teilnehmer das Repository geklont haben, beginnt die Zeit. Die Teilnehmer können jetzt beginnen, Rollen und Namen zu `abspann.txt` beizutragen.

3. **Beitragsregeln:**
   - Jeder Commit darf nur entweder eine neue Rolle eintragen oder einen Namen in eine bestehende Rolle eintragen. 
   - Beispiel für eine neue Rolle:
     ```plaintext
     Regisseur:
     ```
   - Beispiel für einen neuen Namen in eine Rolle:
     ```plaintext
     Regisseur: <Mein-Name>
     ```
   - Es ist nicht erlaubt, den Namen anderer Leute einzutragen.
   - Es ist auch nicht erlaubt, den eigenen Namen in selbst eingetragene Rollen einzutragen.

4. **Commit-Bedingungen:**
   - Bevor ein neuer Beitragscommit erstellt wird, muss der vorherige Commit bereits Vorfahre des `main`-Branches auf dem Server-Repo sein. Das bedeutet, dass nach jedem Commit ein `git pull` und `git push` notwendig ist, um sicherzustellen, dass alle Änderungen integriert sind.
     - Beispielablauf:
       ```bash
       git add abspann.txt
       git commit -m "Added role: Regisseur"
       git pull origin main
       # Auflösen von möglichen Konflikten
       git push origin main
       ```

5. **Konfliktlösung:**
   - Bei Merge-Konflikten, die entstehen, wenn zwei Teilnehmer gleichzeitig an der gleichen Rolle arbeiten, muss einer der Teilnehmer die Rolle aufgeben und eine neue Rolle eintragen. Der Konflikt wird manuell gelöst, indem die Konfliktbereiche in der `abspann.txt` bearbeitet werden.

6. **Abschlussbedingungen:**
   - Die Aufgabe endet, wenn auf dem `main`-Branch des Server-Repos eine `abspann.txt`-Datei vorhanden ist, in der jeder Teilnehmer mindestens fünf Rollen hat und keine zwei Teilnehmer sich eine Rolle teilen. 

#### Beispiel für `abspann.txt`

```plaintext
Regisseur: John Doe
Produzent: Jane Smith
Drehbuchautor: Max Mustermann
Kameramann: John Doe
Schnitt: Jane Smith
```
