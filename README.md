# DnDWiki

Ein **TiddlyWiki 5** (Node.js-Edition) für D&D-Kampagnen, Inhalte auf Deutsch.
Dieses Repo ist die **kopierbare Kampagnen-Vorlage**: pro-Wiki-Konfig,
Datendatei-Vorlagen (`Datum`, `Erfahrungspunkte`) und (leerer) Content in
`tiddlers/` sowie Assets (`images/`, `data/`). Engine und Formatschicht kommen als
Abhängigkeiten:

- **Engine:** offizielles [`tiddlywiki`](https://www.npmjs.com/package/tiddlywiki)
  aus npm, in `package.json` gepinnt.
- **Formatschicht:** aus [`TiddlyDnD-Plugins`](https://github.com/WkoD/TiddlyDnD-Plugins),
  fest versioniert gepinnt - dort das Plugin `dndwiki-core` (+ `staticfiles`).
- **Graph-Stack:** [`flibbles/tw5-graph`](https://github.com/flibbles/tw5-graph) +
  [`tw5-vis-network`](https://github.com/flibbles/tw5-vis-network) +
  [`tw5-relink`](https://github.com/flibbles/tw5-relink), einzeln als
  npm-Git-Dependency auf Release-Tags gepinnt.

## Neue Kampagne einrichten

1. Dieses Repo **1:1 kopieren** (z. B. über "Use this template" auf GitHub) und in
   `DnDWiki-<Name>` umbenennen.
2. `name` in `package.json` auf den Kampagnennamen setzen.
3. `npm install` (holt Engine + gepinnte Formatschicht/Graph-Stack).
4. Pro-Wiki-Konfig in `tiddlers/` befüllen: `$:/SiteTitle`, `$:/SiteSubtitle`,
   `$:/DefaultTiddlers`.
5. `tiddlers/Datum.tid` (In-World-Startdatum) und `tiddlers/Erfahrungspunkte.tid`
   (Start-XP, meist `0`) setzen.
6. `CAMPAIGN.md` ausfüllen - kampagnenspezifischer Kontext für Claude (Identität,
   Tisch-Meta, Konventionen); Anleitung dazu im Dateikopf.
7. Lore-Content unter `tiddlers/`, Bilder unter `images/`, PDFs unter `data/Buch/`
   ergänzen.
8. Repo auf GitHub pushen; `.github/workflows/npm-build-pages.yml` baut und
   deployt automatisch nach `gh-pages` (Pages-Settings einmalig auf den
   `gh-pages`-Branch stellen).

Keine Ordner ausschließen - Formatschicht/Plugins kommen aus dem Pin.

## Bearbeitung

Lokal mit Live-Editing bearbeiten:

```bash
npm install    # einmalig: Engine + Formatschicht + Graph-Stack holen
npm start      # Server auf http://localhost:8080 mit Live-Editing starten
```

Im Browser gemachte Änderungen werden automatisch als `.tid`-Dateien in
`tiddlers/` zurückgeschrieben - kein manuelles Speichern nötig. Details/Konventionen:
`CLAUDE.md` -> "Befehle & CI".

## Veröffentlichung

Die per CI nach `gh-pages` deployte Kopie ist **rein lesbar**.

Weitere Doku: `CLAUDE.md` (Entwicklung/Konventionen), `CAMPAIGN.md`
(kampagnenspezifisch).
