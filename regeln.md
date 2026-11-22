# Regelwerk Fermenter-Konfigurator

**Stand:** 21.11.2026 (Quellen abgerufen am 21.11.2026), MEZ (Europe/Berlin)  
**Für:** Volker Staffendt · **Erstellt von:** Anlagen-Designer  
**Geltung:** schematische Vorplanung stehender runder Biogasbehälter (Fermenter, Nachgärer, Gärrestlager). **Keine Ausführungs-, Genehmigungs- oder Statikplanung.** Keine Prozesswerte (Gasertrag, Volumina, Leistungen) und keine Preise. Rührwerksleistungen bleiben offen.

Status-Begriffe: **Rechtsnorm/Quelle** = belegt; **systembezogen** = Wert aus der Zulassung eines bestimmten Leckageerkennungssystems (DIBt Z-59.26-470), für andere Systeme gilt deren Zulassung; **Entwurfsstand – prüfen** = Sekundärquelle zum Regelwerksentwurf, Endfassung DWA-A 793-1 nicht eingesehen; **Annahme** = eigene schematische Festlegung ohne Quelle.

## Kernaussage Leckagefolie / Hochzug

| Einbindung (Sohle-OK unter GOK) | Ausführung der Dichtungsbahn | Quelle |
|---|---|---|
| 0 m (oberirdisch, flacher Boden vollflächig aufgestellt) | LES trotzdem erforderlich (einwandig, flüssige wassergefährdende Stoffe). Bodendichtungsbahn unter der Sohle, am Sohlrand/Wandfuß hochgeschlagen bis ca. 30 cm über OK Gelände. | AwSV § 37 Abs. 2, § 2 Abs. 15; Z-59.26-470 Abschn. 3.1 (15), 3.2.3 (17) (systembezogen) |
| > 0 bis ≤ 1,30 m | Einteiliges System: Bodendichtungsbahn an der Wand hochgeschlagen bis ca. 30 cm über OK Gelände; gilt als unterirdische Anlage. | Z-59.26-470 Abschn. 3.1 (14), (15), 3.2.3 (17); AwSV § 2 Abs. 15 |
| > 1,30 m | Zweiteiliges System: Boden- + Wanddichtungsbahn (Y-Anschluss), je Wandbahnlage max. 6 m, darüber zweite Lage; bis ca. 30 cm über OK Gelände. | Z-59.26-470 Abschn. 3.1 (16), 3.2.3 (14), (17) |
| vollständig eingebunden (Krone ≤ GOK) | Befestigungspunkt ≥ 10 cm über max. zulässiger Füllhöhe; Kontrollschächte nicht überfahrbar, tagwasserdicht. | Z-59.26-470 Abschn. 3.1 (17), 3.2.3 (18); Beispielauflage LK Ludwigslust-Parchim 2024 |
| allgemein | Dichtungsbahn muss die gesamte (erdberührte) Behältersäule bis GOK erfassen, niederschlagswasserdicht befestigt; ≥ 1,5 mm vor Ort bzw. ≥ 1,0 mm vorkonfektioniert. | DWA-A 793-1 lt. Vortrag Niehage (Entwurfsstand) – Endfassung prüfen |
| Grundwasser | LES-Tiefpunkt ≥ 50 cm über höchstem Grundwasserstand (systembezogen). Liegt die Bodenplattenunterkante eines unterirdischen Behälters unter dem höchsten Grundwasserstand oder im Schutzgebiet → doppelwandig mit Leckanzeigesystem. | Z-59.26-470 Abschn. 3.1 (10); AwSV § 37 Abs. 5 |
| Kontrolldrainage | Dränschicht, Drain-Ringleitung DN 100, Gefälle ≥ 0,5 % zum Kontrollschacht; mind. 2 Kontrollschächte, je Schacht eine Leckagesonde; Behörde kann mehr fordern (Beispiel 4 bei D > 20 m). | Z-59.26-470 Abschn. 3.1 (4), (9), (13); NRW 2009; LK Ludwigslust-Parchim 2024 |

