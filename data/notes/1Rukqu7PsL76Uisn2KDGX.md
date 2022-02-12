
# Info

- Jeder Prozess bekommt eine Priorität
- Prozess mit höchster Priorität erhält CPU
- Prozesse mit gleicher Prio: [[Betriebssysteme.Prozesse.Scheduling.Round_Robin]] o. [[Betriebssysteme.Prozesse.Scheduling.First_Come_First_Serve]]

## Problem
Starvation

### Lösungsansätze

- Zwei Queues ($Q_{Ready\_High}, Q_{Ready\_Low}$), die abwechselnd bedient werden
- Dynamische Anpassung der Prioritäten
    - Prozesse mit viel I/O bekommen hohe Prio
    - Prozesse die viel CPU-Zeit hatten runterstufen
    - Prozesse die viel Ready-Zeit hatten hochstufen

![Scheduling](/assets/images/2022-01-20-10-18-30.png)