---
id: 531BnTAsV0DoHg5lQqXev
title: Trigger
desc: ''
updated: 1643802364165
created: 1643802031667
---

## Eigenschaften
- Zeitpunkt: `BEFORE` | `AFTER`
- Auslöser: `INSERT`| `UPDATE` | `DELETE`
- Tabelle: `ON <table>`
- Typ: Zeilen- oder Befehlsorientiert
- Einschränkung: `WHEN`-Klausel

## Syntax

```sql
CREATE [OR REPLACE] TRIGGER trigger_name
timing event1 [OR event2 OR event3]
ON table_name
[REFERENCES OLD AS old | NEW AS new]
[FOR EACH ROW]
[WHEN condition]
PL/SQL block;
```
