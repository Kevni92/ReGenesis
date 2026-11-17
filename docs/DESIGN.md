# Reduziertes, sachliches Designsystem

## Gestaltungsziel
ReGenesis soll wie ein technisches Handbuch und eine wissenschaftliche Bibliothek wirken, nicht wie ein Spiel. Ruhige, barrierearme Leseflächen, verständliche Hierarchien und hoher Nutzwert auch auf kleinen Displays und Papier.

## Seitenaufteilung
Desktop: linke Inhaltsnavigation, zentrale Lesespalte, rechts optional Quellen/Verweise. Mobil: einspaltige Inhalte mit übersichtlichem Inhaltsverzeichnis. Lange Anleitungen erhalten eine verankerte Abschnittsübersicht; Druck entfernt Navigation vollständig.

## Typografie und Farben
Systemschriften lokal (keine Font-Downloads), großzügiger Zeilenabstand, kontrastreiche Textfarben. Primär helle Oberfläche, zurückhaltende Akzentfarbe; Warnhinweise sprachlich und symbolisch zusätzlich kennzeichnen. Farblose Schaltpläne und SVGs bleiben interpretierbar. Zahlen und Maße mit SI-Einheiten, formelhafte Angaben maschinenlesbar.

## Komponenten (geplant)
`ArticleHeader`, `SafetyNotice`, `MaterialsTable`, `ProcedureSteps`, `VerificationChecklist`, `FailureModes`, `SourceList`, `RelatedArticles`, `PrintControls`, `StaticDiagram`, `MechanismAnimation`, `ParameterSimulation`.

Vor jedem Komponenten-Neubau prüfen, ob ein bestehendes Element passend erweitert werden kann. Keine visuell eindrucksvollen, aber fachlich unnötigen 3D-Lösungen.

## Textkonventionen
Imperative nur in ausdrücklich erlaubten praktischen Schritten. Risikohinweise vor dem Ablauf. Möglichst kurze Definitionen bei der ersten Nutzung eines Fachbegriffs. Keine Alarmrhetorik; keine Versprechen, welche die geprüften Quellen nicht stützen.

## Barrierefreiheit
Semantische Überschriften, Fokuszustände, Tastaturbedienung, sinnvolle Label, Alttexte für zwecktragende Abbildungen, Transkripte/Bildfolgen statt bewegungsabhängiger Information, `prefers-reduced-motion`. Interaktive Berechnungen sind nicht nur per Drag-Geste steuerbar.

Die konkrete Umsetzung und Tests folgen in der Frontend-Phase.

