# MatrixKeypad
Arduino Keyboard Controller.

<img src="https://github.com/ArduinoNanoProjects/MatrixKeypad/blob/main/screenshot1.jpg"/>


## Erster Start der MatrixKeypad.exe

1. Starte MatrixKeypad.exe: Es wird eine Installation durchgeführt und die aktuelle Version der Arduino IDE, wie alle zusätzlichen Komponenten heruntergeladen, installiert und entzipt.

(Achtung: Das Herunterladen und automatische Einrichten kann ca. 15 Minuten dauern!)

2. MatrixKeypad und das Arduino Sketch werden danach automatisch gestartet: Du kannst den Einstellungen-Dialog von MatrixKeypad mit [x] schließe und über den Tastenbefehl `STRG+y` wieder aufrufen. 

**Menü**
- Umgebung: Hier kann auf den Speicherort gesprungen werden, an dem alle Daten für MatrixKeypad.exe abgelegt werden:
<pre>"C:\Users\&lt;username&gt;\AppData\Roaming\_MC\MatrixKeypad"</pre>
- Arduino Sketch: Das dazugehörige Arduino Sketch erneut über die Arduino IDE aufrufen. Es wird bei der Installation in der Umgebung mit abgelegt.
- Fenster schließe: kann das Einstellen-Dialog minimiert werden. Mit dem festgelegten Tastenkürzel (Standard:`STRG+y`), kann das Einstellen-Dialog wieder aufgerufen werden.
- Programm beenden: Beendet das Programm

<img src="https://github.com/ArduinoNanoProjects/MatrixKeypad/blob/main/screenshot3.jpg"/>


## Festlegen der Funktionstasten

Über die Programmtasten A bis D lassen sich 12 Funktionstasten von 0 bis 9 und die roten Tasten &#9839; und &lowast; mit einzelnen Ausführungen belegen.

<img src="https://github.com/ArduinoNanoProjects/MatrixKeypad/blob/main/screenshot4.jpg"/>


### Sendekanäle

Dies sind die Sendekanäle des Arduinos. Mittels der Funktionstasten A bis D werden die Funktionen zur Verwendung der Ziffertasten 0-9 und &#9839;, &lowast; gewechselt. Die Sendekanäle werden vom Arduino genutzt um Befehle an das Programm MatrixKeypad.exe zu übertragen. Dieses entfängt die Tastenkobinationen und ruft die jeweiligen Funktion mit den für diese Taste hinterlegt Daten auf. So kann z.B. ein Programm geöffnet werden, dessen Pfad für eine Taste hinterlegt wurde. Über die 4 Programmtasten können so jeweils 48 Kombinationen anhand der 12 Funktionstasten hinterlegt werden.

#### Kanäle der Programmtasten:
A - `SHIFT+STRG+ALT+a` - Tastenkombinationen mit Funktionen<br>
B - `SHIFT+STRG+ALT+b` - Tastenkombinationen mit Funktionen<br>
C - `SHIFT+STRG+ALT+c` - Tastenkombinationen mit Funktionen<br>
D - `SHIFT+STRG+ALT+d` - Tastenkombinationen für festgelegte Programme<br>

#### Kanäle der Funktionstasten:
0 - `SHIFT+STRG+WIN+ALT+F10`<br>
1 - `SHIFT+STRG+WIN+ALT+F1`<br>
2 - `SHIFT+STRG+WIN+ALT+F2`<br>
3 - `SHIFT+STRG+WIN+ALT+F3`<br>
4 - `SHIFT+STRG+WIN+ALT+F4`<br>
5 - `SHIFT+STRG+WIN+ALT+F5`<br>
6 - `SHIFT+STRG+WIN+ALT+F6`<br>
7 - `SHIFT+STRG+WIN+ALT+F7`<br>
8 - `SHIFT+STRG+WIN+ALT+F8`<br>
9 - `SHIFT+STRG+WIN+ALT+F9`<br>
&#9839; - `SHIFT+STRG+WIN+ALT+F11`<br>
&lowast; - `SHIFT+STRG+WIN+ALT+F12`<br>



### Funktionen

- **PROGRAM:** Starte ein ausgewähltes Programm. Nach der Auswahl kann über betätigen des Buttons ein Auswahl-Dialog gestartet werden oder der die Pfadangabe im Eingabefeld direkt vergeben werden.
- **EXPLORER:** Öffne einen beliebigen Ordner per Pfadangabe.
- **MACRO:** Liest die Tastenkombinationen aus einer Text-Datei aus und sendet diese an den PC. Diese Funktion nutzt auch MagicWords. Siehe <a href="https://github.com/ArduinoNanoProjects/MatrixKeypad/blob/main/doc/help.md">Übersicht in der Dokumentation</a>.
- **SENDSTRING:** Gibt den Inhalt des Eingabefeldes aus. / Es kann auch als Tastenkombination eingetragen werden, die nach auslösen ausgeführt werden soll.
- **SENDKEY:** Gibt den Inhalt des Eingabefeldes aus. / Es kann auch als Tastenkombination eingetragen werden, die nach auslösen ausgeführt werden soll.
- **COPYCONTENT:** Liest den Inhalt einer Text-Datei in die Zwischenablage ein und gibt ihn danach aus.
- **COPYFILE:** Kopiere eine ausgewählte Datei (z.B. zip) per Dialog in einen Ordner. 
- **COPYPAST:** Liest den Inhalt einer Text-Datei aus und legt ihn in die Zwischenablage. (Mit STRG+C kann der Inhalt ausgegeben werden.)
- **AUSCRIPT:** Ein über den Pfad zu einem AU3-Script wird direkt ausgeführt.
- **WINDOWS:** Startet Windows eigene CPL-Programme. (z.B.: Programme löschen mit Appwiz.cpl)
- **ZIP:** Nutzt den festgelegenten Order um daraus eine zip-Datei mit Datum und Uhrzeit anzufertigen. Durch die Eingabe des Pfad, wird der Ablageplatz definiert. Der festgelegte Ordner kann im Menü unter `"Umgebung > Zip-Ordner öffnen"` direkt aufgerufen werden.


