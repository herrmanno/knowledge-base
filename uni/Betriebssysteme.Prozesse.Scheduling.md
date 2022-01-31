---
id: z1piZPreVuAkRpDEHQYOG
title: Scheduling
desc: ''
updated: 1642671398782
created: 1642667894953
---

# Ziele
- Fairness
- Effizient
- Interaktivität (u.U.)

## Leistungsorientierte Ziele
- Durchsatz
- Antwortzeit
- Effizienz

## Steuerungsorientierte Ziele
- Balance zwischen Fairness und aufgabenorientierter Ressourcenzuordnung
- Dringlichkeit
- Ressourcenorientiert
    - maximale Auslastung
    - Energie, Wirtschaftlichkeit

# Prozesszustände
![Prozesszustände](/assets/images/2022-01-20-09-38-18.png)

## Zeiten

| Name | Abkürzung | Beschreibung |
|------------|--------------------------------------------------------|--|
| CPU-Bursts | $T_{Burst}$ | Summe der Zeiten im Zustand ''running'' |
| IO-Bursts | $T_{IO}$ | Summe der Zeiten im Zustand ''blocked'' oder ''blocked suspend'' |
| Readyzeit | $T_{Ready}$ | Summe der Zeiten im Zustand ''ready'' oder ''ready suspend'' |
| Verweilzeit | $T_{V} = T_{Burst} + T_{IO} + T_{Ready}$ | |
| Wartezeit | $T_{W} = T_{IO} + T_{Ready}$ | |

# Prozesswechselzeit
![Prozesswechselzeit](/assets/images/2022-01-20-09-39-24.png)

**Es muss gelten**: $t_{switch} << t_{cycle}$

# Kriterien
- preemptive oder non-preemptive
- Interaktiv (UI) oder Nicht-Interaktiv (Stapelverarbeitung)
- Warte- und Antwortzeiten (Deadlines, z.B. in Echtzeitsystemen)
- Effiziente Nutzung der Hardware (Durchsatz)
- Gestufte Ressourcenzuordnung / Durchsetzung von Richtlinien

# Strategien

- [[Betriebssysteme.Prozesse.Scheduling.First_Come_First_Serve]]
- [[Betriebssysteme.Prozesse.Scheduling.Round_Robin]]
- [[Betriebssysteme.Prozesse.Scheduling.Shortest_Job_First]]
- [[Betriebssysteme.Prozesse.Scheduling.Shortest_Time_to_Completion_First]]
- [[Betriebssysteme.Prozesse.Scheduling.Prioritätsscheduling]]
- [[Betriebssysteme.Prozesse.Scheduling.Multi-Level_Feedback_Queue]]
