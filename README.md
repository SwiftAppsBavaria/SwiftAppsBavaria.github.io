# SwiftAppsBavaria.github.io — Stand 2026-09-23

Familienwebsite der Mac-Apps, **12 Sprachen**. Dient als **Marketing-URL** in App Store Connect.

## Die Seiten werden ERZEUGT, nicht von Hand gepflegt

```
python3 ~/Documents/Claude/Xcode/_Shared/tools/website/build.py
```

Das Skript liegt im `_Shared`-Repo (nicht hier, damit keine lokalen Pfade öffentlich werden) und
schreibt `index.html`, `scollect/`, `sname2date/` (Englisch, Wurzel) sowie `de/ … zh-hant/` neu.
**Wer eine erzeugte Seite von Hand ändert, verliert die Änderung beim nächsten Lauf.** Quellen:

| Inhalt | Quelle |
|---|---|
| Untertitel, Werbetext, Beschreibung | `App Store/<CODE>/Docs/DESCRIPTION_<CODE>.md` der App |
| Bildschirmfotos (je Sprache) | `App Store/<CODE>/Screenshots/` der App |
| App-Liste, Einzeiler, Symbole, „Kostenlos“ | `_GeneralSystemKit/StoreApps.swift` + dessen Paketkatalog |
| Menü, Überschriften, Fußzeile | `_Shared/tools/website/texte.json` |

Von Hand und nur deutsch/englisch: `impressum.html`, `privacy.html`, `assets/style.css`, `assets/banner.jpg`.

## Marketing-URLs je Store-Sprache

| Store | Adresse (sCollect / sName2Date) |
|---|---|
| EN | `https://swiftappsbavaria.github.io/scollect/` · `…/sname2date/` |
| DE, ES, FR, IT, JA, KO, RU | `…/<sprache>/scollect/` — z. B. `…/de/scollect/` |
| PT-BR, PT-PT | `…/pt-br/…`, `…/pt-pt/…` |
| ZH-Hans, ZH-Hant | `…/zh-hans/…`, `…/zh-hant/…` |

## Regeln
- **Store-Link nur für LIVE-Apps** — das Skript nimmt ihn aus `StoreApps` (`.imStore(id:)`). Wird eine App
  live, dort umstellen und das Skript fahren. Die Links haben keine Länderkennung: Apple öffnet den Store
  des Besuchers.
- **„Oktober 2026“ ist eine datierte Zusage** (`texte.json` → `monat`), wie in `StoreApps`.
- **Kein Preis im Text.**
- ⚠️ `/scollect/` (diese Website) und `/sCollect/` (Datenschutz/Support, Repo `sCollect`) unterscheiden sich
  nur im Großbuchstaben.
