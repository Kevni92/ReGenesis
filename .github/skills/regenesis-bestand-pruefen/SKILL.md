---
name: regenesis-bestand-pruefen
description: Prüft den realen GitHub-Repository-Bestand, vorhandene Themen, Visualisierungen, Querverweise und Umsetzungsstatus vor einer ReGenesis-Änderung.
---

# Bestandsaufnahme und Dublettenprüfung

**Auslöser:** neuer Chat, neues Thema, Änderung eines Artikels oder Frage "was ist bereits umgesetzt?"

1. GitHub-Repository auf dem aktuellen Branch lesen; `README.md`, `AGENTS.md`, `docs/STATUS.md`, `content/catalog.json` und die Verzeichnisstruktur prüfen. Keine Vermutung aus früheren Chat-Antworten.
2. Alle passenden IDs, Titel, Synonyme und Kategorien im Katalog finden; anschließend dazu existierende Inhaltsdateien und Visual-Assets prüfen.
3. **Geplant ≠ vorhanden:** `planned` mit `path:null` gilt nicht als Artikel. `draft` bedeutet vorhanden, aber nicht freigegeben. `reviewed` nur mit dokumentierter unabhängiger Prüfung.
4. Für angefragtes Thema fachliche Überschneidungen, alternative Verfahren, Quellenlücken, offene Visuals und Dokumentationsbedarf notieren.
5. Falls die Suche auf einen partiellen oder unzugänglichen Repository-Stand beschränkt ist, das als Unsicherheit kennzeichnen.
6. Ausgabe: kurze Inventartabelle (ID, Titel, Status, Pfad, relevante Querverweise) + Empfehlung "ergänzen" oder "neu" + konkrete nächsten Dateien.
7. Bei Umsetzung und nach Änderung Katalog/Status erneut gegen tatsächliche Dateien prüfen.

**Fertig, wenn:** keine auf Mutmaßung beruhenden Statusangaben; jeder referenzierte Artikelpfad geprüft; tatsächliche und geplante Inhalte sauber getrennt.

