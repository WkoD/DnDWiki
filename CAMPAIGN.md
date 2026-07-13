<!--
CAMPAIGN.md - SKELETT-TEMPLATE (DnDWiki-Vorlage).
Dies ist die kanonische Vorlage. In DnDWiki bleibt sie leer/generisch.
Jede Kampagne füllt beim 1:1-Kopieren der Vorlage ihre EIGENE Kopie aus.
Diese Datei ist kampagnen-eigen - sie wird nicht zwischen Repos verteilt und
überschreibt anderswo nichts.
-->

# CAMPAIGN.md

Kampagnenspezifischer Kontext für Claude. **Strikt pointer-basiert**: Diese Datei
enthält nur stabile Meta-Infos und Zeiger auf die Wiki-Tiddler - **keine** aus
Tiddlern ableitbaren Daten (Namen, XP-Zahlen, Datumswerte, Plot-Status), damit sie
nicht veraltet. Den echten Stand immer live aus den Tiddlern lesen.

## Identität

<!-- Kampagnen-Identität: 1-2 Zeilen, z. B. Homebrew-Setting oder offizielles
     WotC-Abenteuer. Keine weiteren narrativen Details. -->

## Tisch-Meta (steht NICHT in Tiddlern)

- **Spieler <-> Charakter:** <!-- reale Spielernamen <-> Charaktere; leer lassen, wenn n/a -->
- **Hausregeln:** <!-- abweichende Regeln -->

## Konventionen (DM-Entscheidung)

Das Format bietet mehrere optionale Mechanismen an. Für jeden legt der DM fest,
ob/wie er ihn für diese Kampagne nutzt - Claude richtet sich danach:

- **Session-Doku:** <!-- Standardvorschlag: keine separaten Session-Log-Tiddler;
  Sitzungen als Ergänzung an das jeweilige `Ereignis`-Tiddler anhängen (mehrere
  In-World-Zeitpunkte, getrennt durch `---` mit Datums-Überschrift). Alternative:
  eigene datierte Session-Tiddler. -->
- **Offene Punkte/Plot-Fäden:** <!-- Standardvorschlag: das `OffenePunkte`-Snippet
  inline in `Ereignis`-Tiddlern nutzen (Callout-Box, entfernen/verkleinern sobald
  aufgelöst). Alternative: zentraler Tracker-Tiddler. -->
- **Karten zu Orten:** <!-- Standardvorschlag: begleitender Karten-Tiddler
  `<Ort>_Karte` (Tag `Karte`, `bild`-Feld) neben dem Haupt-Ort-Tiddler, wo eine
  Karte sinnvoll ist. -->
- **Spieler-Sichtbarkeit:** <!-- Standardvorschlag: `$:/state/Spieler`-Umschaltung
  nutzen, um am Tisch zwischen DM- und Spieler-Perspektive zu wechseln (reine
  Render-Bequemlichkeit, kein Zugriffsschutz). Alternative: nicht nutzen. -->
- **Kampagnenspezifische Ordner/Assets:** <!-- z. B. zusätzliche Unterordner unter
  images/ für externe Tools (VTT-Kampfkarten o. Ä.), falls genutzt. -->
- **Erzählstil (Tempus):** <!-- Standardvorschlag: keine feste Vorgabe, DM legt
  fest. Beispiel für eine mögliche Wahl: durchgängige Vergangenheitsform
  (Präteritum) als Chronik-Stil, auch für andauernde Eigenschaften/Fakten -
  impliziert dann nicht Tod/Nicht-Existenz. Übliche Ausnahmen dafür: wörtliche
  Rede/Zitate, primäre In-World-Dokumente, TBC-Callout-Boxen, Trivia-Quiz-Blöcke. -->


## Story-Planungs-Workflow für Claude

**Erst den echten Tiddler-Stand über diese Pointer lesen, nie aus dem Gedächtnis
oder aus dieser Datei planen:**

- **Fraktionen / Orte / NPCs:** Tiddler mit dem jeweiligen Typ-Tag. Startpunkte:
  `Index.tid` und die Kategorie-Hub-Tiddler `Person.tid`, `Ort.tid`,
  `Organisation.tid`, `Ereignis.tid`, `Abenteuer.tid`, ...
- **Aktuelles In-World-Datum:** Body von `Datum.tid`.
- **XP-Gesamtstand:** Body von `Erfahrungspunkte.tid`.
- **Offene Plot-Fäden:** Suche nach dem `OffenePunkte`-Snippet in `Ereignis`-Tiddlern.
- **Kampagnenstruktur / Handlungsbögen:** `Abenteuer`-getaggte Tiddler.
- **Spielercharaktere:** `Spieler`-getaggte Tiddler bzw. `Spieler.tid`.

*Dann* konsistente Vorschläge machen, die an bestehende Tiddler/Tags anknüpfen
(explizite `[[WikiLinks]]` setzen).
