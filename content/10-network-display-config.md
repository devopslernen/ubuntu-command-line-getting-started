# Netzwerkkonfiguration anzeigen und testen: Grundlegende Befehle

Um die Netzwerkkonfiguration auf einem Linux-System zu verifizieren, sind folgende grundlegende Befehle äußerst hilfreich: 

* **`ip addr` oder `ip a`- Infos über Netzwerkschnittstellen anzeigen:**
   Zeigt die Netzwerkschnittstellen auf dem System an, u.a. inklusive IP-Adressen und Statusinformationen.
* **`cat /etc/resolv.conf` - enthält die DNS-Konfiguration:**
   Textdatei, enthält Informationen darüber enthält, wie das System DNS (Domain Name System) Anfragen auflösen soll.
* **`ping <host>` - Netzwerkkonnektivität prüfen:**
   Überprüft die Erreichbarkeit eines Hosts über das Netzwerk.
* **`traceroute <host>` - Netzwerkpfad und verfolgen:**
   Verfolgt den Pfad, den IP-Pakete zu einem bestimmten Host nehmen.
   Wird gerne verwendet, um Verbindungsprobleme zu analysieren.
* **`hostname` oder `cat /etc/hostname`- Hostname anzeigen:**
   Zeigt den aktuellen Hostnamen des Systems an.
* **`hostnamectl set-hostname <neuerhostname>` - Hostnamen ändern:**
   Ändert den Hostnamen des Systems.
* **`dhclient <interface>` - EINMALIGE DHCP-Konfiguration für Schnittstelle <interface> durchführen:**
   Ermöglicht temporär eine DHCP-Konfiguration für eine bestimmte Netzwerkschnittstelle.
* **`netstat` - Netzwerkverbindungen anzeigen und analysieren:**
   Netstat (Network Statistics) wird verwendet, um verschiedene Informationen über das Netzwerkverbindungen auf dem lokalen Hosts anzuzeigen.
   Einfach zu merken: `netstat -tulpen`:
   - Alle TCP-Verbindungen (`-t`).
   - Alle UDP-Verbindungen (`-u`).
   - "Listening" Sockets anzeigen (`-l`).
   - Prozessinformationen (`-p`).
   - Erweiterte Informationen (`-e`).
   - Verwendung von numerischen Adressen (`-n`).