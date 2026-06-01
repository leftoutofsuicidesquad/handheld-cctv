# Project: Tactical Surveillance Handgrip (TSH-1)

Ein modulares, handgeführtes Kamera-System zur Videoaufzeichnung und Echtzeit-Vorschau. Dieses Projekt wurde entwickelt, um ein stabiles und professionelles Aufnahmegerät für mobile Einsätze zu schaffen.

## 🏗️ System-Architektur
Das System besteht aus zwei Haupt-Subsystemen: der autarken Stromversorgung und der aktiven Signalverarbeitung.

```mermaid
graph LR
    subgraph Stromversorgung
    Batt[12V Akku] --> Switch[Schalter am Griff]
    Switch --> Dist[12V Verteiler/Schiene]
    Dist --> Cam[Kamera]
    Dist --> Mon[4.3 Zoll Monitor]
    Dist --> Amp[Aktiver Video-Booster]
    Dist --> Step[Step-Down Wandler 12V auf 5V]
    Step --> DVR[Mini DVR]
    end

    subgraph Signalfluss
    Cam -->|BNC| Amp
    Amp -->|Out 1| DVR
    Amp -->|Out 2| Mon
    end

## 🛠️ Komponentenliste
* **Kamera:** JVC TK 930E (CCTV)
* **Aufnahme:** FPV Mini-DVR
* **Vorschau:** 4,3" TFT LCD Monitor
* **Verteilung:** Aktiver Video-Booster (1-auf-3)
* **Strom:** 12V Li-Ion Akku mit 12V-auf-5V Step-Down-Konverter
* **Mechanik:** Hama Stativ-Pistolengriff

## 🚀 Status
- [ ] Hardware-Beschaffung
- [ ] Schaltplan-Design (KiCad)
- [ ] Signalweg-Test
- [ ] Gehäuse-Integration & Lötarbeiten
- [ ] Finales Testing

## 💡 Technische Herausforderungen (Level 3)
* **Spannungsmanagement:** Präzise Reduzierung der Spannung auf 5V für den DVR ohne Rauschinterferenzen.
* **Signalintegrität:** Verwendung eines aktiven Boosters, um Signalverluste bei der Aufteilung auf Monitor und DVR zu verhindern.
* **Ergonomie:** Mechanische Integration aller Komponenten in einen kompakten Pistolengriff.

---
