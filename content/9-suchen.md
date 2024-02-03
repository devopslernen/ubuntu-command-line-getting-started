# Suchen mittels Konsole

## Dateien suchen mit `find`

- Verwende den Befehl `find`, um Dateien basierend auf verschiedenen Kriterien zu suchen.
- Beispiel: `find /pfad/zum/verzeichnis -name dateiname`

**Nützliche Optionen von `find`:**

- `-name muster`: Sucht nach Dateien mit einem bestimmten Namensmuster
- `-type [f|d]`: Filtert nach Dateien (`f`) oder Verzeichnissen (`d`)
- `-mtime n`: Sucht nach Dateien, die in den letzten `n` Tagen geändert wurden
- `-size n[unit]`: Sucht nach Dateien einer bestimmten Größe. Zum Beispiel: `-size +1M` für Dateien größer als 1 Megabyte
- `-exec befehl {} \;`: Führt einen Befehl für jedes gefundene Element aus.

  Beispiel: `find /pfad -type f -exec chmod 644 {} \;` ändert die Berechtigungen aller gefundenen Dateien auf 644.

## Text in Dateien suchen mit `grep` 

- Nutze `grep`, um Text in Dateien zu finden
- Beispiel: `grep "suchtext" dateiname`

**Nützliche Optionen von `grep`:**

- `-i`: Macht die Suche case-insensitive (Groß-/Kleinschreibung ignorieren)
- `-r`: Durchsucht rekursiv Verzeichnisse
- `-n`: Zeigt die Zeilennummern der Übereinstimmungen an
- `-A n`: Zeigt `n` Zeilen nach einer Übereinstimmung
- `-B n`: Zeigt `n` Zeilen vor einer Übereinstimmung
- `-C n`: Zeigt `n` Zeilen vor und nach einer Übereinstimmung
- `-v`: Zeigt Zeilen an, die **nicht** mit dem Suchmuster übereinstimmen
