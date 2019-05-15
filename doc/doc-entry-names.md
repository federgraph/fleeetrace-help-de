---
layout: default
lang: de
title: Namen
---

# String-Tabelle mit Namen

## Intro

Die Datenbeispiele enthalten KEINE Namen. 
Dadurch wird auch die Größe der Dateien reduziert.
Im realen Anwendungsfall müssen Sie natürlich **Vornamen**, 
**Nachnamen**, **Ländercode** oder **Club** der Teilnehmer an der Veranstaltung bereitstellen, 
um diese auf den Reports anzuzeigen. 
In diesem Artikel will ich beschreiben, 
wie Sie die **Stammdatentabelle** einrichten und *Anzeigeoptionen* für die Namen einstellen.
Mehr über das Füllen der Stammdatentabelle finden Sie bei den Themen 
[Spreadsheet](doc-spreadsheet-use.html) und 
[Export](doc-data-export.html).

## Stammdaten

### Tabelle

Die Tabelle für die Namen der Athleten/Entries (Stammdatentabelle) existiert 
unabhängig von den Race Daten und den Event Daten. Ein Entry im Race/Event kann 
die Namen über die **SNR** (Zahl) in der Tabelle nachschlagen und anzeigen.

Sie pflegen die Stammdaten unabhängig von den Race- und Event Daten, 
stellen aber die Verknüpfung über die SNR sicher. 
Die SNR muss natürlich eindeutig sein. 
Die SNR (*Stammdaten-Nr.* oder *Sportler-Nr.*) ist der **Primärschlüssel** und sollte nicht mit der *Segel-Nr.* verwechselt werden. 
Die SNR ist *immer* eine **positive Ganzzahl**.

In vielen Fällen sollten Sie die Segelnummer in eine ganz normale Spalte der Tabelle einspeichern, 
mit oder ohne alphanumerischem Bestandteil. 
In anderen Fällen könnten Sie es bevorzugen, die numerische Segelnummer als SNR zu verwenden. 
Wichtig ist nur, dass Sie die Bedeutung von SNR als **Verknüpfung** zwischen den Tabellen Race, Event und Stammdaten verstehen.

Änderungen am Inhalt der Tabelle werden sichtbar, 
wenn die Ausgabe im Grid das nächste mal aktualisiert wird. 
Dies erfolgt regelmäßig wie bei einem Scheibenwischer, 
sie müssen eine Sekunde **Geduld** haben.

Die Stammdaten werden zusammen mit dem Event gespeichert. 
Wenn das Programm nicht läuft, liegen die Informationen also im Text- oder Xml File, 
im Dateisystem oder einem Blob Feld einer Datenbank. 
Standardmäßig sind Sie damit unabhängig von einem zentralen Speicher. 
Die Stammdatentabelle existiert vollständig **im Hauptspeicher**, wenn das Programm läuft.

### Zeilen

Sie können zum Beispiel auf die Eingabe der Namen komplett verzichten oder in 
der Tabelle mehr Zeilen vorrätig halten als es Entries im Event gibt. 
Damit könnten Sie zum Beispiel immer den gleichen **Pool** an Stammdaten für eine Serie von Club-Wettfahrten verwenden. 
Eine spätere Optimierung durch Löschen unbenutzter Information ist jederzeit möglich.

Standardmäßig sind *keine* Zeilen in der Tabelle vorhanden. 
In der grafischen Oberfläche müssen Sie den Button **Add** drücken, 
um eine Zeile hinzuzufügen.

Ein Hinweis: Das verwendete Grid zur Anzeige der Daten muss immer eine Zeile anzeigen, 
auch wenn eigentlich noch keine existiert. 
Die eigentlich nicht existierende **Pseudo-Zeile** erkennen Sie an einer SNR mit dem **Wert 0**. 
Fügen Sie also immer mindestens eine Zeile mit dem Add Button hinzu, 
bevor Sie mit der Eingabe in eine Zelle beginnen.

