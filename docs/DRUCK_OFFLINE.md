# Druck, PDF und dauerhafte Offline-Verfügbarkeit

## Gleichwertige Ausgabeformen
ReGenesis ist **print-first**. Jede wichtige Information muss als Artikel in HTML **und** auf Papier verständlich bleiben. Animationen sind Ergänzungen, nicht Voraussetzung. PDF ist ein eigenständiges Archivformat.

## Druckmodi (geplant)
1. Aktuellen Artikel in A4 hochkant oder bei großen Schaltplänen gezielt quer.
2. Kompakte Werkstatt-Anleitung mit Materialliste, Schritten, Sicherheit und Prüfmerkmalen.
3. Themenband mit Inhaltsverzeichnis, Seitenzahlen, Bildverzeichnis, Quellen und Stichwortindex.
4. Vollarchiv als mehrere Bände, nicht als ein riesiges PDF. Version und Exportdatum auf Deckblatt.

## Druckgestaltung
Schwarz auf Weiß, ausreichend große Schriften (Fließtext etwa 10–11 pt), sinnvolle Absatzabstände, Tabellen mit wiederholten Kopfzeilen. Navigation, interaktive Controls, Animation und dekorative Elemente ausblenden. Warnungen als Wörter und Formen, nicht ausschließlich farblich. Abbildungen mitsamt Beschriftung zusammenhalten; lange Tabellen sauber über Seiten umbrechen; Überschriften nicht am Seitenende isolieren. Praktische Anleitungen beginnen nach Möglichkeit mit einer neuen Seite.

Jede Abbildung: Figurennummer, aussagekräftige Unterschrift, Quellenhinweis; SVG und Schriftgrößen auf realem A4-Ausdruck überprüfen. Keine QR-Codes als einzige Quelle für wesentliche Inhalte.

## Interaktiv -> statisch
- Simulator: aus festem Ausgangszustand reproduzierbare Zeichnung plus Parameter-/Ergebnistabelle.
- Animation: nummerierte Schlüsselbilder (Vorher/Zwischenzustand/Nachher) plus erklärender Text.
- Interaktives Flussdiagramm: vollständiger statischer Entscheidungsbaum.
- 3D: bemaßte Ansichten/Schnittzeichnungen und Legende.
- Eine Druckversion darf nie leer sein, nur weil JavaScript abgeschaltet wurde.

## Offline-Testmatrix (Definition of Done)
- Statische HTML-Seiten im Browser ohne Netzwerk.
- USB-/SD-Archiv per `file://`, einschließlich relativer Links und Abbildungen.
- Website nach PWA-Installation und anschließendem vollständigem Netzabbruch.
- JavaScript deaktiviert: alle Kerntexte, Warnungen, Materiallisten und statischen Bilder weiterhin sichtbar.
- A4-Printvorschau in Chromium und Firefox; Schwarzweiß sowie Graustufen.
- PDF-Ausgabe kontrolliert auf fehlende Assets, Umbrüche, Seitenzahlen, Tabellen und Quellen.
- Such-Fallback: alphabetisches Inhaltsverzeichnis/Stichwortliste auch ohne JS.
- Langzeitarchiv: UTF-8, offene Dateiformate, lokale Kopien aller wesentlichen Materialien, dokumentierte Build-Anleitung.

## Technische Grenzen
Service Worker benötigen geeignete Ursprünge wie HTTPS oder localhost; sie sind **nicht** die Portable-Strategie für `file://`. Browser-Caches können gelöscht werden. Darum ist ein entpackbares, eigenständig lesbares statisches Archiv verpflichtend. Siehe https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps/Guides/Offline_and_background_operation und https://developer.mozilla.org/en-US/docs/Web/CSS/Guides/Media_queries/Printing.

## Freigabe
Print-/Offline-Kriterien sind bereits beim Erstellen eines Artikels und seiner Visuals zu prüfen. Bis eine Testpipeline existiert, dürfen sie in Statusberichten nicht als automatisiert erfüllt bezeichnet werden.

