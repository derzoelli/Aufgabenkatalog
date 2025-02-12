Aufgabenkatalog zum Thema Linux zur selbständigen Bearbeitung durch die Teilnehmer.

Um die folgenden Aufgaben lösen zu können, müssen Sie sich per SSH an einer Linux VM anmelden. Bitte dokumentieren Sie ihre Arbeitsschritte nachvollziehbar, so dass Probleme im Anschluss evtl. zusammen gelöst werden können.

Alle Aufgaben beziehen sich auf die aktuelle Version von Ubuntu Server 22.04 LTS. 

Bitte führen Sie die Befehle nur dann mit Admin Rechten aus (`sudo`), wenn Sie in der Aufgabenstellung dazu aufgefordert werden.

***

# 1. Einführung in Linux und die Shell

#### **Ziel:** Entwicklung eines grundlegenden Verständnisses für das Linux-Betriebssystem und die Shell.

#### Hilfe: 

- - Spedtest: https://www.speedtest.net/de/apps/cl

**Aufgaben**:

- **Aufgabe 1.1:** Geben Sie den Befehl `uname -a` ein, um Systeminformationen anzuzeigen. Was bedeutet die Ausgabe und welche Informationen enthält sie?

- **Aufgabe 1.2:** Ermitteln sie die aktuelle Systemauslastung mit dem Befehl `htop`
- **Aufgabe 1.3:** Nutzen Sie den Befehl ip -a um sich ihre aktuelle IP Adresse anzeigen zu lassen
- **Aufgabe 1.4:** Nutzen Sie den Befehl `ping` um die Verbindung zu einem beliebigen Host zu testen 
- **Aufgabe 1.5:** Installieren Sie das tool `speedtest`um ihre aktuelle Verbindungsgeschwindigkeit zu testen
- **Aufgabe 1.6:** Überprüfen Sie mit dem Befehl `ps` welche Prozesse aktuell auf ihrem System laufen





# 2. Dateisystem und Navigation

#### **Ziel:** Die Teilnehmer sollen das Linux-Dateisystem verstehen und sich sicher darin bewegen können.

#### Hilfe: 

- Verzeichnisse: https://wiki.ubuntuusers.de/Verzeichnisstruktur/
- Navigations Befehle:

  - https://www.pluralsight.com/resources/blog/guides/beginner-linux-navigation-manual
  - https://contabo.com/blog/linux-navigation-and-file-management/


**Aufgaben:** 

- **Aufgabe 2.1:** Dokumentieren Sie alle grundlegenden Befehle zur Navigation im Dateisystem
- **Aufgabe 2.2:** Finden Sie heraus, in welchem Verzeichnis Sie sich befinden (`pwd`).
- **Aufgabe 2.3:** 

  - Wechseln Sie mittels `cd` Befehl in das Root Verzeichnis
  - Lassen Sie sich mittels `ls` Befehl alle Unterverzeichnisse anzeigen 
  - Listen Sie die Standard Verzeichnisstruktur auf und erklären sie, wofür die einzelnen Verzeichnisse benötigt werden

- **Aufgabe 2.4:** 

  - Wechseln Sie in das `/temp` Verzeichnis
  - Legen Sie nun ein neues Verzeichnis an (`mkdir`) 
  - Starten sie die Maschine nun mittels <code><span style="color:rgba(245,158,11,1)">sudo reboot</span></code> neu
  - Kehren sie in das `/temp` Verzeichnis zurück und suchen sie das eben neu erstellte Verzeichnis
  - Erklären Sie, warum sie das neue Verzeichnis nun nicht mehr auffinden können

- **Aufgabe 2.5:** 

  - Wechseln Sie anschließend in das `/mnt` Verzeichnis und versuchen sie ein Unterverzeichnis anzulegen (`mkdir`)
  - Falls diese Operation fehlschlagen sollte, geben Sie bitte den Grund dafür an

- **Aufgabe 2.6:**

  - Legen Sie ein Verzeichnis im Verzeichnis `/tmp` an
  - Kopieren sie dieses Verzeichnis nun in ihren Benutzerordner (`cp`)
  - Wechseln sie in ihr Benutzerverezichnis und kontrollieren sie, dass das neue Verzeichnis dort vorhanden ist
  - Wechseln sie zurück in das `/temp` Vereichnis und löschen sie das ursprünglich angelegte Verzeichnis (`rmdir`)

- **Aufgabe 2.7:** 

  - Legen Sie ein weiteres Verzeichnis im Verzeichnis `/tmp` an
  - Verschieben Sie das Verzeichnis nun in ihren Benutzerordner (`mv`)
  - Überprüfen sie mittels `ls` im Verzeichnis `/tmp`ob das Verschieben erfolgreich war
  - Überprüfen sie anschließend in ihrem Benutzerverzeichnis, ob das Verzeichnis dort vorhanden ist

