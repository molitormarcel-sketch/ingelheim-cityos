# INGELHEIM // CITYOS — Modul 01

Interaktive, mobile 2.5D-Stadtkarte für Ingelheim am Rhein (React + Vite + MapLibre GL). **Inoffizielles Konzept, kein Angebot der Stadtverwaltung.**

## Loslegen

```bash
npm install
npm run dev
```

## GitHub + Netlify

1. Dateien in ein neues GitHub-Repository hochladen (oder lokal `git init`, `git add .`, `git commit`, `git push`).
2. Bei Netlify **Add new project → Import an existing project → GitHub**.
3. Repository auswählen. Build-Befehl `npm run build`, Veröffentlichungsordner `dist` (bereits in `netlify.toml`).
4. Deployment starten. Bei jedem Push wird die Website aktualisiert.

## Funktionen

- Matrix / Straße / Satellit; echte OpenStreetMap-Vektordaten via OpenFreeMap, Satellitenkacheln via Esri World Imagery.
- 3D-Gebäude als extrudierte OSM-Grundrisse, wo vorhanden; unvollständige Höhenangaben sind möglich.
- Orte-Suche aus einer kuratierten POI-Liste sowie freie Adresseingabe über OpenStreetMap Nominatim (nur nach explizitem Suchklick).
- Klickbare Ortsmarker, Kartenrotation, Zoom, Nordausrichtung, GPS-Ortung mit Browsererlaubnis, QR-/Share-Link.
- Responsive Bedienung, reduzierte Animation bei `prefers-reduced-motion`.

## Externe Dienste & Datenschutz

Die Karten laden Daten von `tiles.openfreemap.org` (OpenFreeMap), Satellitenbilder von `server.arcgisonline.com` und Suchergebnisse von `nominatim.openstreetmap.org`. Beim Abruf gehen übliche technische Verbindungsdaten an die Dienste. Standortdaten werden nur auf ausdrückliche Nutzeraktion vom Browser angefordert und nicht an einen eigenen Server übertragen; es erfolgt keine Nutzerverwaltung. Für einen öffentlichen Betrieb müssen die Datenschutztexte, Karten- und Bildlizenzen und das Nutzungsvolumen geprüft werden. OSM-Daten © OpenStreetMap-Mitwirkende, ODbL; OpenFreeMap und Esri haben eigene Nutzungsbedingungen. Nominatim-Suche nur mit Benutzeraktion (kein Autocomplete), geringe Nutzungshäufigkeit; bei stärkerem Traffic ist ein eigener oder vertraglich zugelassener Geocoding-Dienst erforderlich.