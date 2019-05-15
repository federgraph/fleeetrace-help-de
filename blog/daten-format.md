---
layout: default
lang: de
title: Datenformate
---

# Datenformate

FR verwendet verschiedene Datenformate:
1. **Kanonischer Text**: Dieses Format ist nützlich wenn Sie 
einzeilige Nachrichten über das Netzwerk zum Programm senden.
1. **Kompakter Text**: Dieses Format verbraucht weniger Platz 
und erlaubt das direkte Einfügen von Excel-Daten über die Zwischenablage.
1. **Xml**: Das Xml Format ist zu empfehlen, wenn Sie UTF-8 
kodierte Daten im Web veröffentlichen, komplett mit Byte-Order-Marker, ohne 
Probleme mit der Zeichenkodierung oder den Zeilenenden.
1. **Html**: Stellen Sie sich ein html5 Fragment vor; Sie 
können es intern zu einem gültigen XHTML Dokument ergänzen, und dann mit 
einem Xml Parser in das kanonische Text Format transformieren lassen. Das 
html Format wurde ganz zuletzt noch ergänzt, weil es einfach praktisch ist!

Ganz egal, welches Format Sie benutzen, alle lassen sich ohne Verlust umwandeln.

Das jeweils zweckmäßige Format sollte in den verschiedenen Situationen 
verwendet werden; es gibt kein einziges, bestes Format. Der Ansatz, einen Satz 
von konvertierbaren Formaten bereitzustellen ist der Schlüssel beim Aufbau eines 
eleganten und flexiblen Systems.

FR wurde ausgehend von der Definition von sehr effizienten einzeiligen 
Nachrichten entwickelt, die über das Netzwerk geschickt werden können. Das 
wichtigste ist, das das Datenformat vollständig offengelegt wird.
