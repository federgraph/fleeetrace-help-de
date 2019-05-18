---
layout: default
lang: de
title: Mehr oder Weniger
---
		
# Mehr oder Weniger

Auf Seite Menu schalten Sie mit dem Button More/Less den Modus um.

Im Modus More (wenn Less sichtbar ist), werden zusätzliche Schaltflächen 
(Buttons) sichtbar. Diese Schaltflächen sind hilfreich, wenn Sie einen neuen 
Workspace oder einen neuen Event einrichten. Die Schaltflächen werden nicht 
gebraucht, wenn Sie einen fertigen Event nur ansehen.

### Schalflächen für EventMenu.xml

**Text**: Dieser Button liefert die transformierte 
Version des Xml-Beispiels. Der Button Transform muss die gleiche Ausgabe 
bringen, wenn zuvor mit Button Xml das Xml-Beispiel geladen wurde. Das Ergebnis 
kann von der Plattform abhängen, auf der das Programm läuft - je nachdem, 
welcher Xml-Parser verwendet wird. Das Programm hat die Auswahl zwischen dem 
externen Parser, der zum Betriebssystem gehört (MS-XML), oder einem sehr 
einfachen Parser, der eingebaut ist und auf allen Plattformen läuft.

**Xml**: Damit wird ein Beispiel-EventMenu.xml in das 
Memo geladen.

**Download**: Damit wird das EventMenu.xml (kann anders 
benannt sein) von der Quelle geladen, die in der Combo (oben links) ausgewählt 
wurde. Das Ergebnis erscheint im Memo.

**Transform**: Damit wird das EventMenu.xml im Memo 
transformiert. Das Programm wird immer die transformierte Version verarbeiten. 
Mit diesem Button können Sie Fehler im EventMenu.xml finden.

### Schaltflächen für EventData.*

**Convert**: Der Button Convert arbeitet nicht mit 
EventMenu.xml, sondern mit EventData.*. Es geht hier um die Event-Daten, die im 
Format Text, Xml oder Html vorliegen können. Der Button Convert konvertiert die 
Event-Daten, wenn erforderlich, und schreibt das Ergebnis in das Memo.

**Read**: Der Button Read liest die Daten vom Memo und 
lädt diese in die Anwendung.

Das untere Memo auf Seite Report ist ein mehrzeiliges Editierfeld, welches 
Text anzeigt. Die EventDaten kommen in das Memo, indem Sie den Button für den 
Event in der Buttonleiste drücken (nur im Modus More), indem Sie den Button Text 
oder Html auf Seite Report drücken, oder indem Sie die Daten über die 
Zwischenablage hineinkopieren. Das Memo ist editierbar.

Mit Modus More und Button Read können Sie die abgerufenen Text-Daten 
verändern, bevor diese von der Anwendung geladen werden.

Indem Sie die Textausgabe des Events in das Memo schreiben, verändern, und 
wieder laden, können Sie bei einem lokalen Workspace den Umweg über die 
Festplatte vermeiden bzw. bei einem nur lesbaren Workspace auf diese Weise 
Parameter und Properties ändern, für die es im Programm keine graphische 
Oberfläche gibt.

