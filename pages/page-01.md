---
layout: default
lang: de
title: Übersicht
---

# Fleetrace

## Abstrakt

FleetRace (FR) ist ein kompaktes Timing- und Auswertesystem für den 
Segelsport. Es wurde aus einer Hand konzipiert für die Verwendung gleichermaßen 
durch Teilnehmer und Veranstalter. Die Idee ist, dass die Ergebnisse in 
elektronischer Form zur Verfügung stehen und jeder Knotenpunkt rechnet. Damit 
kann der Konsument der Daten eine Was-Wäre-Wenn Analyse unabhängig durchführen, 
dass heißt er kann die Daten verändern. Das System wurde für den Einsatz im 
Netzwerk entworfen. Im günstigsten Fall erfolgt die gesamte Abwicklung papierlos 
und in Echtzeit.

## Datenerfassung

Die Datenerfassung erfolgt manuell aber effektiv.
Sie tippen auf einen Button für die Bib um eine Zeit für das Boot zu generieren.
Oder Sie wählen in der Matrix der Boote ein Boot und drücken dann die Leertaste.
Das kann unterschiedlich sein, je nachdem welches Programm Sie benutzen,
es wird viele Programme dafür geben.

Dieser Vorgang wiederholt sich für alle Boote an jeder Bahnmarke, mindestens für das Ziel. 

Durch die Zusammenarbeit von zwei Personen kann die Datenerfassung produktiv abgewickelt werden. 
Eine Person wird beobachten und ansagen, die andere Person bedient das Programm. 
Auf diese Weise kann auch eine handgeschriebene Liste auf Papier nachträglich digitalisiert werden.

Andere Eingabeformen sind möglich, auch ein Anschluss an das Trackingsystem könnte realisiert werden.

## Datenformat

Alle Daten liegen im zugänglichen Txt oder Xml Format vor. 
Das Format wurde mit Rücksicht auf den Faktor Mensch entworfen!
Sie können einen Texteditor benutzen und Ihr Spreadsheet einsetzen. 
Nur die Eingangsdaten werden erfasst. 
Berechnete Felder werden nicht gespeichert.

Das Programm hat einen robusten Parser für die Daten. 
Trauen Sie sich, die Daten direkt mit einem Texteditor zu bearbeiten.

## Server

Der Server kann eine ganz normale Desktop Anwendung sein. 
Er muss nicht konfiguriert werden. 
Sie können den Server einfach starten und lassen ihn laufen, solange Sie ihn brauchen. 
Verwenden Sie einen aktuellen Rechner für die Serverfunktion und erlauben Sie dem Programm die Annahme von Verbindungen aus dem (lokalen) Netz. 
Sie brauchen nur das Programm selbst zu kopieren, es wird normalerweise keine Datenbank verwendet.

## Client

Der Client auf der Ausgangsseite kann auch eine normale Desktop Anwendung sein oder ein SPA Client, welcher im Browser läuft. 
Es handelt sich bei den Fleetrace Clienten um rechnende Anwendungen. 

[weiter](page-02.html)