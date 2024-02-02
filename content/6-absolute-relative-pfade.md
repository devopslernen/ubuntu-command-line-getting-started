# Absolute und relative Pfade

**Absoluter Pfad:** startet mit **"/"**, listet alle Verzeichnisse/Dateien ausgehend vom root-Verzeichnis auf.

**Relativer Pfad:** startet **nicht** mit **"/"**, sondern listet alle Verzeichnisse/Dateien ausgehend vom **aktuellen Verzeichnis** auf.

Beispiele:
```bash
ls /etc/fstab # absoulut
ls /home/myuser/myfile # absolut

cd /etc/
ls fstab # relativ

cd /home/myuser # or "cd ~"
ls myfile #relativ
```