**Nicht belegt / projektspezifisch:** Ein allgemeingültiger Grenzwert der Einbindetiefe in AwSV oder TRwS, ab dem die Folie an der Wand hochgeführt werden muss, wurde nicht gefunden. Die 1,30 m und 30 cm stammen aus einer Systemzulassung. Der Volltext DWA-A 793-1 (März 2021, korr. Sept. 2021) ist kostenpflichtig und wurde nicht eingesehen.

## Regeln

| ID | Bereich | Regel | Begründung | Quellen | Status |
|---|---|---|---|---|---|
| S1 | Substrat | Input-Misch-TS = Σ(Massenanteil × TS-Referenzwert) / Σ Massenanteile; manueller TS-Override ersetzt den Rechenwert. | Gewichtetes Mittel der Frischmasse. Referenzwerte sind Literatur-Mittelwerte, Analysewerte des Betriebs haben Vorrang. | Q12, Q13, Q14, Q15 | Rechenregel, Referenzwerte mit Quelle |
| S2 | Substrat | TS-Klasse der Inputmischung: < 15 % niedrig, 15–25 % mittel, > 25 % hoch. | Grobe Einstufung des Rühraufwands. Die Klassengrenzen sind KEINE Normwerte; sie lassen sich im Projekt-JSON anpassen. | A | Annahme – projektspezifisch prüfen |
| S3 | Substrat | Faser-/Schwimmschichtindex = gewichteter Mittelwert der Faserfaktoren (0 = gering … 3 = hoch); < 1,0 niedrig, 1,0–1,8 mittel, > 1,8 hoch. | FNR nennt Gras, Festmist, strohreichen Mist und Einstreu/Fasern als hydraulisch herausfordernd (Verstopfungen, Sink- und Schwimmschichten). Faktoren und Grenzen sind eigene Einstufung. | Q12, A | Annahme mit fachlichem Bezug |
| S4 | Substrat | Fermenter-TS (optional, vom Projektentwickler): > 12 % Hinweis Grenze Nassvergärung, > 15 % Warnung Pumpfähigkeit. | FNR: Nassvergärung bis ca. 12 % TS im Fermenter, Faustregel 15 % für Pumpfähigkeit (qualitativ). | Q12 | Quelle (qualitativ) |
| S5 | Substrat | Anteil sinkschichtfördernder Substrate (Schweinegülle, HTK, Zuckerrübe, Bioabfall) ≥ 25 % → Hinweis Sedimentaustrag/Bodenräumung. | FNR: Schweinegülle und Hühnerkot fördern Sinkschichten; Bioabfall hat Störstoffpotenzial. Grenzwert 25 % = Annahme. | Q12, A | Annahme mit fachlichem Bezug |
| R1 | Rührtechnik | Anforderungsklasse = höhere von TS-Klasse und Faserklasse. | Beide Größen erhöhen Viskosität bzw. Schwimmschichtneigung. | Q12, A | Annahme |
| R2 | Rührtechnik | Klasse niedrig: Tauchmotor-Propellerrührwerke (TMR) an Führungsmast mit Hubwinde. | FNR Tab. 3.22: TMR für alle Substrate der Nassvergärung in stehenden Fermentern, turbulente Strömung, Schwimmdecken-Zerstörung; nicht für extrem hohe Viskositäten. | Q12 | Quelle |
| R3 | Rührtechnik | Klasse mittel: Kombination Stab-/Langachsrührwerk(e) mit außenliegendem Antrieb + TMR. | FNR Tab. 3.23: Langachsrührwerke sehr gute Durchmischung, Antrieb außen wartungsfreundlich; bei stationärer Installation Bereiche mit Schwimmschichten möglich → bewegliches TMR ergänzt. | Q12 | Quelle + Annahme (Kombination) |
| R4 | Rührtechnik | Klasse hoch: ein Paddel-/Haspelrührwerk mit horizontaler Welle + schubbasierte Begleitrührwerke (Langachs/TMR). Propeller-TMR allein nicht empfohlen. | FNR Tab. 3.25: Paddelrührwerke besonders für TS-reiche Substrate; in stehenden Rührkesselfermentern Strömung durch schubbasierte Begleitrührwerke. Tab. 3.22: Propeller-TMR bei TS-reichen Substraten Kavernenbildung möglich. | Q12, Q16 | Quelle |
| R5 | Rührtechnik | Gärrestlager: bevorzugt TMR; bei Faserklasse hoch zusätzlich ein Langachsrührwerk. | Kompost & Biogas Verband: Propellerrührwerke im Endlager weiterhin die beste Wahl. | Q16, A | Quelle + Annahme |
| R6 | Rührtechnik | Anzahl schematisch: n = gerundet(D / 8 m), mindestens 2, höchstens 6; Klasse hoch +1. | Stückliste nennt 2–4 Rührwerke je Fermenter „je nach Auslegung“; FNR: in großen Fermentern mehrere Rührwerke. Die Formel ist eine Platzhalter-Annahme, die Auslegung macht der Hersteller. | Q17, Q12, A | Annahme – Hersteller-/Projektentwickler-Auslegung |
| R7 | Rührtechnik | Rührwerksleistungen werden nicht festgelegt (offen). | Keine projektbezogene Quelle; FNR nennt nur verfügbare Leistungsbereiche, keine Auslegung. | Q12 | offen |
| R8 | Rührtechnik / Einbindung | Langachsrührwerk: Wellendurchführung im oberen Wandbereich oberhalb max. Füllstand (Tragluftdach) bzw. durch die Decke (Betondecke). Liegt die Durchführung weniger als 0,5 m über GOK → Antrieb auf Kronenbühne/Decke, Durchführung im Kronenbereich. | FNR: Durchführung durch Fermenterdecke oder bei Foliendächern im oberen Wandbereich, gasdicht; Kompost & Biogas: oberhalb max. Flüssigkeitsstand. 0,5-m-Marge = Annahme für Zugänglichkeit. | Q12, Q16, A | Quelle + Annahme |
| R9 | Rührtechnik / Einbindung | Paddelrührwerk (horizontale Welle, Antrieb außen an der Wand, Durchführung unter dem Flüssigkeitsspiegel): nur wenn die Wellenachse ≥ 0,5 m über GOK liegt. Sonst nicht zugänglich → Ersatz durch Langachsrührwerk (Großflügel) von der Krone oder begehbarer Antriebsschacht (projektspezifisch). | Wanddurchführungen unterhalb des Flüssigkeitsspiegels müssen kontrollierbar sein (TRwS 792 Abschn. 6.6 Abs. 13 lt. SGD RLP); unter GOK sind Antrieb und Wellendichtung nicht wartbar. Achshöhe 0,45 × max. Füllhöhe = Modellannahme. | Q12, Q8, A | Quelle + Annahme |
| R10 | Rührtechnik / Einbindung | TMR: Führungsmast Sohle bis Krone, Hubwinde und Kabeleinführung im Kronenbereich, Service-/Montageöffnung oben; unabhängig von der Einbindung. | FNR Tab. 3.22: Führungsrohre durch Decke gasdicht, Wartung erfordert Öffnung, meist ohne Entleeren bei Winde. | Q12, Q17 | Quelle |
| R11 | Zugang | Kronenhöhe über GOK > 1,0 m → Kronenbühne mit Treppe; sonst Zugang vom Gelände/Podest. Absturzsicherung und Überfahrschutz projektspezifisch. | Antriebe, Winden, Füllstands- und Drucksensoren sitzen im Kronenbereich. Schwelle 1,0 m = Annahme. | Q17, A | Annahme |
| M1 | Sensorik | Füllstand kontinuierlich: oberirdisch (Einbindung 0) hydrostatisch am unteren Wandstutzen mit Absperrung ODER Radar; eingebunden → berührungslos (Radar) von oben über Stutzen oberhalb max. Füllstand bzw. Decke, alternativ hydrostatische Tauchsonde von oben. | Der untere Wandstutzen läge unter GOK und wäre nicht zugänglich; jede zusätzliche Durchdringung unter GOK muss kontrollierbar sein und ins LES eingebunden werden. | Q8, Q17, A | fachliche Ableitung |
| M2 | Sensorik | Überfüllsicherung / unabhängiger Max-Grenzwert immer, von oben im Kronenbereich, Alarm auf Meldekette. | TRwS 793-1 (lt. Vortrag Niehage): Überfüllsicherungen, Füllstandsanzeiger, Alarmgebung auf Meldekette. | Q5, Q6 | Quelle (Entwurfsstand) – Endfassung prüfen |
| M3 | Sensorik | Temperatur: Messstellen in 3 Höhen (0,2 / 0,5 / 0,8 × max. Füllhöhe), bei D > 20 m in 2 Messachsen. Je Messstelle: ≥ 0,5 m über GOK → Tauchhülse seitlich; sonst Fühler von oben in Tauchrohr/Messlanze. | Stückliste: 3–6 Substratfühler. Seitliche Tauchhülsen unter GOK wären nicht zugänglich. | Q17, A | Annahme mit Bezug |
| M4 | Sensorik | Druck: Gasraum (1–2) im Kronenbereich/Decke; bei Tragluftdach zusätzlich Stützluft/Zwischenraum (1) und Membranlage-/Dachfüllstand. | Stückliste Baugruppe I, Zusammenfassung Sensorik. | Q17 | Projektunterlage |
| M5 | Sensorik | Gasanalyse (CH4, CO2, H2S, O2): Entnahme in der Gasstrecke nach dem Gasabgang, nicht unter GOK. | Stückliste: oft gemeinsame Messstelle in der Gasstrecke. | Q17 | Projektunterlage |
| M6 | Sensorik | Leckage: elektrische Leckagesonde je Kontrollschacht (systemabhängig), Sichtkontrolle mindestens wöchentlich (JGS-Praxis). | Z-59.26-470 Abschn. 3.1 (9): je Kontrollschacht eine Leckagesonde. SGD RLP Nr. 34a (TRwS 792 Abschn. 8.2): Leckageerkennung mindestens wöchentlich kontrollieren. | Q4, Q8 | Systemzulassung / JGS – für BGA TRwS 793-1 prüfen |
| M7 | Sensorik | Gaswarnung: Feldmelder an Bühne/Mannloch; bei Schächten unter GOK (Kontroll-, Pumpen-, Antriebsschacht) zusätzlich Schacht prüfen. | Stückliste Pos. 82; Gasansammlung in Vertiefungen. Umfang projektspezifisch (TRAS 120/TRGS 529). | Q17, A | Projektunterlage + Annahme |
| P1 | Leitungen | Gasabgang immer oben: im Kronenbereich oberhalb max. Füllstand (Tragluftdach) bzw. über die Decke. | Gasraum liegt oberhalb des Substratspiegels; Stückliste Pos. Gasabgang. | Q17 | Vorgabe |
| P2 | Leitungen | Substratzulauf/-ablauf, Heizung, Feststoffeintrag: Stutzen ≥ 0,5 m über GOK → Wanddurchführung über GOK mit Absperrung direkt am Behälter. Unter GOK → bevorzugt über den Kronenbereich führen (Zulauf mit Tauchrohr, Entnahme als Saugleitung ohne Heberwirkung); alternativ Wanddurchführung unter GOK mit Schutz-/Mantelrohr und Kontrolleinrichtung, ins LES eingebunden. | TRwS 793-1 Nr. 9.7.1/9.7.2 (lt. Vortrag Niehage): unterirdische Rohrleitungen mit LES oder als Saugleitung; Schutzrohr PE-HD/PVC mit überwachbarer Kontrolleinrichtung. SGD RLP Nr. 16: Kontrollierbarkeit der Wanddurchführung bei unterirdischer Zuleitung unterhalb des max. Flüssigkeitsspiegels (TRwS 792 Abschn. 6.6 Abs. 13). | Q5, Q6, Q8 | Quelle (Entwurfsstand / JGS) – Endfassung prüfen |
| P3 | Leitungen | Durchdringungen flüssigkeitsundurchlässig (z. B. Ringblech). | SGD RLP Nr. 16 mit Verweis TRwS 792 Abschn. 6.6 Abs. 12. | Q8 | Quelle (JGS) |
| P4 | Leitungen | Mannloch bodennah nur, wenn ≥ 0,5 m über GOK; sonst Einstieg/Revision über Krone bzw. Decke – Räumung und Entleerung gesondert planen. | Zugänglichkeit; Stückliste Mannloch DN 800 bei 1,0 m. | Q17, A | Annahme |
| L1 | Leckage | Einwandiger Behälter mit flüssigen Gärsubstraten/Gärresten → Leckageerkennungssystem (LES) erforderlich. | § 37 Abs. 2 AwSV; für Gärrestlager als JGS-Anlage zusätzlich Anlage 7 Nr. 3.1 AwSV (> 25 m³). | Q1, Q3, Q7 | Rechtsnorm |
| L2 | Leckage | Einbindung > 0 → „unterirdische Anlage“ (vollständig oder teilweise im Erdreich); Einbindung 0 mit flachem Boden vollflächig aufgestellt → oberirdisch. | § 2 Abs. 15 AwSV. | Q2 | Rechtsnorm |
| L3 | Leckage | Dichtungsbahn muss den gesamten erdberührten, nicht einsehbaren Behälterteil bis über GOK erfassen und niederschlagswasserdicht am Behälter befestigt sein. | TRwS 793-1 lt. Vortrag Niehage: „Muss die gesamte Behältersäule bis GOK erfassen“, „Befestigung am Behälter niederschlagswasserdicht“. BMUKN: LES erfasst Leckagen aus Boden und erdverdeckter Wand. | Q5, Q6, Q11 | Quelle (Entwurfsstand) – Endfassung prüfen |
| L4 | Leckage | Einbindung ≤ 1,30 m: einteiliges System – Bodendichtungsbahn unter der Sohle, an der Wand hochgeschlagen bis ca. 30 cm über OK Gelände. | Z-59.26-470 Abschn. 3.1 (14), (15) und 3.2.3 (17). Die Werte 1,30 m und 30 cm gelten für dieses System; andere Systeme: eigene abZ/aBG. | Q4 | systembezogen – projektspezifisch prüfen |
| L5 | Leckage | Einbindung > 1,30 m: zweiteiliges System – Boden- und Wanddichtungsbahn (Y-Anschluss), je Wandbahnlage max. 6 m Höhe, darüber zweite Lage; bis ca. 30 cm über OK Gelände. | Z-59.26-470 Abschn. 3.1 (16), 3.2.3 (14), (17). | Q4 | systembezogen – projektspezifisch prüfen |
| L6 | Leckage | Vollständig eingebunden (Krone ≤ GOK): Befestigungspunkt mindestens 10 cm über der max. zulässigen Füllhöhe; Kontrollschächte nicht überfahrbar, tagwasserdicht. | Z-59.26-470 Abschn. 3.1 (17), 3.2.3 (18). Behördenbeispiel LK Ludwigslust-Parchim: im nicht einsehbaren Bereich bis Höhe max. zulässiger Flüssigkeitsstand. | Q4, Q10 | systembezogen / Einzelfall |
| L7 | Leckage | Dichtungsbahn: Kunststoffdichtungsbahn, Dicke ≥ 1,5 mm bei Vor-Ort-Fertigung bzw. ≥ 1,0 mm vorkonfektioniert; Ausführung nur durch Fachbetrieb. | TRwS 793-1 lt. Vortrag Niehage (Gelbdruckstand). Historisch NRW 2009: ≥ 0,8 mm. Endfassung DWA-A 793-1 prüfen. | Q5, Q6, Q9 | Entwurfsstand – Endfassung prüfen |
| L8 | Leckage | Kontrolldrainage: Dränschicht über der Dichtungsbahn, Drain-Ringleitung DN 100 entlang des Fundaments mit durchgängigem Gefälle ≥ 0,5 % zum Kontrollschacht; Schutz gegen Zementschlämme beim Betonieren. | Z-59.26-470 Abschn. 3.1 (4), (13) (DN 100, ≥ 0,5 %); LK Ludwigslust-Parchim 7.2; NRW 2009. | Q4, Q10, Q9 | systembezogen / Behördenbeispiel |
| L9 | Leckage | Kontrollschächte: mindestens 2 je Behälter; die zuständige Behörde kann mehr fordern (Beispiel: 4 bei D > 20 m). Tagwasserdicht, Probenahme möglich. | Z-59.26-470 Abschn. 3.1 (9): mind. 2; NRW 2009: 2 je Behälter; LK Ludwigslust-Parchim 2024: 4 bei D > 20 m (Einzelfall). | Q4, Q9, Q10 | systembezogen – Anzahl projektspezifisch |
| L10 | Leckage / Grundwasser | Tiefster Punkt des LES mindestens 50 cm über dem höchsten zu erwartenden Grundwasserstand; kein Eindringen von Grund- oder Niederschlagswasser. | Z-59.26-470 Abschn. 3.1 (10) (systembezogen); BMUKN-FAQ; SGD RLP Nr. 8. | Q4, Q11, Q8 | systembezogen – projektspezifisch prüfen |
| L11 | Leckage / Grundwasser | Unterirdischer Behälter, dessen Bodenplattenunterkante unter dem höchsten zu erwartenden Grundwasserstand liegt, oder unterirdischer Behälter im Schutzgebiet → doppelwandig mit Leckanzeigesystem. | § 37 Abs. 5 AwSV. | Q1, Q7 | Rechtsnorm |
| L12 | Leckage / Rückhaltung | Können Leckagen oberhalb GOK auftreten (Füllstand über GOK), ist eine Umwallung erforderlich (mind. Volumen des größten Behälters) – Anlagenebene. | § 37 Abs. 3 AwSV. | Q1, Q7 | Rechtsnorm |
| L13 | Leckage | Wanddurchführungen unter GOK und Sammeleinrichtungen in das LES einbeziehen; Durchdringungen kontrollierbar. | AwSV Anlage 7 Nr. 3.2 (JGS); SGD RLP Nr. 16. | Q3, Q8 | Rechtsnorm (JGS) / Merkblatt |

