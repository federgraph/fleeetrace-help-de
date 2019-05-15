---
layout: default
title: About
---

# About

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
- Das ist der hauptsächliche Vorteil von FR.

Startpunkt kann FR01 auf dem Desktop sein. 
Es solle eigentlich als erstes ausprobiert werden.
Allerdings gehe ich davon aus, 
das des die browserbasierte SPA Anwendung [FREO](https://federgraph.de/freo/index.html) sein wird, die Sie als erstes kennenlernen werden.

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

Dann kann mit installieren und lokal starten.
```ruby
bundle install
bundle exec jekyll serve
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

Also alles was nicht auf GitHub im fleetrace-help-de repo ist, wegen .gitignore findet sich im repo von Cayman.