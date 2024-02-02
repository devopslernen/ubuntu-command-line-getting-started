# Übung: Shell-Skript

Dieses Skript ermöglicht es dem Benutzer, ein angegebenes Verzeichnis zu sichern:

* es erstellt im Homeverzeichnis ein Verzeichnis mit dem aktuellen Datum im Namen
* kopiert die Dateien aus dem Quellverzeichnis bei Bedarf in dieses 
* optional kann eine tar.gz-Datei erstellt werden, welches die Daten aus dem Quellverzeichnis enthält

```bash
#!/bin/bash

# Benutzereingabe für das Quellverzeichnis
echo "Welches Verzeichnis soll gesichert werden?"
read quellverzeichnis

# Aktuelles Datum im Format JJJJMMTT
aktuelles_datum=$(date +"%Y%m%d")

# Erstellung des Backup-Datum-Verzeichnisses im Homeverzeichnis
backup_verzeichnis="$HOME/Backup-$aktuelles_datum"
mkdir -p $backup_verzeichnis

# Benutzereingabe für die Auswahl der Aktionen
echo "Möchtest du eine .tar.gz-Datei erstellen? (j/n)"
read tar_erstellen

echo "Möchtest du Kopien der Dateien anlegen? (j/n)"
read kopien_erstellen

# Kopieren der Dateien in das Backup-Datum-Verzeichnis, falls angegeben
if [ "$kopien_erstellen" == "j" ]; then
  cp -r $quellverzeichnis/* $backup_verzeichnis/
  echo "Dateien wurden ins $backup_verzeichnis Verzeichnis kopiert."
fi

# Erstellen der tar.gz-Datei, falls angegeben
if [ "$tar_erstellen" == "j" ]; then
  tar -czvf $backup_verzeichnis/backup_$aktuelles_datum.tar.gz -C $quellverzeichnis .
  echo "tar.gz-Datei wurde im $backup_verzeichnis Verzeichnis erstellt."
fi

echo "Backup abgeschlossen."
```

