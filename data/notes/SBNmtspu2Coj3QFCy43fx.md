
# Info

Wechsel zwischen Prozessen. Dabei muss als Snapshot festgehalten werden
- General Purpose Register
- Stack Register
- Program Counter
- Statusregister [(Processor Status Word)](https://de.wikipedia.org/wiki/Statusregister)

Diese Informationen werden im [[Betriebssysteme.Prozess.ProcessControlBlock]] gespeichert.

# Ursachen
- TRAP (z.B. Division durch Null)
- Systemcall (Wechsel von Anwendungs- zu BS-Kontext)
- Signal von E/A-Gerät (Wechsel von BS- zu Anwendungs-Kontext)
- Geplanter Prozesswechsel
