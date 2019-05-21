---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
---

Also doch, erst veröffentlichen und dann verbessern.

Der größte Teil des Inhaltes hier wurde wiederverwendet vom alten Blog und der Html-Hilfe-Datei (chm). 
Der Inhalt ist also teilweise veraltet und wird ersetzt oder gelöscht.
Aber ich will das Repository mit dieser Version starten, so dass etwas von der Historie erhalten bleibt.

Es wird von Clienten die Rede sein, nicht von [Klienten](Rechtschreibung.html), 
weil es mir weh tun würde es richtig zu schreiben, 
ich kann einfach keinen Clienten mit K sehen, soweit dazu.

# FR01

## Ein Open Source Projekt

FR01 ist das Programm, mit dem Sie die Event-Daten einer Segelregatta im Fleetrace-Format analysieren.

Beispiel: Unmittelbar nach Schluss der Wettfahrt laden Sie sich per Button-Click in FR01 den aktuellen Stand von gestern herunter. 
Den Zieldurchgang der aktuellen Wettfahrt können Sie schnell eingeben. 

Anschließend können Sie die Anzahl der Streicher ändern, Penalties hinzufügen oder löschen, 
und natürlich Zielpositionen ändern. Das könnte interessant werden!

> Ihre Ergänzungen können auch zurückgepostet werden, wenn der Server es erlaubt.

FR01 soll auf mehreren Plattformen verfügbar sein, Sie können mithelfen.

## Nur eine Idee, Sie können es anders machen
 
Die von FR01 verwendeten Daten könne einfach strukturierte Html-Fragmente sein, 
welche unverändert auf der Website des Events eingebunden werden können. 
Sie haben also nicht etwa Text, Xml oder Json, sondern Html. 
Das Besondere am Html ist, dass es eine vollständige Repräsentation der Daten des Events enthält. 
Damit ist die Voraussetzung dafür gegeben, dass der Event von der Anwendung rekonstruiert werden kann. 

Während das Html vom Programm aktuell gehalten wird
kann das Aussehen im Browser verbessert und Inhalt ergänzt werden.

## Verwendung von statischen Dateien

Für einen einzelnen Event genügt es, eine einzelne statische Html-Datei auf dem Server abzulegen.

Im Normalfall haben Sie jedoch mehrere Dateien, für jede Bootsklasse eine, 
und zusätzlich eine Xml-Datei, EventMenu.xml wäre ein guter Name, die als Inhaltsverzeichnis dient,
so dass die Applikation weiß, wo sich die Daten befinden.

Eine Url in der Combobox von FR01 zeigt dann auf das Inhaltsverzeichnis. 
Nach dem Download des Inhaltsverzeichnisses erscheinen die Bootsklassen automatisch als Buttons in der Buttonleiste.




