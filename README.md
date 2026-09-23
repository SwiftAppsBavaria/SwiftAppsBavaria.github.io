# SwiftAppsBavaria.github.io — ENTWURF (2026-09-23)

Familienseite der Mac-Apps; gedacht als **Marketing-URL** in App Store Connect
(`https://swiftappsbavaria.github.io/scollect/`, `…/sname2date/`). Noch **nicht** auf GitHub.

## Aufbau
- `index.html` — alle Apps, Reihenfolge und Texte wie `_GeneralSystemKit/StoreApps.swift` (englisch)
- `scollect/`, `sname2date/` — je eine App-Seite: Untertitel, Werbetext, sechs Punkte aus der
  Store-Beschreibung, zwei Bildschirmfotos, Anforderungen, „More apps“
- `impressum.html`, `privacy.html` — **Platzhalter, vor Veröffentlichung ausfüllen und prüfen lassen**
- `assets/` — `style.css` (keine Webfonts, kein JavaScript, nichts von außen), Symbole aus
  `_GeneralSystemKit/Resources` (128 px, gerendert), Banner, Bildschirmfotos (JPEG aus `App Store/EN/Screenshots`)

## Regeln
- **Store-Link nur für LIVE-Apps.** Prüfen: `curl -s "https://itunes.apple.com/lookup?id=<ID>&country=de"`.
  Wird sCollect oder sName2Date live: Badge durch Link ersetzen, auf Start- und App-Seiten.
- **Texte kommen aus den Store-Dateien** (`App Store/EN/Docs/DESCRIPTION_EN.md`) — wer dort ändert, zieht hier nach.
- **Kein Preis im Text** (ändert sich ohne Review); „Free“ nur für Lite-Ausgaben, wie in `StoreApps`.
- **„October 2026“ ist eine datierte Zusage** — sie steht hier so wie in `StoreApps`; verstreicht der Monat, beide nachziehen.

## Offen vor dem Veröffentlichen
1. ✅ Impressum: Anschrift eingetragen (2026-09-23). Impressum und Website-Datenschutz vor dem Freischalten prüfen lassen.
2. Repo `SwiftAppsBavaria/SwiftAppsBavaria.github.io` anlegen, pushen, Pages einschalten
   (Settings → Pages → Branch `main`, Ordner `/`).
3. Auf den App-Seiten die Links zu Support und Datenschutz ergänzen, sobald die `*-privacy`-Repos
   Pages eingeschaltet haben (derzeit bei keinem Repo der Familie).
