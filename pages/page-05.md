---
layout: default
lang: de
title: Einsatzfälle
---

# Use Cases

Use Cases = Einsatzfälle

```
Warum soll Ich eigentlich den 'Markt' vorbereiten, und für wen?

Sie müssen das alles hier mit Humor nehmen, 
  außer wenn ich rede von Sozialismus.
```

## UC 1

> Sie wollen die Ergebnisse im Silverlight Client zur Verfügung stellen.

Bausteine:
- [FR93](../applications/FR93.html)
- [FRIA04](../silverlight/FRIA04.html)
- Web Editor (Visual Studio Code) und FTP Client Programm (FileZilla).
- statische Website (GitHub Pages)

Mit FR93 erstellen Sie die Text Datei oder Xml Datei für die Ergebnisse. 
Die Ergebnisse werden mit FileZilla via FTP auf die statische Website hochgeladen. 
Über einen Link auf der Website kann der Silverlight Client FRIA04 im Browser angezeigt werden. 
Der Silverlight Client lädt als erstes das EventMenu.xml file vom Server, 
und später - nach Auswahl durch den Benutzer - die einzelnen Event.xml Dateien.

Es können beliebig viele EventMenu.xml Dateien und beliebig viele Event.xml Dateien verwaltet werden.
Wenn eine konstante Anzahl von Events angelegt wird, die wiederverwendet werden, 
dann kann das EventMenu.xml unverändert bleiben. 
Die Aktualisierung eines Events reduziert sich dann auf das Hochladen der jeweiligen Event.xml Datei.

**Update 2019**: Angular ist das neue Silverlight, siehe FR03A1 oder FR03E1.

## UC 2

> Sie wollen die Ergebnisse im Desktop Client zur Verfügung stellen.

Bausteine:
- FR93
- FR94
- Web Editor, FTP Client
- statische Website

Es funktioniert im Prinzip genau so wie bei UC 1, 
nur dass Sie keine Lizenz für den Silverlight Client benötigen.

**Update 2019**: Das mit der Lizenz hat sich sowieso erledigt, wir sind jetzt wieder sozialistisch.

## UC 3

> Sie wollen die Kosten maximal reduzieren.

Bausteine:
- Spreadsheet und Texteditor
- FR94
- Web Editor, FTP Client
- statische Website

Es funktioniert wie bei UC 2,
nur dass Sie die Daten mit dem Spreadsheet und einem Texteditor vorbereiten, 
bzw. FR94 selbst dafür benutzen. 
Sie können die Text Dateien auch von einem anderen Programm exportieren.

**Update 2019**: Kosten? Es kostet nur Zeit, und die kann mit FR minimiert werden.

## UC 4

> Sie betreiben eine Team Seite und wollen aktuelle Ergebnisse bereitstellen - von den Events, an denen Sie teilnehmen.

Bausteine:
- keine

Es kann so eingerichtet werden, dass die Daten und der Silverlight Client von 
einer anderen Site geladen werden. Dann reicht es, wenn etwas Html mit dem 
Object-Tag für den Silverlight Client in eine Html-Seite eingefügt wird. Das 
passende EventMenu.xml und die Event.xml Dateien werden auf der anderen Website 
bereitgestellt. Organisieren Sie, dass sich jemand um die Ergebnisse kümmert. 
Stellen Sie dieser Partei die Eingangsdaten zur Verfügung.

**Update 2019**: Müsste aktualisiert werden, Stichwort Web Assembly. 

## UC 5

> Sie wollen Live-Daten vom Race empfangen.

Bausteine:
- [FR38](../applications/FR38.html)
- FR04
- FRIA04

Mit FR38 senden Sie Timing Messages zum Server FR04.
Dieser leitet die Nachrichten zum Client weiter.
Mit Hilfe von FRIA04 (Silverlight Applikation) können die Nachrichten in Echtzeit empfangen werden.

**Update 2019**: Funktioniert mit Angular Client, der über Web Sockets an einen Node.js Proxy Server angebunden ist.
FR38 kann durch eine moderne Variante ersetzt werden.

## UC 6

> Sie wollen Live Daten vom Race empfangen, aber möglichst direkt und mit minimalem Aufwand.

Bausteine:
- FR38
- FR92

Mit FR38 senden Sie Timing Messages direkt zu FR92. Beliebig viele Sender können angeschlossen werden.

**Bemerkung 2019**: Absolut, via TCP, geht immer noch, wird immer funktionieren.

## UC 7

> Sie wollen den aktuellen Stand vom zentralen System abrufen und lokal speichern.
 
Bausteine:
- FR92 (zentrales System)
- FR91 (beliebig viele)

FR92 übernimmt die Funktion des Bridge Servers.
FR91 kann sich als Bridge Client mit FR92 verbinden und Daten abrufen.
FR91 als Bridge Client kann auch Daten senden, zum Beispiel Penalties aktualisieren.

**Bemerkung 2019**: Es werden praktisch zwei fast gleiche Applikationen miteinander verbunden.
Niemand versteht wie die Bridge funktioniert, und es wurde auch lange nicht mehr getestet.
Wie ein Angular SPA Client funktioniert wird eher verstanden, obwohl es komplizierter ist.

## UC 8

> Sie benutzen bereits einen Server FR04 und wollen UC 7 damit realisieren.
 
Bausteine:
- FR91 (Master)
- FR04 (Server)
- FR91 (beliebig viele)

