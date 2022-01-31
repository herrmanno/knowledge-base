---
id: OtZNWHfqgbl5LHdERT013
title: ProcessControlBlock
desc: ''
updated: 1642667360228
created: 1642667205436
---

- Speicherbereich in dem alle mit dem Prozess assoziierten Referenzen ind Informationen gespeichert werden.
- Kann nur vom BS verändert werden
- Beinhaltet
    - Prozess-ID ($P_{ID}$)
    - Besitzer
    - Tabelle geöffneter Dateien
    - E/A Assoziationen
     -Netzwerk- und Interprozess-Abstraktionen
     - Speicherbereiche
        - Stack-Pointer
        - Heap-Pointer
        - [MMIO](https://de.wikipedia.org/wiki/Memory_Mapped_I/O)
