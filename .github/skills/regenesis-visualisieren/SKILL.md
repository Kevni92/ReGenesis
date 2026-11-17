---
name: regenesis-visualisieren
description: Plant und erstellt fachlich sinnvolle SVG-Diagramme, technische Schnittbilder, Animationen und Simulationen inklusive statischer Druckfassung.
---

# Diagramme und Funktionsmodelle

**Auslöser:** ein Prozess benötigt einen Ablauf, Mechanismus, Schnitt, Schaltplan oder mathematische Interaktion.

1. `docs/VISUALISIERUNG.md`, `docs/DESIGN.md`, `docs/DRUCK_OFFLINE.md`, `visuals/_TEMPLATE.md` und bereits bestehende Visuals lesen.
2. Exakt formulieren, **welche Lernfrage** eine Darstellung klärt. Wenn Text/Tabelle ausreichen, kein bewegtes Modell erstellen.
3. Format auswählen: Tabelle → SVG-Schema → Bildfolge → Animation → Simulation; die kleinste fachlich geeignete Variante bevorzugen.
4. Wissenschaftliche Grundlage und Daten prüfen; bei Simulation Formel, Einheiten, Eingabebereich, Grenzen, Referenzfall und erwartete Ergebnisse dokumentieren.
5. Spezifikation und eindeutige ID erstellen; Bauteile, Maßstäbe, Pfeile, Legende, deutsche Labels, Textbeschreibung und Quelle festhalten.
6. Als Erstes **statische druckfähige Hauptdarstellung** entwerfen. Danach optional Bewegung/Interaktion ergänzen.
7. Pause/Reset/Einzelschritt, Tastaturbedienung, zugängliche Beschriftung, reduzierte Bewegung und Bildschirmgrößen prüfen; keine externe Runtime-Ressource.
8. Für A4 eine gleichwertige SVG-Grafik bzw. Abfolge von Einzelbildern und Wertetabelle liefern; alle wichtigen Informationen müssen erhalten bleiben.
9. Visual in Artikel und Katalog referenzieren; Quelle, Urheber/Lizenz und Reviewstatus dokumentieren.
10. Nichts als "technisch simuliert und validiert" bezeichnen, bevor Referenztests tatsächlich durchgeführt wurden.

**Fertig, wenn:** die fachliche Kernaussage auch ohne Animation, JavaScript, Farbe und Internet lesbar und druckbar ist.

