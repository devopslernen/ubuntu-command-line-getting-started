# Administrative Tätigkeiten: Root-Rechte erlangen

Als "normaler" Benutzer sind aus Sicherheitsgründen viele administrative Aufgaben nicht möglich. Vergleichbar mit dem Administrator-Konto unter Windows hat der Root-Benutzer unter Linux vollständige administrative Berechtigungen am lokalen System. Obwohl die einfachste Lösung darin besteht, sich als Root-Benutzer anzumelden, gilt dies nicht als Best Practice, da so schnell irrtümlich schwerwiegende Auswirkungen entstehen können. Einige Linux-Distributionen, darunter Ubuntu, haben daher den direkten Root-Login somit standardmäßig deaktiviert. Der `sudo`-Befehl erlaubt hingegen das Ausführen einzelner Befehle mit Root-Rechten.

**sudo-Befehl:**
- `sudo` ("Substitute User Do") erlaubt das Ausführen einzelner Befehle mit Root-Rechten.
  - Beispiel (Befehl als Superuser ausführen): `sudo befehl` - Führt den angegebenen Befehl mit Superuser-Rechten aus.
  - Beispiel (Superuser-Shell öffnen): `sudo -s` - Öffnet eine Superuser-Shell.

**sudo-Konfiguration:**
- Benutzer müssen in der `/etc/sudoers`-Datei zur Ausführung von Befehlen mit `sudo` autorisiert sein.
  - Beispiel (Benutzer zu `sudoers` hinzufügen): `sudo visudo` - Öffnet die `sudoers`-Datei im Editor zur Bearbeitung.

**su-Befehl:**

- Der `su`-Befehl ("Substitute User") ermöglicht das Ändern der Benutzersitzung.
  - Beispiel (zu einem anderen Benutzer wechseln): `su benutzer` - Wechselt zur Sitzung des angegebenen Benutzers.
  - Beispiel (zu Superuser wechseln): `su` oder `su -` - Wechselt zur Superuser-Sitzung.

**sudo und su im Vergleich:**
- `su` benötigt das Passwort des Zielbenutzers.
- `sudo` verwendet das eigene Benutzerpasswort.
- `sudo` verwenden, um einzelne Befehle auszuführen, und `su`, um vollständige Benutzersitzungen zu wechseln.
