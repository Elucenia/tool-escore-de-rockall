<!-- ELUCENIA technical documentation · escore-de-rockall · de · no clinical/professional/rights approval -->

# Rockall-Score

[Bedingungen, Quellen und Berechtigungen](https://elucenia.org/de/werkzeuge/escore-de-rockall)

## Verwendung

Verwenden Sie das Werkzeug im Portal oder öffnen Sie index.html über einen lokalen HTTP-Server. Wählen Sie die Sprache, füllen Sie die Felder aus und berechnen Sie das Ergebnis.

## Eingaben und Einheiten

### Alter

`idade`

- `0` — \< 60 Jahre
- `1` — 60 bis 79 Jahre
- `2` — ≥ 80 Jahre

### Schock

`choque`

- `0` — Kein Schock (systolischer Blutdruck ≥ 100 und Herzfrequenz \< 100)
- `1` — Tachykardie (systolischer Blutdruck ≥ 100 und Herzfrequenz ≥ 100)
- `2` — Hypotonie (systolischer Blutdruck \< 100 mmHg)

### Begleiterkrankungen

`comorb`

- `0` — Keine wesentlichen
- `2` — Herzinsuffizienz, ischämische Herzkrankheit oder andere wesentliche Begleiterkrankung
- `3` — Niereninsuffizienz, Leberinsuffizienz oder disseminierter Krebs

### Endoskopische Diagnose

`diag`

- `0` — Mallory-Weiss oder keine Läsion (ohne Stigmata)
- `1` — Alle anderen Diagnosen
- `2` — Neoplasie des oberen Gastrointestinaltrakts
- `na` — Endoskopie noch nicht durchgeführt

### Stigmata einer kürzlichen Blutung

`estigma`

- `0` — Keine oder nur dunkler Fleck (Hämatin)
- `2` — Blut im oberen Gastrointestinaltrakt, anhaftendes Koagel, sichtbares Gefäß oder spritzende Blutung
- `na` — Endoskopie noch nicht durchgeführt

## Fassung der Methode

Rockall 1996: präendoskopisch 0–7 und vollständig 0–11; nicht mit GBS verwechseln

## Dokumentierte Formel

Präendoskopisch (0 bis 7): Alter (0 bis 2) + Schock (0 bis 2) + Komorbiditäten (0, 2 oder 3).

Vollständig (0 bis 11): zusätzlich Diagnose (0 bis 2) und Stigmata einer kürzlichen Blutung (0 oder 2).

## Grenzen und Population

Rockall von 1996 wurde bei Personen über 16 Jahren mit akuter oberer gastrointestinaler Blutung untersucht. Die vollständige Version hängt von Diagnose und endoskopischen Stigmata ab; die präendoskopische Version enthält diese Informationen nicht. Die Einteilung hilft bei der Versorgungserwägung, bestimmt aber weder individuelle Entlassungssicherheit noch das Ausbleiben einer Nachblutung.

## Referenzen

- [Rockall TA et al. Risk assessment after acute upper gastrointestinal haemorrhage. Gut, 1996.](https://doi.org/10.1136/gut.38.3.316)

- [Stanley AJ et al. Comparison of risk scoring systems for patients presenting with upper gastrointestinal bleeding: international multicentre prospective study. BMJ, 2017.](https://doi.org/10.1136/bmj.i6432)

## Technische Tests reproduzieren

Führen Sie node test.cjs im Stammverzeichnis dieses Repositorys aus, um die dokumentierten synthetischen Fälle zu wiederholen. Ursprüngliche Eingaben, erwartete Ergebnisse und Toleranzen bleiben erhalten. Technische Tests stellen keine klinische Validierung dar.

```sh
node test.cjs
```

tool.json enthält Quellen, Ausgabe und Umfang der Überprüfung. examples.json bewahrt die synthetischen Eingaben und erwarteten Ergebnisse; results.json dokumentiert die tatsächlich erhaltenen Ergebnisse.

[Eintrag und Referenzen](../tool.json) · [JavaScript-Code](../calculator.js) · [Referenzfälle](../examples.json) · [results.json](../results.json)

## Überprüfung und Nutzungsbedingungen

Eine unabhängige klinische Prüfung wurde nicht durchgeführt.

Diese Benutzeroberfläche ist eine selbst erstellte Übersetzung und keine offizielle oder zertifizierte Ausgabe. Eine unabhängige klinische Überprüfung, eine professionelle sprachliche Prüfung und eine Klärung der Rechte an den Instrumenten wurden nicht durchgeführt.

Ergebnis der Formel oder Klassifikation. Interpretation, Vorgehen und Anwendbarkeit hängen von der fachlichen Beurteilung und der ausgewählten Quelle ab.

## Lizenz und Urheberangaben

Apache-2.0 gilt nur für den ELUCENIA-Code. Die Rechte an Instrumenten, Veröffentlichungen, Übersetzungen und Daten verbleiben bei den jeweiligen Rechteinhabern. Bewahren Sie LICENSE und NOTICE auf.

ELUCENIA · Felipe Guedes · Copyright © 2026
