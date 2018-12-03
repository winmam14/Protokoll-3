# Protokoll-3
## Thema: Microcontroller

Ersteller: Winter Matthias  
Klasse:    4AHME  
Gruppe:    3   

Anwesend: Vezonik Sarah, Vollmaier Alois, Wegl Patrick, Wesonig Mercedes, Winter Matthias, Winter Thomas   
   
## Entwicklungsumgebung Atmel Studio
Als Entwicklungsumgebung wurde uns in dieser Einheit [Atmel Studio](https://www.mikrocontroller.net/articles/Atmel_Studio) gezeigt und grundlegente Funktionen von diesem Programm nähergebracht. Atmel Studio ist eine **kostenlose** Entwicklungsumgebung welche von Atmel Corporation zur verwendung bereit gestellt wird. Diese Programm hat den Vorteil, dass man Chips mehrerer Hersteller programmieren kann und dieses Programm auch sofort im selben Programm simulieren kann. Jedoch ein Nachteil ist es, dass man dieses Programm **nur** auf Microsoft eigene Betriebssysteme verwenden kann, da *Atmel Studio* auf *Visual Studio Shell* von Microsoft basiert.  

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
![Stack](https://www.google.at/url?sa=i&rct=j&q=&esrc=s&source=images&cd=&cad=rja&uact=8&ved=2ahUKEwiCnPL_kITfAhUSdxoKHTQQDBwQjRx6BAgBEAU&url=https%3A%2F%2Fwww.der-wirtschaftsingenieur.de%2Findex.php%2Fstack-datenstruktur-in-c%2F&psig=AOvVaw1AS0vRkHQ8NBydR_HNDKjl&ust=1543942560267683"Stack")
