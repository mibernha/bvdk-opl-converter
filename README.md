# BVDK Scoreboard → OpenPowerlifting

Statisches Ein-Datei-Tool, das Ergebnisse von `scoreboard.vportal-online.de` (BVDK)
in das Format des [OpenPowerlifting-Projekts](https://gitlab.com/openpowerlifting/opl-data)
umwandelt (`meet.csv`, `entries.csv`, `URL`) und auf Wunsch direkt einen
Merge Request gegen `openpowerlifting/opl-data` erstellt.

## Nutzung

1. Scoreboard-Eventseite laden (URL-Abruf, gespeicherte HTML-Datei oder Quelltext einfügen)
2. Ort/Bundesland ergänzen, Vorschau prüfen (Fehlversuche = rot/negativ, Gäste = G)
3. Dateien herunterladen **oder** mit GitLab-Token (Scope `api`) den MR automatisch erstellen

Alles läuft im Browser; es werden keine Daten an Dritte gesendet
(außer an gitlab.com beim Erstellen des MR und optional an den CORS-Proxy beim URL-Abruf).

## Hinweise

- Team-Wertungen (`teamBoard`) werden noch nicht unterstützt
- Geburtsjahre stehen nicht im Scoreboard; optional aus der passenden
  `bvdk.de/wettkaempfe/results/…`-Seite zusammenführbar (experimentell)
