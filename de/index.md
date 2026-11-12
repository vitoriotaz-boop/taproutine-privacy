---
layout: page
title: "Datenschutzerklärung für TapRoutine"
lang: de-DE
permalink: /de/
description: "Datenschutz- und Datenverwendungsinformationen für TapRoutine für Android."
eyebrow: "Datenschutz und Datennutzung"
brand_label: "Datenschutz"
home_label: "Startseite der TapRoutine-Datenschutzerklärung"
footer_label: "TapRoutine · Android"
contact_label: "Kontakt"
---

<p class="last-updated">Zuletzt aktualisiert: 12. November 2026</p>
<nav class="language-nav" aria-label="Sprachauswahl">
<a href="{{ '/' | relative_url }}" lang="pt-BR">Português (Brasil)</a>
<a href="{{ '/en/' | relative_url }}" lang="en-US">English</a>
<a href="{{ '/es/' | relative_url }}" lang="es-419">Español</a>
<a href="{{ '/fr/' | relative_url }}" lang="fr-FR">Français</a>
<span aria-current="page" lang="de-DE">Deutsch</span>
<a href="{{ '/it/' | relative_url }}" lang="it-IT">Italiano</a>
<a href="{{ '/ja/' | relative_url }}" lang="ja-JP">日本語</a>
</nav>

## Über diese App-Version

TapRoutine ist eine Android-Vorschau-App, mit der Sie eine Routine für eine ausgewählte App konfigurieren, auf dem Gerät planen, vom Nutzer festgelegte Schritte ausführen und Bildschirmpunkte anhand ihrer Farbe überprüfen können. Die untersuchte Vorschau-APK hat die Paketkennung `io.github.vitoriotaz.taproutine`, `minSdk` 24, `targetSdk` 36 und `android:allowBackup=true`. Die Aussagen in diesem Text beziehen sich auf diese Vorschau-APK und gelten möglicherweise nicht für künftige Versionen.

## Vom App erstellte oder abgerufene Daten

- **Routine und Nutzereinstellungen:** Dazu können der Name der Routine, Name und Paketkennung der ausgewählten App, Uhrzeiten, Wochentage und Zeitzone, Schritte und Gesten (zum Beispiel Tippen, Wischen, Warten, Zurück oder Startbildschirm) sowie deren Positionen gehören. Ebenfalls enthalten sein können die für die Überprüfung verwendete Farbe, der Prüfpunkt und die Toleranz sowie Parameter wie die Prüfhäufigkeit und die Einstellung, ob die Ziel-App erneut geöffnet werden soll. Zu den Einstellungen können auch der Wächter und ein alternativer Bildschirm mit einer weiteren vorkonfigurierten Schrittfolge gehören.
- **Zur Auswahl verfügbare Apps:** TapRoutine fragt Android ab, um Apps mit verfügbarer Startaktivität anzuzeigen. Sie wählen die Ziel-App aus; ihr Name und ihre Paketkennung werden in der lokalen Routine gespeichert.
- **Vorübergehende Information zum Fenster im Vordergrund:** Solange der Android-Bedienungshilfedienst von TapRoutine aktiv ist, empfängt er Android-Ereignisse `TYPE_WINDOW_STATE_CHANGED` und hält den vom System gemeldeten Paketnamen im Arbeitsspeicher. Der Dienst liest weder den Benutzeroberflächenbaum noch Texte, Eingabefelder oder andere Bildschirminhalte aus.
- **Lokale Daten und Protokoll:** Routinen und Protokolleinträge können Zeitangaben, das Paket der Ziel-App, Fortschritt und Ergebnisse von Schritten und Versuchen, technische Fehlerdetails sowie Farbwerte, Punkte/Positionen und die Bildschirmauflösung enthalten. In `SharedPreferences` werden außerdem die mit der Offenlegung verbundene Einwilligung sowie Status und Zeitangaben zu Zeitplänen und zum Wächter gespeichert.
- **Vorübergehende Bildschirmaufnahme zur Farbprüfung:** Bei einer Prüfung erfasst die App vorübergehend den gesamten aktuell angezeigten Bildschirm im Arbeitsspeicher, um ausschließlich den durchschnittlichen Farbwert eines 3×3-Pixel-Bereichs am angegebenen Punkt zu berechnen. Eine solche Aufnahme kann bei Routineprüfungen, beim Erkennen eines alternativen Bildschirms und durch den Wächter erfolgen; sie ist nicht zwingend auf das Fenster oder die Ziel-App beschränkt. Die App speichert die Aufnahme nicht absichtlich als Datei. Sie ist vorübergehend; im normalen Ablauf werden die zugehörigen Ressourcen nach der Berechnung freigegeben. Für diese Bildschirmprüfung ist Android 11 oder höher erforderlich.

