---
layout: default
lang: de
title: Beispieldaten
---

# Wie Sie Beispieldaten herunterladen

Es funktioniert mit FR01. Bei den Daten, die FR01 herunterladen kann handelt es sich entweder 
um das Inhaltsverzeichnis EventMenu.xml oder die EventData.* Dateien mit den Daten der einzelnen Events.

In beiden Fällen können die heruntergeladenen Daten im Memo (mehrzeiliges Editierfeld) auf Seite Reports angezeigt werden.
Die Daten liegen also im Quelltext vor.

Vom Memo aus können Sie die Daten über die Zwischenablage in Notepad einfügen und von dort aus auf der Festplatte speichern,
gegebenenfalls mit der Kodierung UTF-8. 
Strg A (alles Markieren), Strg C (Kopieren) und Str V (Einfügen)
sind dabei die wichtigsten Tastenkombinationen (unter Windows und Ubuntu).

Wenn Sie auf Seite Menu (im oberen Container) den Button More anklicken, dann werden zusätzliche Schaltflächen sichtbar,
darunter der Button Download, mit dem Sie das EventMenu.xml in das Memo laden.

Wenn Sie die zusätzlichen Schaltflächen sehen und auf einen Event Button drücken,
dann wird EventData.* heruntergeladen und im Memo angezeigt,
und zwar die unverarbeitete Version.

EventMenu.xml und EventData.* können anders benannt sein, wichtig ist der Inhalt.
Egal, ob TXT, XML, oder HTML, es sind in diesem Sinne immer Textdateien,
die Sie auf Ihrer Festplatte ablegen können.

Sollte das heruntergeladene EventData.* im Format Xml oder Html vorliegen, 
dann können Sie es trotzdem als Text speichern, weil das Programm FR01 die 
Formate verlustfrei konvertieren kann.

Um die Formate zu konvertieren müssen Sie den Event zuerst laden. 
Das passiert standardmäßig, wenn der Modus More im Menu nicht aktiv ist. 
Beim Laden der Daten des Events erfolgt eine strikte Validierung. 
Die Ausgabe von Text oder Html auf Seite Reports liefert daher immer eine gefilterte Version der Daten, 
die zusätzlich Ihre Änderungen enthält,
welche Sie mit Hilfe der grafischen Oberfläche (Grid) eventuell schon hinzugefügt haben.

Wenn sie mit Ihren eigenen Daten arbeiten wollen, dann macht es Sinn vom *Template* auszugehen,
indem Sie sich ein passendes Beispiel herunterzuladen.
So legen Sie die Beispieldaten in einen lokalen Workspace:

- Ordner anlegen (zum Beispiel C:\FR\Workspace)
- EventMenu.xml herunterladen und im Ordner speichern als EventMenuLocal.xml
- EventData.txt herunterladen und speichern (zum Beispiel als ED01.txt)
- EventMenuLocal.xml editieren (dazu unten mehr)

Auf Seite Workspace (im unteren Container) können Sie den Zugriff auf Ihren 
lokalen Workspace konfigurieren:

- Button Laden drücken (Memo kann dann leer sein)
- Url zum Memo hinzufügen (am besten ganz oben)
- Button Save drücken
- Url-Combo auf Seite Menu aktualisieren mit Button auf Seite Workspace (Buttonbeschriftung ist selbsterklärend)

Die Zeile mit der Url sollte im Beispiel etwa so aussehen:
```
* MyLocalWorkspace = C:\FR\Workspace\EventMenuLocal.xml
```

Der * vorn bedeutet, dass Ihr lokaler Workspace editierbar ist.

So wird das EventMenuLocal.xml angepasst:

- Löschen Sie als erstes die Sektionen für die EventDaten, die Sie nicht brauchen.
- Ignorieren Sie die Pfade zu den Bildern (leer lassen), die Buttons für die Events in FR01 zeigen nur den Namen an.
- Ändern Sie den Namen des Events.
- Am wichtigsten ist der Pfad. Ausgehend von Root müssen die kombinierten Pfade die korrekte Url zur Datei ergeben.
- Achten Sie bei Root und den Ordnern auf das abschließende Pfad-Trennzeichen (Schrägstrich oder umgekehrter Schrägstrich).

So könnten Sie später die Dateien aus Ihrem lokalen Workspace ins Web schieben:

Legen Sie EventMenu.xml als Kopie von EventMenuLocal.xml im Workspace-Ordner an. 
Nun brauchen Sie in der Kopie nur noch den Pfad anzupassen. Die Pfade der 
einzelnen Events sind relativ, egal wie viele Events Sie in der Datei auflisten, 
es sind nur minimale Änderungen notwendig, wenn Sie einen Workspace verpflanzen 
wollen. Das ist der Hauptvorteil der gewählten Struktur für EventMenu.xml.

Nachdem Sie einen lokalen Workspace angelegt haben, können Sie von FR01 aus 
damit genau so arbeiten, wie mit den Daten aus dem Web, nur besser, weil Sie 
offline sein können und weil der Write Button auf Seite Menu funktioniert (wenn 
Sie Ihren lokalen Workspace mit * versehen haben).

Ist es so besser, als sich immer wieder mit dem Datei-Öffnen-Dialog herumzuquälen?
Am Anfang vielleicht nicht, aber wenn Sie später die Daten kostengünstig im Web sichtbar machen wollen, dann schon, oder?
