---
layout: default
lang: de
title: Nachrichtenbeispiel
---

# Nachrichtenbeispiel

## Übersicht

Die Daten der Anwendung FR (Eventdaten) können im Xml-Format, dem kompakten
Textformat oder im nativen Textformat vorliegen. Die einzelnen Formate können
verlustfrei in jede Richtung umgewandelt werden. Die Eventdaten bestehen im Kern
aus einer Liste von einzeiligen Nachrichten (Telegramme, Messages).

## Einzeilige Message

Die einzeiligen Nachrichten entsprechen dem Key=Value Muster.

So ist es gedacht (Indizes in Klammern):

```
FR.*.W[2].Bib[2].QU=DSQ
```

Real müssen die Klammern weggelassen werden (spart Platz und lässt sich einfacher schreiben):

```
FR.*.W2.Bib2.QU=DSQ
```

- Links vom Gleichheitszeichen steht der Key.
- FR kennzeichnet die Anwendung (den Typ)
- Im zweiten Abschnitt steht * für die anonyme Division (ausreichend wenn Telegramme nur für eine Bootsklasse gesendet werden).
- W2 ist die 2. Wettfahrt (Race 2)
- Bib2 kennzeichnet die Zeile in der Tabelle
- QU bedeutet, dass ein Penaltywert (QUIT packet) gesendet wird.
- DSQ rechts vom Gleichheitszeichen ist der Value.

## Protokoll

Die einzeiligen Messages entsprechen dem selbst definierten Protokoll. Das
Programm enthält einen robusten Parser für das Protokoll.

Der Key (links vom Gleichheitszeichen) ist hierarchisch aufgebaut. Die
einzelnen Ebenen werden immer durch Punkt getrennt. Der Entwurf für das
Protokoll kann übersichtlich in einer Tabelle dargestellt werden. Die mit (X)
endenden Einträge sind indizierte Token. Leaf Alias ist eine alternative
Bezeichnung für den letzten Eintrag im Pfad.

<table>
<tr>
<th>Level1</th>
<th>Level2</th>
<th>Level3</th>
<th>Level4</th>
<th>Level5</th>
<th>Level6</th>
<th>Leaf Alias</th>
</tr>
<tr>
<td>FR</td>
<td>Division</td>
<td>SNR(X)</td>
<td>FN</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>N1</td>
</tr>
<tr>
<td></td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>LN</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>N2</td>
</tr>
<tr>
<td></td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>SN</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>N3</td>
</tr>
<tr>
<td></td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>NC</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>N4</td>
</tr>
<tr>
<td></td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>GR</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>N5</td>
</tr>
<tr>
<td></td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>PB</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>N6</td>
</tr>
<tr>
<td></td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>N(X)</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
</tr>
<tr>
<td></td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
</tr>
<tr>
<td></td>
<td>&nbsp;</td>
<td>W(1)</td>
<td>STL</td>
<td>Pos(X)</td>
<td>Bib </td>
<td>&nbsp;</td>
</tr>
<tr>
<td></td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>SNR</td>
<td>&nbsp;</td>
</tr>
<tr>
<td></td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
</tr>
<tr>
<td></td>
<td>&nbsp;</td>
<td>W(X)</td>
<td>Bib(X) | Pos(X)</td>
<td>XX</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
</tr>
<tr>
<td></td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>QU</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
</tr>
<tr>
<td></td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>ST</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
</tr>
<tr>
<td></td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>FT</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
</tr>
<tr>
<td></td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>DG</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
</tr>
<tr>
<td></td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>Rank</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
</tr>
<tr>
<td></td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>RV</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
</tr>
<tr>
<td></td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td>IT(X)</td>
<td>&nbsp;</td>
<td>&nbsp;</td>
</tr>
</table>

STL initialisiert Zeilen in Tabelle W bzw. in den Tabellen W(X).

Wie in Level 4 definiert können die für eine Zeile in W(X) bestimmten
Nachrichten auf die Bib (eindeutige Kennzeichnung der Zeile in Tabelle W) oder
auf Pos (Position der Zeile in der Tabelle) zugewiesen werden.

## Text (natives Format)

In jedem Fall wird die Anwendung Xml oder kompakten Text zunächst in das
native Textformat transformieren. Das native Format ist im Hauptteil eine Liste
von einzeiligen Messages, die so auch einzeln über das Netzwerk (oder eine
interne Verbindung) an das Programm gesendet werden können. Vorangestellt sind
die Parameter und Properties für den Event.

