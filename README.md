# Bot-Betrieb — Landingpage & Kennzahl-Rechner

Zweisprachige Website (DE/EN) für «Bot-Betrieb», ein Praxis-Framework für den
Aufbau, die Messung und den Betrieb von Support-Bots.

## Inhalt

| Datei | Zweck |
|-------|-------|
| `site/index.html` | Landingpage DE |
| `site/index-en.html` | Landingpage EN |
| `site/rechner.html` | Kennzahl-Rechner DE — die 10 Kennzahlen, live gerechnet |
| `site/calculator.html` | KPI calculator EN |

Alle Seiten sind self-contained: kein Build, kein Framework, keine Abhängigkeiten
ausser Google Fonts. Lokal ansehen heisst, eine der Dateien im Browser zu öffnen.

Der Rechner speichert Eingaben ausschliesslich im `localStorage` des Browsers.
Es werden keine Daten übertragen, es gibt kein Tracking und keine Cookies.

## GerüstPlaner (erste Version)

Unter `site/geruest/` liegt eine eigenständige Web-App: Gebäude fotografieren,
vier Fassadenecken antippen, reale Masse eingeben — das Gerüst wird perspektivisch
ins Foto gelegt und eine Materialliste gerechnet.

| Datei | Zweck |
|-------|-------|
| `site/geruest/index.html` | App (Kamera, Fassaden-Markierung, Gerüst-Overlay, Materialliste) |
| `site/geruest/manifest.webmanifest` | Web-App-Manifest («Zum Startbildschirm hinzufügen») |
| `site/geruest/icon.svg` | App-Icon |

Funktionen v0.1:

- Foto per Kamera (`getUserMedia`, Rückkamera) oder aus der Galerie; Demo-Gebäude zum Ausprobieren.
- Fassade über vier Eckpunkte markieren, Punkte nachträglich verschiebbar; Perspektive über Homographie.
- Gerüstarten: Rahmengerüst, Modulgerüst, Rohr-Kupplungsgerüst; Feldlänge, Breitenklasse W06/W09, Belag alle Lagen oder nur Arbeitslage.
- Overlay mit Stielen, Riegeln, Belägen, Geländer, Bordbrettern, Diagonalen (jedes 5. Feld), Leitergang und Ankern.
- Materialliste mit Stückzahlen und Richtgewichten, Kennzahlen (Felder × Lagen, Gerüstfläche, Anker, Gewicht); Export als PNG, Text-Kopie oder Druck/PDF.
- Alles läuft im Browser, Foto und Eingaben bleiben im `localStorage`.

Die Mengen sind Richtwerte nach Regelausführung (EN 12811 / DIN 4420, Lastklasse 3) und
ersetzen keine Statik. Die Kamera-API setzt HTTPS voraus — über GitHub Pages gegeben.

## Deployment

Jeder Push auf `main` veröffentlicht den Ordner `site/` über GitHub Pages
(`.github/workflows/pages.yml`).

## Hinweis

Alle Beispielzahlen auf diesen Seiten sind frei erfunden und dienen der
Illustration. Die Produktinhalte selbst (Modultexte, Kennzahl-Seiten,
Berechnungs-Sheet) sind nicht Teil dieses Repositories.