Wenn Telegramme mit Informationen zu den Namen empfangen werden, 
dann wird **automatisch** eine Zeile hinzugefügt, 
wenn noch keine Zeile für das Schlüsselfeld SNR vorhanden ist.

### Spalten

Die Anzahl der bereitgestellten Spalten kann mit Event Property `FieldCount` erhöht werden. 
Standard ist sechs, es sind immer mindestens sechs.

Die Spalten und Zellen sind alle gleich. 
Alle haben den gleichen Datentyp **String**. 
Alle Zellen haben die gleiche Aufnahmekapazität, unabhängig von der angezeigten Breite der Spalten. 
Durch die Validierung des Inputs kann aber die Länge der gespeicherten Strings begrenzt werden, 
und zwar für jede Spalte anders.

## Event Properties

### EP.NameSchema

Standard ist das Schema `NX`. Dabei werden die Spalten mit `N1`, `N2`, `N3` usw. bezeichnet. 
Die Anzahl der im Programm vorgehaltenen Spalten ist mit `EP.FieldCount` festgelegt, 
standardmäßig sechs.

Das ursprüngliche Schema, Default, hat exakt sechs Spalten mit den Bezeichnungen:
```
FN (N1,FirstName)
LN (N2,LastName)
SN (N3,ShortName)
NC (N4,NOC) 
GR (N5,Gender)
PB (N6,PersonalBest)
```
Dieses Schema ist in der Regel ausreichend und kann in Verbindung mit der Möglichkeit die 
Spaltenüberschriften anzupassen für viele Fälle verwendet werden.

Das Schema `LongNames` entspricht dem Default-Schema, mit dem Unterschied, 
dass bei der Ausgabe der Daten die langen Spaltenbezeichnungen verwendet werden. 
Allgemein steuert die Festlegung des Schemas die Ausgabe und nicht die Eingabe von Daten.

Eine Erweiterung der Tabelle der Namen um **zusätzliche Spalten** ist unabhängig vom Schema möglich. 
Die zusätzlichen Spalten müssen mit `NX`, beginnend ab Index 7 angesprochen werden.

Es sollte in Zukunft nur noch das Schema NX verwendet werden, 
da es die **interne Gleichheit** der Spalten am besten zum Ausdruck bringt.

Ein an das Programm gesendetes Telegramm `FR.*.SNR1000.N1=A` hat die gleiche 
Wirkung wie das Telegramm `FR.*.SNR1000.FN=A` und würde den Vornamen für Entry mit SNR 1000 auf A setzen.

### EP.FieldMap

Es gibt eine virtuelle Spalte `DN` (DisplayName). 
Welche Werte in diese Spalte projiziert werden, 
kann mit dem Event Property EP.FieldMap angegeben werden.

Die Angabe `EP.FieldMap=SN` würde die Spalte `SN` (N3, ShortName) auf die Spalte `DN` (N0, DisplayName) abbilden. 
Sollten Sie dann die Spalte `DN` in einem Report einblenden, würde dort der `ShortName` erscheinen.

Der **Trick** ist, dass durch die Auswertung der Eigenschaft EP.FieldMap auch Verknüpfungen von Spalten realisiert werden können. 
Die Angabe `EP.FieldMap=LN,Komma,Space,FN` würde zum Beispiel in der Spalte `DisplayName` genau so erscheinen, 
wie Sie es erwarten.

### EP.FieldCaptions

Damit können Sie die Bezeichnungen der Spalten für die Ausgabe auf den Reports **überschreiben**. 
`NX` wird also durch die angegebene Bezeichnung ersetzt. 
Die erste Angabe in der kommagetrennten Liste ist die Bezeichnung für die erste auf dem Report erscheinende Spalte. 
Die Anzahl der Angaben in der Liste soll `EP.NameFieldCount` Werte haben. 
Zusätzliche Werte würden vorerst ignoriert werden, 
können aber wieder eine Bedeutung erlangen, 
wenn Sie den Wert von `EP.NameFieldCount` erhöhen. 
Sie müssen also nicht immer alles löschen, 
während Sie noch die optimale Einstellung für die Ausgabe suchen.

