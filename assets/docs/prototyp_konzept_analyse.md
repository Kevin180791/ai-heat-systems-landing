# Prototyp-Konzept: KI-Hardware mit Abwärmenutzung für Eigentumswohnungen

## Executive Summary

Das vorliegende Konzept entwickelt einen innovativen Prototyp für die Integration von KI-Hardware mit Abwärmenutzung in Eigentumswohnungen. Durch geschickte Finanzierung über Forschungs-, KI- und Fortbildungsbudgets des Arbeitgebers entsteht ein wirtschaftlich tragfähiges Modell, das technologische Innovation mit praktischer Energieeffizienz verbindet.

---

## 1. Konzept-Grundlagen

### 1.1 Inspirationsquellen

Das Konzept basiert auf mehreren erfolgreichen Referenzprojekten:

**Thermify HeatHub (UK):** Das SHIELD-Programm von UK Power Networks demonstriert die erfolgreiche Integration von 500 Raspberry Pi Compute Modules pro Einheit in Wohngebäuden. Die Systeme erzielen eine Energiekostenreduktion von 20-40% bei monatlichen Kosten von nur £5.60 (~€6.50). Der Ansatz kombiniert Ölimmersionskühlung mit direkter Anbindung an Zentralheizung und Warmwassersysteme.

**Heata (British Gas):** Zeigt die Machbarkeit der direkten Montage von Servern auf Warmwassertanks. Das Modell nutzt Cloud-Computing-Workloads (Civo) zur Finanzierung der Wärmebereitstellung.

**Deep Green:** Fokussiert auf gewerbliche Anwendungen (Schwimmbäder, Unternehmen) und hat bereits £200M Finanzierung von Energieversorgern erhalten, was die Marktreife des Konzepts unterstreicht.

**NetworkChuck und DIY-Community:** Demonstrieren die technische Machbarkeit von selbstgebauten KI-Clustern und inspirieren zu modularen, erweiterbaren Ansätzen.

### 1.2 Kernidee für Eigentumswohnungen

Der Prototyp verbindet drei zentrale Elemente:

1. **KI-Computing-Kapazität:** Bereitstellung von Rechenleistung für Forschung, Entwicklung und Fortbildung des Arbeitgebers
2. **Wärmenutzung:** Direkte Integration der Abwärme in das Heizsystem der Eigentumswohnungen
3. **Dual-Revenue-Modell:** Finanzierung durch Arbeitgeber (Computing) und Energiekosteneinsparung (Wärme)

---

## 2. Technisches Konzept

### 2.1 Hardware-Architektur

**Modularer Aufbau (Skalierbar):**

**Einstiegskonfiguration (Prototyp):**
- 50-100 Raspberry Pi Compute Modules (CM4/CM5) oder vergleichbare RISC-V basierte Module
- Immersionskühlung in dielektrischer Flüssigkeit (z.B. 3M Novec oder Alternativen)
- Wärmetauscher zur Übertragung an Heizkreislauf
- Dedizierte Netzwerkanbindung (1-10 Gbit/s)
- Modulares Gehäuse (ca. Größe einer Waschmaschine)

**Erweiterte Konfiguration:**
- 200-500 Compute Modules für höhere Leistung
- Mehrere verteilte Einheiten über verschiedene Wohnungen
- Integration mit Wärmepumpe für Temperaturanhebung

### 2.2 Kühlungs- und Wärmeintegration

**Immersionskühlung:**
- Komplette Eintauchung der Hardware in dielektrische Flüssigkeit
- Abwärmetemperatur: 40-60°C (ideal für Niedertemperatur-Heizsysteme)
- Höchste Effizienz bei Wärmeübertragung
- Minimaler Wartungsaufwand
- Geräuscharm (wichtig für Wohnumgebung)

**Wärmeintegration - Drei Szenarien:**

**Szenario A: Direkte Fußbodenheizung**
- Vorlauftemperatur: 28-35°C (direkt nutzbar)
- Keine Wärmepumpe erforderlich
- Höchste Effizienz (COP effektiv ∞, da Abwärme)
- Ideal für Neubau oder sanierte Wohnungen

**Szenario B: Warmwasser-Vorwärmung**
- Vorwärmung von 10°C auf 40-50°C
- Nachheizung durch konventionelles System auf 60°C
- Reduziert Energiebedarf um 60-70%
- Retrofit-fähig für Bestandsgebäude

