
Konfigurations Dateien fuer RaspBerryPI
=======================================

Installation
------------
- Standard mittels NOOBS - http://www.raspberrypi.org/downloads

- Zus�tzliche Packete installieren:
    sudo apt-get install tightvncserver git samba arduino
    
- Arduino anschliessen    
- Arduino Entwicklungsumgebung starten und Sketchbook Verzeichnis auf /home/pi/microSRCP/microSRCP/arduino aendern
- Entwicklungsumgebung neu starten 
- Board und Serielle Schnittstelle entsprechend Board einstellen
- Sketch microSRCPSRCPSimple compilieren und uploaden in Arduino
    
- RocRail von http://rocrail.net/software/rocrail-snapshot/ downloaden
- RocRail installieren (beim ersten Befehl kommt Fehlermeldung, ignorieren)
    sudo dpkg -i rocrail-XXXX-wheezy-armhf.deb
    sudo apt-get -f install 
- WICHTIG: Device vom Arduino auf 666 setzen, z.B. sudo chmod 666 /dev/ttyUSB0, sonst kann RocRail sich nicht verbinden.   
    
- microSRCP Sourcen clonen oder ab https://github.com/mc-b/microSRCP/tags downloaden und entpacken
    git clone https://github.com/mc-b/microSRCP.git
    
- Dateien aus microSRCP/microSRCP/RocRail wie folgt kopieren:
    *.desktop nach ~/Desktop
    smb.conf nach /etc/samba
    
- microSRCP Verzeichnis �ffnen f�r Zugriff, z.B. von Windows, via \\raspberrypi
\microSRCP
    chmod -R g=u,o=u microSRCP    
    
- RaspBerryPI neu starten    
    
- X-Windows local mittels startx, oder Remote mittels vncserver und vncviewer starten
- RocRail Server und RocView starten
  
Juni 2013 / Marcel Bernet

      
