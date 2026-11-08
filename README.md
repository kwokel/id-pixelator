# Ausweis-Pixelator

Ausweis- oder DNI-Kopien feldweise verpixeln/schwärzen und mit Wasserzeichen versehen – **komplett im Browser, ohne Upload**.

Pixela o tacha campos de tu DNI o Personalausweis y añade una marca de agua – **todo en tu navegador, sin subir nada**.

## Warum man dem Tool vertrauen kann

- Keine Netzwerkaufrufe: Die Content-Security-Policy in `index.html` setzt `connect-src 'none'`. Der Browser blockiert damit jeden Versuch, Daten zu senden.
- Keine externen Skripte, Schriften, Cookies oder Tracker.
- Der gesamte Code steckt in `index.html` und ist hier öffentlich einsehbar.

## Dateien

| Datei | Zweck |
|---|---|
| `index.html` | Die komplette App (HTML, CSS, JS in einer Datei) |
| `sw.js` | Service Worker: macht die App offline verfügbar (speichert nur App-Dateien) |
| `manifest.webmanifest`, `icon*.png`, `icon.svg` | „Zum Home-Bildschirm hinzufügen“ / installierbar als App |
| `privacy.html` | Datenschutzerklärung (DE/ES) |
| `legal.html` | Impressum / Aviso legal (DE/ES) – **Platzhalter ausfüllen!** |

## Veröffentlichen mit GitHub Pages

1. Neues öffentliches Repository auf GitHub anlegen, z. B. `id-pixelator`.
2. Alle Dateien aus diesem Ordner hochladen (Web-Oberfläche: *Add file → Upload files*).
3. *Settings → Pages → Build and deployment*: Source **Deploy from a branch**, Branch **main**, Ordner **/ (root)** → *Save*.
4. Nach 1–2 Minuten ist die App unter https://kwokel.github.io/id-pixelator/ erreichbar.

### Updates

Nach Änderungen an `index.html` in `sw.js` die Zeile `const CACHE = 'ausweis-pixelator-v1';` hochzählen (v2, v3 …), damit installierte Versionen die neuen Dateien sicher übernehmen.

## Lokal nutzen

`index.html` einfach per Doppelklick öffnen – funktioniert auch ohne Server (dann ohne Offline-Cache, der ist dort aber auch nicht nötig).
