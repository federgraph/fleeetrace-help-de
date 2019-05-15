---
layout: default
lang: de
title: Warum 500
old_permalink: "http://www.fleetrace.org/blog/2012/06/warum-500/"
---

# Warum 500

Bei der Eingabe der Zielpositionen für Boote in einer Wettfahrt wird zum 
Beispiel die Nachricht `FR.*.W1.Bib1.RV=500` erzeugt,
wenn Sie im Programm FR01 im Grid auf Seite Timing das Feld 1 selektieren,
und dann die Leertaste drücken oder Enter. (Auf dem Mac nur die Enter Taste).

Die Nachricht enthält eine Zuweisung vom Typ RaceValue (RV) an Bib1 
(Bug-Nummer 1) in W1 (Wettfahrt 1, hier ein deutscher Ausdruck!), bezogen auf 
die anonyme Division (Bootsklasse *) im Namespace FR (FleetRace).

Was Sie damit bezwecken ist die Eingabe des Zieldurchgangs für Bugnummer 1. 
Wenn Sie die korrekte Zielposition für das Boot mitloggen, dann können Sie diese 
statt der 500 manuell eintragen, bevor Sie die Nachricht manuell senden. Der 
Trick ist hier, dass Sie nicht wissen müssen, welche Zielposition das Boot 
bekommt. Die 500 ist auf jeden Fall viel zu groß, das Programm wird daher die 
nächste freie Position verwenden.

Wie Sie die Nachricht erzeugen spielt keine Rolle. Auf Seite Keying im 
Programm geben Sie die Bugnummer ein und drücken Enter. In anderen Versionen des 
FR Programms können Sie eine Nachricht über das Netzwerk schicken.

Es wäre möglich, die Anzeige der Nachricht zu maskieren, aber ich will die 
Funktionsweise des Programms nicht verschleiern, sondern verständlich machen.

Zum Kontext wäre noch folgendes zu sagen:
Wenn Sie Zielpositionen eingeben, sollten Sie sich im Eingabemodus Strikt 
befinden, das ist Standard und ich bin hier davon ausgegangen.

Mit `R-` und `R+` wechseln Sie das aktuelle Race (Wettfahrt). Der Button 
dazwischen zeigt Ihnen das aktuell ausgewählte Race an. Nach Auswahl der 
Wettfahrt müssen Sie also nur die Bugnummern anklicken und Space drücken, um 
Zieldurchgänge zu generieren. Easy!

Es wird Varianten für die Eingabe der Zielpositionen geben, das Format der 
Nachricht ist jedoch fix. Statt 500 könnte man auch 1000 eingeben, Hauptsache 
die Zielposition ist größer als Sie sein soll!

Es handelt sich hier um eine der Stellen, wo das Programm mitdenkt. Eine 
zweite Stelle, wo das Programm als Schlaumeier auftritt, finden Sie bei der 
Korrektur von bereits eingegebenen Zielpositionen, zum Beispiel im Grid auf 
Seite Event. Dort werden die folgenden Positionen automatisch angepasst - aber 
nur im Modus Strikt.

