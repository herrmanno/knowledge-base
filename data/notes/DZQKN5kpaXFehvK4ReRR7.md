
## Ziele
- Vermeidung von Diebstahl und Fälschung
- Geheimhaltung
- Wahrung der Privatsphäre
- Integrität
- Verfügbarkeit

## Zugriffskontrolle (Autorisierung)
- Vergabe von Zugriffsrechten auf DB-Objekten
- Subjekte (B)
     - Benutzer(gruppen)
     - Andere Clients
- Objekte (O)
    - Anwendungs- und Dienstprogramme
    - DB-Objekte
- Operationen (P)
    - Lesen, Ändern, Erzeugen, Ausführen, Erteilen von Zugriffsrechten

$\Rightarrow$ Berechtigungsmatrix $\langle B_j, O_j, [P_i] \rangle$

## Klassifikation der Autorisierung

### Dezentrale Vergabe von Rechten durch Eigentümer
*Besitzer* eines Objekts vergibt Rechte für dieses Objekt

## SQL-Grant

```sql
GRANT privileges ON object TO user [WITH GRANT OPTION]
```
```sql
REVOKE [GRANT OPTION FOR] privileges ON object FROM users {RESTRICT | CASCADE}
```
mit Privilegien
- `SELECT`
- `INSERT [colname]`
- `UPDATE [colname]`
- `DELETE`
- `REFERENCES [colname]`
- `ALL`
- `EXECUTE` (für Funktionen und Prozeduren)

### Rollenbasierte Autorisierung

```sql
CREATE ROLE role
GRANT privileges ON object TO rolle
GRANT rolle TO users
```

### Mandatory Access Control
Systemweite Policy, die nicht durch Benutzer verändert werden kann

- Jedes DB-Objekt hat eine **Security-Klasse**
- Jedes Subjekt hat eine **Clearance** für eine bestimmte Security-Klasse
- Regeln für Security-Klassen und Clearances steuern Read/Write-Operationen auf Objekten