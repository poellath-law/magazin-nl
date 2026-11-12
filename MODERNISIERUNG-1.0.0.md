# PE-Magazin Newsletter 1.0.0

## Dateien und Versionierung

Branch: `newsletter/modernisierung-1.0.0`. Neue Versandvorlage: `HTML5 PE-Mag-NL-1.0.0.html`. Neue Dokumentation: `MODERNISIERUNG-1.0.0.md`. Die März-2026-Quelle `HTML5 PE-Mag-NL.html` bleibt unverändert. Version 1.0.0 bezeichnet die erste modernisierte Ausgabe; weitere Korrekturen erhalten Patch-, Funktionserweiterungen Minor- und grundlegende Änderungen Major-Versionen. Kein Commit und kein Push ausgeführt.

## Darstellung

HTML5-Doctype, deutsche Dokumentensprache, UTF-8, Viewport und Apple-Mail-Meta-Angaben. Zentrierte, fließende Tabellen mit maximal 740 px für den Hauptbereich; links maximal 495 px einschließlich des bisherigen rechten Abstands, rechts 235 px. Inline-Tabellen umbrechen auch ohne Media Queries; bis einschließlich 740 px stehen beide Spalten vollständig untereinander, Hauptinhalt zuerst. Mobile Innenabstände 10 px, Fließtext 16/23 px und kompakterer Logo-Abstand. Farben, Texte und wesentliche Desktop-Abstände bleiben erhalten. Layouttabellen sind als Präsentationstabellen markiert. Keine Flexbox- oder Grid-Abhängigkeit.

Bilder behalten ihre Quellen und expliziten Breiten/Höhen; `max-width:100%; height:auto` erlaubt proportionale Skalierung. Beschreibende Alternativtexte wurden ergänzt. Nicht funktionierende JavaScript-Fehlerhandler wurden entfernt. Kalender-/Abmeldeaktionen und Social-Links erhalten mobil mindestens 44 px hohe Klickflächen. Redaktionelle Links bleiben im Fließtext; sie haben keine pauschalen 44-px-Boxen, da dies den Textfluss verändern würde.

## Silbentrennung und Fallbacks

Alle manuellen weichen Trennzeichen entfernt, einschließlich möglicher numerischer Schreibweisen und U+00AD. `lang="de"` gilt für das gesamte Dokument. Textzellen, Absätze und Überschriften erhalten inline `-webkit-hyphens:auto; -ms-hyphens:auto; hyphens:auto`, vererbbar auch auf enthaltene Links und Spans. Widersprechende `word-break:keep-all`-Regeln und atomare Link-Spans wurden entfernt. `overflow-wrap:break-word`, zusätzlich `overflow-wrap:anywhere` in unterstützenden Clients sowie `word-wrap:break-word` verhindern Überlauf. `word-break:normal` erhält normale Wortgrenzen; kein `break-all`. Frühere `nobr`-Elemente wurden durch umbrechbare Spans ersetzt. Geschützte Bindestriche und andere bestehende Zeichen bleiben inhaltlich unverändert.

## Outlook und andere E-Mail-Clients

Für klassisches Outlook mit Word-Renderer: bedingte MSO-Tabelle mit festen Desktop-Spalten, Tabellenattribute, Inline-Formatierung, keine Flexbox und 96-DPI-Office-Einstellung. Klassisches Outlook unterstützt Media Queries, Maximalbreiten und CSS-Silbentrennung nur eingeschränkt beziehungsweise nicht; dort ist die feste Desktop-Darstellung vorgesehen. Auch `overflow-wrap`/`word-wrap` sind im Word-Renderer kein universell verlässlicher Notumbruch. Extrem lange untrennbare Zeichenfolgen müssen dort echt getestet werden.

„Outlook Version 2606“ allein bestimmt den Renderer nicht: klassisches Outlook und neues Outlook getrennt testen. Das neue Outlook sowie Outlook Web filtern CSS anders; automatische deutsche Silbentrennung nicht als garantiert ansehen. Gmail Web und Gmail-Apps unterstützen CSS-Silbentrennung nicht zuverlässig; Android-Mail-Apps unterscheiden sich nach Hersteller, Renderer und Kontoart. Apple Mail und iOS Mail unterstützen automatische deutsche Silbentrennung voraussichtlich am besten, abhängig von Wörterbuch und Systemeinstellungen. Nicht unterstützende Clients dürfen Wörter ohne sichtbaren Trennstrich umbrechen. Browserprüfungen ersetzen keine Mailclient-Prüfung.

