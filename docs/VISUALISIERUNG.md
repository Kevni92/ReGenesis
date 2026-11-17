# Bibliothek für Diagramme, Animationen und Simulationen

## Entscheidungsregel: so wenig wie möglich, so viel wie nötig
**Keine Grafik als Dekoration.** Für eine Anleitung sinnvoll sind:
- Tabelle: Mengen, Materialvergleich, Fehlersuche, Messwerte.
- Schaubild/Schema (SVG): Aufbau, Zu-/Abfluss, elektrische Verbindung, Schnittzeichnung.
- Explosionszeichnung: Reihenfolge beim Zusammenbau eines mechanischen Gerätes.
- Ablaufdiagramm: Entscheidungssituationen und Sicherheitsstopps.
- Animation/Bildfolge: zeitliche Bewegung oder ein Prozess, den ein statisches Bild nicht ausreichend vermittelt.
- Simulation: veränderliche Beziehungen (z. B. Hebelarm/Kraft, Durchfluss/Druck) mit mathematisch oder empirisch begründetem Modell.

Eine komplexe 3D-Darstellung nur, wenn sie nachweislich mehr erklärt als 2D.

## Komponentenkatalog (geplant; noch keine Laufzeitbibliothek)
1. `StaticDiagram`: versioniertes SVG, Figurennummer, Legende, Alttext.
2. `AnnotatedCutaway`: Schnittzeichnung, nummerierte Bauteile; Druck zeigt alle Labels.
3. `ProcessSteps`: Bildfolge eines Vorgangs; Druck verwendet alle relevanten Zustände.
4. `FlowChart`: reproduzierbares Entscheidungsdiagramm; Textstruktur zusätzlich.
5. `MechanismAnimation`: Start/Pause/Zurücksetzen/Einzelschritt, reduzierte Bewegung.
6. `ParameterSimulation`: physikalische Eingaben mit Einheit, Grenzwerten, Formel, Referenzwerten; Druck zeigt Referenzfall und Wertetabelle.
7. `ComparisonChart`: Vergleich und Unsicherheitsangaben; Farbunabhängigkeit.
8. `TechnicalDrawing`: Maße, Material, Toleranzen soweit belegt; Maßstab nur wenn tatsächlich maßstäblich.

## Layoutregeln
- Nummerierte Bauteile und selbsterklärende Pfeile, Legende neben der Darstellung.
- Beschriftungen auf Deutsch, SI-Einheiten, konsistente Notation.
- Keine Sicherheitshinweise allein in Hover-Tooltips; alle Pflichtinformationen als Text.
- Mobil bedienbar; Steuerung tastaturfähig und mit zugänglichen Labels.
- Druck: Vektor vor Raster, Kontrast in Graustufen, keine abgeschnittenen Legenden.

## Verbindliche Assets
Jedes Visual enthält:
- eindeutige `visual_id`, verwendende Artikel-IDs und kurze Lernfrage,
- Typ und statische Hauptdarstellung (`static_fallback`),
- genaue fachliche Aussagen, Quellen, Formeln und verwendete Näherungen,
- Interaktionsbeschreibung, Wertebereiche, Ausgangszustand, Reset,
- druckbare Beschriftung, Ersatz-Tabelle/Bildfolge, Alternativtext,
- Urheber/Lizenz/Version, Reviewer und bekannten Grenzen.

Vorlage: visuals/_TEMPLATE.md. Neue Visuals im Katalog referenzieren und Existenz prüfen.

## Technische Bibliotheken
**Bevorzugt:** semantisches HTML, SVG, CSS, einfaches lokales JavaScript. **Optional nach Bedarfsnachweis:** Mermaid für aus Quelltext generierbare Abläufe, D3 für komplexe mathematische und datengetriebene Diagramme. Abhängigkeiten versioniert lokal einbinden, Lizenz prüfen, Druck-SVG beim Build erzeugen. Kein CDN. Keine Bindung an ein Framework in den Quelldaten.

## Animation vs. Druck
Interaktive Darstellung niemals das einzige Exemplar der Information. Zu jedem dynamischen Asset gehören eine definierte Momentaufnahme, eine Ablauf-/Wertetabelle oder mehrere nummerierte Einzelbilder und ein vollständiger Begleittext. Diese Inhalte werden im PDF automatisch verwendet.

## Fachliche Validierung
Simulationen brauchen Referenzrechnungen mit Einheitentests, Randwertprüfungen und dokumentierte Näherungen. Visuell plausibles Verhalten genügt nicht. Ein Diagramm mit nicht validierter Skalierung darf nicht als technische Messgrafik auftreten.