Sie können so auch gemeinsam am gleichen Event *arbeiten*.
Stellen Sie sicher, das mindestens einer die Arbeit speichert, und machen Sie regelmäßige Backups.

**Bemerkung 2019**: Ja ja, das ist gut, aber akademisch, für Insider.

## UC 9

> Sie wollen ganz normale html Seiten mit dem aktuellen Stand abrufen.
 
Bausteine:
- FR91 (Client)
- FR04 (Server)
- Browser (viele)

Sie benutzen FR91 als Bridge Client und senden die Daten zu FR04 (via Upload).
FR04 hat einen eingebauten Webserver. Mit dem Browser rufen Sie die Html Seiten von FR04 ab.

**Bemerkung 2019**: Ich habe die Quelle von FR69 veröffentlicht.
Man kann FR69 anstelle von FR04 bzw. FR91 verwenden.
Als Client für die Datenerfassung kann alles Mögliche verwendet werden.

# UC 10

> Sie wollen UC 9 benutzen, sind aber vom Design der Webseiten nicht beeindruckt.
 
Zusätzliche Bausteine:
- Web Editor

Erstellen Sie Ihr verbessertes Design und benutzen Sie es als Template.

**Bemerkung 2019**: Im Prinzip richtig, aber die Webseiten sollten von einem Web Frontend an den Browser geliefert werden.
Dort können Sie machen was Sie wollen, müssen keine Rücksicht auf die spezielle Umgebung der Delphi-Applikation nehmen.

## UC 11

> Sie verwenden UC 1 mit Erfolg und wollen das Sponsor Logo im Silverlight Client unterbringen.
 
Bausteine:
- Logo
- Visual Studio oder Expression Blend

Sie haben bereits eine Lizenz für den Silverlight Client. 
RiggVar Software erstellt eine neue Version mit Sponsor Logo. 
Sie können die Oberfläche des Silverlight Client auch selbst gestalten.

**Update 2019**: Die Lizenz ist GPL 3.0, die haben Sie quasi schon.
Die Oberfläche des Angular Client verändern Sie nach Bedarf selbst.
( `git clone .../fleetrace-angular-fr03e1`)

# UC 12

> Sie sind allgemein am Timing interessiert und wollen das System beim Schulsport einsetzen.

Bausteine:
- FR38
- FR95

Mit FR38 senden Sie Timing Messages direkt zu FR95. 
Es funktioniert auch mit FR04 oder FR92. Beliebig viele Sender können angeschlossen werden.

**Bemerkung 2019**: Gute Idee, ich müsste dazu noch die Quelle von FR38 veröffentlichen.
Und die von FR95, aber FR69 (auf GitHub) kann anstelle von FR95 verwendet werden,
zumindest um nachzuweisen, dass es funktioniert.
Genau genommen ist es nicht schwer einen aktuellen Ersatz für FR38 komplett neu zu schreiben.
Das Protokoll ist dokumentiert.
Es werden nur kurze Text Nachrichten vom Timing Client FR38 and den Result Server gesendet.

# UC 13

> Sie verwalten viele Wettkämpfe und brauchen mehr Dynamik in der Verwaltung.

Bausteine:
- Visual Studio 2010
- ASP.NET Website
- Datenbank

RiggVar Software stellt Ihnen einen Prototyp für die ASP.NET MVC Anwendung zur Verfügung.
Damit können Sie Workspaces verwalten, Eventdaten hochladen und mehr.
Die Event-Website kann natürlich auch mit Ruby on Rails realisiert werden. 

**Bemerkung 2019**: Die Möglichkeiten sind vielfältig.
Ich glaube nicht dass Sie mein altes Projekt von 2012 als Vorlage brauchen.
Machen Sie es einfach so wie immer.

## UC 14

> Sie wollen das Trackingsystem anzapfen und die Timing Daten im Silverlight Client sehen.

Bausteine:
- Interface Spezifikation
- Adapter (zu programmieren)
- FR04
- FRIA04

Die Anbindung wird im Rahmen eines Pilotprojektes realisiert. 
Sie können auf die Mitwirkung von RiggVar Software zählen. 
Sie können es aber auch selbst machen, 
da das Protokoll für die Datenübertragung im System FR öffentlich ist.

**Bemerkung 2019**: Im Prinzip richtig, vorausgesetzt Sie wollten den Angular Client oder etwas Ähnliches verwenden,
in Verbindung mit FR69.
Was die Mitwirkung anbetrifft bin ich skeptisch - das wäre teuer, jetzt wo alles Open Source ist erst recht.
Aber als Vision nicht schlecht (Fata Morgana). Glauben Sie, dass Sie Zugang zum Tracking-System bekommen?

## UC 15

> Sie wollen einen Browser für das Timing verwenden und die Timing Daten im Desktop Client sehen.

Bausteine:
- Browser mit javascript
- FR04 (mit angepassten Sicherheitseinstellungen)
- FR91

Es gibt Beispiele für die JavaScript Timing Widgets. 
Es ist eine gute Netzwerkverbindung erforderlich, die nur im Intranet gegeben ist. 
FR91 benutzt die Client Bridge, um sich mit FR04 zu verbinden.

Andere Kombinationen sind möglich.

**Bemerkung 2019**: Die Netzwerkverbindung sollte heute kein Problem mehr sein.
Die Infrastruktur ist jetzt da, und die Geräte gibt es auch.
Ich empfehle einen Node.js proxy server in Verbindung mit FR69.
Als Browser Client käme FR05I in Frage, siehe GitHub repo.

