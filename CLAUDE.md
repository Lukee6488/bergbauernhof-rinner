# Bergbauernhof Rinner – Website Projekt

## Projektübersicht
Redesign der Website für den Bergbauernhof Rinner in Riezlern / Kleinwalsertal (Österreich).
Ursprüngliche Website: bergbauernhof-rinner.de (Jimdo-Basis, gecrawlt und neu aufgebaut).

## Technologie
- Reines HTML/CSS (kein Framework, kein Build-Tool)
- Hosting: **Vercel** (via GitHub-Integration)
- Repository: https://github.com/Lukee6488/bergbauernhof-rinner
- GitHub-Account: Lukee6488

## Git-Konfiguration – WICHTIG
Commits müssen immer mit diesem Account gemacht werden, damit Vercel den GitHub-User erkennt:
- **Name:** `Lukee6488`
- **E-Mail:** `lukasruschepaul@gmail.com`

Lokale Repo-Konfiguration prüfen/setzen:
```bash
git config user.name "Lukee6488"
git config user.email "lukasruschepaul@gmail.com"
```

## Vercel-Workflow – WICHTIG
**Nach jeder Änderung muss `git push` gemacht werden**, damit Vercel automatisch deployed.

```bash
cd "C:\Users\lukas\Desktop\Arbeit\rinner_website"
git add .
git commit -m "Beschreibung der Änderung"
git push
```

Vercel erkennt den Push auf `master` und deployed automatisch innerhalb von ~30 Sekunden.

## Dateistruktur
```
rinner_website/
├── index.html          # Startseite
├── ueber-uns.html      # Über uns
├── zimmer.html         # Zimmerübersicht
├── zimmer-2.html       # Zimmer 2
├── zimmer-3.html       # Zimmer 3
├── zimmer-5.html       # Zimmer 5
├── zimmer-6.html       # Zimmer 6
├── ferienwohnung-a.html
├── ferienwohnung-b.html
├── impressum.html
├── style.css           # Globales Stylesheet
└── bilder/
    ├── logo.png        # Aktuelles Logo (Kuh-Illustration, removebg)
    ├── header.png      # Altes Logo (nicht mehr verwendet)
    └── ...             # Weitere Bilder
```

## Logo
- **Neu:** `bilder/logo.png` — Bergbauernhof-Logo mit Kuh-Illustration, freigestellter Hintergrund (via remove.bg)
- Das Logo wird überall im `<nav>` und im `<footer>` verwendet (CSS-Klassen: `.logo-img`, `.footer-logo`)
- Quelle: `header-removebg-preview.png` aus Downloads

## Kontaktdaten Bauernhof
- Familie Rinner, Außerschwende 46, A-6991 Riezlern / D-87567 Riezlern
- Kleinwalsertal, Österreich

## Vercel Setup (einmalig)
1. vercel.com → "Import Git Repository" → `Lukee6488/bergbauernhof-rinner`
2. Framework: Other (statische HTML-Seiten)
3. Root Directory: `/` (kein Build nötig)
4. Deploy klicken → fertig
