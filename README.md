# BVDK Scoreboard → OpenPowerlifting

Statisches Ein-Datei-Tool, das Ergebnisseiten von `scoreboard.vportal-online.de` (BVDK)
in das Format des [OpenPowerlifting-Projekts](https://gitlab.com/openpowerlifting/opl-data)
umwandelt (`meet.csv`, `entries.csv`, `URL`) und auf Wunsch direkt einen
Merge Request gegen `openpowerlifting/opl-data` erstellt.

## Nutzung

1. Scoreboard-Eventseite im Browser öffnen → `Strg+S` („Webseite, nur HTML“) → Datei im Tool ablegen
   (alternativ Quelltext per `Strg+U` kopieren und einfügen)
2. Ort/Bundesland ergänzen, Vorschau prüfen (nach Gewichtsklassen gruppiert,
   Fehlversuche rot/negativ, Gäste = G)
3. Dateien/ZIP herunterladen **oder** mit GitLab-Token (Scope `api`) den MR automatisch erstellen –
   eine Schritt-für-Schritt-Anleitung zum Token ist im Tool enthalten

Alles läuft im Browser; Daten verlassen die Seite nur beim Erstellen des MR (gitlab.com).

## Grenzen

- Team-Wertungen (`teamBoard`) werden noch nicht unterstützt
- Geburtsjahre stehen nicht im Scoreboard – die Spalten BirthDate/BirthYear sind vorhanden, bleiben aber leer