### EP.NameFieldCount

Die Anzahl der Spalten, die auf den Reports erscheinen soll, 
kann mit dem Event Property `EP.NameFieldCount` gesteuert werden.

### EP.NameFieldOrder

Das Event Property `EP.NameFieldOrder` steuert das Layout der Spalten, 
wenn diese auf den Reports ausgegeben werden sollen.

- Es ist eine kurze Liste von **Ziffern**.
- Die Liste definiert die Spaltenreihenfolge durch Angabe der **Indexwerte** der Spalten, ohne Trennzeichen.
- Mindestens soll die Liste die Länge von EP.NameFieldCount haben, kann aber länger sein.
- Die überschüssigen Werte werden ignoriert. 
- Der Standardwert für EP.NameFieldOrder ist `041256`.
- Dies würde die Spalten `DisplayName`, `NOC`, `FirstName`, `LastName`, `Gender` und `PersonalBest` in dieser Reihenfolge anzeigen.
- Die Spalte `DN` (DisplayName) hat den Pseudo-Index `0`.
- Die anderen Spalten haben den Index `X` entsprechend der Spaltenbezeichnung `NX`.

Beispiel folgt:

```
EP.NameSchema = 
EP.FieldMap = SN
EP.FieldCaptions = 
EP.FieldCount = 6
EP.NameFieldCount = 2
EP.NameFieldOrder = 041256
```

Die Auswertung des Beispiels ergibt folgendes:

- Es wird NameSchema NX verwendet, da dies Standard ist.
- Die virtuelle Spalte DisplayName zeigt jetzt auf Spalte `SN`.
- Die voreingestellten Spaltenüberschriften werden verwendet.
- Die Stammdatentabelle hat sechs Spalten.
- `NameFieldCount=2` legt fest, dass zwei Spalten anzuzeigen sind.
- Die anzuzeigenden Spalten sind Spalte `DisplayName` (Index **0**) und Spalte `N4` (Index **4**) in dieser Reihenfolge.

Damit entspricht die Anzeige dem ursprünglichen Entwurf. 
In den meisten Fällen ist auf dem Report nur für zwei Spalten Platz vorhanden. 
Die schmale Spalte `N4` (NC) sollten Sie mit Information füllen, 
die immer angezeigt werden soll. 
Die etwas breitere Spalte `DisplayName` mappen Sie so gut wie möglich auf die Information, 
die Sie in der Stammdatentabelle vorfinden.

## Fazit

Die Namen liegen in der Stammdatentabelle im Hauptspeicher der Anwendung. 
Mit der gezielten Einstellung der Properties sollten Sie vernünftige Anzeigen realisieren können. 
Es hilft, wenn Sie beim Füllen der Stammdatentabelle mit einem **Plan** zu Werke gehen.

Das für die Anzeige in der grafischen Oberfläche verwendete Grid ist ein relativ einfaches Grid, 
welches auf **mehreren Plattformen** in der gleichen Funktionsweise zur Verfügung gestellt werden kann. 

Alle grafischen Darstellungen der Extraklasse, 
die zusätzlich eine Vielzahl von **externen Datenquelle** anzapfen und Links zu externen Informationen im Web bereitstellen, 
sollten Sie außerhalb der Kernanwendung in einem Reportclient generieren. 
Die primäre Datenquelle für diese Reports liefert das Programm FR in Form von Xml. 
Sie sind also in keiner Weise limitiert und ich hoffe, 
dass Sie die Flexibilität des Entwurfs der Anwendung FR ausnutzen, 
um ansprechende Reports zu erstellen.
