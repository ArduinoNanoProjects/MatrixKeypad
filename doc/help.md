# Automation
1. Erstelle eine Text-Datei (z.B. automation.txt) und Suche eines der Funktionstasten `[0]` bis `[9]` aus bzw. ein Programm, über die Programmauswahl `[D]` (wenn du eine Programm automatisieren möchtest). <br>
2. Wähle eine Funktionstaste aus und setze die Funktion `MACRO`.<br>
3. Öffne die Text-Datei und vergebe einzelne Schritte, die per Tastatur oder Maus durchgeführt werden sollen. Z.B. könnte ein folgender Ablauf durchzuführen sein:<br>
<pre>
;                       # Warte 2500ms bis die Aktion beginnt
^n                      # Starte Tastenkombination Strg+N
,                       # Warte erneut nur 1500ms bis ein Fenster angezeigt wird
{TAB}{TAB}{TAB}         # Drücke 3x schnell hintereinander die Tabulator-Taste
{TAB}{TAB}{TAB}         # Warte 100ms und drück erneut 3x schnell nacheinander die Tab-Taste
Das ist ein Test.       # Schreibe nun in ein Feld "Das ist ein Test."
.                       # Warte nun 500ms ab
{TAB}{ENTER}            # Klicke nun auf OK mit Tab und danach sofort Enter
</pre>

4. Es kann auch zuerst ein weiteres Programm geöffnet werden. Z.B. den Taschenrechner starten und eine Rechnung durchführen:<br>
<pre>
Run(calc.exe)           # Starte das Windows eigene Programm "calc.exe". (Dies braucht keine Pfadangaben!)
;                       # Warte 2500ms bis das Programm "Taschenrechner" gestartet wurde.
100{*}200               # Sende die Tastenangaben 100 x 200 
{ENTER}                 # Klicke die Enter, um das Ergebnis im Taschenrechner anzuzeigen
</pre>


## Ein Programm starten:
<pre>
Run(C:\path\to\programm.exe)
</pre>
Beispiel: `Run(calc.exe)`

## Kommentar:
Beispiel: `^n  # das ist ein Kommentar und dieser wird nicht ausgelesen`

## Mausklicks:
<pre>
&lsaquo; = links
&rsaquo; = rechts
</pre>

## Schlüsseltasten gleichzeitig gedrückt:
Beispiel: `^n =  Strg + N`
<pre>
^ = Strg 
! = Alt
+ = Shift (Hochstelltaste)
# = Windows Taste
</pre>