**Szenario C: Wärmepumpen-Integration**
- Abwärme als Wärmequelle für Wärmepumpe
- Anhebung auf 70-85°C für konventionelle Heizkörper
- COP 5-7 durch hohes Ausgangsniveau
- Maximale Flexibilität

### 2.3 Computing-Kapazität

**Leistungsberechnung (100 Raspberry Pi CM4):**
- CPU: 100 × 4 Cores = 400 Cores (ARM Cortex-A72)
- RAM: 100 × 8 GB = 800 GB
- Stromverbrauch: ~1.500-2.000 W unter Last
- Wärmeleistung: ~1.500-2.000 W (100% Umwandlung)

**Anwendungsfälle:**
- Machine Learning Training (kleinere Modelle)
- Inference-Workloads
- Datenanalyse und -verarbeitung
- Entwicklungs- und Testumgebungen
- Container-Orchestrierung (Kubernetes)
- Edge-AI-Anwendungen

---

## 3. Wirtschaftlichkeitsanalyse

### 3.1 Investitionskosten (Prototyp mit 100 Modulen)

| Position | Kosten | Anmerkungen |
|----------|--------|-------------|
| **Hardware** | | |
| 100× Raspberry Pi CM4 (8GB) | €7.000 | ~€70/Stück |
| Carrier Boards & Cluster-System | €3.000 | Custom oder Turing Pi |
| Immersionskühlungs-System | €5.000 | Tank, Pumpen, Flüssigkeit |
| Wärmetauscher & Integration | €3.000 | Plattenwärmetauscher, Anschlüsse |
| Netzwerk-Hardware | €2.000 | Switch, Verkabelung |
| Gehäuse & Montage | €2.000 | Professionelles Gehäuse |
| **Installation** | | |
| Heizungsintegration | €3.000 | Fachinstallation |
| Elektrische Installation | €2.000 | Separate Zuleitung |
| Netzwerkanbindung | €1.000 | Glasfaser/Kupfer |
| **Sonstiges** | | |
| Steuerung & Monitoring | €1.500 | Software, Sensoren |
| Puffer & Unvorhergesehenes | €2.500 | 10% Reserve |
| **GESAMT** | **€32.000** | Prototyp-Konfiguration |

### 3.2 Betriebskosten (jährlich)

| Position | Kosten/Jahr | Berechnung |
|----------|-------------|------------|
| **Energie** | | |
| Stromverbrauch | €3.150 | 1.750W × 24h × 365d × €0.25/kWh |
| Netzwerkanbindung | €600 | Dedizierte Leitung |
| **Wartung** | | |
| Systemwartung | €500 | Jährliche Inspektion |
| Software-Updates | €300 | Lizenzen, Updates |
| Ersatzteile-Reserve | €500 | Ausfallreserve |
| **Versicherung** | €200 | Zusatzversicherung |
| **GESAMT** | **€5.250** | |

### 3.3 Einnahmen & Einsparungen (jährlich)

| Position | Wert/Jahr | Berechnung |
|----------|-----------|------------|
| **Wärmeeinsparung** | | |
| Heizenergie-Ersatz | €2.100 | 15.330 kWh × €0.137/kWh (Fernwärme) |
| Warmwasser-Ersatz | €700 | 5.110 kWh × €0.137/kWh |
| **Computing-Wert** | | |
| Cloud-Äquivalent | €8.400 | Vergleichbare Cloud-Kosten |
| Forschungsbudget-Nutzung | €10.000 | Interne Verrechnungsposition |
| **GESAMT** | **€21.200** | |

### 3.4 ROI-Berechnung

**Netto-Cashflow (Jahr 1):**
- Einnahmen/Einsparungen: €21.200
- Betriebskosten: -€5.250
- **Netto-Benefit: €15.950**

**Amortisation:**
- Investition: €32.000
- Jährlicher Netto-Benefit: €15.950
- **Payback-Period: 2,0 Jahre**

**10-Jahres-Betrachtung (NPV bei 5% Diskontrate):**
- Kumulierter Netto-Benefit: €159.500
- Abzgl. Investition: -€32.000
- Abzgl. diskontierte Betriebskosten: -€40.500
- **NPV: €87.000**
- **ROI: 272%**

---

## 4. Finanzierungsmodell über Arbeitgeber