## Verwendung der Daten

Die Daten werden auf dem Gerät verwendet, um die Routine zu speichern und zu laden, ihre Ausführung zu planen, die vom Nutzer festgelegten Schritte auszuführen, die Farbe am konfigurierten Punkt zu vergleichen und Ergebnisse zu protokollieren. Je nach Konfiguration kann die Farbe eine bereits vorkonfigurierte alternative Schrittfolge auswählen oder die vorkonfigurierte Aktion des Wächters auslösen. Die App erfindet keine Aktionen und wertet weder Text noch Bildschirminhalte aus, um zu entscheiden, was zu tun ist.

## Verarbeitung, Speicherung und Übertragung

Routinen und Protokolleinträge werden im privaten lokalen Speicher der App abgelegt. `SharedPreferences` speichern außerdem die oben beschriebenen Daten, einschließlich der mit der Offenlegung verbundenen Einwilligung sowie Status und Zeitangaben zu Zeitplänen und zum Wächter. Das vom Dienst beobachtete Fensterpaket wird im Arbeitsspeicher gehalten. Die Bildschirmaufnahme ist vorübergehend; die App speichert sie nicht absichtlich als Datei und gibt die zugehörigen Ressourcen im normalen Ablauf frei.

Der untersuchte APK-Code implementiert weder ein Konto noch einen Server, eine Synchronisierung, Analytics, Werbung, Zahlungen oder eigene Netzwerkaufrufe. Das bedeutet nicht, dass keine Kopie das Gerät verlassen kann: Die automatische Sicherung von Android/Google kann Daten wie im folgenden Abschnitt beschrieben kopieren. Auch die als Ziel ausgewählte App kann eigene Verbindungen und eigene Datenpraktiken haben, die TapRoutine nicht kontrolliert.

Wenn Sie den Support per E-Mail kontaktieren, werden Ihre Nachricht und die dafür verwendete Absenderadresse über Ihren E-Mail-Dienst übertragen, damit wir die Nachricht empfangen und beantworten können. Dies ist eine von Ihnen ausgelöste externe Handlung und kein eigener Netzwerkaufruf von TapRoutine.

## Automatische Sicherung durch Android/Google

In der untersuchten Vorschau-APK ist `android:allowBackup` auf `true` gesetzt. Wenn die automatische Sicherung von Android aktiviert ist, kann Android private App-Dateien und Daten aus `SharedPreferences` – darunter möglicherweise Routine, Protokolleinträge, Einwilligung sowie Status und Zeitangaben zu Zeitplänen und zum Wächter – gemäß dem Android-Dienst in das Google-Konto/Drive des Nutzers kopieren. Das Verhalten hängt von den Sicherungseinstellungen, der Android-Version und dem Gerät ab.

Diese Sicherung ist ein Dienst von Android/Google und keine Übertragung durch TapRoutine an einen Server des Entwicklers. Die App und der Entwickler haben keinen Zugriff auf die Sicherungskopie. Das Löschen lokaler Daten oder die Deinstallation der App ist keine Garantie dafür, dass eine separate Kopie entfernt wird, die der Sicherungsdienst möglicherweise aufbewahrt.

## Aufbewahrung und Optionen für Nutzer

