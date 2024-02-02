# Operationen für Dateien & Verzeichnisse:

Dateien erstellen:

```bash
touch new_file.txt
# Erstellt eine leere Datei mit dem Namen "new_file.txt"

touch documents/updated_file.txt
# Aktualisiert die Zeitstempel einer existierenden Datei ("updated_file.txt") oder erstellt sie, falls sie nicht existiert
```


Verzeichnisse anlegen:

```bash
mkdir documents images
# Verzeichnisse "documents" und "images" erstellen

mkdir -p projects/code/project1
# Verzeichnisse "projects", "code" und "project1" erstellen
```

Dateien und Verzeichnisse kopieren:

```bash
cp file.txt backup_file.txt
# Datei "file.txt" nach "backup_file.txt" kopieren

cp file1.txt file2.txt documents
# Dateien "file1.txt" und "file2.txt" nach "documents" kopieren

cp -r images projects backup
# Verzeichnisse "images" und "projects" rekursiv (inkl. aller Unterordner und enthaltenen Dateien) nach "backup" kopieren
```

Dateien und Verzeichnisse verschieben (umbenennen):

```bash
mv file.txt new/location/
# Verschiebt die Datei "file.txt" in das Verzeichnis "new/location/"

mv documents backup/documents/
# Verschiebt alle Dateien und Unterverzeichnisse aus "documents" in das Verzeichnis "backup/documents/"
```

Dateien und Verzeichnisse löschen:


```bash
rm file
# Date "file" löschen

rm -r documents
# Verzeichnis "documents" und dessen Inhalt rekursiv löschen
```