### 4.1 Forschungszulage (Deutschland)

**Förderfähigkeit:**
- KI-Projekte sind grundsätzlich förderfähig
- Forschungszulage: **25% der förderfähigen Aufwendungen**
- Für KMU: **bis zu 35%** (auf Antrag)
- Maximale Bemessungsgrundlage: €10 Mio./Jahr

**Anwendung auf Prototyp:**
- Förderfähige Investition: €32.000
- Forschungszulage (25%): **€8.000**
- Effektive Investition: **€24.000**

**Voraussetzungen:**
- Bescheinigung durch BSFZ (Bescheinigungsstelle Forschungszulage)
- Dokumentation des Forschungscharakters
- Nachweis systematischer, kreativer Arbeit
- Erweiterung des Wissensstandes

### 4.2 Fortbildungsbudget

**Steuerliche Absetzbarkeit:**
- Fortbildungskosten sind vollständig als Betriebsausgaben absetzbar
- Umfasst: Kursgebühren, Fachliteratur, Hardware für Lernzwecke
- Keine Obergrenze bei beruflichem Bezug

**Integration in Prototyp:**
- Hardware als Lernplattform für KI/ML
- Praktische Schulung in:
  - Container-Orchestrierung (Kubernetes)
  - Distributed Computing
  - AI/ML Model Training & Deployment
  - Hardware-Integration und Thermal Management
  - Energieeffizienz-Optimierung

**Budgetansatz:**
- Anteil Fortbildung: €10.000 (31% der Investition)
- Steuerersparnis (30% KSt): **€3.000**

### 4.3 KI-Forschungsbudget

**Interne Verrechnung:**
- Bereitstellung von Computing-Ressourcen für Arbeitgeber
- Äquivalent zu Cloud-Kosten: €8.400/Jahr
- Langfristiger Vertrag (5 Jahre): **€42.000**

**Geschäftsmodell:**
- Arbeitgeber zahlt monatliche Nutzungsgebühr: €700
- Deckt Betriebskosten und Amortisation
- Win-Win: Günstiger als Cloud, eigene Kontrolle

### 4.4 Energieeffizienz-Förderung (BAFA/KfW)

**Bundesförderung für Energie- und Ressourceneffizienz (EEW):**
- Förderung für Abwärmenutzung
- Zuschuss: bis zu **40% der förderfähigen Kosten**
- Alternativ: KfW-Kredit mit Tilgungszuschuss

**Anwendung:**
- Wärmetauscher, Integration: €6.000 förderfähig
- Zuschuss (40%): **€2.400**

### 4.5 Gesamtfinanzierung

| Finanzierungsquelle | Betrag | Anteil |
|---------------------|--------|--------|
| Eigenanteil (initial) | €32.000 | 100% |
| **Rückflüsse:** | | |
| Forschungszulage | -€8.000 | 25% |
| Steuerersparnis Fortbildung | -€3.000 | 9% |
| BAFA-Förderung | -€2.400 | 8% |
| **Netto-Investition** | **€18.600** | **58%** |
| | | |
| **Refinanzierung Jahr 1:** | | |
| Arbeitgeber-Nutzungsgebühr | €8.400 | |
| Wärmeeinsparung | €2.800 | |
| **Gesamt Jahr 1** | **€11.200** | |
| | | |
| **Effektive Amortisation** | **1,7 Jahre** | |

---

## 5. Rechtliche und steuerliche Strukturierung

### 5.1 Vertragsmodell mit Arbeitgeber

**Option A: Dienstleistungsvertrag**
- Bereitstellung von Computing-Kapazität
- Monatliche Vergütung: €700
- Laufzeit: 5 Jahre (mit Verlängerungsoption)
- SLA (Service Level Agreement) für Verfügbarkeit

**Option B: Forschungskooperation**
- Gemeinsames Forschungsprojekt
- Arbeitgeber als Ko-Finanzier
- Ergebnisse werden geteilt
- Bessere Förderbarkeit

**Option C: Miet-/Leasingmodell**
- Arbeitgeber least Hardware
- Installation in Eigentumswohnung
- Arbeitnehmer erhält Wärme kostenlos
- Steuerlich optimiert

### 5.2 Steuerliche Behandlung

**Für Arbeitnehmer:**
- Wärmenutzung als geldwerter Vorteil?
  - Nein, wenn Arbeitgeber Eigentümer bleibt
  - Ja, wenn als Sachbezug gewertet → Pauschalversteuerung möglich