Die Routine und die Protokolleinträge bleiben im App-Speicher, bis sie ersetzt oder entfernt werden. Die Schaltfläche **Limpar** (Portugiesisch für „Löschen“) im Prototyp entfernt das Ausführungsprotokoll. Wenn das Protokoll sehr groß wird, kann der Prototyp außerdem ältere Einträge entfernen und die neuesten beibehalten. Beim Speichern geänderter Einstellungen wird die lokale Routine ersetzt; das Abbrechen des Zeitplans beendet die geplante Ausführung, löscht aber nicht von selbst die gespeicherte Konfiguration. Um lokale App-Daten zu entfernen, verwenden Sie die Android-Speichereinstellungen, um die App-Daten zu löschen, oder deinstallieren Sie die App. Das garantiert nicht, dass eine separate Sicherungskopie entfernt wird, falls eine solche vorhanden ist. Das Betriebssystem kann die Bezeichnungen der Einstellungen unterschiedlich anzeigen.

## Android-Dienste und Berechtigungen

- **Android-Bedienungshilfedienst:** Muss vom Nutzer in den Systemeinstellungen aktiviert werden, damit die konfigurierten Gesten ausgeführt und Prüfungen vorgenommen werden können. Der Dienst empfängt Ereignisse `TYPE_WINDOW_STATE_CHANGED` und hält das vom System gemeldete Paket im Arbeitsspeicher; er liest weder den Benutzeroberflächenbaum noch Texte oder Eingabefelder aus. Die vorübergehende Bildschirmaufnahme dient dazu, den oben beschriebenen durchschnittlichen Farbwert zu berechnen.
- **`SCHEDULE_EXACT_ALARM`:** Steht im Zusammenhang mit der Planung exakter Alarme. Wenn Android exakte Alarme nicht zulässt, kann der Zeitplan ungenauer sein und sich verzögern.
- **`RECEIVE_BOOT_COMPLETED`:** Ermöglicht dem Modul, das Ereignis eines Geräteneustarts zu empfangen und die Neuplanung von Routinen zu behandeln.
- **`WAKE_LOCK`:** Ermöglicht, das Gerät während einer Ausführung aktiv zu halten, die im Hintergrund fortgesetzt werden muss.
- **`KILL_BACKGROUND_PROCESSES`:** Steht im Zusammenhang mit der vorkonfigurierten Aktion, den Prozess der Ziel-App im Hintergrund zu beenden, wenn die Routine vorsieht, sie erneut zu öffnen.
- **`POST_NOTIFICATIONS`:** Steht im Zusammenhang mit der Anzeige lokaler Benachrichtigungen, zum Beispiel einer Ergebnisbenachrichtigung.

Verfügbarkeit, Erteilung und Autorisierung dieser Berechtigungen werden von Android gesteuert und können je nach Einstellungen, Systemversion und Gerät variieren. Dieser Text setzt nicht voraus, dass für jede Berechtigung ein bestimmter Laufzeitdialog angezeigt wird. Erteilen Sie nur Berechtigungen, die Sie für die gewünschten Funktionen für erforderlich halten.

## Vorgesehenes Alter

Diese Beta-Version von TapRoutine richtet sich an Erwachsene ab **18 Jahren**; sie wurde nicht für Kinder oder Jugendliche entwickelt.

## Künftige Änderungen

Die hier beschriebenen Funktionen und Praktiken beziehen sich auf die untersuchte Vorschau-APK und können sich ändern. Sollte eine künftige Version andere Daten erheben, übertragen, weitergeben oder aufbewahren oder weitere Dienste hinzufügen, muss diese Richtlinie vor der Verteilung überarbeitet werden, damit sie die betreffende Version korrekt beschreibt. Bitte beachten Sie die Richtlinienversion, die dem freigegebenen Build beiliegt.

## Kontakt

Fragen oder Anliegen zu dieser Richtlinie: [vitoriotaz@gmail.com](mailto:vitoriotaz@gmail.com).
