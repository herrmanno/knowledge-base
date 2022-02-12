
## Ausprägungen
- Tupelrelationenkalkül
- Domänenrelationenkalkül

Ausdrücke im Kalkül heißen **Formeln**. Ein Antworttupel ist eine Zuweisung, für die die Formel
*true* ergibt.

## Tupelrelationenkalkül (TRK)

Variablen bezeichnen Tupel (d.h. werden daran gebunden)

### Konzepte
- Query: $\{T \,|\, p(T)\}$, mit
    - $T$ Tupelvariable
    - $p(T)$ Formel, die $T$ beschreibt
- Resultat: Menge der Tupel $t$, für die die Formel $p(T)$ *true* ergibt
- Formel: rekursiv definiert, aufbauend auf **atomaren Formeln**

### Atomare Formeln
- $R \in R_{Name}$
- $R.a~op~S.b$
    - $op \in\, <,>,=,\leq,\geq,\neq$

### Formel
- Atomare Formel
- $\neg q, q \lor p, q \land p$
- $\exist R~(p(R))$, $X$ *frei* in $p(X)$
- $\forall R~(p(R))$, $X$ *frei* in $p(X)$

### Beispiele
- $\{P \,|\, \exists S \in Sailors~\exists B \in Boats~(S.boatId = B.BoatId \land P.name = S.name)\}$


## Domänenrelationenkalkül (DRK)

Variablen bezeichnen Domänenelemente (Wertebereiche von Attributen)

### Beispiele

Namen und Alter aller Segler mit einem Rating größer sieben
- $\{\langle I,N,T,A \rangle \mid \langle I,N,T,A \rangle \in Sailors \land T.rating > 7 \}$

## Relationale Vollständigkeit

Eine Query Language (z.B. SQL) kann jede Anfrage ausdrücken, die sich in Relationenalgebra /
Relationenkalkül ausdrücken läßt.