- Vermietung von Stellfläche an Arbeitgeber
  - Mieteinnahmen: €100-200/Monat
  - Steuerlich absetzbar: Anteilige Wohnkosten

**Für Arbeitgeber:**
- Betriebsausgaben: Vollständig absetzbar
- Forschungszulage: 25% Steuererstattung
- Abschreibung: 3-5 Jahre (Hardware)
- Energiekosten: Betriebsausgaben

### 5.3 Regulatorische Aspekte

**Energieeffizienzgesetz (ab Juli 2026):**
- Prototyp erfüllt 10%-Abwärmenutzungs-Pflicht
- Kann als Best-Practice-Beispiel dienen
- Dokumentation für Compliance

**Gebäudeenergiegesetz (GEG):**
- Abwärme als erneuerbare Energie anrechenbar
- Reduziert Primärenergiebedarf
- Verbessert Energieausweis der Immobilie

**Datenschutz (DSGVO):**
- Keine personenbezogenen Daten auf System
- Oder: Verschlüsselung und Zugriffskontrolle
- Arbeitgeber als Verantwortlicher

---

## 6. Technische Umsetzung - Phasenplan

### Phase 1: Konzeption & Planung (Monat 1-2)

**Aktivitäten:**
- Detaillierte Systemplanung
- Auswahl der Hardware-Komponenten
- Heizungstechnische Planung
- Einholung von Angeboten
- Beantragung Forschungszulage
- Vertragsverhandlung mit Arbeitgeber

**Deliverables:**
- Technisches Konzept
- Kostenplan
- Verträge
- Förderanträge

### Phase 2: Beschaffung & Vorbereitung (Monat 3-4)

**Aktivitäten:**
- Bestellung Hardware
- Vorbereitung Installationsort
- Elektrische Vorarbeiten
- Netzwerkanbindung vorbereiten
- Software-Architektur entwickeln

**Deliverables:**
- Beschaffte Hardware
- Vorbereiteter Installationsort
- Software-Stack

### Phase 3: Aufbau & Integration (Monat 5-6)

**Aktivitäten:**
- Zusammenbau Cluster-System
- Installation Immersionskühlung
- Integration Wärmetauscher
- Heizungsanbindung durch Fachfirma
- Elektrische Installation
- Netzwerk-Setup

**Deliverables:**
- Funktionsfähiges System
- Integrierte Heizungsanbindung
- Monitoring-Dashboard

### Phase 4: Inbetriebnahme & Test (Monat 7)

**Aktivitäten:**
- Systemtests
- Lasttests
- Wärmeintegration testen
- Performance-Optimierung
- Dokumentation
- Schulung

**Deliverables:**
- Abgenommenes System
- Dokumentation
- Betriebshandbuch

### Phase 5: Produktivbetrieb & Monitoring (ab Monat 8)

**Aktivitäten:**
- Workload-Deployment
- Kontinuierliches Monitoring
- Optimierung
- Wartung
- Datensammlung für Forschung

**Deliverables:**
- Produktives System
- Monatliche Reports
- Forschungsergebnisse

---

## 7. Risiken und Mitigation

### 7.1 Technische Risiken

| Risiko | Wahrscheinlichkeit | Impact | Mitigation |
|--------|-------------------|--------|------------|
| Hardware-Ausfälle | Mittel | Mittel | Redundanz, Ersatzteile, Garantie |
| Kühlsystem-Probleme | Niedrig | Hoch | Qualitätskomponenten, Monitoring, Notabschaltung |
| Netzwerk-Ausfälle | Niedrig | Mittel | Redundante Anbindung, Failover |
| Software-Bugs | Hoch | Niedrig | Testing, Updates, Community-Support |
| Inkompatibilität Heizung | Niedrig | Hoch | Fachplanung, Vorab-Tests |

### 7.2 Wirtschaftliche Risiken

| Risiko | Wahrscheinlichkeit | Impact | Mitigation |
|--------|-------------------|--------|------------|
| Energiepreis-Änderungen | Hoch | Mittel | Langfristvertrag, Diversifikation |
| Förderung abgelehnt | Niedrig | Mittel | Sorgfältige Antragstellung, Alternativen |
| Arbeitgeber kündigt | Niedrig | Hoch | Langfristvertrag, alternative Nutzung |
| Höhere Betriebskosten | Mittel | Niedrig | Puffer eingeplant, Optimierung |

