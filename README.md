# MatrixKeypad
Arduino Keyboard Controller.

<img src="https://github.com/ArduinoNanoProjects/MatrixKeypad/blob/main/screenshot1.jpg"/>


## Erster Start der MatrixKeypad.exe

1. Starte MatrixKeypad.exe: Es wird eine Aktualisierung durchgeführt und die die aktuelle Version der Arduino IDE, wie alle zusätzlichen Komponenten heruntergeladen und danach automatisch entzipt.

(Achtung: Das herunterladen und autimatische Einrichten kann ca. 15 Minuten dauern!)

2. MatrixKeypad und das Arduino Sketch werden danach automatisch gestartet: Du kannst den Einstellungen-Dialog von MatrixKeypad mit [x] schließe und über den Tastenbefehl `STRG+y` weider aufrufen. 

**Menü**
- Umgebung: Hier kann auf den Speicherort gesprungen werden, an dem alle Daten für MatricKeypad.exe abgelegt wurden.
<pre>"C:\Users\&lt;username&gt;\AppData\Roaming\_MC\MatrixKeypad"</pre>
- Arduino Sketch: Das dazugehörige Arduino Sketch erneut über die Arduino IDE aufrufen. Es wird bei der Installation in der Umgebung mit abgelegt.
- Fenster schließe: kann das Einstellen-Dialog minimiert werden. Mit dem festgelegten Tastenkürzel (Standard:`STRG+y`), kann das Einstellen-Dialog wieder aufgerufen werden.
- Programm beenden: Beendet das Programm

<img src="https://github.com/ArduinoNanoProjects/MatrixKeypad/blob/main/screenshot3.jpg"/>


## Festlegen der Funktionstasten

Über die Funktionstasten A bis D lassen sich 12 Funktionstasten von 0 bis 9 und die roten Tasten + und # mit einzelnen Ausführungen belegen.

<img src="https://github.com/ArduinoNanoProjects/MatrixKeypad/blob/main/screenshot4.jpg"/>

- **PROGRAM:** Starte ein ausgewähltes Programm. Nach der Auswahl kann über betätigen des Buttons ein Auswahl-Dialog gestartet werden oder der die Pfadangabe im Eingabefeld direkt vergeben werden.
- **EXPLORER:** Öffne einen beliebigen Ordner per Pfadangabe.
- **SENDCONTENT:** Liest den Inhalt einer Text-Datei aus und gibt den Inhalt aus. (z.B.: als Vorlage)
- **SENDSTRING:** Gibt den Inhalt des Eingabefeldes aus. / Es kann auch als Tastenkombination eingetragen werden, die nach auslösen ausgeführt werden soll.
- **COPYCONTENT:** Liest den Inhalt einer Text-Datei in die Zwischenablage ein und gibt ihn danach aus.
- **COPYPAST:** Liest den Inhalt einer Text-Datei aus und legt ihn in die Zwischenablage. (Mit STRG+C kann der Inhalt ausgegeben werden.)
- **SCRIPT:** Ein über den Pfad zu einem AU3-Script wird direkt ausgeführt.
- **WINDOWS:** Startet Windows eigene CPL-Programme. (z.B.: Programme löschen mit Appwiz.cpl)
- **ZIP:** Nutzt den festgelegenten Order um daraus eine zip-Datei mit Datum und Uhrzeit anzufertigen. Durch die Eingabe des Pfad, wird der Ablageplatz definiert. Der festgelegte Ordner kann im Menü unter `"Umgebung > Zip-Ordner öffnen"` direkt aufgerufen werden.

## Arduino Script

1. Arduino an den Rechner anschließen
2. Auswahl der Libraries und downloaden:
- https://github.com/arduino-libraries/Keyboard/blob/master/src/Keyboard.h
- https://playground.arduino.cc/Code/Keypad/
3. In diesem Beispiel wird ein Arduino Micro (ATmega32U4) aks Tastatursimulation verwendet.
Dieser muss unter Werkzeuge mit dem Port ausgewählt werden.
4. Das Keypad 4x4 wird über GND und an den Pins 2 bis 9 angeschlossen:
<img src="https://github.com/ArduinoNanoProjects/MatrixKeypad/blob/main/screenshot5.jpg"/>
5. Scetch kompilieren, prüfen und auf den Arduino hochladen
6. Die Funktion kann über den Seriellen Monitor durch drücken einer Taste geprüft werden.

## 3D-Druck & Gehäuse

1. Der einfach Demodruck kann über <a href="https://github.com/ArduinoNanoProjects/MatrixKeypad/blob/main/3dPrint/MatrixKeypad.stl">MatrixKeypad.stl</a> bezogen werden.
<img src="https://github.com/ArduinoNanoProjects/MatrixKeypad/blob/main/screenshot6.jpg"/>
2. Je nach Drucker und Filament muss das Objekt im Slicer erstellt werden.
3. Den 3D-Printer konfigurieren und drucken  
4. Zusammenbauen, fertig.
<img src="https://github.com/ArduinoNanoProjects/MatrixKeypad/blob/main/screenshot2.jpg"/>

### License

CC BY-NC-SA
https://creativecommons.org/licenses/by-nc-sa/4.0/deed.de

Copyright 2022 by Michael McCouman Jr.