# Git-Workshop Aufgabe 4

**Git Workshop: Kooperative Erstellung eines fiktiven Abspanns**

#### Aufgabenstellung
Erstellt gemeinsam einen fiktiven Abspann (wie für einen Film) in der Datei abspann.txt. Jeder Teilnehmer trägt abwechselnd neue Rollen oder Namen ein und führt regelmäßig Commits durch, um die Änderungen ins zentrale Repository zu integrieren. Die Zeilen dieses Abspanns
sollten aussehen wie: 
- Rolle: Name (z.B. Regissuer: John Doe)

1. **Token genrieren und Repository Initialisierung:**
   - Token generieren über: https://github.com/settings/tokens
      - New personal access token (classic) auswählen
      - Name für Token eingeben   
      - Unter select scopes 'repo' auwählen und Token generieren
   - Ein Teilnehmer erstellt ein neues privates Git-Repository auf GitHub und fügt eine Datei namens `abspann.txt` hinzu
   - Der Teilnehmer soll andere Mitglieder als Collaborators hinzufügen
     
3. **Klonen des Repositories:**
   - Jeder Teilnehmer klont das Repository auf seine lokale Maschine:
     ```bash
     git clone https://[username]:[token]@[repository-url]
     ```

#### Regeln und Ablauf

1. **Eigenständige Arbeit:**
   - Jeder Teilnehmer arbeitet ausschließlich auf seinem eigenen Klon des Repositories. Änderungen werden lokal vorgenommen.

2. **Beitragsregeln:**
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
   - Man darf nur dann wieder was pushen, wenn mindestens ein Teammitglied eine Rolle oder einen Namen in das Repository gepusht hat.

5. **Konfliktlösung:**
   - Bei Merge-Konflikten, die entstehen, wenn zwei Teilnehmer gleichzeitig an der gleichen Rolle arbeiten, muss einer der Teilnehmer die Rolle aufgeben und eine neue Rolle eintragen. Der Konflikt wird manuell gelöst, indem die Konfliktbereiche in der `abspann.txt` bearbeitet werden.

6. **Abschlussbedingungen:**
   - Die Aufgabe endet, wenn auf dem `main`-Branch des Server-Repos eine `abspann.txt`-Datei vorhanden ist, in der jeder Teilnehmer mindestens drei Rollen hat und keine zwei Teilnehmer sich eine Rolle teilen. 

#### Beispiel für `abspann.txt`

```plaintext
Regisseur: John Doe
Produzent: Jane Smith
Drehbuchautor: Max Mustermann
Kameramann: John Doe
Schnitt: Jane Smith
etc.
```

# Hinweis für benötigte Befehle

<details>
  <summary>Klicke hier, wenn du Hilfe benötigst</summary>
  
  - Beispielablauf:
    ```bash
    git add abspann.txt
    git commit -m "Added role: Regisseur"
    git pull 
    # Auflösen von möglichen Konflikten
    git push 
    ```

</details>
