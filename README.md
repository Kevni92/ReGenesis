# ReGenesis – Praktische Wissensbibliothek für Krisen und Wiederaufbau

ReGenesis ist eine **ernst gemeinte, deutschsprachige, offline nutzbare und druckbare Wissensplattform**. Sie erklärt grundlegende Fähigkeiten, naturwissenschaftliche Zusammenhänge und den improvisierten Wiederaufbau nützlicher Technik mit verbreiteten, wiederverwendbaren Materialien.

**Keine Spielelemente:** keine Skilltrees, Freischaltungen, Punkte, Erfolge oder fiktiven Fortschrittsbalken. Im Mittelpunkt stehen verständliche, überprüfbare **Anleitungen**, Sicherheitsinformationen, Diagramme und bei fachlichem Mehrwert Animationen oder Simulationen.

## Orientierung

- [Konzept](docs/KONZEPT.md) – Ziel, Nutzerbedürfnisse, Informationsarchitektur
- [Technische Architektur](docs/ARCHITEKTUR.md) – Inhaltsmodell und Offline-Website
- [Inhalts- und Qualitätsregeln](docs/REDAKTION.md) – Recherchieren, schreiben, prüfen
- [Visualisierungen](docs/VISUALISIERUNG.md) – Diagramme, Animationen, Simulationen
- [Drucken und archivieren](docs/DRUCK_OFFLINE.md) – A4, PDF, statische Alternativen
- [Quellenstrategie](docs/QUELLEN.md) – belastbare Referenzquellen und Lizenzen
- [Roadmap](docs/ROADMAP.md) – konkrete Phasen und Abnahmekriterien
- [Bestandsübersicht](docs/STATUS.md) und [Themenkatalog](content/catalog.json)
- [ChatGPT-Projektanweisungen](CHATGPT_PROJECT_INSTRUCTIONS.md)
- [Agent-Anweisungen](AGENTS.md) und [Copilot-Anweisungen](.github/copilot-instructions.md)

## Arbeitsweise

1. **Vor jeder Änderung** Repository, `content/catalog.json` und `docs/STATUS.md` lesen; vorhandene Themen und Assets auf Überschneidung prüfen.
2. Recherchieren, Aussagen belegen, Risiken benennen und machbare Varianten für verbreitete Materialien beschreiben.
3. Neue Beiträge nach [Vorlage](content/topics/_TEMPLATE.md) erstellen und Quellen inklusive Abrufdatum dokumentieren.
4. Interaktive Elemente nur verwenden, wenn sie fachlich helfen; jedes davon benötigt eine textliche und druckbare Alternative.
5. Themenkatalog, interne Verweise, Status und Dokumentation in derselben Änderung aktualisieren.

## Geplanter Betrieb

Quelltexte bleiben als Markdown/MDX, strukturierte Metadaten und versionierte lokale Assets im Git-Repository. Die spätere Site wird **statisch** gebaut (Architekturvorschlag: Astro + TypeScript + SVG, sparsame interaktive Komponenten). Sie muss ohne Internet lesbar und als einzelne Artikel oder thematische Sammelbände druckbar sein. **Ein funktionsfähiges Web-Frontend ist noch nicht implementiert.**

## Mitarbeit mit ChatGPT

Ein ChatGPT-Projekt namens *ReGenesis* anlegen, den Inhalt von [CHATGPT_PROJECT_INSTRUCTIONS.md](CHATGPT_PROJECT_INSTRUCTIONS.md) in die Projektanweisungen kopieren und dieses GitHub-Repository für neue Chats zugänglich machen. Der Agent muss vor jeder Inhaltsarbeit den aktuellen Repository-Stand erneut prüfen; Projektanweisungen allein synchronisieren Repository-Dateien nicht automatisch.

## Lizenz

Die Lizenzierung eigener Inhalte, Bilder und möglicher Fremdmaterialien ist **noch zu entscheiden**. Bis dahin keine ungeprüften fremden Abbildungen oder längeren Textpassagen übernehmen. Quellenhinweise allein ersetzen keine Nutzungsrechte.
