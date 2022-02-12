
## DDL

### Create

```sql
CREATE TABLE Reserves ( sid INTEGER ,
bid INTEGER,
day DATE,
PRIMARY KEY (sid,bid),
FOREIGN KEY (sid) REFERENCES Sailors, FOREIGN KEY (bid) REFERENCES Boats(bid));
```

```sql
CREATE VIEW view [(attribute-list)] AS table-expression
```

### Alter

```sql
 ALTER TABLE base-table ADD column-definition
```

## DML

### Insert

```sql
INSERT INTO table [(attribute-list)] {
    VALUES (value-list) | SELECT-QUERY
}
```

### Select

```sql
SELECT * | [columns]
FROM table [AS id]
JOIN table [AS id] on id.foo = id.bar
WHERE <WHERE-CLAUSE>
ORDER BY <column> [ASC|DESC]
GROUP BY <columns>
HAVING <group-columns-clause>
```

- `LIKE`
    - `_` - ein beliebiges Zeichen
    - `%` - 0 oder mehr beliebige Zeichen

## Funktionen

- String
    - `LOWER`
    - `UPPER`
    - `INITCAP`
    - `CONCAT`
    - `SUBSTR`
    - `LENGTH`
    - `INSTR`
    - `LPAD`
- Numbers
    - `ROUND`
    - `TRUNC`
    - `MOD`
- Date
    - `NEXT_DAY`
    - `LAST_DAY`
    - `ADD_MONTHS`
- NULL
    - `NVL(value, default)`
- Konvertierung
    - `TO_NUMBER`
    - `TO_CHAR`
    - `TO_DATE`

## Mengenoperationen
- `UNION` ($A \cup B$)
- `INTERSECT` ($A \cap B$)
- `EXCEPT` ($A - B$)

## Where-Operatoren
- `(NOT) IN`
- `(NOT) EXISTS` (prüft, ob Menge leer ist)
- `(NOT) UNIQUE` (prüft, ob Menge Singleton ist)
- `<op> ANY <set>`
- `<op> ALL <set>`

## Aggregations-Operatoren
- `COUNT([distinct] *)`
- `SUM([distinct] *)`
- `AVG([distinct] *)`
- `MAX(*)`
- `MIN(*)`

## NULL
- Vergleich mit `NULL` ergibt immer `FALSE`
- Aggregationsoperatoren ignorieren `NULL`-Werte
- `COUNT` zählt `NULL`-Werte mit