```
#Params

DP.StartlistCount=8
DP.ITCount=0
DP.RaceCount=2

#Properties

EP.Name=
EP.ScoringSystem=Low Point System
EP.Throwouts=0
EP.DivisionName=*
EP.InputMode=Strict
EP.RaceLayout=Finish
EP.NameSchema=
EP.FieldMap=SN
EP.FieldCaptions=
EP.FieldCount=6
EP.NameFieldCount=2
EP.NameFieldOrder=041256
EP.UseFleets=False
EP.TargetFleetSize=8
EP.FirstFinalRace=20
EP.IsTimed=False
EP.UseCompactFormat=True

#NameList

FR.*.SNR1000.N1=abc
FR.*.SNR1000.N2=def
FR.*.SNR1000.N3=ghi
FR.*.SNR1000.N4=jkl
FR.*.SNR1000.N5=mno
FR.*.SNR1000.N6=pqr

#StartList

FR.*.W1.STL.Pos1.SNR=1000
FR.*.W1.STL.Pos1.Bib=1
FR.*.W1.STL.Pos2.SNR=1001
FR.*.W1.STL.Pos2.Bib=2
FR.*.W1.STL.Pos3.SNR=1002
FR.*.W1.STL.Pos3.Bib=3
FR.*.W1.STL.Pos4.SNR=1003
FR.*.W1.STL.Pos4.Bib=4
FR.*.W1.STL.Pos5.SNR=1004
FR.*.W1.STL.Pos5.Bib=5
FR.*.W1.STL.Pos6.SNR=1005
FR.*.W1.STL.Pos6.Bib=6
FR.*.W1.STL.Pos7.SNR=1006
FR.*.W1.STL.Pos7.Bib=7
FR.*.W1.STL.Pos8.SNR=1007
FR.*.W1.STL.Pos8.Bib=8

#FinishList

FR.*.W1.Bib1.Rank=2
FR.*.W2.Bib1.Rank=3
FR.*.W1.Bib2.Rank=7
FR.*.W2.Bib2.Rank=4
FR.*.W1.Bib3.Rank=5
FR.*.W2.Bib3.Rank=8
FR.*.W1.Bib4.Rank=1
FR.*.W2.Bib4.Rank=7
FR.*.W1.Bib5.Rank=6
FR.*.W2.Bib5.Rank=5
FR.*.W1.Bib6.Rank=8
FR.*.W2.Bib6.Rank=6
FR.*.W1.Bib7.Rank=4
FR.*.W2.Bib7.Rank=2
FR.*.W1.Bib8.Rank=3
FR.*.W2.Bib8.Rank=1

FR.*.W2.Bib2.QU=DSQ

EP.IM=Strict
```

## TXT (kompakt)

Die Desktop-Anwendung speichert die Event-Daten standardmäßig im kompakten
Text-Format. Die tabellarischen CSV-Daten für NameList (Entries), StartList,
FinishList und FleetList (nicht im Beispiel) können so einfach mit CUT-AND-PASTE
eingefügt werden.

```
#Params

DP.StartlistCount = 8
DP.ITCount = 0
DP.RaceCount = 2

#Event Properties

EP.Name =
EP.ScoringSystem = Low Point System
EP.Throwouts = 0
EP.DivisionName = *
EP.InputMode = Strict
EP.RaceLayout = Finish
EP.NameSchema =
EP.FieldMap = SN
EP.FieldCaptions =
EP.FieldCount = 6
EP.NameFieldCount = 2
EP.NameFieldOrder = 041256
EP.UseFleets = False
EP.TargetFleetSize = 8
EP.FirstFinalRace = 20
EP.IsTimed = False
EP.UseCompactFormat = True

NameList.Begin
SNR;N1;N2;N3;N4;N5;N6
1000;abc;def;ghi;jkl;mno;pqr
NameList.End

StartList.Begin
Pos;SNR;Bib
1;1000;1
2;1001;2
3;1002;3
4;1003;4
5;1004;5
6;1005;6
7;1006;7
8;1007;8
StartList.End

FinishList.Begin
SNR;Bib;R1;R2
1000;1;2;3
1001;2;7;4
1002;3;5;8
1003;4;1;7
1004;5;6;5
1005;6;8;6
1006;7;4;2
1007;8;3;1
FinishList.End

#W1


#W2

FR.*.W2.Bib2.QU=DSQ

EP.IM = Strict
```

## Xml

Die Eventdaten liegen normalerweise im XML-Format vor, wenn sie in einem
Blob-Feld der Datenbanktabelle gespeichert sind oder über das Web ausgeliefert
werden.

```xml
<?xml version="1.0"?>
<FR>
  <Properties StartlistCount="8" ITCount="0" RaceCount="2"
      DivisionName="*" InputMode="Strict">
    <EP K="Name" V=""/>
    <EP K="ScoringSystem" V="Low Point System"/>
    <EP K="Throwouts" V="0"/>
    <EP K="DivisionName" V="*"/>
    <EP K="InputMode" V="Strict"/>
    <EP K="RaceLayout" V="Finish"/>
    <EP K="NameSchema" V=""/>
    <EP K="FieldMap" V="SN"/>
    <EP K="FieldCaptions" V=""/>
    <EP K="FieldCount" V="6"/>
    <EP K="NameFieldCount" V="2"/>
    <EP K="NameFieldOrder" V="041256"/>
    <EP K="UseFleets" V="False"/>
    <EP K="TargetFleetSize" V="8"/>
    <EP K="FirstFinalRace" V="20"/>
    <EP K="IsTimed" V="False"/>
    <EP K="UseCompactFormat" V="True"/>
  </Properties>
  <Entries>
    <SNR oID="1000" N1="abc" N2="def" N3="ghi" N4="jkl" N5="mno" N6="pqr"/>
  </Entries>
  <StartList>
    <Pos oID="1" Bib="1" SNR="1000"/>
    <Pos oID="2" Bib="2" SNR="1001"/>
    <Pos oID="3" Bib="3" SNR="1002"/>
    <Pos oID="4" Bib="4" SNR="1003"/>
    <Pos oID="5" Bib="5" SNR="1004"/>
    <Pos oID="6" Bib="6" SNR="1005"/>
    <Pos oID="7" Bib="7" SNR="1006"/>
    <Pos oID="8" Bib="8" SNR="1007"/>
  </StartList>
  <FinishList>
    <FL>SNR;Bib;R1;R2</FL>
    <FL>1000;1;2;3</FL>
    <FL>1001;2;7;4</FL>
    <FL>1002;3;5;8</FL>
    <FL>1003;4;1;7</FL>
    <FL>1004;5;6;5</FL>
    <FL>1005;6;8;6</FL>
    <FL>1006;7;4;2</FL>
    <FL>1007;8;3;1</FL>
  </FinishList>
  <MsgList>
    <ML>FR.*.W2.Bib2.QU=DSQ</ML>
  </MsgList>
</FR>
```
