# Layoutkorrekturen 1.0.1

Neue Datei: `HTML5 PE-Mag-NL-1.0.1.html`, auf Basis der unveränderten Version 1.0.0. Dokumentation: `MODERNISIERUNG-1.0.1.md`. Branch bleibt `newsletter/modernisierung-1.0.0`; diese Korrekturen sind noch nicht committet oder gepusht.

## Mobil

- Verlinkte Überschriften „17. Funds Forum Frankfurt“ und „MUPET 2026“ ohne Unterstreichung; die Regel steht direkt am umschließenden Link und ergänzend im CSS und gilt auch auf Desktop.
- Aufzählungszeichen von 18 auf 9 px reduziert; ihre Tabellenzellen sind vertikal zentriert.
- „Ihre Meinung zählt!“ erscheint nach der gesamten Seitenleiste, vor Social-/Impressumsfooter. Dafür gibt es zwei inhaltlich identische Feedbacktabellen: Desktop zeigt das Original, mobil nur die untere Kopie. Die mobile Kopie ist inline versteckt und für Word-Outlook ausgeschlossen. Ohne Media Queries bleibt der Desktopblock sichtbar, damit das Feedback nicht verloren geht. Die Darstellung dieser Umschaltung nach Verarbeitung durch das Newsletter-Plugin mit Testmailings prüfen.
- LinkedIn-Logo in einer festen 40-px-Zelle links, daneben 20 px Abstand; der Satz steht bei den geprüften mobilen Breiten in einer Zeile.
- Terminüberschriften mit 115 % Zeilenhöhe statt 44 px. Kalender-Links nutzen ebenfalls 115 % und vertikales Padding für die Klickfläche. Event-Kastenbeschriftungen nutzen 21 px Zeilenhöhe.

## Desktop

- Editorial: erster Leerzeilenumbruch entfernt, stattdessen 5 px Innenabstand unter der oberen Linie; der linke Rahmen endet entsprechend früher.
- Eine echte Tabellenzelle mit 20 px rechtem Innenabstand schafft durchgehend Abstand zur Seitenleiste. Dies umfasst Rahmen, Überschriften, Fließtexte, Aufzählungen und den grauen Feedbackhintergrund. Der Container bleibt maximal 740 px breit.
- Blaue Kategoriekennzeichnungen erhalten jeweils 20 px zusätzliches oberes Padding.
- LinkedIn: Float und bisherige variable Logo-Zelle entfernt. Feste 40 px für das Logo und 20 px Abstand zum Text.
- Graue Eventkästen: Überschriften unten 10 px Padding zum Bild; Orts-/Datumsbeschriftungen jeweils 10 px mehr Padding oben und unten.

## Prüfung und Grenzen

Chromium/Playwright bei 320, 375, 390, 414, 740, 768 und 1024 px: kein horizontaler Überlauf; Desktopspalten nebeneinander, mobil Seitenleiste unten; mobil genau die untere Feedbacktabelle sichtbar. Unterstreichung der Eventüberschriften, 9-px-Aufzählungszeichen, 115-%-Terminzeilenhöhe sowie 20-px-Desktopspaltenabstand geprüft. Desktop-/Mobil-Screenshots kontrolliert, externe Bilder dabei blockiert; dies prüft das Layout mit Alternativtexten, nicht die Bildinhalte.

Texte, Bilder und Ziel-URLs bleiben erhalten; lediglich der Feedbackinhalt samt Mailto-Link existiert wegen der responsiven Platzierung zweimal im Quelltext. Je Ansicht wird nur eine Fassung angezeigt. Silbentrennung und Outlook-Fallbacks bleiben aus Version 1.0.0 bestehen; dort beschriebene Einschränkungen gelten weiterhin. Echte Testmailings aus WordPress insbesondere für Outlook 2606, Apple Mail/iOS und Gmail bleiben erforderlich. Vorhandene ungültige Kalenderziele bleiben unverändert.
