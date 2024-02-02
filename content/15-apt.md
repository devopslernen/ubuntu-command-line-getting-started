# Softwareverwaltung mittels APT-Paketmanager 

Der Paketmanager **APT (Advanced Packaging Tool)** ermöglicht die Installation, Deinstallation und Aktualisierung von Softwarepakete.
Als Paketverwaltungssystem für Debian-Pakete, wird APT von zahlreichen Debian-basierten Distributionen wie Ubuntu oder Linux Mint eingesetzt.

- **Paketquellen (Liste an verfügbaren Paketen) aktualisieren:**
  ```bash
  sudo apt update
  ```
  
- **Softwarepakete installieren:**
  
  ```bash
  sudo apt install paketname
  ```

- **Installation einer .deb-Datei und Abhängigkeiten auflösen:**
  
  ```bash
  sudo apt install ./paketdatei.deb
  ```

- **Softwarepaket deinstallieren:**
  
  ```bash
  sudo apt remove paketname
  ```

- **Paket in Paketdatenbank suchen:**
  
  ```bash
  apt search suchbegriff
  ```

- **Verfügbare Pakete auflisten:**
  
  ```bash
  apt list
  ```

- **Installierte Pakete auflisten:**
  
  ```bash
  apt list --installed
  ```

- **Alle installierten Pakete aktualisieren:**
  
  ```bash
  sudo apt upgrade
  ```

- **Vollständige Aktualisierung, bei Bedarf nicht mehr benötigte Pakete entfernen:**
  
  ```bash
  sudo apt full-upgrade
  ```

- **Automatische Deinstallation nicht mehr benötigter Pakete und Abhängigkeiten:**
  
  ```bash
  sudo apt autoremove
  ```

- **Zwischengespeicherte Pakete aus Cache löschen:**
  
  ```bash
  sudo apt autoclean
  ```

- **Infos zu Paket anzeigen:**
  
  ```bash
  apt show paketname
  ```