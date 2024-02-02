# Erstellen und entpacken von Archiven: Eine Kurzübersicht

Neben dem bekannten **".zip"-Format**, stößt man im Linux-Umfeld auch oft auf **".tar"**- bzw. **".tar.gz"**-Archive.
Nachfolgend ist der Umgang mit diesen Formaten innerhalb der Konsole zusammengefasst.

- **tar-Kommando:**
  - Ermöglichen das Erstellen, Anzeigen und Extrahieren von tar-Archiven.
  - **Beispiel (erstellen):** `tar cvf archiv.tar datei1 datei2` - Erstellt ein Archiv namens "archiv.tar" mit den angegebenen Dateien.
  - **Beispiel (entpacken):** `tar xvf archiv.tar` - Entpackt das Archiv "archiv.tar".
  - **Hinweis:** Die Dateiendung ".tar.gz" wird oft auch als ".tgz" abgekürzt.
  - **Optionen von tar:**
    - **`c` (create):** Erstellt ein neues Archiv.
    - **`v` (verbose):** Gibt detaillierte Informationen über den Prozess aus.
    - **`f` (file):** Legt den Dateinamen des Archivs fest.
    - **`x` (extract):** Entpackt ein vorhandenes Archiv.
    - **`t` (list):** Zeigt den Inhalt eines Archivs an.
  
- **tar.gz-Dateien**
  - Die tar-Option `z` komprimiert/dekomprimiert Archive mit gzip.
  - **Beispiel (erstellen):** `tar czvf archiv.tar.gz datei1 datei2` - Erstellt ein komprimiertes Archiv "archiv.tar.gz".
  - **Beispiel (entpacken):** `tar xvzf archiv.tar.gz` - Entpackt das komprimierte Archiv "archiv.tar.gz".

- **zip- und unzip-Kommando:**
  - Ermöglichen das Erstellen, Anzeigen und Extrahieren von ZIP-Archiven.
  - **Beispiel (erstellen):** `zip -r archiv.zip verzeichnis1/ verzeichnis2/` - Erstellt ein ZIP-Archiv aus den angegebenen Verzeichnissen.
  - **Beispiel (entpacken):** `unzip archiv.zip` - Entpackt das ZIP-Archiv.
