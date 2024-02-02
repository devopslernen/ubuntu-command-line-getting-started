# Ein- und Ausgabeumleitung

1. **Ausgabeumleitung**
   - **`>`: Standardausgabe umleiten**
     - Schreibt die Standardausgabe (STDOUT) eines Befehls in eine Datei oder ein schreibbares Gerät. Existiert die Datei, wird sie überschrieben.
     - **Beispiel:** `ls > dateiliste.txt` - Speichert die Dateiliste des aktuellen Verzeichnises in "dateiliste.txt".
     - **Beispiel:** `cat /dev/sda >/dev/sdb` - Kopiert den Inhalt des schreibbaren Geräts `/dev/sda` in das schreibbare Gerät `/dev/sdb`.
   - **`>>`: Standardausgabe anhängen**
     - Hängt die Standardausgabe (STDOUT) eines Befehls an eine Datei oder ein schreibbares Gerät an oder erstellt diese, wenn nicht vorhanden.
     - **Beispiel:** `echo "Neuer Text" >> datei.txt` - Fügt "Neuer Text" zur Datei "dateiliste.txt" hinzu.
   - **`2>`: Standardfehler umleiten**
     - Schreibt die Standardfehlerausgabe (STDERR) eines Befehls in eine Datei oder ein schreibbares Gerät.
     - **Beispiel:** `befehl 2> fehlermeldung.txt` - Speichert Fehlermeldungen des Befehls in "fehlermeldung.txt".
   - **`&>`: Umleitung von STDOUT und STDERR**
     - Schreibt sowohl die Standardausgabe (STDOUT) als auch die Standardfehlerausgabe (STDERR) eines Befehls in eine Datei oder ein schreibbares Gerät.
     - **Beispiel:** `befehl &> ausgabe_und_fehler.txt` - Speichert Ausgabe und Fehlermeldungen des Befehls in "ausgabe_und_fehler.txt".
2. **Eingabeumleitung**
   - **`<`: Standardeingabe umleiten**
     - Liest die Eingabe eines Befehls aus einer Datei oder aus einem Gerät anstelle der Standardeingabe (STDIN).
     - **Beispiel:** `wc -l < dateiname.txt` - Zählt die Zeilen innerhalb der angegeben Datei.
3. **Pipes**
   - **`|`: Pipe**
     - Leitet die Standardausgabe (STDOUT) eines Befehls direkt an einen anderen Befehl (STDIN) weiter.
     - **Beispiel:** `ls -l | grep ".*.txt"` - Zeigt Dateien mit ".txt" im aktuellen Verzeichnis an.
4. **tee-Kommando**
   * Ermöglicht es, die Ausgabe anzuzeigen und gleichzeitig in einer Datei zu speichern
   * **Beispiel:** `ls -l | tee dateiliste.txt` - Speichert die Dateiliste des aktuellen Verzeichnisses in "dateiliste.txt" und gibt diese innerhalb der Shell aus.