- **Aufgabe 2.8:** 

  - Installieren sie `tree` und nutzen sie das tool um sich die Hierarchie des Root Verzeichnis anzeigen zu lassen

    


  


# 3. Dateimanipulation

#### **Ziel:** Die Teilnehmer sollen grundlegende Dateimanipulationsbefehle kennen und sicher anwenden können.

**Aufgaben:** 

- **Aufgabe 3.1:** 

  - Erstellen Sie ein neues Verzeichnis in ihrem Benutzerordner 
  - Legen Sie dort anschließend eine Datei mit dem Befehl `touch` an
  - Öffnen Sie die Datei mit dem Texteditor `nano` und tragen Sie einen beliebigen Text ein
  - Lassen sie sich den Inhalt der Textdatei mit dem Befehl `echo` in der Shell ausgeben

- **Aufgabe 3.2:** 

  - Erstellen Sie ein weiteres Verzeichnis und kopieren sie die Datei in das neue Verzeichnis 
  - Prüfen Sie ob sie die Datei im neuen Verzeichnis finden können
  - Löschen sie die Datei anschließend

- **Aufgabe 3.3:** 

  - Verschieben sie die Datei nun in das neu erstellte Verzeichnis 
  - Prüfen Sie ob sie die Datei im neuen Verzeichnis finden können
  - Prüfen Sie ob die Datei im ursprungs Verzeichnis noch vorhanden ist

- **Aufgabe 3.4:**

  - Erstellen Sie das neue Verzeichnis `script`und wechseln Sie in das erstellte Verzeichnis 
  - Erstellen sie die Datei `script.sh` innerhalb des Verzeichnisses und füllen Sie sie mit folgendem Inhalt: 

    ```bash
    #!/bin/bash
    echo "Hallo, $(whoami)! Willkommen auf deinem Linux-System!"
    ```

  - Nutzen Sie den Befehl `chmod +x script.sh`um das Script ausführbar zu machen
  - Führen Sie das Script über den folgenden Befehl aus `./script.sh`

- **Aufgabe 3.5:** 

  - Erstellen Sie ein neues Verzeichnis im ihrem Benutzerverzeichnis 
  - Nutzen den Befehl `tar` um das Verzeichnis in ein Archiv zu packen
  - Nutzen Sie den Befehl erneut um das Archiv wieder zu entpacken 


#### 



# 4. Benutzer und Berechtigungen

#### **Ziel:** Die Teilnehmer sollen den Umgang mit Benutzerkonten und Datei-Berechtigungen erlernen.

#### Hilfe: 

- chmod: https://wiki.ubuntuusers.de/chmod/
- chgrp: https://wiki.ubuntuusers.de/chgrp/
- 

<br/>

- **Aufgabe 4.1:**

  - Erstellen Sie mit dem Befehl `sudo adduser` die zwei neuen User `user1 & user2`
  - Nutzen Sie `nano` um die Datei `/etc/passwd` zu öffnen
  - Kontrollieren Sie ob die User angelegt wurden
  - Kontrollieren sie ob die Benutzerordner für die beiden neuen User angelegt wurden

- **Aufgabe 4.2:**

  - Wechseln Sie mit dem Befehl `su` zu `user1`, erstellen Sie im Verzeichnis `/tmp` das Unterverzeichnis `user1` und die Textdatei `user1.txt`
  - Wechseln Sie nun zu `user2` und versuchen Sie die Datei user1.txt zu bearbeiten
  - Wechseln Sie zurück zu `user1` und passen Sie die Zugriffsrechte des Verzeichnisses `/tmp/user1` mit `chmod` so an, dass alle User das Verzeichnis öffnen dürfen
  - Wechseln Sie nun zu `user2` und versuchen erneut die Textdatei `user1.txt` zu bearbeiten
  - Falls das nicht gelingt, erklären Sie bitte, warum dem so ist

- **Aufgabe 4.3:**

  - Wechseln sie mit dem Befehl `sudo su root` zum Admin Benutzer und passen sie die Zugriffsrechte des Verzeichnisses `/tmp/user1` rekursiv so an, dass alle Benutzer des Systems das Verzeichnis öffnen dürfen 
  - Wechseln Sie nun erneut zu `user2` und versuchen Sie noch einmal die Textdatei zu bearbeiten
  - Überprüfen Sie die Zugrifsrechte der Datei `user1.txt` und des Verzeichnisses `user1` mit `ls-l`

- **Aufgabe 4.4:** 

  - Erstellen sie mit dem Befehl `addgroup` die neue gruppe `permissiontest`
  - Überprüfen Sie die korrekte Erstellung der neuen Gruppe mit dem Befehl `compgen -g`
  - Fügen Sie `user1` & `user2` der neuen Gruppe `permissiontest` hinzu (`adduser`)
  - Legen sie ein neues Unterverzeichnis mit `user1` im Verzeichnis `/tmp` an
  - Wechseln sie zu `user2` und versuchen Sie das durch `user1` erstellte Verzeichnis zu öffnen

