# Layoutkorrekturen 1.0.2

Neue Vorlage: `HTML5 PE-Mag-NL-1.0.2.html`. Die bisherigen Versionen bleiben unverändert. Ergänzende Dokumentation: `MODERNISIERUNG-1.0.2.md`. Noch kein Commit/Push dieser Version.

- Mobil: Aufzählungszeichen von 9 auf 10,8 px (+20 %). Ihre Zellen werden oben ausgerichtet; ein 19-px-Zeilenkasten mit 4 px oberem Padding entspricht der ersten Textzeile. So stehen Zeichen nicht mehr mittig neben dem gesamten mehrzeiligen Absatz und dadurch zu weit unten.
- Mobil: Feedbackblock mit 30 px oberem Margin, weiterhin nach der vollständigen Seitenleiste. Clients ohne Media Queries behalten wie bisher die Desktopposition.
- LinkedIn-Link direkt inline ohne Unterstreichung, auf Mobil und Desktop. Feste 50-px-Logozelle, darin 40-px-Logo um 10 px nach rechts versetzt; separate 20-px-Abstandszelle und Text ohne zusätzliches linkes Padding. Gemessene Distanz zwischen Bildkante und Textzelle: 20 px. Bilddatei unverändert; eventuell bildinterne transparente Flächen gehören zur Originalgrafik.
- Desktop: rechter Innenabstand der gesamten Hauptspalte von 20 auf 30 px erhöht. Alle Inhalte einschließlich Rahmen und Feedbackhintergrund enden dadurch 10 px früher; Gesamtcontainer und Seitenleistenposition bleiben erhalten.
- Desktop: oberes Padding der drei blauen Kategorien von 20 auf 40 px verdoppelt, inline auch für klassisches Outlook. Mobil bleiben 20 px erhalten.
- Graue Eventkästen: Überschriften erhalten unten 20 statt 10 px Padding; Orts-/Datumsbeschriftungen oben 25 statt 15 und unten 30 statt 20 px. Die zusätzlichen Innenabstände gelten in beiden Ansichten.

Prüfung: Chromium/Playwright bei 320, 375, 390, 414, 740, 768 und 1024 px ohne horizontalen Überlauf. Mobile Feedbackposition, 10,8-px-Zeichen, Desktopspalten, 30-px-Innenabstand sowie LinkedIn-Abstand und fehlende Unterstreichung geprüft. Texte, Link-Ziele und Bildquellen gegenüber 1.0.1 unverändert. Screenshots verwenden blockierte externe Bilder; Bildinhalte sind dadurch nicht geprüft. Echte Testmailings aus WordPress an Outlook 2606, Apple Mail/iOS und Gmail bleiben erforderlich, insbesondere für Zeichenpositionen, Tabellenabstände und den mobilen Feedback-Margin. Vorher dokumentierte Einschränkungen bei CSS-Silbentrennung und bestehende Kalender-Link-Probleme gelten weiterhin.
