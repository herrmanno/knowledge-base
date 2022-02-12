
## Block

### Anonymous

```sql
[DECLARE]
BEGIN --statements
[EXCEPTION]
END;
```

### Procedure

```sql
PROCEDURE name IS
[DECLARE]
BEGIN --statements
[EXCEPTION]
END;
```

### Function

```sql
FUNCTION name
RETURN datatype
IS
[DECLARE]
BEGIN --statements
RETURN value;
[EXCEPTION]
END;
```

## Variables

```sql
DECLARE
v_hiredate DATE;
v_deptno NUMBER(2) NOT NULL := 10;
v_location VARCHAR2(13) := 'Atlanta';
c_comm CONSTANT NUMBER := 1400;
foo table.col%TYPE;
bar foo%TYPE;
```

## SQL-Attribute

| Attribute | Bedeutung |
|-----------|------------|
|`SQL%ROWCOUNT` | Anzahl Zeilen, die vom letzten SQL- Befehl betroffen ist |
| `SQL%FOUND` | Boolesches Attribut, ist gleich TRUE, wenn der letzte SQL-Befehl mehr als eine Zeile betrifft |
| `SQL%NOTFOUND` | Boolesches Attribut, ist gleich TRUE, wenn der letzte SQL-Befehl überhaupt keine Zeile betrifft |
| `SQL%ISOPEN` | FALSE, weil PL/SQL implizite Cursor unmittelbar nach Ausführung schließt |

## Stored Procedures

```sql
CREATE [OR REPLACE] PROCEDURE procedure_name
(argument1 [IN|OUT|IN OUT] datatype1,
 argument2 [IN|OUT|IN OUT] datatype2,
...
IS [AS]
PL/SQL Block;
```

## Stored Functions

```sql
CREATE [OR REPLACE] FUNCTION function_name
(argument1 datatype1,
 argument2 datatype2,
...
RETURN datatype
IS [AS]
PL/SQL Block;
```

## Vergleich Prozedur <> Funktion

| Prozedur | Funktion |
|-|-|
|Ausführen als PL/SQL Befehl | Aufruf als Teil eines Ausdrucks |
| Kein RETURN Datentyp | RETURN Datentyp |
| Kann einen oder mehrere Werte zurückgeben | Muss einen Wert zurückliefern |
| Schachtelung: Aufruf einer Prozedur innerhalb einer Prozedur | Schachtelung: Argument der Funktion kann selbst das Ergebnis einer Funktion sein |

## [[Datenbanken.Trigger]]