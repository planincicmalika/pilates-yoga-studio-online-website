# Yoga & Pilates nur für Frauen – Online-Website

Eine schlanke, rein statische One-Page-Website für ein Online-Yoga- und Pilates-Studio, das Kurse exklusiv für Frauen anbietet. Der Fokus liegt auf einem sanften Einstieg ohne Vorkenntnisse, Live-Kursen per Zoom sowie einer On-Demand-Videothek – alles bequem von zu Hause aus.

## Inhaltsverzeichnis

- [Features](#features)
- [Technologien](#technologien)
- [Projektstruktur](#projektstruktur)
- [Erste Schritte](#erste-schritte)
- [Lokale Entwicklung](#lokale-entwicklung)
- [SEO & Meta-Daten](#seo--meta-daten)
- [Accessibility (Barrierefreiheit)](#accessibility-barrierefreiheit)
- [Dokumentation](#dokumentation)
- [Roadmap](#roadmap)
- [Lizenz](#lizenz)

## Features

- **Responsive Design** – optimiert für Desktop und Mobilgeräte (Breakpoint ab 768 px).
- **Buchungsinteraktion** – Kurs-Slots im Kalender befüllen das Anmeldeformular automatisch vor.
- **Live-Konzept** – eigener Abschnitt für den "Kino-Modus" mit Live-Badges und Player-Platzhalter.
- **Kurs-Kalender** – wöchentlicher Live- und On-Demand-Stundenplan.
- **Mitgliedschaften** – zwei Angebote: kostenloses Probetraining und 10er-Karte.
- **Kontakt-/Anmeldeformular** – mit clientseitiger Validierung und Statusmeldung (aria-live).
- **SEO & Structured Data** – JSON-LD (Schema.org `Service`/`Offer`) für Rich-Results.
- **Barrierefreiheit** – Skip-Link, Fokus-Styles, `prefers-reduced-motion`-Support, semantische Struktur.

## Technologien

- HTML5
- Inline-CSS (CSS-Designsystem mit CSS-Variablen / Design-Tokens)
- Vanilla JavaScript (keine externen Abhängigkeiten)
- Keine Build-Tools oder Frameworks

## Projektstruktur

```
.
├── index.html              # Haupt-Landingpage (komplett in sich geschlossen)
├── index_mit_styles.html   # Alternativversion mit inlined Styles
├── assets/
│   └── banner.svg          # Header-Banner (Golden-Hour-Motiv)
├── docs/
│   └── style-guide.md      # Design-System & Markenrichtlinien
├── robots.txt              # Suchmaschinen-Crawling-Regeln
├── sitemap.xml             # Sitemap für Suchmaschinen
└── readme.md
```

## Erste Schritte

Das Projekt benötigt **keine Installation** und keine Abhängigkeiten. Du kannst die Website direkt im Browser öffnen.

**Option 1 – direkt öffnen**

```bash
open index.html   # macOS / Linux
start index.html  # Windows
```

**Option 2 – lokaler Webserver** (empfohlen, um `robots.txt` / `sitemap.xml` korrekt zu testen):

```bash
# Python 3
python -m http.server 8080
```

Anschließend im Browser zu `http://localhost:8080` navigieren.

## Lokale Entwicklung

1. Repository klonen:
   ```bash
   git clone https://github.com/planincicmalika/pilates-yoga-studio-online-website.git
   cd pilates-yoga-studio-online-website
   ```
2. `index.html` in einem Browser oder mit einem lokalen Server öffnen.
3. Änderungen an `index.html` vornehmen und im Browser prüfen (Liveserver/Task-Runner optional).

## SEO & Meta-Daten

Die Seite ist für Suchmaschinen optimiert:

- **Meta-Description** und **Open-Graph**-Tags für Social Sharing.
- **Canonical URL** – in `index.html` aktuell auf einen Platzhalter (`https://example.com/index.html`) gesetzt; vor dem Deploy auf die echte Domain ändern.
- **JSON-LD Structured Data** – `Service` mit `Offer`s (kostenloses Probetraining, 10er-Karte) für Rich Results in der Google-Suche.
- **`sitemap.xml`** und **`robots.txt`** – liegen im Projektroot bereit und müssen nach dem Deploy auf die echte Domain aktualisiert werden.

## Accessibility (Barrierefreiheit)

Die Seite erfüllt grundlegende WCAG-Praktiken:

- **Skip-Link** zum direkten Sprung zum Hauptinhalt.
- **Sichtbarer Fokus-Stil** über `:focus-visible`.
- **`prefers-reduced-motion`** – deaktiviert Animationen für Nutzer mit Reduzierung von Bewegung.
- **Semantisches HTML** – `header`, `main`, `section`, `footer`, korrekte Formular-Labels (`for`/`id`).
- **`aria-live`** Status für Formular-Rückmeldungen und `aria-describedby` im Formular.

## Dokumentation

Weitere Details zum Design-System (Farben, Typografie, Buttons, Komponenten) findest du in:

- [`docs/style-guide.md`](docs/style-guide.md)

## Roadmap

- [ ] Canvas-Canonical-URL und Deployment-Domain finalisieren.
- [ ] Echtes Backend/Formular-Endpunkt hinter dem Anmeldeformular anbinden.
- [ ] Integrierten Video-Player mit echtern Video-Stream.
- [ ] Mehrsprachigkeit (DE / EN).
- [ ] Newsletter-Anbindung und Bestell-/Zahlungs-Flow für die 10er-Karte.

## Lizenz

Alle Rechte vorbehalten. © 2026 Yoga & Pilates nur für Frauen.