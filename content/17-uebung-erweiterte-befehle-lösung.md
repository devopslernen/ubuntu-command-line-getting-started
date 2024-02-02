# Lösung für Übung: erweiterte Befehle

1. Finde heraus, in welchem Verzeichnis sich die Datei **"sshd_config"** befindet.
   ```bash
   find / -name "sshd_config"
   ```

2. Leite beim Suchvorgang die Fehlermeldungen nach **"/dev/null"** um.
   ```bash
   find / -name "sshd_config" 2>/dev/null
   ```

3. Welche Informationen enthält die Datei **"sshd_config"**? Lass dir denn Inhalt der Datei ausgeben.
   ```bash
   less /etc/ssh/sshd_config
   ```

4. Filtere den Output der Datei nach dem Muster **".\*Port.\*"**
   ```bash
   grep ".*Port.*" /etc/ssh/sshd_config
   ```

5. Finde folgende Informationen über die Datei **"sshd_config"** heraus: Besitzer, Gruppenzugehörigkeit, Zugriffsrechte

   ```bash
   ls -l /etc/ssh/sshd_config
   ```

6. Lege ein Verzeichnis namens "backup" in deinem Homeverzeichnis an. Kopiere die Datei **"sshd_config"** in dieses Verzeichnis.
   ```bash
   mkdir ~/backup
   cp /etc/ssh/sshd_config ~/backup
   ```

7. Erstelle eine .tar-Datei, welche das erstellte Verzeichnis "backup" inklusive dem Inhalt enthält.
   ```bash
   tar cvf backup.tar ~/backup
   ```

8. Lösche die erstellte .tar-Datei und das Verzeichnis "backup" wieder.
   ```bash
   rm backup.tar
   rm -r ~/backup
   ```

9. Welcher Prozess verursacht am System aktuelle die höchste CPU-Auslastung?

   ```bash
   top
   ```

10. Läuft aktuell ein Prozess namens sshd?
   ```bash
   ps axu | grep sshd
   ```

11. Wie kannst du weitere Informationen zur Verwendung des SSH-Befehls erhalten?
    ```bash
    ssh --help
    man ssh
    ```

12. Zeige die aktuelle IP-Adresse und den Hostnamen des Systems an.
    ```bash
    ip a
    hostname
    ```
