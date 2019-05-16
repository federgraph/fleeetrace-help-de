---
layout: default
title: About
---

# About

## Über die Hilfe zu FR

```
Also als erstes will ich hier mal aufräumen und überprüfen.
Und erst danach ergänzen.

We will elimiate the typos as we go.

Wenn Sie etwas verwenden möchten, 
und die Verwendung konkret beschreiben wollen für Ihr Team,
dann können Sie das natürlich machen, wir sind hier bei GitHub,
und mit Markdown ist es einfach.
```

## History

ToDo: Screenshot einfügen, von .chm Datei.

## Die *Bedienungsanleitung* für FR01

Das Programm FR01 ist einfach zu benutzen, alles was Sie wissen müssen sollten Sie hier finden.

Das Besondere am Programm ist dass die Daten des Events - also der Regatta, bezogen auf
eine Bootsklasse - immer in der Originalversion heruntergeladen werden.

Die Daten sind vollständig und können damit auch verändert werden,
die neuen Ergebnisse werden vom Programm berechnet.

> FR ist das erste System, welches diesen Ansatz konsequent umsetzt.

- Im Gegensatz dazu sind die üblichen Berichte in der Regel nicht vollständig.
- Zum Beispiel fehlt die Information, welche Zielplatzierung ein Boot hatte, das nach dem Zieleinlauf disqualifiziert wurde.
- Mit unvollständigen Informationen kann keine Was-Wäre-Wenn-Analyse erfolgen.

Startpunkt kann FR01 auf dem Desktop sein.
Es solle eigentlich zuerst ausprobiert werden.
Allerdings gehe ich davon aus,
das es die browserbasierte SPA Anwendung [FREO](https://federgraph.de/freo/index.html) sein wird,
die Sie als erstes kennenlernen werden.

FREO soll zukünftig auch von GitHub aus geladen werden.

[Ganz nach oben](index.html)

## Using Jekyll locally

Vom Cayman Theme brauchen Sie zusätzlich:
```
assets/css/style.scss

_sass
  jekyll-theme-cayman.scss
  normalize.scss
  rouge-github.scss
  variable.scss

jekyll-theme-cayman.gemspec
```

Dann kann man installieren und lokal starten.
```
bundle install //einmal
bundle exec jekyll serve //nach Bedarf, für Vorschau
```

Das ist in .gitignore:
```
_site/
_sass/
.sass-cache/
.jekyll-cache/
.jekyll-metadata/
.vscode/spellright.dict
.vscode/settings.json
jekyll-theme-cayman.gemspec
assets/css/style.scss
Gemfile
Gemfile.lock
*.gem
```

Also alles was sich nicht auf GitHub im `fleetrace-help-de` repository
befindet (wegen .gitignore) findet sich im repo von [Cayman](https://github.com/pages-themes/cayman).