### 7.3 Rechtliche Risiken

| Risiko | Wahrscheinlichkeit | Impact | Mitigation |
|--------|-------------------|--------|------------|
| Steuerliche Nachteile | Niedrig | Mittel | Steuerberater einbinden |
| Haftungsfragen | Niedrig | Hoch | Versicherung, klare Verträge |
| Regulatorische Änderungen | Mittel | Niedrig | Flexibles Design, Compliance |
| Nachbarschaftskonflikte | Niedrig | Niedrig | Geräuscharmes System, Information |

---

## 8. Skalierung und Weiterentwicklung

### 8.1 Skalierungspfade

**Horizontale Skalierung:**
- Erweiterung auf weitere Eigentumswohnungen
- Vernetzung mehrerer Einheiten
- Lastverteilung über Standorte
- Redundanz und Ausfallsicherheit

**Vertikale Skalierung:**
- Upgrade auf leistungsstärkere Module
- Erhöhung der Moduldichte
- Integration von GPU-Beschleunigern
- Speicher-Erweiterung

### 8.2 Technologische Weiterentwicklung

**Kurzfristig (1-2 Jahre):**
- Optimierung der Workload-Verteilung
- KI-gestützte Lastprognose
- Integration mit Smart Home
- Predictive Maintenance

**Mittelfristig (3-5 Jahre):**
- Migration zu RISC-V Architektur
- Eigene Hardware-Designs
- Integration von Energiespeichern
- Vehicle-to-Grid (V2G) Integration

**Langfristig (5+ Jahre):**
- Vollständig selbst entwickelte Hardware
- Lokale Produktion (Fab-Lab, Makerspace)
- Community-basierte Fertigung
- Open-Source Hardware-Plattform

### 8.3 Geschäftsmodell-Evolution

**Phase 1: Prototyp (Jahre 1-2)**
- Fokus: Proof of Concept
- Finanzierung: Arbeitgeber + Förderung
- Ziel: Technische Validierung

**Phase 2: Optimierung (Jahre 3-5)**
- Fokus: Effizienzsteigerung
- Zusätzliche Einnahmen: Wärmeverkauf an Nachbarn
- Ziel: Wirtschaftliche Optimierung

**Phase 3: Skalierung (Jahre 5-10)**
- Fokus: Replikation
- Geschäftsmodell: Beratung, Bausätze, Dienstleistung
- Ziel: Marktdurchdringung

**Phase 4: Plattform (Jahre 10+)**
- Fokus: Ökosystem
- Modell: Open-Source Community + kommerzielle Services
- Ziel: Standard etablieren

---

## 9. Innovationspotenziale

### 9.1 Technische Innovationen

**Adaptive Thermal Management:**
- KI-gesteuerte Lastverteilung basierend auf Wärmebedarf
- Prädiktive Heizungssteuerung
- Optimierung von Computing-Last und Wärmeabgabe
- Integration von Wetterprognosen

**Hybrid-Systeme:**
- Kombination mit Solarthermie
- Integration mit Wärmepumpe
- Saisonale Wärmespeicherung
- Kopplung mit Photovoltaik

**Edge-AI-Optimierung:**
- Spezialisierte Workloads für konstante Last
- Inference-Optimierung für Energieeffizienz
- Federated Learning über verteilte Systeme
- Privacy-preserving Computing

### 9.2 Geschäftsmodell-Innovationen

**Community-Computing:**
- Nachbarschafts-Cloud
- Geteilte Computing-Ressourcen
- Lokale Datenverarbeitung
- Dezentrale Services

**Energy-as-a-Service:**
- Wärme-Flatrate für Nachbarn
- Dynamische Preisgestaltung
- Peer-to-Peer Energiehandel
- Blockchain-basierte Abrechnung

**Circular Economy:**
- Refurbished Hardware nutzen
- Modulare, reparierbare Designs
- Lokale Wertschöpfung
- Cradle-to-Cradle Ansatz

### 9.3 Gesellschaftliche Innovationen

**Demokratisierung von Computing:**
- Zugang zu KI-Ressourcen
- Bildung und Fortbildung
- Open-Source Wissenstransfer
- Community-Building

