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

## Deployment

Jeder Push auf `main` veröffentlicht den Ordner `site/` über GitHub Pages
(`.github/workflows/pages.yml`).

## Hinweis

Alle Beispielzahlen auf diesen Seiten sind frei erfunden und dienen der
Illustration. Die Produktinhalte selbst (Modultexte, Kennzahl-Seiten,
Berechnungs-Sheet) sind nicht Teil dieses Repositories.
