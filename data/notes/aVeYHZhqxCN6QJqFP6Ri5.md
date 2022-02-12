
# Infos

[Website](https://rechnernetze.htwk-leipzig.de/~jeanm/edu/operatingsystems/) (Credentials [in OPAL](https://bildungsportal.sachsen.de/opal/auth/RepositoryEntry/20425539586/CourseNode/100545223954335))

# Ziele

- Robustheit
    - Das Betriebssystem soll auch in Fehlersituationen einen zuverlässigen Betrieb des Rechners sicherstellen.
- Isolation und Schutz
    - Jeder Prozess (laufende Anwendung) hat die Illusion, alle Ressourcen des Rechnern exklusiv zu benutzen.
- Effizienz
    - [[Betriebssysteme.Lokalitaetsprinzip]]
- Sicherheit
    - Die Integrität des Systems und der darin gespeicherten Daten sind abhängig davon, dass vom Be- triebssystem Konzepte und Methoden zur Zugangssteuerung und Zugriffssteuerung umsetzt.


# Themen

## Allgemeines

- [[Betriebssysteme.Lokalitaetsprinzip]]

### Ausführungsschichten

- Anwendungsprozesse = Problemstatus
    - **Nicht**:
        - Zugriff auf Speichermedien
        - Maschinenbefehle zum dirketen Hardwarezugriff
- Betriebssystem = Überwacherstatus

### Systemcall

- Ausführung einer BS-Funktion aus einem Anwendungsprozess
- Verursacht [TRAP](https://en.wikipedia.org/wiki/Trap_(computing)) und Kontextwechsel
- Ausführung der BS-Funktion benötigt Überwacherstatus

- [[Betriebssysteme.Prozesse.Scheduling]]
- [[Betriebssysteme.Prozesse.Process_Control_Block]]

## Prozesse

- [[Betriebssysteme.Prozess.Speicheraufbau]]
- [[Betriebssysteme.Prozess.ProcessControlBlock]]
- [[Betriebssysteme.Prozess.Kontextwechsel]]
- [[Betriebssysteme.Prozess.Preemtive_Prozesse]]


## Speichermanagement

- [[Betriebssysteme.Paging]]
- [[Betriebssysteme.Segmentierung]]
- [[Betriebssysteme.RAID]]

## Persistenz

- [[Betriebssysteme.Scanning]]
- [[Betriebssysteme.FAT]]
- [[Betriebssysteme.INode]]

## Sicherheit

- [[Betriebssysteme.Sicherheit.Authentisierung]]
