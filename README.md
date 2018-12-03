# Protokoll-3
## Thema: Microcontroller


Ersteller: Winter Matthias  
Klasse:    4AHME  
Gruppe:    3   

Anwesend: Vezonik Sarah, Vollmaier Alois, Wegl Patrick, Wesonig Mercedes, Winter Matthias, Winter Thomas   
   
## Entwicklungsumgebung Atmel Studio
Als Entwicklungsumgebung wurde uns in dieser Einheit [Atmel Studio](https://www.mikrocontroller.net/articles/Atmel_Studio) gezeigt und grundlegente Funktionen von diesem Programm nähergebracht. Atmel Studio ist eine **kostenlose** Entwicklungsumgebung welche von Atmel Corporation zur verwendung bereit gestellt wird. Diese Programm hat den Vorteil, dass man Chips mehrerer Hersteller programmieren kann und dieses Programm auch sofort im selben Programm simulieren kann. Jedoch ein Nachteil ist es, dass man dieses Programm **nur** auf Microsoft eigene Betriebssysteme verwenden kann, da *Atmel Studio* auf *Visual Studio Shell* von Microsoft basiert.  
![alt text](https://hackadaycom.files.wordpress.com/2016/10/atmelmicrochip.png?w=800)

## Unterrichtsmittel

Im Labor Unterricht, sowie auch in FIV, werden wir den [ATmega328p](https://www.sparkfun.com/datasheets/Components/SMD/ATMega328.pdf) verwenden. Da dieser jedoch nicht in Atmel Studio nicht vertreten ist nutzen wir den ATmega328 als alternative da dieser sehr ähnlich ist.  
Eckdaten **ATmega328p**:  
* Taktfrequenz: 16MHz
* 32kB Flashspeicher
* 32 Register
* 2kB SRAM
* 1kB EEPROM  
  
## Der Stack
Der Stack, im Deutschen auch Stapelspeicher genannt, ist ein wichtiger Teil des Speichers. Hier werden Daten nach dem LastIn-FirstOut(LIFO) Prinzip abgelegt bzw. aufgerufen. Dieses Prinzip ist mit einem Stapel Bücher zu vergleichen. Das letzte Buch welches auf den Stapel gelegt wurde wird auch als Erstes wieder vom Stapel herunter genommen.  
Mehr Informationen zum Stack findest du [hier](https://de.wikipedia.org/wiki/Stapelspeicher).  
  ![alt text](https://www.der-wirtschaftsingenieur.de/bilder/stack.PNG "Stack im Dateisystem")

## Stackpointer
Der Stackpointer ist ein Zeiger welcher auf den nächsten freien Platz im Stack zeigt. Falls dieser auf den letzten Platz zeigt ist der Stack leer. In unserer Einheit zeigte er jedoch auf die Adresse "08FF", was kein Problem darstellt. Sollte er jedoch auf eine Adresse die außerhalb seines deffinierten Bereiches liegt zeigen spricht man von einem **Stackoverflow**. Dieser Stackoverflow kann zu Probleme führen welche nicht immer sofort erkennbar sind.  
## Praktisches Arbeiten
Am Ende der Einheit erstellten wir eine Quelltext welcher in Atmel Studio Simuliert wurde. Wir mussten dann herausfinden was die entstandenen Maschinenbefehle bedeuteten. Dies machten wir mithilfe des Atmel Instruction Set Manual. Hierbei ist zu achten dass das richtige Handbuch zum richtigen Prozessor verwendet wird, da es kleine abweichungen der Maschinenbefehle geben kann.  
Das richtige Handbuch zum verwendeten Prozessor findest du [hier](http://ww1.microchip.com/downloads/en/DeviceDoc/Atmel-0856-AVR-Instruction-Set-Manual.pdf).  

Maschienenbefehl | Ausführung
--- | --- 
JMP | Sprung zu einer bestimmten Adresse (benötigt 8 Bytes) 
RJMP | Sprung zu einer Adresse (Offset muss eingehalten werden, benötigt 4 Bytes) 
CLR | Register wird mit Nullen überschrieben (Realisierung durch XOR-Verknüpfung mit sich selbst) 
OUT | schreibt Daten von einem in ein anderes Register 
LDI | Konstante wird in Register geschrieben (nur bei Registern 16-31 möglich) 
SER | Register wird auf den höchstmöglichen Wert gesetzt 

