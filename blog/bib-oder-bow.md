---
layout: default
lang: de
title: Bib oder Bow
---

# Bib oder Bow

Die beiden Begriffe sind identisch. Bib - die Startnummer - wird allgemein im Sport verwendet.
Es ist das verbindende Schlüsselfeld zum Bereich Timing.

Über das andere Schlüsselfeld - SNR - wird die Verbindung zur Stammdatentabelle (Tabelle Entries) hergestellt.
Die Stammdatentabelle enthält Zusatzinformationen, 
die für die Berechnung des Wettkampfes keine Rolle spielen. 
Die Stammdatentabelle kann leer sein.

SNR und Bib müssen eindeutig sein.
Es macht Sinn, die Bib, also beim Segeln die Bugnummer, immer vom Programm aus zu ändern.
Dadurch wird automatisch sichergestellt,
dass die Bib in allen Tabellen (StartList, FleetList, FinishList)
und auch bei den Penalty-Zuweisungen aktualisiert wird.

Das dritte Schlüsselfeld - die ID  -wird vom Programm vergeben, intern benutzt, und ist immer korrekt.
Bei der Eingabe der Bib und der SNR können Sie Fehler machen, diese werden farbig angezeigt.

Wenn erst später bekannt wird, wie die Bugnummern vom Veranstalter vergeben werden, 
könnte man den Wettkampf (Event) zunächst so einrichten, 
dass relativ hohe Bugnummern verwendet werden. 
Damit vermeidet man (temporär) doppelte Werte, 
wenn später die Bib auf den tatsächlichen Wert gesetzt wird.

Nur wenn das Timing extern erfolgt, oder die Liste der Timing-Nachrichten geteilt wird,
müssen Sie sich mit den Bow-Nummern nach der externen Vorgabe richten.

Die Simulation für das Timing auf Seite Timing geht von fortlaufenden Bib-Nummern aus,
von eins beginnend. Wenn das nicht der Fall ist, 
kann das Timing-Grid nicht verwendet werden. 
Sie müssen entscheiden, ob Sie die tatsächlichen Bow-Nummern verwenden wollen, 
oder die eigenen.

Seite Keying ist davon nicht betroffen, dort ist der Wertebereich für die Bib, die Sie eingeben, nicht begrenzt.

Versuchen Sie nicht, die Segelnummer im Feld SNR unterzubringen. 
Die Segelnummer, zum Beispiel *Beil GER 1234*, 
sollten Sie in geeigneter Weise in der Stammdatentabelle unterbringen.
(Die ISAF ID für die Bio-Datenbank gehört auch in die Stammdatentabelle.)

Wenn Sie Zeilen hinzufügen, zu Tabelle Event mit Parameter StartListCount oder Tabelle Entries mit Button Add,
dann müssen Sie eventuell die Schlüsselfelder ausfüllen (früher was das so).
Bei der Einrichtung eines neuen Events ist es daher oft einfacher,
von einem Beispiel auszugehen, wo Einträge nur noch herausgelöscht werden müssen.

**Update 2019**: Beim Hinzufügen von Zeilen werden die Schlüsselfelder mit sinnvollen Vorgabewerten belegt,
so dass meistens nichts mehr zu tun ist.
