
# Info

- Prozess mit höherer bekommt CPU
- Prozesse mit gleicher Prio kommen in gemeinsame Queue mit Round-Robin
- Prio der Prozesse wird dynamisch angepasst

## Ansätze
- Neue Jobs erhalten höchtes Prio
- Prozess wird runtergestuft, wenn er mehr als $t_{Zeitscheibe}$ aktiv war
- Zyklisch erhalten alle Prozesse die höchste Priorität (da andere runtergestuft werden)

# Systematik
- Verwalten mehrerer Warteschlangen
    - die nach verschiedenen Schedulingstrategien abgearbeitet werden
    - hierarchisch angeordnet sind
- Zuordnung von Prozessen zu Warteschlangen erfolgt dynamisch



Siehe [[Betriebssysteme.Prozesse.Scheduling.Prioritätsscheduling]]
