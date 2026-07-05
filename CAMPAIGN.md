<!--
CAMPAIGN.md — SKELETT-TEMPLATE (Base/DnDWiki).
Dies ist die kanonische Vorlage. In DnDWiki bleibt sie leer/generisch.
Jeder Kampagnen-Fork füllt seine EIGENE Kopie aus.
Diese Datei ist NICHT Teil des Sync — sie wird nie in die Forks verteilt und
überschreibt dort nichts. CAMPAIGN.md niemals in die Sync-Pfadliste von
repo-sync.yml aufnehmen.
-->

# CAMPAIGN.md

Kampagnenspezifischer Kontext für Claude. **Strikt pointer-basiert**: Diese Datei
enthält nur stabile Meta-Infos und Zeiger auf die Wiki-Tiddler — **keine** aus
Tiddlern ableitbaren Daten (Namen, XP-Zahlen, Datumswerte, Plot-Status), damit sie
nicht veraltet. Den echten Stand immer live aus den Tiddlern lesen.

## Identität

<!-- Kampagnen-Identität: 1–2 Zeilen, z. B. Homebrew-Setting oder offizielles
     WotC-Abenteuer. Keine weiteren narrativen Details. -->

## Tisch-Meta (steht NICHT in Tiddlern)

- **Spieler ↔ Charakter:** <!-- reale Spielernamen ↔ Charaktere; leer lassen, wenn n/a -->
- **Hausregeln:** <!-- abweichende Regeln -->
- **Kalender-Besonderheiten:** <!-- eigenes Kalendersystem etc. -->

## Aktuellen Stand aus dem Wiki lesen (Pointer statt Daten)

- **Fraktionen / Orte / NPCs:** Tiddler mit dem jeweiligen Typ-Tag. Startpunkte:
  `Index.tid` und die Kategorie-Hub-Tiddler `Person.tid`, `Ort.tid`,
  `Organisation.tid`, `Ereignis.tid`, `Abenteuer.tid`, …
- **Aktuelles In-World-Datum:** Body von `Datum.tid`.
- **XP-Gesamtstand:** Body von `Erfahrungspunkte.tid`.
- **Offene Plot-Fäden:** Suche nach dem `OffenePunkte`-Snippet in `Ereignis`-Tiddlern.
- **Kampagnenstruktur / Handlungsbögen:** `Abenteuer`-getaggte Tiddler.
- **Spielercharaktere:** `Spieler`-getaggte Tiddler bzw. `Spieler.tid`.

## Story-Planungs-Workflow für Claude

Immer **erst den echten Tiddler-Stand verifizieren**, nie aus dem Gedächtnis oder
aus dieser Datei planen:

1. Relevante Hub-/Kategorie-Tiddler lesen (siehe Pointer oben).
2. Offene Punkte via Suche nach dem `OffenePunkte`-Snippet sammeln.
3. Betroffene NPCs / Orte / Fraktionen über ihre Tags auflösen.
4. In-World-Datum (`Datum.tid`) und XP (`Erfahrungspunkte.tid`) prüfen.
5. *Dann* konsistente Vorschläge machen, die an bestehende Tiddler/Tags anknüpfen
   (explizite `[[WikiLinks]]` setzen — es gibt kein freelinks).
