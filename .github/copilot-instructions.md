# ReGenesis: GitHub Copilot / Coding-Agent-Anweisungen

Lies **zuerst** `AGENTS.md`, `README.md`, `docs/STATUS.md` und `content/catalog.json`. Je nach Auftrag anschließend `docs/REDAKTION.md`, `docs/INHALTSMODELL.md`, `docs/VISUALISIERUNG.md`, `docs/DRUCK_OFFLINE.md` und die relevanten `SKILL.md`-Dateien in `.github/skills/` konsultieren.

**Produktziel:** sachliche, deutschsprachige, offline- und A4-druckfähige Praxisbibliothek; **keine Spielelemente**. Kein fremder CDN- oder API-Zugriff zur Laufzeit. Inhaltsquellen und Frontend streng trennen. Bei jeder Änderung Katalog-/Datei- und Statuskonsistenz prüfen.

Derzeit ist das Repository ein **Konzeptfundament ohne implementierte Website**. Bestehende Features nicht erfinden. Nicht geprüfte Artikel bleiben Entwürfe. Jede künftige Animation und Simulation braucht eine fachlich korrekte, eigenständige statische Druckalternative.

Agent-Skills:
- `regenesis-bestand-pruefen`: Bestandsaufnahme und Dubletten
- `regenesis-recherchieren`: Quellen- und Sicherheitsprüfung
- `regenesis-artikel-erstellen`: redaktionelle Erweiterung
- `regenesis-visualisieren`: Diagramm/Animation/Simulation
- `regenesis-druck-offline`: Print-/Offline-Prüfung
- `regenesis-review`: fachlicher und redaktioneller Audit

Berichte nur tatsächliche Commits, geänderte Pfade und ausgeführte Tests. Bei GitHub-Konflikten aktuellen Stand neu einlesen; keine bestehenden Arbeiten blind überschreiben.

