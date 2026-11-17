---
name: regenesis-druck-offline
description: Definiert und prüft Offline-Lesbarkeit, A4-Druck, PDF-Bände und statische Fallbacks in ReGenesis.
---

# Print- und Offline-Abnahme

**Auslöser:** neues Website-Feature, Visual, Artikel-Template, PDF-Export, Release oder Offline-Frage.

1. `docs/DRUCK_OFFLINE.md` und `docs/ARCHITEKTUR.md` lesen. Bestehende Implementierung, Buildskripte und Testberichte prüfen, nicht annehmen.
2. Anforderungen auflisten: Netzwerk aus, `file://`, No-JS, A4-Print, Schwarzweiß, PDF, Querverweise, statische Visuals, lokaler Such-Fallback.
3. Statische Lesefassung prüfen: Inhalt im HTML vorhanden, Pfade relativ, Bilder lokal, kein obligatorischer `fetch()`-Aufruf, keine externen Fonts/CDNs.
4. Falls Tests ausführbar sind: Website ohne Netzwerk laden, portable Kopie unter `file://` öffnen, JavaScript deaktivieren, Printansichten prüfen, PDF exportieren, Bilder/Tabellen/Quellen sichten.
5. Animierte/3D/Canvas-Inhalte gegen druckbare Schlüsselbilder und Tabellen abgleichen. Kein leerer Bereich in PDF.
6. Ausgabe klar nach **bestanden / fehlgeschlagen / nicht getestet** getrennt, mit Umgebung, Browser, Pfaden und Reproduktionsschritten.
7. Regressionsliste und konkrete Reparaturpunkte dokumentieren. Ohne tatsächliche Ausführung keine "Offline-Tests bestanden"-Aussage.

**Fertig, wenn:** getestete Verteilungsform(en) klar benannt und Ausfälle nicht verdeckt sind.

