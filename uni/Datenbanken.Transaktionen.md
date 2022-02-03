---
id: PTcli50jdhX8B4XutVFfm
title: Transaktionen
desc: ''
updated: 1643877542930
created: 1643875169397
---

## ACID

### Atomicity
Eine Transaktion wird vollständig oder gar nicht ausgeführt

### Consistency
Eine Transaktion hinterlässt die Datenbank in einem konsistenten Zustand

### Isolation
Aktionen einer Transaktion sind für andere Transaktionen nicht sichtbar

### Durability
Folgen einer Transaktion sind persistent (auch im Falle eines Systemfehlers)


## Schedules

### Serieller Schedule
Keine Aktionen aus unterschiedlichen Transaktionen ineinander verschachtelt

### Äquivalente Schedules
Effekt der Ausführung zweier Schedules führt zu identischem Datenbankzustand

### Serialisierbarer Schedule
Schedule, der äquivalent zu irgendeiner seriellen Ausführung der Transaktion ist

## Anomalien

### Verlorengegangene Änderungen (Lost updates)
Gleichzeitige Änderung desselben Objekts durch zwei Transaktionen

![](/assets/images/2022-02-03-09-12-24.png)

### Zugriff auf *schmutzige Daten* (Dirty Read)

Lesen von Daten, die in einer anderen Transaktion verändert wurden
- Andere Transaktion wird u.U. zurückgerollt

![](/assets/images/2022-02-03-09-12-57.png)

### Nicht-wiederholbares Lesen (Unrepeatable Read)
Eine Transaktion sieht (aufgrund paralleler Änderungen) unterschiedliche Zustände eines Objekts

![](/assets/images/2022-02-03-09-13-08.png)

### Phantom-Problem

1. Lesen von Menge mit Prädikat $P$
2. Parallele Änderung an Objekten, die unter $P$ fallen
3. Folge: Phantom-Objekte, die durch parallele Vorgänge in Ergebnismenge aus 1. auftauchen oder verschwinden

## Zwei-Phasen-Sperrverfahren (2-Phase-Locking)

### 1. Phase: Wachstumsphase
Transaktion darf Sperren anfordern, aber keine freigeben

### 2. Phase: Schrumpfungsphase
Transaktion darf Sperren freigeben, aber keine neuen anfordern

### Problem
- Bei Systemausfall kann es zu kaskadierendem Abort komme
    - Transaktionen, die schon freigegebene Daten haben (und vielleicht selbst schon normal beendet
    wurden) müssen zurückgesetzt werden

## Striktes Zwei-Phasen-Sperrverfahren (2-Phase-Locking)

Vermeidung von kaskadierendem Abort, falls Systemabsturz in der Freigabephase

### Protokoll
- Jede Transaktion muss eine **S**-Sperre (shared lock) auf dem Objekt vor dem Lesen erwerben und
eine **X**-Sperre (exklusive lock) vor dem Schreiben
- Alle Sperren werden bei Beendigung der Transaktion (Commit) freigegeben
- Wenn eine Transaktion eine X-Sperre auf einem Objekt hält kann keine andere Transaktion eine Sperre
auf diesem Objekt erwerben

$\Rightarrow$ Nur striktes 2PL erlaubt serialisiebare Schedules

## Zurücksetzen einer Transaktion

### Kaskadierender Abort
- Führen von Log-Daten einer Transaktion (Aufzeichnung aller Write-Aktionen)
- Auch nutzbar für die Wiederherstellung der Daten bei System-Crash (Recovery): alle Transaktionen,
die zum Zeitpunkt des System-Crashs aktiv waren werden beim Wiederanlauf zurückgesetzt

### Log-Datei
Speicherung von Änderungsaktionen mit Parametern (alter und neuer Wert)
- Muss auf Platte gespeichert werden vor der geänderten Seite

## 3 Phasen im Recovery-Algorithmus

### Analyse-Lauf
- Sequentielles Lesen der Log-Datei vom letzten Checkpoint bis zu ihrem Ende
- Bestimme die zum Checkpoint-Zeitpunkt laufenden Transaktionen
- Bestimme davon Gewinner (Ts mit Commit-Eintrag im Log) und Verlierer (Ts mit Rollback)

### Redo-Lauf
- Wiederhole die Änderungen, welche noch nicht in den betroffenen Seiten vorliegen (Lese Log dabei
von hinten nach Vorne)

### Undo-Lauf
- Zurücksetzen der Verlierer-Transaktionen, die während des Crash aktiv waren (durch schreiben des
*before value*, der im Log-Satz steht)
- Lesen des Logs von vorne nach hinten, bis zum Beginn der ältesten Transaktion, die beim letzten
Checkpoint aktiv war