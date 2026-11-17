# Architekturvorschlag (Planungsstand)

## Entscheidung
**Content-first / static-first.** Inhaltsdaten sind unabhängig von Framework, Hosting und UI. Empfohlener Stack für die spätere Implementierung: **Astro (statische Ausgabe), Markdown/MDX, TypeScript, lokale SVG-Assets, wenige gezielte JavaScript-Inseln**. Vor Produktionsbeginn einen kleinen Prototypen hinsichtlich Print und Portable-Export testen.

Die Website selbst ist **noch nicht implementiert**. Diese Datei ist die Architekturvorgabe, kein Funktionsnachweis.

## Struktur
- `content/catalog.json`: zentrale, maschinenlesbare Artikelübersicht und Status.
- `content/topics/<gebiet>/<slug>.md`: einzelner Fachartikel, Metadaten und Quellennachweise.
- `visuals/`: Visualisierungs-Spezifikationen und künftig Quell-SVG/Animationsdateien plus statische Fallbacks.
- `docs/`: Architektur, Redaktion, Qualität, Druck und technische Entscheidungen.
- `.github/skills/`: wiederverwendbare Agent-Workflows.
- Geplant bei Implementierung: `src/` (Templates, UI, Komponenten), `public/assets/` (lokale Assets), `scripts/` (Validierung/Export), `tests/`, `dist/` (nicht handbearbeiten).

## Verarbeitung
Markdown + strukturierte Metadaten -> Schemavalidierung -> Inhalts- und Quellenindex -> statische HTML-Artikel -> Suchindex -> Druckstylesheet/Printansicht -> thematische PDF-Bände -> Offline-Paket.

**Inhalt niemals ausschließlich clientseitig laden.** Jede Kanon-Seite soll ohne JavaScript direkt lesbar sein. Schaltbare Diagramme sind progressive Verbesserung.

## Offline-Vertrieb: zwei getrennte Betriebsarten
1. **Statische Site/PWA:** GitHub Pages oder eigener HTTPS-Host; lokal gecachte Dateien und ein versioniertes Offline-Manifest; Service Worker als Komfortfunktion. Nach Erstinstallation bei Netzausfall nutzbar. Bei Updates atomare Cache-Strategie und kontrolliertes Entfernen alter Caches.
2. **Portables Archiv:** entpackbare HTML-/CSS-/Bild-Dateien auf USB/SD, **ohne laufenden Server und ohne PWA-Abhängigkeit**. Lesen der Artikel über `file://` auch bei gesperrten fetch-/Modulzugriffen; statische HTML-Navigation mit relativen Links. Eine portable Suche benötigt einen eingebetteten Index statt `fetch()`; mit deaktiviertem JS gibt es Inhaltsverzeichnis und Stichwortregister. Das ist separat zu testen.

PDFs sind **dritte, vollständig server- und JavaScript-unabhängige Form**. Die Website darf sich nicht allein auf Browser-Cache oder lokale Datenbanken verlassen.

## Suche und Verknüpfung
Build erzeugt aus Katalog und Frontmatter einen deterministischen Offline-Volltextindex; Suche über Titel, Problem, Synonyme, Materialien und Warnbegriffe. IDs sind dauerhaft. Build validiert alle Referenzen, Pfade, Kategorien und Quellenformate; kein erfundener Link bei nicht vorhandenem Inhalt.

## Visual-Engine
- Statisch: Inline-/externe SVGs mit Textalternativen, optional rasterisierte PDF-Fallbacks.
- Animation: CSS/JS/SVG oder Canvas nur lokal und sparsam, mit Pause/Reset/Schrittnavigation.
- Simulation: explizit dokumentierte Gleichungen, Einheiten, Eingabegrenzen und Prüfwerte; keine willkürlichen Effekte.
- Fremdbibliotheken optional: lokal paketiertes Mermaid für abstrakte Abläufe, D3 für Datenvisualisierung. Keine Bibliothek ist Pflicht; für einfache Grafiken native SVG bevorzugen.
- Jede dynamische Darstellung muss eine statische Zustandsgrafik und eine druckbare Tabelle oder eine Bildsequenz anbieten.

## Technische Qualität
Semantisches HTML, WCAG-orientierte Tastatursteuerung, `prefers-reduced-motion`, klare Kontraste, keine Informationen nur in Farben. Keine Telemetrie/Tracking, externen Fonts, CDNs oder Runtime-API-Aufrufe. Skripte und Dependencies inklusive Lizenzen versionieren; generierte Artefakte reproduzierbar.

## Geplante Prüfpipeline
Schema + ID-Eindeutigkeit + Querverweise + tote Quellenlinks (nur beim Online-Build) + Sicherheits-/Quellen-Checkliste + statische HTML-Erzeugung + Druck-Snapshots + Offline-Laufzeitprüfung unter unterbrochenem Netzwerk + Portable-Test mit `file://`. Externe Linkverfügbarkeit ist kein Offline-Kriterium, lokale Vollständigkeit dagegen schon.

Siehe docs/DRUCK_OFFLINE.md, docs/INHALTSMODELL.md und docs/ENTSCHEIDUNGEN.md.