## WordPress / The Newsletter Plugin

Die neue Datei als vollständige HTML-Vorlage im HTML-/Custom-HTML-Modus verwenden. Nicht durch einen visuellen Blockeditor neu serialisieren lassen. Der bestehende Platzhalter `{unsubscription_confirm_url}` bleibt exakt erhalten, ebenso alle Trackingparameter, Mailto-, Webcal- und Kalender-Links. Kein zusätzlicher Versanddienst oder externes Stylesheet erforderlich. Nach Speichern und beim Testversand prüfen, ob das eingesetzte Plugin beziehungsweise dessen CSS-Inliner den Head, Media Queries, MSO-Kommentare und Sprachangaben erhält. Abmeldeplatzhalter muss im tatsächlichen Versand aufgelöst werden. Die genaue Plugin-Version und ihre Verarbeitung waren hier nicht verfügbar.

## Durchgeführte Prüfungen

- Automatischer Vergleich: alle 66 Ziel-URLs, 27 Bildquellen und sichtbaren Texte unverändert, lediglich weiche Trennzeichen entfernt. Alle Bilder mit nicht leerem Alternativtext und expliziten Abmessungen.
- Chromium/Playwright bei 320, 375, 390, 414, 740, 768 und 1024 px: kein horizontaler Dokumentüberlauf, Hauptbereich mobil vor rechter Spalte, Desktop-Spalten nebeneinander und zentriert.
- Zusätzlicher künstlicher Langwort-Test mit deaktivierten Media Queries: kein horizontaler Überlauf im Browser. Keine JavaScript-Fehler.
- Statischer HTTP-Abruf aller acht HTML-Dateien: Status 200 und bytegleicher Inhalt. Desktop-/Mobil-Screenshots mit blockierten externen Assets geprüft; damit keine vollständige Bilddarstellungsprüfung.
- Externer Bildabruf von www.pe-magazin.de: Netzwerkproxy antwortet 403 auf den Tunnelaufbau. Remote-Bilder und externe Link-Erreichbarkeit konnten daher nicht vollständig überprüft werden. Lokale Pfad-/URL-Vergleiche sind erfolgreich; sie belegen keine Erreichbarkeit.

## Vorhandene Auffälligkeiten, unverändert

Zwei Kalender-Links bestehen nur aus `&utm_source=newsletter&utm_medium=email&utm_campaign=pemag_202603` und besitzen kein eigentliches Ziel. Daneben bestehen URLs mit doppeltem Slash, alten Kampagnenwerten und einem Trackingzusatz hinter einem Fragment. Gemäß Vorgabe wurden keine Ziel-URLs korrigiert. Diese Stellen vor dem Versand redaktionell prüfen.

## Noch erforderliche Testmailings

1. Aus WordPress/The Newsletter Plugin an klassisches Outlook 2606, neues Outlook, Outlook Web, Apple Mail, iOS Mail, Gmail Web sowie Gmail unter Android/iOS senden.
2. Desktop-Zweispaltigkeit, mobile Reihenfolge und Breiten einschließlich 320 px, Bildgrößen und -proportionen, deutsche lange Wörter, Buttons/Links sowie Footer/Abmeldung prüfen.
3. Bilder sowohl geladen als auch blockiert; Hell-/Dunkelmodus und Outlook bei Windows-Skalierung 100/125/150 Prozent prüfen.
4. Onlineansicht, alle Kalender-Links einschließlich Webcal, Tracking und personalisierte Abmeldung testen. Keine Test-Abmeldung oder Registrierung wurde hier ausgelöst.
5. Tatsächlichen versendeten HTML-Quelltext auf erhaltene Styles/MSO-Kommentare und Gmail-Abschneiden prüfen. Die Vorlage liegt unter der typischen Gmail-Grenze von ungefähr 102 KB, kann aber durch Plugin-Tracking anwachsen.
