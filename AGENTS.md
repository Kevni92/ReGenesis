# Verbindliche Agent-Anweisungen für ReGenesis

Diese Regeln gelten für alle KI-Assistenten, IDE-Agenten, ChatGPT-Projektchats und Automatisierungen, die an diesem Repository arbeiten.

## Mission und Grenzen
ReGenesis ist eine ernsthafte, wissenschaftlich belastbare Praxisbibliothek für Versorgung, Reparatur, Improvisation und schrittweisen technischen Wiederaufbau. **Kein Spiel, kein Gamification-System.** Keine Skilltrees, Erfolge, XP, Freischaltungen, künstliche Stufen oder Rollenspielmechaniken. Der frühere Technologiebaum-Prototyp ist **kein Produktvorbild**; sinnvolle technische Abhängigkeiten dürfen nüchtern als Querverweise dargestellt werden.

Das Leitprinzip lautet: **Mit einfachen, verbreitet verfügbaren Materialien machbare Verfahren beschreiben, ohne Qualität, Sicherheit oder Erfolg zu versprechen, die nicht nachgewiesen sind.** Nachnutzung vorhandener Infrastruktur hat häufig Vorrang vor Herstellung aus Rohstoffen.

## Vor jeder Arbeit
1. Aktuellen Repository-Stand lesen: README, AGENTS.md, docs/STATUS.md, content/catalog.json, relevante Artikel, bestehende Visuals und Skills. Nicht aus Chat-Erinnerungen auf den Bestand schließen.
2. Titel, Synonyme, IDs, Ordner und Querverweise auf Dubletten prüfen; bestehende Artikel ergänzen statt doppelt anzulegen.
3. Auftrag eingrenzen, recherchierbare Teilfragen und benötigte Quellen benennen; Unsicherheiten offen kennzeichnen.
4. Bearbeitung in bestehender Konvention durchführen; keine Themen als fertig ausgeben, wenn sie nur geplant sind.

## Inhalte
- Deutsch, sachlich, präzise; verständlich für Menschen ohne Fachausbildung.
- Kurzer Zweck, Ausgangslage, Voraussetzungen, Materialalternativen, Werkzeuge, Zeit/Kosten nur belastbar, Sicherheitsmaßnahmen, nummerierte Arbeitsschritte, Funktionsprüfung, Fehlersuche, Wartung, Grenzen, Alternativen, Grundlagen, Quellen.
- Klare Trennung: **theoretisch erklärbar**, **mit geborgenen Bauteilen machbar**, **mit einfachen Werkzeugen nachbaubar**, **nur mit spezialisierter Infrastruktur realistisch**.
- Keine improvisierte Methode als gleichwertig zu einem zertifizierten Produkt ausgeben. Bei medizinischen, chemischen, elektrischen, baulichen oder lebensmittelhygienischen Risiken konservative Grenzen und professionelle Standards benennen.
- Kritische Anleitungen mit unbelegten Werten, fehlenden Prüfmethoden oder unklarer Sicherheit bleiben Entwurf.
- Keine Herstellung von Waffen, Explosivstoffen, Giften oder gefährliche experimentelle Behandlungsverfahren als praktische Anleitung; Fokus auf Prävention, sichere Alternativen und etablierte öffentliche Empfehlungen.
- Für jede nicht triviale fachliche Behauptung nachvollziehbare Quellen; Primärquellen/Normen/Fachliteratur priorisieren. Nicht zitierfähige KI-Aussagen sind keine Evidenz.
- Nicht behaupten, praktische Tests oder eine fachliche Freigabe durchgeführt zu haben, wenn das nicht erfolgt ist.

## Gestaltung, Offline, Druck
- Website ist ein Nachschlagewerk, keine Anwendung mit Spieloberfläche.
- Lesbarer Artikeltext und statische Grafiken funktionieren ohne JavaScript. Lokale Assets; kein CDN, keine externe Laufzeit-API, kein Tracking.
- Animation/Simulation nur bei echtem didaktischem Nutzen und immer mit statischem SVG, Bildfolge oder Tabelle, erläuterter Gleichung und druckbarer Beschriftung.
- A4-Schwarzweißdruck sowie PDF-Export ab Architekturentwurf bedenken; Aussagen nicht nur über Farbe, Ton oder Bewegung vermitteln.
- Barrierefreiheit: Tastatur, Kontrast, sinnvolle Alternativtexte, Textgrößen, reduzierte Bewegung.

## Abschluss jeder Änderung
- content/catalog.json und docs/STATUS.md synchronisieren; bei Inhaltsänderungen auch Querverweise/Quellen prüfen.
- Neue Dateien auf bestehende Vorlagen, konsistente Metadaten, kaputte Links, Dubletten, Druckalternative und Lizenz prüfen.
- Tatsächlich ausgeführte Prüfungen nennen, ungetestete Annahmen offen ausweisen.
- Keine Technologien oder Artikel als "publiziert" markieren, solange fachliche Prüfung bzw. Projektfreigabe fehlt.
- Neue ChatGPT-Chats sollen bei Bedarf die passenden Skills unter .github/skills/ lesen; Skills sind Anleitungen, keine implizit installierten ChatGPT-Projektfunktionen.

Nähere Regeln: docs/REDAKTION.md, docs/INHALTSMODELL.md, docs/VISUALISIERUNG.md, docs/DRUCK_OFFLINE.md.

