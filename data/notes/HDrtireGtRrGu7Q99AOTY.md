
## 1. Normalform

> Ein Relationenschema R ist in 1NF genau dann, wenn all seine Wertebereiche nur atomare Werte besitzen. Atomar heißt hier: keine Mengen oder Tupel von Werten.

- Jedes verschachtelte Tupel muss eigene Relation (Tabelle) sein
- Schlüssel der übergeordneten Relation wird an Kindrelation angefügt

## 2. Normalform

> Ein Relationenschema R ist in 2NF, wenn es in 1NF ist und jedes Nicht-Primärattribut voll funktional von jedem Schlüssel- kandidaten von R abhängt.

Primäratribut
- Attribut eines Relationenschemas,  das zu mindestens einem Schlüsselkandidaten des Schemas gehört

### Überführung

1. Bestimme funktionale Abhängigkeiten zwischen Nicht- Primärattributen und Schlüsselkandidaten.  2.
Eliminiere partiell abhängige Attribute und fasse sie in eigener Relation zusammen (unter Hinzunahme
der zugehörigen Primärattribute)

## 3. Normalform

> Ein Relationenschema R ist in 3NF, wenn es in 2NF ist und jedes Nicht-Primärattribut von keinem Schlüsselkandidaten von R transitiv abhängig ist.

Transitive Abhängigkeit
- Eine Attributmenge $Z$ von Relationenschema $R$ ist transitiv abhängig von einer Attributmenge
$X$ in $R$, wenn gilt:
- $X$ und $Z$ sind disjunkt
- Es existiert eine Attributmenge $Y$ in $R$, so daß gilt:
    - $X \to Y, Y \to Z, \neq (Y \to X), Z \not \subset Y$

## Boyce/Codd-Normalform (BCNF)

> Ein Relationenschema R ist in BCNF, wenn jeder Determinant ein Schlüsselkandidat von R ist.
>
> Ein Attribut (oder eine Gruppe von Attributen), von dem andere voll funktional abhängen, heißt
Determinant.