**Energiewende von unten:**
- Dezentrale Energienutzung
- Bürger als Prosumer
- Lokale Wertschöpfung
- Resilienz durch Dezentralität

**Neue Arbeitsformen:**
- Home-Office mit eigener Infrastruktur
- Unabhängigkeit von Cloud-Anbietern
- Datensouveränität
- Lokale Innovation Hubs

---

## 10. Handlungsempfehlungen

### 10.1 Sofortmaßnahmen (Woche 1-4)

1. **Gespräch mit Arbeitgeber initiieren**
   - Konzept vorstellen
   - Interesse und Budget klären
   - Vertragsmodell diskutieren

2. **Steuerberater konsultieren**
   - Optimale Strukturierung
   - Forschungszulage prüfen
   - Steuerliche Fallstricke vermeiden

3. **Technische Machbarkeitsstudie**
   - Heizungssystem analysieren
   - Platzbedarf prüfen
   - Elektrische Kapazität checken

4. **Erste Angebote einholen**
   - Hardware-Komponenten
   - Kühlsystem
   - Installation

### 10.2 Kurzfristig (Monat 2-6)

1. **Förderanträge stellen**
   - Forschungszulage beantragen
   - BAFA-Förderung prüfen
   - Dokumentation vorbereiten

2. **Detailplanung durchführen**
   - Technisches Konzept finalisieren
   - Zeitplan erstellen
   - Budget detaillieren

3. **Verträge abschließen**
   - Arbeitgeber-Vertrag
   - Lieferanten-Verträge
   - Installateur beauftragen

4. **Community aufbauen**
   - GitHub-Repository erstellen
   - Dokumentation beginnen
   - Netzwerk aktivieren

### 10.3 Mittelfristig (Monat 6-12)

1. **Prototyp realisieren**
   - Aufbau durchführen
   - Tests und Optimierung
   - Dokumentation vervollständigen

2. **Monitoring etablieren**
   - Datenerfassung
   - Performance-Tracking
   - Optimierung

3. **Forschungsergebnisse publizieren**
   - Fachartikel schreiben
   - Konferenzen besuchen
   - Best Practices teilen

4. **Skalierung vorbereiten**
   - Lessons Learned dokumentieren
   - Standardisierung
   - Replikationskonzept

---

## 11. Fazit und Ausblick

### 11.1 Zusammenfassung

Das vorliegende Konzept demonstriert die technische und wirtschaftliche Machbarkeit eines innovativen Prototyps, der KI-Computing mit Abwärmenutzung in Eigentumswohnungen verbindet. Durch geschickte Finanzierung über Arbeitgeber-Budgets und staatliche Förderungen reduziert sich die effektive Investition auf €18.600 bei einer Amortisationszeit von nur 1,7 Jahren.

**Kernvorteile:**
- **Wirtschaftlich:** ROI von 272% über 10 Jahre
- **Ökologisch:** CO₂-Einsparung durch Abwärmenutzung
- **Innovativ:** Kombination von Computing und Energieeffizienz
- **Skalierbar:** Modulares Konzept für Erweiterung
- **Förderbar:** Multiple Finanzierungsquellen

### 11.2 Kritische Erfolgsfaktoren

1. **Engagement des Arbeitgebers:** Langfristiger Vertrag essentiell
2. **Technische Exzellenz:** Zuverlässiges System erforderlich
3. **Wirtschaftliche Disziplin:** Kostenrahmen einhalten
4. **Regulatorische Compliance:** Alle Vorschriften beachten
5. **Community-Building:** Wissensaustausch und Weiterentwicklung

### 11.3 Vision

Dieses Projekt hat das Potenzial, über einen einfachen Prototyp hinauszuwachsen und zu einem Modell für dezentrale, energieeffiziente Computing-Infrastruktur zu werden. Die Kombination von KI-Hardware mit praktischer Energienutzung adressiert zwei der drängendsten Herausforderungen unserer Zeit: den wachsenden Bedarf an Computing-Kapazität und die Notwendigkeit der Energiewende.

Durch Open-Source-Ansätze, Community-Building und kontinuierliche Innovation kann aus diesem Prototyp eine Bewegung entstehen, die Computing demokratisiert, Energie effizient nutzt und lokale Wertschöpfung ermöglicht.

**Der erste Schritt beginnt jetzt – mit Ihrem Prototyp in Ihren Eigentumswohnungen.**

