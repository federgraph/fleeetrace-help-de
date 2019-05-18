---
layout: default
lang: de
title: Programme
---

# Verfügbare Programme

## FR01

[FR01](../applications/FR01.html) ist die neueste Ergänzung von 2012.
Es ist der frei verfügbare Desktop Client.

**Update 2019**: Quelle jetzt auf GitHub, GPL 3.0.

## FR02

[FR02](../applications/FR02.html) ist ein minimalistischer Server für die Daten des Events,
die mit FR01 betrachtet und bearbeitet werden können.

**Bemerkung 2019**: Es ist eine normale Desktop Anwendung, extrem einfach.
Einfach Doppelklick - die Anwendung startet - und Zugriff auf die Daten über Http ist möglich.
Kann aber heute durch einen einfachen `node.js/express` Server ersetzt werden,
der einfacher zu verstehen ist und auf einem Raspberry Pi laufen kann.

**ToDo**: Link mit Beispiel für Script einfügen.

## FR99

[FR99](../applications/FR99.html) soll die vorbereitenden Arbeiten optimal unterstützen.
FR99 wird zusammen mit FR01 und FR02 genutzt.

**Bemerkung 2019**: Ich habe die Quelle von FR01 veröffentlicht, also fast das gleiche wie FR99.

## Silverlight Client

~~Veraltet (von 2012): Überprüfen Sie Ihre Silverlight Installation, bevor Sie den Client laden.~~

Ab 2018: Angular SPA (Single Page Application) ist der Ersatz für Silverlight!

Ersetzen Sie in Gedanken `immer` *Silverlight* mit **Angular**.

Anstelle von Angular kann man auch was anderes nehmen, 
es gibt gute Alternativen, nur die Angular Anwendungen gibt es schon.

How about Flutter?

## FR94

Die gleichen Daten, die der Silverlight Client anzeigen kann,
können auch mit dem Desktop Client FR94 geladen werden.

Mit [FR94](../applications/FR94.html) können Sie auch Daten **erzeugen**, 
es steht eine Teilmenge der vollen Funktion von FR zur Verfügung.
Der Race Teil wurde entfernt, der Event Teil ist enthalten.

**Bemerkung 2019**: FR94 ist vergleichbar mit **Angular FR03E1**, siehe GitHub repository.

**ToDo**: Angular Projekte listen, beschreiben, und Link bereitstellen.

## FR93

[FR93](../applications/FR93.html) ist für die Erzeugung der Daten gedacht.

**Bemerkung 2019**: Mit Eingabe der Ergebnisse über die graphische Oberfläche.
Danach werden die Ergebnisse über die Zwischenablage entnommen.

## FR38

[FR38](../applications/FR38.html) ist ein externer Timing Client.
Es gibt Varianten für unterschiedliche Szenarien.

**Bemerkung 2019**: FR38 benutzt eine TStringGrid Komponente.
Sie navigieren im Grid mit den Pfeiltasten von Zelle zu Zelle
(oder selektieren eine Zelle mit der Maus) und drücken dann den Space-Bar um eine Nachricht zu generieren.
Der Angular Client hat eine bessere Oberfläche, besser für Touch.
Neue Timing Clienten sollten eine Oberfläche haben, die besser ist oder mindestens gleichwertig zum Angular Client,
der neue Maßstäbe setzt.

## FR04

[FR04](../applications/FR04.html) ist ein Server, welcher Daten Live im Netz bereitstellt.

**Bemerkung 2019**: Verwenden Sie FR69.

## FR97

[FR97](../applications/FR97.html) ist die Einheit, mit der der Silverlight Client ausgeliefert wird.

- Damit können die Ergebnisse sehr einfach im Intranet für die Nutzung im Browser bereitgestellt werden.
- Der gleiche Silverlight Client kann auch für eine Website im Internet benutzt werden.
- Der Silverlight Client ist für eine bestimmte Domain lizensiert.

**Bemerkung 2019**: Silverlight gibt es nicht mehr.
Angular Client ist aktuell und Open Source.
Der Client könnte eine native App für die Geräte sein, das kommt später.
Hier geht es um den Test Server für zu Hause.
Das können Sie alles selbst machen.
FR69 kann anstellen von FR97 benutzt werden,
es ist immer möglich mit Kanonen nach Spatzen zu schießen.
Warum nicht Node.js oder Asp.Net?

[Feature Matrix](page-04.html)
