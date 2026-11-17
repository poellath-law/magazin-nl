# Desktop-Raster 1.0.4

Neue Datei: `HTML5 PE-Mag-NL-1.0.4.html`, Basis ist die zuletzt gepushte Versandfassung 1.0.3. Die verworfenen Wörterbuch-/Generatorentwürfe sind nicht Bestandteil dieser Version. Keine Änderung am Generator oder der bisherigen Silbentrennung. Noch kein Commit/Push.

## Maße

- Zentrierter Hauptbereich maximal 775 px. Desktop als echte Tabellenzeile mit drei Zellen: Hauptspalte 470 px, leere Abstandsspalte 50 px, Seitenleiste 255 px. Feste HTML-Breitenattribute und Inline-Breiten ersetzen die bisherigen Inline-Tabellen mit bedingter MSO-Zusatztabelle.
- Hauptspalte: Inhalte mit einmaligem 20-px-Einzug links innerhalb der 470 px. Kein zusätzlicher 20-px-Artikel-Wrapper und kein innenliegender rechter 50-px-Abstand mehr. Editorial: 15 px Padding plus 5 px Rahmen = 20 px Textabstand. Überschriften, Fließtexte, Listen und Bilder beginnen ebenfalls bei 20 px. Die blauen Kategoriekennzeichnungen behalten ihren bis zum linken Spaltenrand reichenden farbigen Hintergrund; der innere Textabstand bleibt erhalten.
- „Ihre Meinung zählt!“: 450 px breite Tabelle, rechts innerhalb der 470 px ausgerichtet. Das ergibt 20 px Abstand links, ohne von unzuverlässigem Tabellen-Margin in Outlook abhängig zu sein.
- Seitenleiste und graue Eventhintergründe 255 px statt 235 px. Die 215-px-Eventbilder bleiben unverändert; der Hintergrund wächst auf beiden Seiten um 10 px.
- LinkedIn: links ausgerichtete, feste 255-px-Tabelle. Breiten per colgroup, HTML-Attribut und Inline-CSS: 10 px Einrückung, 40 px Logo, 20 px Zwischenraum, 185 px Text. Kein Float, kein Bild-Margin und kein zusätzliches Textpadding. So werden die Abstände nicht aus automatisch verteilten Zellen abgeleitet. Bilddatei unverändert; ihre möglicherweise vorhandenen internen Freiflächen gehören zum Originalbild.

## Mobil und Mailclients

Bis einschließlich 775 px werden Hauptspalte und Seitenleiste gestapelt, die leere Zwischenzelle ausgeblendet. Das mobile Padding, der Feedbackblock unten und die bisherigen 235-px-Eventkästen bleiben erhalten. Der Umschaltpunkt wurde wegen der neuen Desktopgesamtbreite von 740 auf 775 px angepasst. Die linke Hauptspalte hat mobil weiterhin die verfügbare Bildschirmbreite.

Klassisches Outlook erhält dieselbe echte Tabellenstruktur wie andere Clients. CSS-Media-Queries bleiben dort eingeschränkt; feste Desktopbreiten sind als Fallback vorgesehen. WordPress/The Newsletter Plugin muss die komplette HTML-Vorlage einschließlich Styles erhalten. Die konkrete Desktopdarstellung insbesondere in Outlook 2606 muss noch per Testmailing bestätigt werden; Browsermessungen sind dafür kein Ersatz.

## Prüfung

Chromium/Playwright bei 320, 375, 390, 414, 740, 775, 776 und 1024 px: kein horizontaler Überlauf. Ab 776 px exakt 470/50/255 px gemessen; Feedback 450 px breit und um 20 px eingerückt; Eventhintergründe 255 px breit; LinkedIn-Abstand 20 px bei allen Prüfbreiten. Texte, Link-Ziele, Bildquellen, Alternativtexte und Bildabmessungen gegenüber 1.0.3 unverändert. Externe Bilder wurden blockiert; Messungen prüfen die HTML-Geometrie, nicht die Bildinhalte oder Bild-Erreichbarkeit.
