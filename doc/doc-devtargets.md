---
layout: default
lang: de
title: Produktidee
---

```
Ich warne Sie!
( Zum Glück wurde das hier nie veröffentlicht. )
```

# Entwicklungsziele

Da Softwareentwicklung einen zyklischen Verlauf nimmt, gibt es effektiv 
mehrere Ziele/Ausgänge im Kreisverkehr. Die drei Ziele sind:

- Entwicklung eines hochspezialisierten Unikats auf Basis des Frameworks. Die 
Spezifikation wird maßgeblich vom Kunden beeinflusst. Die Anwendung ist nur auf 
der Plattform des Kunden lauffähig.
- Weiterentwicklung des Frameworks.
- Entwicklung einer Verkaufsanwendung auf der Basis der Frameworks. 
  Die Spezifikation wird unabhängig vom Kunden fixiert.
  Diese Anwendung ist praktisch überall lauffähig.

Der Einsprung in den Zyklus ergibt sich wie folgt:
- Eine komplexe Anwendung wird erstellt (Unikat).
- Die Anwendung wird als Verkaufslösung neu entwickelt, jedoch nicht verkauft.
- Es wird eine zweite Anwendung erstellt, mit Ähnlichkeit zur ersten Anwendung.
- Es wird ein Framework herausgearbeitet.
- Mit dem Framework wird eine weitere Anwendung erstellt.
- Das Framework wird verbessert mit den Erkenntnissen der letzten Entwicklung.
- Die Anwendung wird portiert auf eine neue Plattform.
- Die ursprüngliche Anwendung wird auf die neue Plattform portiert.
- Das Framework wird verbessert mit den Erkenntnissen des Ports.

Es ergeben sich eine Reihe von abstrakten Konsequenzen:
- Unterschiedliche Ergebnisse (Ziele): Einzelanwendung, Framework und Verkaufsprodukt.
- Spezialisierung durch Beschränkung auf Anwendungen, die das Framework verwenden können.
- Dichtere Abdeckung des Operationsgebietes durch Varianten für Teile des Systems.
- Höhere Qualität der Einzelanwendung.
- Konzentration auf das Allgemeine, Wiederverwendbare. Das Framework wird zum wichtigsten Produkt.
- Zunehmend Kooperation in Bezug auf das Spezielle.

Ein Beispiel für (rein fiktive) konkrete Konsequenzen:
- Die Anwendung richtet sich als Verkaufslösung an den einzelnen Teilnehmer 
der Sportveranstaltung, der Ergebnisse selbst berechnet, unabhängig vom Veranstalter.
- Die Erfassung der Wettkampfdaten erfolgt im Team, gemeinsam mit anderen 
Teilnehmern oder Personen im Umfeld. Die beteiligten Personen verwenden Ihre 
eigenen Ressourcen wie PDA, Handy, Notebook, LAN oder Internetzugang.
- Die Anwendung existiert auf drei Plattformen. Jeder Akteur benutzt das Programm seiner Wahl.
- Mit Texteditor und Spreadsheet kann sinnvoll zugearbeitet werden, da die Nachrichtenspezifikation dafür ausgelegt wurde.
- Die Ergebnisse stehen allen Beteiligten sofort zur Verfügung, können von jedem kopiert und lokal bearbeitet werden.
- Das Prinzip Calc Everywhere wurde umgesetzt: Jeder Knotenpunkt rechnet selbst, 
  nur die Eingangsdaten werden ausgetauscht. Eine automatische 
  Synchronisation der rechnenden Knoten ist über 'Bridge' oder 'Switch' möglich.
- Das Ergebnis, die vollständigen Wettkampfdaten, können zentral in der 
  Datenbank abgelegt werden. Über die Webanwendung ist der Zugriff auf die Daten 
  jederzeit möglich. Die Desktopanwendung kann Daten direkt vom Web laden.
- Die Webanwendung rechnet ebenfalls. *Was wäre wenn - Analysen* können vom 
  Surfer jederzeit isoliert in der Browsersession durchgeführt werden.
- Da die Webanwendung rechnet, kann der Speicherbedarf in der Datenbank 
  (für die verschiedenen Reports) reduziert werden.
- Ohne eine Framework-Entwicklung, zu der mehrere Projekte beitragen und die Ihr eigenes Budget hat,
  ist ein vergleichbar umfangreiches System nicht realisierbar.
- Durch die Beschränkung auf die Kernfunktion kann die Software in der Regel 
  nicht unverändert für die offizielle Auswertung eingesetzt werden, obwohl die Ergebnisse korrekt berechnet werden.
- Es ist damit zu rechnen, dass Anwender Einsatzmöglichkeiten für das Framework finden.

```
Ich bin geschockt, ist das jetzt schon Neoliberal?
Träumt der Typ von einem Office in Shanghai?

Wo sind eigentlich die automatischen Tests?
```

Zurück zu den [Dokumenten](doc-index).