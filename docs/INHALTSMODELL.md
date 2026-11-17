# Inhaltsmodell und Inventar

## Zentrale Wahrheit
`content/catalog.json` ist das **Verzeichnis**, vorhandene `content/topics/`-Dateien sind die **Inhalte**. Vor einer Änderung beides abgleichen. Ein Katalogeintrag ohne Datei ist geplant; eine Datei ohne Katalogeintrag ist ein Fehler. Status niemals allein aus Dokumententiteln oder alten Chatverläufen ableiten.

## Katalogeintrag
Pflicht: `id` (beständige ID im Format `gebiet.kurzname`), `title`, `category`, `status` (`planned`, `draft`, `reviewed`, `published`), `path` (Pfad oder null bei planned), `priority` (P0, P1, P2), `feasibility` (A-D), `keywords` (Array), `depends_on` (IDs), `related` (IDs), `visuals` (Asset-IDs), `review_notes`. Nicht belegte Angaben auslassen oder als ungeprüft deklarieren.

Status:
- planned: Idee/Katalogeintrag, keine fertige Anleitung
- draft: Inhalt vorhanden, noch nicht vollständig fachlich geprüft
- reviewed: fachlich und redaktionell geprüft; wer/wann/Umfang dokumentiert
- published: explizit freigegeben und tatsächlich in Ausgabe enthalten

`reviewed` oder `published` niemals allein durch KI-Selbsteinschätzung vergeben.

## Fachartikel – Frontmatter
Mindestens: `id`, `title`, `category`, `summary`, `status`, `feasibility`, `risk_level` (low/medium/high), `last_reviewed` (Datum oder null), `depends_on`, `related`, `visuals`. Status muss mit Katalog übereinstimmen.

Textaufbau:
1. Ziel und Kurzantwort
2. Einsatzgrenzen / "Nicht verwenden, wenn …"
3. Materialliste mit Mengen/Dimensionen und zulässigen Alternativen
4. Werkzeugbedarf, Schutzmaßnahmen und notwendiges Fachwissen
5. Schritte mit beobachtbaren Zwischenzuständen
6. Erfolgskriterien, Messung und typische Fehler
7. Pflege, Wartung und Ersatzverfahren
8. Funktionsprinzip: Physik/Chemie/medizinische Grundlagen
9. Quellen mit URL, Titel, Herausgeber, Publikationsstand und Zugriffsdatum
10. Version, offene Prüffragen, passende Querverweise

## Quellenformat
Zu jeder entscheidenden Behauptung eine quellengestützte Erklärung; Inline-Beleg `[Q1]` verknüpft eine bibliografische Quellenzeile im Artikel. Kein generischer Literaturblock ohne Zuordnung. Medien benötigen eigene Herkunft/Urheberrechtshinweise.

## Begriffe und Auffindbarkeit
Artikel-ID bleibt bei Umbenennung stabil. Titel, Synonyme und Suchbegriffe werden gepflegt. Nicht mehrere kanonische Anleitungen für dieselbe Aufgabe erstellen; lieber Varianten und Einsatzszenarien innerhalb desselben Artikels.

## Konsistenzprüfungen (künftig automatisieren)
Eindeutige IDs, existierende `path`-Dateien, Statusgleichheit, erlaubte Kategorien und Werte, referenzierte IDs vorhanden, keine zyklischen harten Voraussetzungen, Visuals mit statischem Fallback und Bildrechten, Quellenliste nicht leer (ab draft), aktualisierte docs/STATUS.md. In der derzeitigen Konzeptphase sind dies **Vorgaben**, noch keine ausgeführten Validatoren.

