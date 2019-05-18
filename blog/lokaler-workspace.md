---
layout: default
lang: de
title: Lokaler Workspace
---
        
# Local Workspace

In FR01 erscheinen die konfigurierten Datenquellen in der ComboBox (auf Seite Menu im oberen Container).

Es ist im Prinzip nur eine Liste von Urls. Für den konfigurierten Workspace in der ersten Zeile des nachfolgenden Beispiels benötigen Sie keinen Webserver.

```plaintext
C:\Users\UserName\Documents\FRDataDir\EventMenu.xml

http://localhost:8080/FR/EventMenu.xml
```

Sie können einen mit Gleichheitszeichen abgetrennten Namen voranzustellen, dann wird in der ComboBox der Name angezeigt und nicht die Url selbst.
Einen Workspace, von dem Sie wissen, dass er editierbar ist, können Sie mit einem Stern kennzeichnen.

```
* Local Workspace = C:\Users\UserName\Documents\FRDataDir\EventMenu.xml
Local Server = http://localhost:8080/FR/EventMenu.xml
```
Wenn Sie auf einer Zeile stop eingeben, dann wird das Programm die restlichen 
Zeilen ignorieren und auch die fest verdrahteten Beispiel-Urls nicht hinzufügen.

```
* Local Workspace = C:\Users\UserName\Documents\FRDataDir\EventMenu.xml
Local Server = http://localhost:8080/FR/EventMenu.xml
stop
```

Einzelne Zeilen können wie üblich mit // oder # auskommentiert werden.

```plaintext
* Local Workspace = C:\Users\UserName\Documents\FRDataDir\EventMenu.xml
# Local Server = http://localhost:8080/FR/EventMenu.xml
// Test Server = http://localhost/WebApplication/EventMenu.aspx
Example Server = http://www.fleetrace.org/EventMenu.xml
stop
```

Im Memo (auf Seite Workspace im unteren Container im Programm FR01) können 
Sie die Urls verwalten. Eine nur temporär in das Memo eingegebene Liste bzw. 
einzelne Url können Sie direkt in die ComboBox übernehmen, ohne die Liste auf 
der Festplatte zu ändern.

Mit dem Button Save wird die Liste im Memo auf der Festplatte gespeichert, so 
dass sie immer beim Start von FR01 geladen wird. (Sie müssen die Liste erst 
Laden, bevor der Button Save verfügbar ist.) Die Datei hat den Namen 
fr-workspace-urls.txt, liegt unter Windows im Ordner AppData/Local/Riggvar/FR, 
und wird von FR01 automatisch angelegt. Benutzen Sie die Zwischenablage um eine 
aktuelle Liste in das Memo zu kopieren. Es macht Sinn, dass Sie die Urls vorher 
im Explorer oder Browser testen.

Grundsätzlich wurde FR01 als Programm konzipiert, welches nichts auf der 
lokalen Festplatte speichert. Die dann doch noch hinzugefügte Option der 
Selbstverwaltung von Urls gibt Ihnen die notwendige Flexibilität.

