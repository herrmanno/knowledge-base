---
id: GRvxv332whjrUYDFp1Ziq
title: Datenbanken
desc: ''
updated: 1643645039015
created: 1643477089680
---

## Vorteile von Datenbanken ggü. Dateisystem
- Effizienz
- Keine Redundanz
- Datenintegrität
- Datensicherheit
- Zugriffskontrolle

## Abstraktionsebenen

### Views
- Ausschnitt des konzeptuellen Schemas

### Konzeptuelles (logisches) Schema
- integrierte, logische Sicht auf gesamte Daten
- keine Details über Speicherstrukturen oder Zugriffspfade

### Physisches Schema
- Daten in Form von Datensätzen (Records)
- Spezifische Zugriffspfade
- Abbildung logischer Records auf Speicherstrukturen (physische Records, Seiten)

## Datenunabhängigkeit

### Logische Datenunabhängigkeit
- Änderungen in logischer Struktur der Daten sind für Anwendungen irrelevant (weil durch
Views abstrahiert)

### Physische Datenunabhängigkeit
- Änderungen an der Speicherstruktur sind für das konzeptuelle (logische) Schema irrelevant

## Weitere Themen

[[Datenbanken.ER-Modell]]
[[Datenbanken.Relationenmodell]]
[[Datenbanken.Logischer_Entwurf]]
[[Datenbanken.Relationenalgebra]]
[[Datenbanken.Relationenkalkül]]
[[Datenbanken.SQL]]
