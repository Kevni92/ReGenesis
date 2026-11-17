# Architekturentscheidungen (Decision Log)

- **ADR-001 – Kein Spiel (2026-11-17, entschieden):** ReGenesis ist eine ernsthafte Wissensbibliothek. Keine Spielmechanik und keine als Gameplay stilisierten Technologiebäume. Sachliche Voraussetzungenverweise sind erlaubt.
- **ADR-002 – Inhalt unabhängig vom Frontend (2026-11-17, entschieden):** Markdown/MDX + strukturierter Katalog + versionierte Assets. Keine feste Kopplung fachlicher Texte an eine JS-Komponente.
- **ADR-003 – Static-first und print-first (2026-11-17, entschieden):** ohne JavaScript lesbarer Primärtext, druckbare Diagramme, lokal archivierte Medien.
- **ADR-004 – Offline doppelt absichern (2026-11-17, entschieden):** statische installierbare Site plus portable `file://`-Fassung; PWA allein genügt nicht.
- **ADR-005 – Astro/TypeScript/SVG (2026-11-17, vorgeschlagen):** bevorzugter technischer Stack, endgültig erst nach kleinem Print- und Offline-Prototyp festlegen.
- **ADR-006 – Fachreview vor Freigabe (2026-11-17, entschieden):** KI-Text ist nicht automatisch fachlich geprüft; riskante Anleitungen brauchen dokumentierte Prüfung.
- **ADR-007 – Projektlizenz (offen):** passende offene Lizenz für eigens erstellten Text, Quellcode und Grafiken getrennt festlegen.

Änderungen an entschiedenen Punkten nur mit Begründung, Auswirkungen auf Archiv/Print und aktualisiertem Datum dokumentieren.