### Programmauswahl

Über die Programmtaste `D` können nun Programme festgelegt werden. Ist eines der festgelegten Programme gerade aktiv und im Fokus, dann wird der Datensatz der hinter diesen Programm hinterlegt wurde für die Sendetasten verwendet.

1. Um ein Programm hinzuzufügen klicken, starte die Tastenkonbination Strg+Y (oder die eigene Festlegtung) bzw. licke auf das TayIcon und im Menü `Einstellungen`.
2. Gehe auf den Reiter `D: (Programmautomation)` und klicke die Schaltfläche `[+ Programm]`
3. Wähle über das Programm-Dialog den Pfad zum Programm, welches Du festlegen möchtest und klicke auf OK
4. Über die Auswahlbox wird das Programm und weitere angezeigt, die Du somit anpassen kannst.
5. Klicke auf deinem Keypad die Taste `D`
6. Starte das Programm aus deiner Liste manuell und fokusiere das Fenster, wenn Du weitere Fenster auf dem Bildschirm hast
7. Klicke eine Kombinationstaste hinter der Du eine Funktion abgelegt hast

<img src="https://github.com/ArduinoNanoProjects/MatrixKeypad/blob/main/screenshot7.jpg"/>

**Tipp:** In Kombination von Macros kannst Du Tastenkombinationen oder ganze Tastaturabläufe hinterlegen und diese mit nur einem Key starten. Es ist auch u.a. auch möglich, andere Programm z.B. am Ende eines Ablaufes zu starten.

Mehr dazu findest Du in der <a href="https://github.com/ArduinoNanoProjects/MatrixKeypad/blob/main/doc/help.md#Automation">Dokumentation</a>, direkt unter `Automation`.



## MagicWords

MWs sind besondere Wörter die Du in Textdateien oder auch für die Funktionen nutzen kannst. Sie werden je nach Funktionalität in der Ausgabe ersetzt. Sie können unter anderm für Funktionen wie MACRO, SENDSTRING, COPYCONTENT oder COPYPAST verwendet werden: Siehe <a href="https://github.com/ArduinoNanoProjects/MatrixKeypad/blob/main/doc/help.md#magicwords">Dokumentation</a>.


## Arduino Script

1. Arduino an den Rechner anschließen
2. Auswahl der Libraries und downloaden:
- https://github.com/arduino-libraries/Keyboard/blob/master/src/Keyboard.h
- https://playground.arduino.cc/Code/Keypad/
3. In diesem Beispiel wird ein Arduino Micro (ATmega32U4) aks Tastatursimulation verwendet.
Dieser muss unter Werkzeuge mit dem Port ausgewählt werden.
4. Das Keypad 4x4 wird über GND und an den Pins 2 bis 9 angeschlossen: <img src="https://github.com/ArduinoNanoProjects/MatrixKeypad/blob/main/screenshot5.jpg"/>
5. Sketch kompilieren, prüfen und auf den Arduino hochladen<br>
6. Die Funktion kann über den Seriellen Monitor durch drücken einer Taste geprüft werden.


## 3D-Druck & Gehäuse

1. Der einfach Demodruck kann über <a href="https://github.com/ArduinoNanoProjects/MatrixKeypad/blob/main/3dPrint/MatrixKeypad.stl">MatrixKeypad.stl</a> bezogen werden.
<img src="https://github.com/ArduinoNanoProjects/MatrixKeypad/blob/main/screenshot6.jpg"/>
2. Je nach Drucker und Filament muss das Objekt im Slicer erstellt werden.<br>
3. Den 3D-Printer konfigurieren und drucken  <br>
4. Zusammenbauen, fertig.<br>
<img src="https://github.com/ArduinoNanoProjects/MatrixKeypad/blob/main/screenshot2.jpg"/>


### Arduino Updates
Es wird die Portable Version der Aurduino IDE beim ersten Start heruntergeladen. 
Wurde eine neue Version dafür vergeben wird diese automatisch beim Start gefunden. 
Sie kann kauf über das Menü `Arduino IDE > Nach Updates suchen` manuell heruntergeladen werden.

### Backups 
Über den Menüeintrage `Sicherungen > Sicherung erstellen` können nun Backups erstellt werden. Sie werden mit Benutzernamen und Datum versehen. Die Sicherung schließt die Ordner "programs", "templates" und die "db" (Datenbankdatei) mit ein. Sie werden als Zip-Datei erstellt und unter dem Ordner "backups" im Hauptverzeichni abgelegt. Um direckt auf die Umgebung zuzugreifen, kann der Backup-Ordner über den Menüeintrag `Sicherungen > Umgebung öffnen` geöffnet werden.

### License

CC BY-NC-SA
https://creativecommons.org/licenses/by-nc-sa/4.0/deed.de

Copyright 2022 by Michael McCouman Jr.