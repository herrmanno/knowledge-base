
## Operatoren
- Selektion $\sigma$
- Projektion $\pi$
- Kreuzproduk $\times$
- Mengendifferenz $-$
- Vereinigung $\cup$
- Zusätzlich:
    - Durchschnitt
    - Join $><$
    - Division
    - Umbenennung $\rho$

Jede Operation liefer eine Relation als Wert zurück.    

### Beispiele

- $\sigma_{rating > 9} (T1)$
- $\pi_{id,name} (\sigma_{rating > 9} (T1))$
- $\rho(K(1 \to ID_1, 5 \to ID_2), R \times S)$
- $R ><_{R.id = S.id} S$

## Joins

### Verlustfrei
Ein Join ist verlustfrei, wenn alle Tupel von $R$ und $S$ am Join teilnehmen.

### Equi-Join
Vergleichsrelation zwischen $R$ und $S$ ist ``$=$''

### Natural-Join
Equi-Join über alle gleichnamigen Spalten

## Division
Es sei $(x,y) \in A,\; (y) \in B$

Dann gilt $A/B = \{(x) \,|\, \exists (x,y) \in A \; \forall (y) \in B \}$

D.h. $A/B$ liefert alle $x$ Werte aus $A$ zurück, wenn es für jedes $y$ in $B$ auch ein $(x,y)$
in $A$ gibt.