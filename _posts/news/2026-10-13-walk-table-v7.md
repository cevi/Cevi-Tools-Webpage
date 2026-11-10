---
layout: post
title: "Marschzeittabellen-Generator 7.0: neuer Routeneditor und mehr Kartenebenen"
date: 2026-10-13 12:00:00 +0200
categories: release
authors:
  - github@wp99cp JPG
  - github@maede97 Scirocco
---

![J+S-Marschzeittabellen Banner](https://github.com/cevi/automatic_walk-time_tables/raw/master/docs/imgs/Claim.png)

<br/>

Die Version 7 des [J+S-Marschzeittabellen-Generators](https://map.cevi.tools) ist da. Der Routeneditor wurde
überarbeitet, die Karte zeigt zusätzliche Ebenen und die Marschzeittabelle hat ein neues Design.

<br/>
[Zum Marschzeittabellen-Generator](https://map.cevi.tools)

## Neue Features

### Routeneditor
- Schwebendes Werkzeugmenü direkt auf der Karte
- Punkte rasten auf Wegen ein und können verschoben oder gelöscht werden
- Änderungen lassen sich rückgängig machen

<br/>
### Wegpunkte
- Wegpunkte werden automatisch benannt
- Vor dem Export können Wegpunkte umbenannt und mit Pausen versehen werden
- Gebäude, Schulen, Sportanlagen, Staumauern, Höhenkoten und Wegkreuzungen werden für die Namen berücksichtigt

<br/>
### Kartenebenen
- ÖV-Haltestellen, Brunnen, SAC-Hütten, Brätlistellen und Schutzgebiete
- Schwarz-weisse Basiskarte
- Info-Popups für ÖV-Haltestellen und Brunnen
- Ein Rechtsklick zeigt die Koordinaten an
- Ortssuche

<br/>
### Marschzeittabelle und Export
- Neu gestaltete Marschzeittabelle und Vorschautabelle
- Der Kartenexport nutzt die native Kachelauflösung von 508 dpi
- Der QR-Code im PDF ist anklickbar
- Eine Route kann höchstens 21 Wegpunkte enthalten

<br/>
### Statistikseite
- Neue Seite mit Statistiken zum Generator

<br/>
## Verbesserungen

- Das Routing berücksichtigt Brücken und Tunnel
- Importierte Routen: KML-Dateien mit Höhe null erhalten Höhendaten, alle KML-Liniengeometrien und GPX-Dateien ohne Höhenangaben werden unterstützt
- Die automatische Wahl des Kartenmassstabs funktioniert wieder
- Sonderzeichen in Wegpunktnamen werden korrekt exportiert
- Sicherheitskorrekturen: Routen-IDs und Dateinamen werden geprüft

<br/>

Das vollständige Changelog findest du in der [Dokumentation](https://docs.map.cevi.tools/changelog/changelog.html), den
Quellcode unter [cevi/automatic_walk-time_tables](https://github.com/cevi/automatic_walk-time_tables). Fehler und Wünsche
kannst du als [Issue auf GitHub](https://github.com/cevi/automatic_walk-time_tables/issues) melden.
