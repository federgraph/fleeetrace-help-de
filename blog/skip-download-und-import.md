---
layout: default
lang: de
old_title: Skip Download und Import
---

# Skip Download und Import

Die beiden Flags **Skip Download** und **Skip Import** auf Seite Menu haben Standardwerte,
die mit dem Modus (Less oder More) verknüpft sind.

Damit wird gesteuert, was passiert, wenn man auf einen der Event-Buttons drückt
(nachdem ein Workspace geladen wurde und damit die Event-Buttons initialisiert sind).

Die Bezeichnungen Less und More beziehen sich auf die Anzahl der sichtbaren Schaltflächen.
Jedes Mal beim Umschalten zwischen More und Less werden die Flags auf den Standard zurückgestellt.
Nur im Modus More können die Flags manuell verändert werden.

Im Modus Less (wenn More sichtbar ist) sind beide Flags deaktiviert,
so dass bei Klick auf einen Event-Button

- die Metadaten des Buttons im oberen Memo angezeigt werden,
- der entsprechende Event heruntergeladen wird,
- der aktuelle Event gesetzt wird (Current Button),
- der Event in die Anwendung geladen (importiert) wird,
- und der Text des Events NICHT im unteren Memo angezeigt wird.

Dieses Verhalten kann nicht geändert werden. Es ist der normale Fall. 
Alles sollte funktionieren und Sie brauchen sich keine Gedanken über die Funktionsweise zu machen.

Im Modus More (wenn Less sichtbar ist) ist das Flag Skip Import standardmäßig aktiv, so dass

- die Metadaten des Buttons im oberen Memo angezeigt werden,
- der entsprechende Event heruntergeladen wird,
- der aktuelle Event gesetzt wird (Current Button),
- der Event NICHT in die Anwendung geladen (importiert) wird,
- aber dafür der Text des Events im unteren Memo angezeigt wird.

Der Event wird also im Modus More nur im Memo angezeigt, aber nicht geladen. 
Im Modus More können Sie die anderen Buttons benutzen, um bestimmte Verarbeitungsschritte einzeln zu testen.

Der Button Write bezieht sich immer auf Current Event, also den aktuellen Event.
Im Modus More können Sie mit einem Klick auf einen Event-Button den aktuellen Event wechseln, 
ohne die Daten des Events in die Anwendung zu laden. 
Damit ist es möglich, einen Event zwischen zwei Slots zu kopieren. 
Zuerst laden Sie den Event im Modus Less, 
dann wechseln Sie den Current Event im Modus More, 
und dann speichern Sie mit Button Write, 
vorausgesetzt der neue Slot ist beschreibbar.

Wenn Sie im Modus More das Flag Skip Download aktivieren (standardmäßig nicht aktiviert), 
dann werden bei einem Klick auf den Event-Button nur die Metadaten des Events im oberen Memo angezeigt,
so dass kontrolliert werden kann, ob die Event-Buttons wie erwartet konfiguriert wurden.

Wenn beide Flags deaktiviert sind, dann läuft alles genau wie im Modus Less.

Also, im Modus Less (dem Produktivmodus) ist wirklich alles ganz einfach. 
Im Modus More (dem Debug-Modus) können Sie nachvollziehen, wie die Anwendung funktioniert. 
Die anderen, zusätzlichen Schaltflächen im Modus More sind im Artikel Weniger oder Mehr beschrieben.
