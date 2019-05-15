---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
---

Also doch, erst veröffentlichen und dann verbessern.

Der größte Teil des Inhaltes hier wurde wiederverwendet vom alten Blog und der Html-Hilfe-Datei (chm). 
Der Inhalt ist also teilweise veraltet und wird ersetzt oder gelöscht.
Aber ich will das Repository mit dieser Version starten, so dass etwas von der Historie erhalten bleibt.

Es wird von Clienten die Rede sein, nicht von Klienten, weil es mir weh tun würde es richtig zu schreiben, ich kann einfach keinen Clienten mit K sehen, soweit dazu.

# FR01

FR01 ist das Programm, mit dem Sie die Event-Daten einer Segelregatta im Fleetrace-Format analysieren.

# Beispiel

Unmittelbar nach Schluss der dritten Wettfahrt laden Sie sich per Button-Click in FR01 den aktuellen Stand von Wettfahrt 2 herunter. 
Den Zieldurchgang der dritten Wettfahrt können Sie schnell eingeben. 
Das Client-Programm rechnet. 
Sie können die Anzahl der Streicher ändern, 
Penalties hinzufügen (oder löschen), 
und natürlich Zielpositionen ändern.

Ihre Ergänzungen können auch zurückgepostet werden, wenn der Server es erlaubt.

FR01 ist auf mehreren Plattformen verfügbar. 
Die Variante für Windows 7 können Sie direkt herunterladen. 
Die 32 Bit Version des Programms wurde auch unter Windows XP, Vista und Ubuntu 10.04 (mit Wine) getestet.

Die von FR01 verwendeten Daten sind einfach strukturierte Html-Fragmente, 
welche unverändert auf der Website des Events eingebunden werden können. 
Sie haben also nicht etwa Text, Xml oder Json, sondern Html. 
Das Besondere am Html ist, dass es eine vollständige Repräsentation der Daten des Events enthält. 
Damit ist die Voraussetzung dafür gegeben, dass der Event von der Anwendung (zum Beispiel FR01) exakt rekonstruiert werden kann. 
Während das Html vom Programm aktuell gehalten wird 
kann das Aussehen im Browser vom Designer der Website mit Css noch beliebig verbessert werden.

Für einen einzelnen Event genügt es, eine einzelne statische Html-Datei auf dem Server abzulegen.
Im Normalfall haben Sie jedoch mehrere Dateien, für jede Bootsklasse eine, 
und zusätzlich eine Xml-Datei **EventMenu.xml**, die als Inhaltsverzeichnis dient.
Eine Url in der Combobox von FR01 zeigt dann auf das Inhaltsverzeichnis. 
Nach dem Download des Inhaltsverzeichnisses erscheinen die Bootsklassen automatisch als Buttons in der Buttonleiste.
Easy.




