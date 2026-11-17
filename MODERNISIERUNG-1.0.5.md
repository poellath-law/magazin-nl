# Geschützte Mailadresse und Footer-Abstände 1.0.5

Neue Vorlage: `HTML5 PE-Mag-NL-1.0.5.html`. Vorversionen unverändert.

- Alle drei Vorkommen von redaktion@pe-magazin.de (Desktopfeedback, mobiles Feedback und Footer) haben direkt am Link und am Textspan `white-space:nowrap`, ausgeschaltete CSS-Silbentrennung und normale Wortumbruchregeln. Der Link ist zusätzlich ein Inlineblock. Das bisherige `white-space:normal` ist entfernt; ein widersprüchliches nobr/normal-Konstrukt wird nicht verwendet. Das Mailto-Ziel bleibt unverändert.
- Footeradresse: `P+&nbsp;Training | F&auml;rbergraben&nbsp;18 | 80331 M&uuml;nchen`.
- Geschäftsführung: `Jens H&ouml;rmann, Dr.&nbsp;Stephan Schade, Dr.&nbsp;Philip Schwarz van&nbsp;Berk, Dr.&nbsp;Frank Thi&auml;ner, ebenda.` Der vorhandene Einleitungstext bleibt erhalten.

Chromium/Playwright bei 320/375/390/414/775/776/1024 px: jeweils beide sichtbaren Mailadressen einzeilig, Silbentrennung deaktiviert, kein horizontaler Dokumentüberlauf. Alle Ziel-URLs und Bildquellen mit 1.0.4 abgeglichen und unverändert. Externe Bilder wurden im Browser blockiert. Outlook-Testmailing nach Verarbeitung durch das Newsletter-Plugin bleibt erforderlich. Die übrigen Layout- und Silbentrennungsregeln bleiben unverändert.

Commit und Push vom Nutzer ausdrücklich beauftragt.
