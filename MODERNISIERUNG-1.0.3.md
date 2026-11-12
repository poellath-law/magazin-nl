# Desktopkorrekturen 1.0.3

Neue Versanddatei: `HTML5 PE-Mag-NL-1.0.3.html`. Frühere Versionen unverändert.

- Hauptspalte: rechter Abstand von 50 statt 30 px in der umschließenden Tabellenzelle. Rahmen, Texte und grauer Feedbackhintergrund enden weitere 20 px früher.
- Die drei Artikelbereiche unter den Headerbildern erhalten je eine zusätzliche Tabellenzelle mit 20 px linkem Innenabstand. Dies umfasst Überschrift, Fließtext und „Lesen Sie auch“ samt Listen. Editorial und Headerbilder bleiben links unverändert.
- LinkedIn: explizit 235 px breite Desktoptabelle mit festen Spalten 10/40/20/165 px; Bildversatz über Abstandszelle statt Bild-Margin. Zwischen dem 40-px-Logo und dem Text stehen 20 px, das Logo ist 10 px vom Seitenleistenanfang eingerückt. Dies vermeidet automatische Breitenverteilung sowie Bild-Margin-Abhängigkeit in Outlook.
- Graue Eventkästen: 30 px Abstand unter den Überschriften; Beschriftung oben 35 und unten 40 px. Padding sitzt direkt auf Tabellenzellen, nicht mehr auf h3/p, weil der Word-Renderer solche Blockabstände nur eingeschränkt verarbeitet.
- Mobile Media Queries setzen die zusätzlichen Einrückungen zurück und stellen die bisherigen Abstände der Kästen wieder her.

Validierung: Chromium/Playwright bei 320/375/390/414/740/768/1024 px ohne horizontalen Überlauf, 50-px-Desktopabstand und 20-px-LinkedIn-Distanz geprüft. Mobile Positionen von Hauptinhalt, Seitenleiste und Feedback entsprechen 1.0.2; der Screenshot bei 375 px ist pixelgleich mit dem vorherigen Screenshot. Externe Bilder waren blockiert. Alle Link-Ziele gegenüber 1.0.2 identisch. Browserprüfung ist kein Nachweis der Outlook-Darstellung: Testmailing in Outlook 2606 erforderlich, besonders Spaltenbreiten, Einrückungen, LinkedIn und Eventkästen. Die bisherigen Einschränkungen zu Silbentrennung, Plugin-Verarbeitung und Kalenderlinks bestehen fort.

Commit und Push dieser Korrekturen wurden vom Nutzer ausdrücklich beauftragt.