## Klassengrenzen und Modellannahmen

- TS-Klasse Input-Mischung: < 15 % niedrig, 15–25 % mittel, > 25 % hoch (Annahme)
- Faserindex: < 1 niedrig, 1–1,8 mittel, > 1,8 hoch (Annahme)
- Zugänglichkeit einer Wanddurchführung: Achse ≥ 0,5 m über GOK (Annahme); bei Einbindung 0 gelten alle Wandstutzen als zugänglich
- Kronenbühne mit Treppe ab 1 m Kronenhöhe über GOK (Annahme)
- Stutzenhöhen über Sohle: Zulauf 1,2 m, Ablauf 0,45 m, Mannloch 1 m (Katalog `fermenter`), Heizung 1,5 m, Feststoffeintrag 2 m (Annahme)
- Max. Füllhöhe ohne Eingabe: H − 0,5 m (Annahme); Paddelachse 0,45 × max. Füllhöhe; Sohldicke 0,5 m; LES-Aufbau 0,15 m (Modellannahmen)
- Anzahl Rührwerke: gerundet(D / 8 m), 2…6, Klasse hoch +1 (Annahme, Auslegung durch Hersteller)

## Substrat-Referenzwerte

| Substrat | TS % | Faserfaktor (0–3, Annahme) | Sinkschicht | Quelle TS |
|---|---:|---:|---|---|
| Rindergülle | 10 | 1 | – | FNR Tab. 4.9: 10 % TS (Q12) |
| Schweinegülle | 6 | 0 | ja | FNR Tab. 4.9: 6 % TS; fördert Sinkschichten (FNR Kap. 3.2.2) (Q12) |
| Festmist | 25 | 3 | – | FNR Tab. 4.9 Rindermist: 25 % TS (Q12) |
| Maissilage | 33 | 1 | – | FNR Tab. 4.9: 33 % TS (Q12) |
| Grassilage | 35 | 3 | – | FNR Tab. 4.9: 35 % TS (Q12) |
| GPS (Getreide-Ganzpflanzensilage) | 33 | 2 | – | FNR Tab. 4.9: 33 % TS (Q12) |
| Zuckerrübe | 23 | 0 | ja | FNR Tab. 4.9: 23 % TS; Sinkneigung (Erdanhang) = Annahme (Q12) |
| Hühnertrockenkot | 45 | 1 | ja | KTBL 2015: HTK ohne Stroh 45 % TS; Sand-/Sinkschichten (FNR Kap. 3.2.2) (Q13) |
| Stroh / faserreich | 86 | 3 | – | LfL: Getreidestroh 86 % TM (Q14) |
| Bioabfall | 40 | 2 | ja | KTBL: Bioabfall 40 % TS; Störstoffpotenzial (FNR Kap. 3.2.1) (Q15) |

