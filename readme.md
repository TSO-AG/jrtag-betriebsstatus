# Betriebsstand

## Beschreibung
Exportiere mir alle 'tenants' mit den Informatonen von lifts, slopes, trails und gastro als einzelne Feeds/Ausgaben.
Diese sollen alle 5min abgerufen und aktulaisiert werden.
Es soll mehere Ausgaben geben für "Formate" die unter ## Ausgabe / Funktion aufgelistet sind. 
Diese Formate sollen unter /api/xy für JSON und RSS oder als HTML unter /operating-status/xy oder als einbindbares Javascript unter /js/xy für andere Webseiten vorhanden sein.

## Daten Quelle
https://export.siscontrol.ch/sismedia/json/B1463C13-F6D8-4270-8C0B-0CFF9E135E62

## Ausgaben / Funktionen
* Ausgabe als JSON im folgenden Format wie in example/output/outputJSON.json
```json
{ "version": "https://jsonfeed.org/version/1", "title": "RSS Feed Kleine Scheidegg", "description": "Alle Stories für Kleine Scheidegg", "items": [ { "id": "123", "title": "Tschuggen Talabfahrt", "url": "https://demo.tourismusweb.site/preview.php/de/index/tschuggen-talabfahrt-123.html", "date_published": "2026-03-29T17:08:58+02:00", "_state": "offen", "_stateRaw": "open", "_tags": "Piste" } ] }
```
* Ausgabe als RSS-Feed Version 2 im Format wie in example/output/example.rss
* Ausgabe als HTML mit gleicher Darstellung wie bei https://demo.tourismusweb.site/de/entdecken/aktuelles/betriebszustaende.html?page_ot52048=2 unter Bergbahnen.
* Ausgabe einbindbares Javascript auf fremden Webseiten mit Best Practices-Methoden für das einbinden von Javascript

## Technisches mit vibecode

* Github Pages mit Github Action
* Alle 5min aktualisiert

## Lösungen prüfen mit 
* n8n
* make
* vibecode (github copilot)