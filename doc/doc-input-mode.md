---
layout: default
lang: de
title: Eingabemodus
---

# Eingabemodus

## Überblick

Der Eingabemodus bezieht sich auf die direkte, manuelle Eingabe von Zielpositionen 
in die Race Spalten des Grids auf Seite Event. 
Beim Eingabemodus wird zwischen Strict und Relaxed unterschieden.

Es ist immer das Ziel, die Konsistenz der Eingangsdaten permanent zu gewährleisten. 
Doppelte Nummern oder Lücken in der Liste der Zielpositionen dürfen nicht vorkommen. 
Der Strict Modus (stringent) dient der strikten Einhaltung von Konsistenzforderungen.

Im Modus Relaxed reagiert das Programm entspannt auf Ihre Eingaben. 
Es nervt Sie nicht mit automatischen Korrekturen. 
Der Strict Modus ist dennoch zu empfehlen, 
da in diesem Fall der Benutzer des Programms langfristig entspannen kann.

Die Eingabe von Zielpositionen ist im Prinzip eine Aufgabe, 
die dem Timing-Provider zufällt. 
Das Ergebnis der Wettfahrt wird nach Abschluss der Wettfahrt vom Race-Teil in den Event-Teil übertragen. 
Daher sollten eigentlich nur wenige Korrekturen direkt in das Event Grid eingegeben werden.

## Modus Strict

Im Modus Strict wird garantiert, dass die fortlaufende Nummerierung der Positionen 
von eins beginnend aufrechterhalten wird.

Sollte eine Nummer schon belegt sein, wird automatisch ein Lücke geschaffen, 
und alle nachfolgenden Nummern rutschen eins weiter nach hinten. 
Dies ist das erwartete Verhalten. 
Es ermöglicht eine einfache Korrektur von Zielplatzierungen, 
ohne dass die ganze Liste manuell gepflegt werden muss.

Sollte die eingegebene Nummer am Ende der Liste eine Lücke aufreißen, 
dann wird der eingegebene Wert automatisch korrigiert. 
Dies ist nicht in jedem Fall das erwartete Verhalten. 
Es kann genutzt werden, wenn Sie die Zielpositionen manuell in Echtzeit eingeben, 
und nicht genau wissen, welche Position aktuell ist. 
Geben Sie einfach eine hohe Nummer ein, um die Bib am aktuellen Ende der Liste zu platzieren.
Ein Event kann nur dann in den Strict Modus geschalten werden, 
wenn die Konsistenzbedingungen erfüllt sind.

## Modus Relaxed

Natürlich gibt es Situationen, wo die Zielpositionen wie eingegeben gespeichert werden sollen. 
Das ist zum Beispiel der Fall, wenn Sie eine vorhandene Liste zeilenweise abschreiben. 
Es sei an dieser Stelle darauf hingewiesen, 
dass dies keine gute Praxis darstellt. 
Wenn Sie einen Eingabefehler machen, 
kann es sehr aufwendig sein, 
am Ende die Konsistenz wieder herzustellen. 
Obwohl das Programm Sie durch farbliche Darstellung von Inkonsistenzen bei der Fehlersuche unterstützt, 
ist die Verwendung des Modus Relaxed nicht die empfohlene Arbeitsweise. 
Es ist besser, den Strict Modus so schnell wie möglich zu erreichen, 
und Korrekturen dann im Strict Modus durchzuführen, bis alles stimmt.

Eine Berechtigung für die Existenz des Relaxed Modus existiert aber dennoch, 
nämlich im Zusammenhang mit dem automatischen Einlesen der Ergebnisse aus der gespeicherten Text- oder Xml-Datei. 
Wenn keine ungültigen Manipulationen an den editierbaren Daten vorgenommen wurden, 
kann das Programm am Ende des Lesevorgangs in den Strict Modus schalten.
Sie können ohne Bedingung jederzeit vom Strict Modus in den Relaxed Modus wechseln.

## Zusammenfassung

Den Strict Modus gibt es schon ewig, so dass davon nicht mehr viel gesprochen wird.
Er ermöglicht die schnelle Was-wäre-wenn-Analyse in der [Desktopapplikation](../applications/FR93.html),
und neuerdings auch im [Silverlight Client](../silverlight/FRIA05.html).

[Zurück](doc-index.html) zu den Dokumenten.