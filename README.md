# Fermenter-Konfigurator

**Stand:** 21.11.2026 (MEZ, Europe/Berlin) · **Für:** Volker Staffendt · **Erstellt von:** Anlagen-Designer · **Version:** 1.0.0

Offline-Werkzeug (eine HTML-Datei, three.js r158 eingebettet) zur **schematischen** Konfiguration stehender runder Biogasbehälter (Fermenter, Nachgärer, Gärrestlager). Es leitet ab, wie Substratmischung, Behältergeometrie und Erdeinbindung Folgendes bestimmen:

- Rührtechnik: Bauart, schematische Anzahl, Einbauort
- Sensorik: Art und Einbauort bzw. -höhe
- Substrat-, Gas- und Heizleitungen: Höhe und Durchführung
- Leckageerkennung: Leckagefolie nur unter der Sohle bzw. an der Wand hochgezogen, Kontrolldrainage, Grundwasser

Grundlage ist die schematische Fermenter-Stückliste vom 15.11.2026 (Projektunterlage, intern).

> **Keine Ausführungs-, Genehmigungs- oder Statikplanung.** Prozesswerte (Gasertrag, Volumina, Leistungen) liefert der Projektentwickler. Rührwerksleistungen bleiben offen. Das Werkzeug enthält **keine Preise**.

## Benutzung

`index.html` im Browser öffnen (Mac, Windows, iPhone Safari). Es braucht weder Internet noch Anmeldung. Der Arbeitsstand wird nur lokal in diesem Browser gespeichert (localStorage). Die Datei läuft offline; eine Bereitstellung über GitHub Pages ist für das iPhone komfortabler.

- **Eingaben:**
  - Substrate in Massen-% (10 Stoffe), optional ein TS-Override und der Fermenter-TS
  - Geometrie: Typ, D, H, Wandstärke, Dach (Tragluft-Doppelmembran oder Betondecke), Mittelstütze, max. Füllhöhe
  - Erdeinbindung: Tiefe, Grundwasser, höchster Grundwasserstand (HGW), Wasserschutzgebiet
  - Rührkonzept: automatisch oder manuell
- **Beispielfälle a/b/c** über Schaltflächen.
- **3-D:**
  - Schnitt- und Vollansicht umschaltbar.
  - Jede Ebene einzeln schaltbar: Gelände, Behälter, Dämmung/Verkleidung, Dach, Füllstand, Rührwerke, Sensoren, Leitungen, Leckagesystem.
  - Im 3-D-View steht nur die Infobox oben links; die Legende sitzt darunter.
- **Ausgaben:**
  - Ergebnisliste bzw. Stückliste mit Regel-ID, Quellen und Status
  - Warnhinweise und offene Punkte
  - Regelwerkstabelle, in der die angewendeten Regeln markiert sind
  - Substrat-Referenzwerte und Quellen
- **Export:**
  - CSV (UTF-8 mit BOM, Trenner `;`, Dezimalkomma)
  - Projekt-JSON zum Speichern und Laden
  - Druckansicht A4 mit 3-D-Bild

## Dateien

| Pfad | Inhalt |
|---|---|
| `index.html` | Fertiges Werkzeug als Einzeldatei |
| `regeln.md` | Regelwerk mit Begründung und Quellen |
| `vorschau.png` | Vorschau (Fall b, Schnittansicht) |
| `.nojekyll` | Schaltet die Jekyll-Verarbeitung auf GitHub Pages ab |

## Wichtigste Regeln (Kurzfassung, Details in `regeln.md`)

- **Rührtechnik:** Die Anforderungsklasse ist die höhere von Input-Misch-TS-Klasse und Faserindex-Klasse. Die Klassengrenzen sind Annahmen.
  - niedrig: Tauchmotorrührwerke
  - mittel: Langachs + Tauchmotor
  - hoch: Paddel + Langachs + Tauchmotor (FNR Leitfaden Biogas, Tab. 3.22–3.25)
  - Ein Paddelrührwerk ist nur zulässig, wenn seine Wellenachse mindestens 0,5 m über GOK liegt. Sonst wird es durch ein Langachsrührwerk von der Krone ersetzt.
  - Langachs-Antriebe werden auf die Kronenbühne bzw. Decke gesetzt, wenn die Durchführung nicht über GOK liegt.
- **Sensorik:**
  - Bei eingebundenem Behälter wird der Füllstand berührungslos von oben gemessen; hydrostatisch seitlich nur bei oberirdischem Behälter.
  - Temperaturfühler unter GOK sitzen in Tauchrohren von oben.
  - Eine Überfüllsicherung ist immer vorgesehen.
- **Leitungen:**
  - Der Gasabgang liegt immer oben.
  - Liegen Stutzen unter GOK, werden die Leitungen über den Kronenbereich geführt (Zulauf mit Tauchrohr, Entnahme als Saugleitung). Alternative: Wanddurchführung mit Mantelrohr und Kontrolleinrichtung.
- **Leckagefolie:**
  - Ein LES ist immer nötig (AwSV § 37 Abs. 2).
  - Einbindung bis 1,30 m: einteiliges System, Folie hochgeschlagen bis ca. 30 cm über GOK.
  - Einbindung über 1,30 m: zusätzlich Wandbahn (max. 6 m je Lage) bis ca. 30 cm über GOK.
  - Vollständig eingebunden: Befestigung mindestens 10 cm über der max. Füllhöhe.
  - Diese Werte stammen aus der Systemzulassung **DIBt Z-59.26-470**. Für andere Systeme gilt deren Zulassung, daher projektspezifisch prüfen.
  - DWA-A 793-1 verlangt laut Vortrag Niehage (Entwurfsstand), dass die Folie „die gesamte Behältersäule bis GOK“ erfasst.
- **Grundwasser:**
  - Der LES-Tiefpunkt muss mindestens 50 cm über HGW liegen (systembezogen).
  - Liegt die Bodenplattenunterkante unter HGW oder steht der Behälter im Schutzgebiet, ist er doppelwandig mit Leckanzeigesystem auszuführen (AwSV § 37 Abs. 5).

## Offene Punkte

- Volltext DWA-A 793-1 (März 2021, korr. Sept. 2021) beschaffen und die Regeln L3–L13 damit abgleichen
- LES-System auswählen und die Werte aus dessen Zulassung übernehmen
- Anzahl der Kontrollschächte mit der unteren Wasserbehörde klären
- HGW und Baugrund klären
- Rührwerksauslegung durch den Hersteller (Leistung, Anzahl)
- Prozesswerte und max. Füllhöhe vom Projektentwickler
- Statik: Auftrieb, Rührwerkslasten, Durchführungen
- Ex-Zonen

## Hinweis

Technische Ersteinschätzung, keine verbindliche Planungs-, Hersteller- oder Preisauskunft. Vorgesehen für GitHub Pages wie die anderen Konfiguratoren; bis zur Freigabe lokal als `index.html` öffnen.
