---
id: LCssW0pj2VndNSGLGBji2
title: First Come First Serve (FCFS)
desc: ''
updated: 1642671066276
created: 1642669073090
---

# Info
- einfaches Verfahren ohne Fristen
- keine gestufte Ressourcenzuordnung -> kein echtes Multitasking
- Abschätzung der Prozesslaufzeit erlaubt Abschätzung der Wartezeit

## Zusammenfassung
Ein einfacher ''non-preemptive'' Algorithmus für die Abarbeitung automatisierter Jobs.

### Vorteile
- gut bei mehrheitlich rechenintensiven Prozessen ohne Zeitvorgaben

### Nachteile
- schlecht bei heterogenen Prozessen
    - rechenintensive Prozesse dominieren
    - IO-lastige Prozesse werden benachteiligt
- **Nicht** gestufte Ressourcenteilung
- **Nicht** Einhaltung von Fristen



## Scheduling-Diagramm

![FSFS_Scheduling](/assets/images/2022-01-20-09-59-03.png)


## FCFS mit ''wait''

`wait` führt zu $P_i = ``blocked''$

Bei wiedereintritt: $FCFS: sort(Q_{ready}, P_{id}(T_{Startzeit}), ASC);$

## FCFS mit ''$Q_{Ready}.append$'' (FIFO)

Bei wiedereintritt: $FCFS: Q_{Ready}.append;$

**Kann zu _Verhungern_ führen**