## Tastenkombinationen einzeln gedrückt:
<pre>
{^} = Grad
{!} = Ausrufezeichen
{+} = Plus
{#} = Raute
{-} = Minus

{SPACE} = SPACE (Leertaste)
{ENTER} = Eingabetaste auf der Haupttastatur
{ALT} = ALT

{BACKSPACE} oder {BS} = BACKSPACE (Rücktaste)
{DELETE} oder {DEL} = DELETE Entfernen (Entf)

{UP} = Nach-Oben-Taste
{DOWN} = Nach-Unten-Taste
{LEFT} = Nach-Links-Taste
{RIGHT} = Nach-Rechts-Taste

{HOME} = HOME (Pos1 – Taste)
{END} = END (Ende - Taste)
{ESCAPE} oder {ESC} = ESCAPE- Taste
{INSERT} oder {INS} = INS (EINFÜGEN (Einfg)-Taste)

{PGUP} = PageUp (Bild-Auf-Taste)
{PGDN} = PageDown (Bild-Ab-Taste)

{F1} - {F12} = Funktionstasten

{TAB} = TAB (Tabulator – Taste)
{PRINTSCREEN} = Druck-Taste

{LWIN} = linke Windows Taste
{RWIN} = rechte Windows Taste

{NUMLOCK on} = NUMLOCK (Num)-Taste (on/off/toggle)
{CAPSLOCK off} = CAPSLOCK-Taste (FESTSTELLTASTE) (on/off/toggle)
{SCROLLLOCK toggle} = ROLLEN-Taste (on/off/toggle)
{BREAK} = STRG+Break = STRG+UNTERBRECHUNG Taste
{PAUSE} = PAUSE-Taste

{NUMPAD0} - {NUMPAD9} = Ziffernblock 0-9 (Numpad = numerisches Tastenfeld)
{NUMPADMULT} = Multiplizieren auf Numpad
{NUMPADADD} = Addieren auf Numpad
{NUMPADSUB} = Subtrahieren auf Numpad
{NUMPADDIV} = Dividieren auf Numpad
{NUMPADDOT} = Punkt (Komma) auf Numpad
{NUMPADENTER} = Eingabe-Taste auf Numpad

{APPSKEY} = Windows-Programm Taste

{LALT} = Linke ALT-Taste
{RALT} = Rechte ALT-Taste
{LCTRL} = Linke STRG-Taste
{RCTRL} = Rechte STRG-Taste
{LSHIFT} = Linke Shift-Taste
{RSHIFT} = Rechte Shift-Taste
{SLEEP} = Computer PAUSE Taste
{ALTDOWN} = Hält die ALT-Taste gedrückt, bis {ALTUP} gesendet wird
{SHIFTDOWN} = Hält die SHIFT-Taste gedrückt, bis {SHIFTUP} gesendet wird
{CTRLDOWN} = Hält die STRG-Taste gedrückt, bis {CTRLUP} gesendet wird
{LWINDOWN} = Hält die linke Windows-Taste gedrückt, bis {LWINUP} gesendet wird
{RWINDOWN} = Hält die rechte Windows-Taste gedrückt, bis {RWINUP} gesendet wird

{ASC nnnn} = Sendet die ALT+nnnn ASCII-CODE-Tastenkombination

{BROWSER_BACK} = Wählt den Browser-Button "Zurück"
{BROWSER_FORWARD} = Wählt den Browser-Button "Vorwärts"
{BROWSER_REFRESH} = Wählt den Browser-Button "Aktualisieren"
{BROWSER_STOP} = Wählt den Browser-Button "Stop"
{BROWSER_SEARCH} = Wählt den Browser-Button "Suche"
{BROWSER_FAVORITES} = Wählt den Browser-Button "Favoriten"
{BROWSER_HOME} = Startet den Browser und geht zur Startseite
{VOLUME_MUTE} = Stellt Lautsprecher auf Stumm
{VOLUME_DOWN} = Reduziert die Lautstärke
{VOLUME_UP} = Vergrößert die Lautstärke
{MEDIA_NEXT} = Wählt den nächsten Track im Media Player
{MEDIA_PREV} = Wählt den vorhergehenden Track im Media Player
{MEDIA_STOP} = Stoppt Media Player
{MEDIA_PLAY_PAUSE} = Wiedergabe/Pause Media Player
{LAUNCH_MAIL} = Startet die Standard-E-Mail-Anwendung
{LAUNCH_MEDIA} = Startet den Media Player
{LAUNCH_APP1} = Startet das Anwender-Programm 1
{LAUNCH_APP2} = Startet das Anwender-Programm 2
</pre>

## Wartezeiten / Timer: Sleep()
<pre>
; = 2500ms
, = 1500ms
. = 500ms
</pre>

## MagicWords (MW):
MagicWords sind wie der Name schon vermuten lässt, ganz besondere Wörter. Du kannst sie in einer Textdateien hinterlegen und sie durch die Funktionen
`MACRO`, `SENDSTRING`, `COPYCONTENT` oder `COPYPAST` verwenden. Der Inhalt wird dann umgewandelt, sodas der Inhalt damit eretzt wird. 

**Beispiel 1:**

Eine Textdatei mit folgenden Inhalt, wurde mit der Funktion `COPYPAST`, auf die Funktionstaste `[0]` im Keypad Programm `[A]` hinterlegt:
<pre>
Vorlage: (test.txt)
-------------------

Heute ist der {HEUTE}. 
Wir habe es gerade {STUNDE} Uhr {MINUTE} und {SEKUNDEN} Sekunden.
</pre>

Wird die Taste `[A:0]` gedrückt, wird der Inhalt der Datei ausgelesen und die MWs ersetzt. Danach wird der Inhalt ausgegeben. Dieser sieht nun wie folgt aus:
<pre>
Ergebnis: 
-------------------

Heute ist der 22.12.2022. 
Wir habe es gerade 13 Uhr 55 und 23 Sekunden.
</pre>

**Beispiel 2:**

Du kannst auch die Funktion `SENDKEY` nutzen um Text und Tastenkombinationen herauszugeben, oder `EXPLORER`, um einen Ordner zu im Explorer öffnen zu lassen:
<pre>
{@MyDocumentsDir}\Meine Schriften
</pre>

Es wird der Ordner `Meine Schriften`, im Explorer angezeigt. Dieser wurde über den Pfad `C:\Users\<Nutzername>\Dokumente\Meine Schriften\` geöffnet.
 
### Alle magischen Wörter im Überblick

**Datumsangaben:**

`{HEUTE}` -> `03.10.2022` <br>

`{JAHR}` -> `2022` <br>
`{MONAT}` -> `10` <br>
`{TAG}` -> `03` <br>

**Zeitangaben:**

`{ZEIT}` -> `17:01:10` <br>

`{STUNDE}` -> `17` <br>
`{MINUTE}` -> `01` <br>
`{SEKUNDEN}` -> `10` <br>

**Pfadangaben:**

`{@HomeDrive}` -> `C:` <br>
`{@WindowsDir}` -> `C:\WINDOWS` <br>
`{@SystemDir}` -> `C:\WINDOWS\system32` <br>
`{@ScriptDir}` -> `C:\KeypadMatrix` <br>
`{@ProgramsDir}` -> `C:\KeypadMatrix\MatrixKeypad.exe` <br>
`{@DesktopCommonDir}` -> `C:\Users\Public\Desktop` <br>
`{@DocumentsCommonDir}` -> `C:\Users\Public\Documents` <br>
`{@HomePath}` -> `\Users\<Nutzername>` <br>
`{@DesktopDir}` -> `C:\Users\Nutzermane\Desktop` <br>
`{@FavoritesDir}` -> `C:\Users\<Nutzername>\Favorites` <br>
`{@FavoritesCommonDir}` -> `C:\Users\<Nutzername>\Favorites` <br>
`{@AppDataDir}` -> `C:\Users\<Nutzername>\AppData\Roaming` <br>
`{@LocalAppDataDir}` -> `C:\Users\<Nutzername>\AppData\Local` <br>
`{@LogonDNSDomain}` -> `C:\Users\<Nutzername>\AppData\Local` <br>
`{@TempDir}` -> `C:\Users\<Nutzername>\AppData\Local\Temp` <br>
`{@MyDocumentsDir}` -> `C:\Users\<Nutzername>\Documents` <br>
`{@UserProfileDir}` -> `C:\Users\<Nutzername>` <br>
`{@ProgramsCommonDir}` -> `C:\Users\<Nutzername>\AppData\Roaming\Microsoft\Windows\Start Menu\Programs` <br>
`{@StartMenuDir}` -> `C:\Users\<Nutzername>\AppData\Roaming\Microsoft\Windows\Start Menu` <br>
`{@ProgramFilesDir}` -> `C:\ProgramData\Microsoft\Windows\Start Menu\Programs` <br>
`{@ScriptFullPath}` -> `C:\ProgramData\Microsoft\Windows\Start Menu` <br>
`{@StartupCommonDir}` -> `C:\ProgramData\Microsoft\Windows\Start Menu\Programs\Startup` <br>
`{@LogonServer}` -> `\\COMPUTERNAME` <br>

**Windows Angaben:**

`{@UserName}` -> `<Nutzername>` <br>
`{@ComputerName}` -> `COMPUTERNAME` <br>
`{@LogonDomain}` -> `COMPUTERNAME` <br>
`{@IPAddress1}` -> `192.168.000.001` <br>
`{@DesktopDepth}` -> `32` <br>
`{@DesktopRefresh}` -> `59` <br>
`{@DesktopHeight}` -> `1080` <br>
`{@DesktopWidth}` -> `1920` <br>
`{@OSArch}` -> `X64` <br>
`{@OSBuild}` -> `19044` <br>
`{@OSLang}` -> `0407` <br>
`{@OSServicePack}` -> `WIN32_NT` <br>
`{@OSType}` -> `WIN_10` <br>
`{@OSVersion}` -> `1234` <br>
`{@KBLayout}` -> `00000207`  <br>