## Quellen

- **Q1** – AwSV § 37 – Besondere Anforderungen an Biogasanlagen mit Gärsubstraten landwirtschaftlicher Herkunft (Abs. 2–5) – https://www.gesetze-im-internet.de/awsv/__37.html _(Rechtsnorm)_
- **Q2** – AwSV § 2 Abs. 15 – Begriff „unterirdische Anlagen“ (vollständig oder teilweise im Erdreich eingebettet); Behälter mit flachem Boden vollflächig aufgestellt = oberirdisch – https://www.gesetze-im-internet.de/awsv/__2.html _(Rechtsnorm)_
- **Q3** – AwSV Anlage 7 Nr. 3.1/3.2 und 8.1 – JGS-Anlagen: Leckageerkennungssystem > 25 m³, Schutzgebiete – https://www.gesetze-im-internet.de/awsv/anlage_7.html _(Rechtsnorm (JGS; für Gärrestlager je nach Geltungsbereich))_
- **Q4** – DIBt, abZ/aBG Z-59.26-470 „Leak Detection 1.0“ vom 11.02.2025 (gültig bis 11.02.2030), Abschn. 3.1 (4), (9), (10), (13)–(17) und 3.2.3 (12), (13), (17), (18) – https://www.dibt.de/pdf_storage/2025/Z-59.26-470(1.59.26-38!24).pdf _(Systemzulassung eines konkreten Produkts – Werte gelten für dieses System, andere Systeme haben eigene Zulassungen)_
- **Q5** – A. Niehage (Sprecher AG IG-6.15), Vortrag „DWA-A 793-1 (TRwS 793-1) Biogasanlagen Teil 1“, NLWKN – Stand Gelbdruck vor Weißdruck – https://www.nlwkn.niedersachsen.de/download/141176/Niehage_-_TRwS_793_Biogasanlagen_Teil_1_Errichtung_und_Betrieb_mit_Gaersubstraten_landwirtschaftlicher_Herkunft.pdf _(Sekundärquelle zum Regelwerksentwurf – Endfassung prüfen)_
- **Q6** – DWA-A 793-1 (TRwS 793-1) Biogasanlagen Teil 1, März 2021, korrigierte Fassung September 2021 (kostenpflichtig, Volltext hier nicht eingesehen) – https://shop.dwa.de/DWA-A-793-1-TRwS-793-1-Technische-Regel-wassergefaehrdender-Stoffe-Biogasanlagen-Teil-1-Errichtung-und-Betrieb-von-Biogasanlagen-mit-Gaersubstraten-landwirtschaftlicher-Herkunft-Maerz-2021-Stand-Korrigierte-Fassung-September-2021/A-793-T1-PDF-21 _(Technische Regel – maßgeblich, Volltext beschaffen)_
- **Q7** – Bayerisches Landesamt für Umwelt, „Anlagen in der Landwirtschaft – Biogasanlagen“ (verweist auf § 37 AwSV und TRwS 793-1 März 2021; Biogashandbuch Kap. 2.2.4) – https://www.lfu.bayern.de/wasser/umgang_mit_wgs/landwirtschaft/index.htm _(Behördeninformation Bayern)_
- **Q8** – SGD Nord/Süd Rheinland-Pfalz, Merkblatt „JGS-Anlagen“ 08/2017, Nr. 8, 16 (Wanddurchführungen, TRwS 792 Abschn. 6.6 Abs. 12/13), 21, 25, 34 – https://www.dlr.rlp.de/Internet/global/themen.nsf/ALL/6F29B44123C52E4BC125819A001F08CA/$FILE/Merkblatt_JGS-Anlagen.pdf _(Landesmerkblatt (RLP, JGS) – Verweis auf TRwS 792)_
- **Q9** – MUNLV NRW, Anforderungskatalog Biogasanlagen, Stand 10/2009, Nr. 3.3.1.2 (noch nach § 19g WHG – historisch) – https://igsvtu.lanuk.nrw.de/vtu/doc.app?DATEI=16%2Fdokus%2F160785.pdf&USER_ID=9 _(Historische Landesvorgabe – nur Einordnung)_
- **Q10** – Landkreis Ludwigslust-Parchim, wasserrechtliche Stellungnahme vom 05.03.2024 zu einer Biogasanlage (Nebenbestimmungen 7.1–7.3) – https://service.mvnet.de/_php/download.php?datei_id=1672735 _(Einzelfall-Auflage einer Behörde – Beispiel, nicht übertragbar)_
- **Q11** – BMUKN-FAQ „Welche Aufgabe hat ein Leckageerkennungssystem bei JGS- und Biogasanlagen?“ – https://www.bundesumweltministerium.de/faq/welche-aufgabe-hat-ein-leckageerkennungssystem-bei-jgs-und-biogasanlagen _(Behördeninformation Bund)_
- **Q12** – FNR, Leitfaden Biogas – Von der Gewinnung zur Nutzung, 7. Aufl. 2016: Kap. 3.1.1 (TS Nassvergärung), Kap. 3.2.2.3 Tab. 3.22–3.25 (Rührwerke), Sinkschichten S. 3.2.2.4, Kap. 3.3.1.2, Tab. 4.1/4.3/4.9 (TS-Werte) – https://www.dieter-bouse.de/app/download/5813189892/FNR_Leitfaden_Biogas%2C+Ausgabe+2016.pdf _(Fachliteratur)_
- **Q13** – KTBL „Gasausbeute in landwirtschaftlichen Biogasanlagen“ 2015, zitiert bei biogaseffizienz.info: HTK ohne Stroh 45 % TS – https://www.biogaseffizienz.info/optimierung-und-sanierung/htk-festmist-nebenprodukte.php _(Fachliteratur (Sekundärzitat))_
- **Q14** – LfL Bayern, Biogasausbeuten-Datenbank: Getreidestroh 86 % TM – https://www.lfl.bayern.de/iba/energie/049711/?anker0=substratanker&sel_list=20%2Cb _(Fachdatenbank)_
- **Q15** – Tabelle „Gaserträge und Nährstoffgehalte – Abfall“ (ARCHEA), Wert „Bioabfall (KTBL)“ 40 % TS – https://www.archea-biogas.de/_mediafiles/9-substrate.pdf _(Sekundärzitat KTBL)_
- **Q16** – Kompost und Biogas Verband Österreich, „Rührwerke“: Langsamläufer-Durchführung oberhalb max. Flüssigkeitsstand, Paddel durchbrechen Schwimmdecken, TMR im Endlager – https://www.kompost-biogas.info/biogas/die-biogasanlage/ruehrwerke/ _(Fachinformation)_
- **Q17** – Schematische Fermenter-Stückliste, Anlagen-Designer, 15.11.2026 (Baugruppen A–I, 83 Positionen) – Projektunterlage, intern, nicht veröffentlicht _(Projektunterlage)_
- **A** – Eigene schematische Annahme des Konfigurators – keine Quelle, projektspezifisch prüfen und ggf. im Regelwerk anpassen _(Annahme)_

Lokale Quellenkopien und Auszüge bleiben intern und sind nicht Bestandteil der veröffentlichten Dateien.
