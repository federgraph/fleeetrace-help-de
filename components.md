---
layout: default
lang: de
title: Komponenten
---

# Komponenten

Zum Projekt FR gehören
- normale Desktopanwendungen,
- Serveranwendungen,
- Timing Clienten,
- Webanwendungen
- und SPA Clienten.


Der Silverlight Client für das FleetRace Projekt wird auch als FleetRace Internetapplikation [FRIA](silverlight/FRIA) bezeichnet.
Vom Silverlight Client gibt es mehrere Varianten, aktive und passive.

Der Silverlight Client als letztes Glied in der Kette kann auch solo genutzt werden, 
zum Beispiel zur Anzeige von statischen Regattaergebnissen.

Statisch bedeutet dabei, dass die Eingangsdaten unveränderbar auf einem Webserver bereitgestellt werden.

Im Silverlight Client werden die Ergebnisse jedoch dynamisch berechnet und können auch nachträglich zum Leben erweckt werden.

Der Silverlight Client kann für den Einsatz auf der Seite Ihres Segelvereins oder der Klassenvereinigung lizensiert werden.

Für alle, die selbst Daten bereitstellen wollen sind Informationen zum [Schnellstart](doc/doc-fria-quick-start) verfügbar.

## Liste der Komponenten

<dl>
<dt><a href="applications/FR04">FR04</a></dt>
<dd>Result Server, abgerüstete Variante, speichert nichts auf der Festplatte,
ohne Konfiguration, mit fest eingestelltem Szenario (Bridgeserver für FRIA).</dd>

<dt><a href="applications/FR38">FR38</a></dt>
<dd>Timing Client, sendet einzeilige Nachrichten.</dd>

<dt><a href="applications/FR62">FR62</a></dt>
<dd>Result Server, voll aufgerüstet, mit Szenario Manager für konfigurationsfreien
Betrieb. Integrierte Website kann Tcp-Inputclient und Tcp Output Client ersetzen.</dd>

<dt><a href="applications/FR63">FR63</a></dt>
<dd>Wie FR62, aber graphische Oberfläche ist leer. Dieses Programm kann zum
Einsatz kommen, wenn kein Bedienpersonal vor Ort am Computer sitzt. Sie nutzen
dann ausschließlich die Serverfunktionalität des Programms. Die Steuerung kann
über ein Webinterface erfolgen (Browser).</dd>

<dt>FR64</dt>
<dd>FR als Webanwendung. Je nach Plattform ausgeführt als ASP.NET generic
handler, Java servlet oder (historisch) Delphi ISAPI DLL. Diese Anwendung steht
für spezielle Einsatzfälle zur Verfügung. Es empfiehlt sich mit einer der
Desktopanwendungen zu beginnen.</dd>

<dt>FR65</a></dt>
<dd>Wie FR63, als Windows Service.</dd>

<dt><a href="applications/FR90">FR90</a></dt>
<dd>Timing Simulator + Pocket Timer Adapter.</dd>

<dt><a href="applications/FR93">FR93</a></dt>
<dd>FR62 minus Switch, Bridge. Dieses Programm ist eine alleinstehende
Desktopanwendung. Die Funktion der automatischen Synchronisation von Daten mit
parallellaufenden Anwendungen wurde aus FR93 entfernt.</dd>

<dt><a href="applications/FR94">FR94</a></dt>
<dd>FR62 minus Timing, Race, Switch, Bridge, Cache, Browser und Output. Es ist
nur noch der sportartspezifische Eventteil enthalten. Dieses Programm kann für
den Import und die Weiterbearbeitung von Spreadsheet Daten benutzt werden.</dd>

<dt><a href="applications/FR95">FR95</a></dt>
<dd>FR62 minus Event, Switch, Bridge, Cache, Browser und Output. Es ist also nur
noch der sportartunabhängige Race Teil enthalten. Dieses Programm kann für viele
Timing Aufgaben eingesetzt werden.</dd>

<dt><a href="applications/FR97">FR97</a></dt>
<dd>Anwendung mit IdHttpServer, minimaler ad hoc Webserver für FRIA-Client und xml.</dd>

<dt><a href="applications/FR98">FR98</a></dt>
<dd>Traditioneller Output Client. Wird benachrichtigt, zieht sich Reports.</dd>

<dt>FRWA01</dt>
<dd>Dynamische Website, ASP.NET MVC, liefert FRIA-Client, holt archivierte Daten
für FRIA aus der Datenbank.</dd>

<dt>FRWA02</dt>
<dd>Statische Website, liefert FRIA-Client, liest xml für FRIA vom Dateisystem.</dd>

<dt><a href="silverligtht/FRIA03">FRIA03</a></dt>
<dd>Silverlight RIA, zeigt Eventpage, manuell verbunden mit Result Server.</dd>

<dt><a href="silverligtht/FRIA05">FRIA05</a></dt>
<dd>Silverlight RIA, mit Eventpage, ausgelegt für das Herunterladen statischer
Daten. Kann in normale Website integriert werden.</dd>

<dt><a href="silverligtht/FRIA11">FRIA11</a></dt>
<dd>Silverlight RIA, zeigt Race Page, manuell verbunden mit Result Server.</dd>

</dl>