- **Aufgabe 4.5:** 

  - Erstellen Sie ein neues Verzeichnis 
  - Nutzen sie nun den Befehl `sudo chgrp` um das Verzeichnis der Gruppe `permissiontest` zuzuweisen



  **Aufgabe 4.6:** 

  - Nutzen sie nun den Befehl `sudo chown` um das Verzeichnis einem neuen Besitzer zuzuweisen






# 5. Paketmanagement

#### **Ziel:** Die Teilnehmer sollen mit dem Paketmanagement in Linux vertraut werden, um Software zu installieren und zu verwalten.

**Aufgaben:**



**Aufgabe 5.1**: Entfernen eines Pakets

- Deinstallieren Sie das installierte Paket `htop`:

  ````
  sudo apt remove htop
  ````

- Überprüfen Sie, ob das Programm entfernt wurde, indem Sie versuchen, es zu starten.

**Aufgabe 5.2:** Installieren eines Pakets

- Installieren Sie das Paket `htop`erneut

  ````
  sudo apt install htop
  ````

- Starten Sie das Programm:`htop`

**Aufgabe 5.3:** Informationen zu einem Paket abrufen

- Finden Sie Informationen über das Paket `curl`:

  ````
  apt show curl
  ````

  - - Was ist die Beschreibung des Pakets?
    - Welche Version ist verfügbar?
    - Welche Abhängigkeiten hat das Paket?

- **Aufgabe 5.4:** Nutzen Sie den befehl `apt list`um sich alle installierten Pakete anzeigen zu lassen. Hinweis: Der Befehl muss um eine Flag ergänzt werden







# 6. Prozesse und Systemüberwachung

#### **Ziel**: Die Teilnehmer sollen lernen, wie man Prozesse überwacht und verwaltet.

**Aufgaben:**

- Aufgabe 6.1:

  - Lassen sie sich die aktuell laufenden Prozesse mit dem Befehl `ps` anzeigen
  - Lassen sie sich die aktuell laufenden Prozesse mit dem Befehl `top` anzeigen












# 7. Netzwerkkonfiguration und -diagnose

#### **Ziel:** Die Teilnehmer sollen grundlegende Netzwerkinformationen abrufen und Netzwerkprobleme diagnostizieren können.

#### Hilfe: 





**Aufgaben:**











# 8. Cronjobs und Automatisierung

#### **Ziel:** Die Teilnehmer sollen einfache Aufgaben automatisieren können.

**Aufgaben:**













# 9. Grundlagen der Sicherheit

#### **Ziel:** Die Teilnehmer sollen ein grundlegendes Verständnis für die Sicherheitspraktiken in Linux haben.

**Aufgaben:**















# 10. Erstellung eines einfachen Webservers

#### **Ziel:** Die Teilnehmer sollen eine einfache Serverumgebung aufbauen und betreiben können.

**Aufgaben:** 

**Aufgabe 10.1:**

- Aktualisieren Sie zunächst die Pakete mit `sudo apt update`
- Installieren Sie nun den Apache Webserver 

  ```bash
  sudo apt install apache2 -y
  ```

- Prüfen Sie nun ob der Webserver automatisch gestartet ist

  ```bash
  sudo systemctl status apache2
  ```

  - Falls der Dienst nicht läuft, starten Sie ihn

    ```bash
    sudo systemctl start apache2
    ```


- Navigieren Sie in das Verzeichnis, in dem Apache die Webseiten bereitstellt:

  ```bash
  cd /var/www/html
  ```

- Erstellen Sie eine neue HTML-Datei:

  ```bash
  sudo nano index.html
  ```

- Schreiben Sie den folgenden HTML-Code in die Datei:

  ```html
  <!DOCTYPE html>
  <html>
  <head>
      <title>Meine erste Webseite</title>
  </head>
  <body>
      <h1>Willkommen auf meiner ersten Webseite!</h1>
      <p>Diese Seite wurde mit Apache ausgeliefert.</p>
  </body>
  </html>
  b
  ```

- Speichern Sie die Datei mit `Ctrl+O`, drücken Sie `Enter`, und verlassen Sie den Editor mit `Ctrl+X`.
- Stellen Sie sicher, dass die Datei die richtigen Berechtigungen hat:

  ````
  sudo chmod 644 index.html
  ````

- Überprüfen Sie den Eigentümer der Datei:

  ````
  ls -l
  ````

- Der Besitzer sollte `root` sein, und die Datei sollte lesbar sein.
- Schalten Sie Port 80 extern frei und testen Sie ob die Website erreichbar ist



# Bonusaufgaben:

Aufgabe 1: Kommandozeilen Spiele 

Hilfe: https://itsfoss.com/best-command-line-games-linux/

- Installieren Sie einige Kommandozeilen Spielen und testen Sie sie

Aufgabe 2: Wordpress Installation 

Hilfe: https://www.digitalocean.com/community/tutorials/install-wordpress-on-ubuntu


