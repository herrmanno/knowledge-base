---
id: AAo9KOryBqtQOFIAW9Ewv
title: Logischer Entwurf
desc: ''
updated: 1643487124557
created: 1643484521760
---

## Funktionale Abhängigkeiten

FD: $X \to Y := \forall u \in R \; \forall v \in R (u[x] = v[x] \rightarrow u[y] = v[y])$

``Wenn zwei Tupel in *x* übereinstimmen, stimmen sie auch in *y* überein''

### Volle funktionale Abhängigkeit

$A_1, A_2, \ldots, A_n \to B_1, B_2, \ldots, B_m$

$B$ ist voll funktional von $A$, wenn B funktional abhängig von A, aber nicht funktional
abhängig von einer echten Teilmenge von $A$ ist.

### Partielle funktionale Abhängigkeit

$A \to B$ ist eine partielle funktionale Abhängigkeit, wenn ein $A_i$ existiert, sodass

$(A - \{A_i\}) \to B$ gilt.

### Armstrong'sche Axiome

- Reflexivität: $X \subseteq Y \rightarrow (Y \to X)$
- Augmention: $(X \to Y) \rightarrow (\forall Z. XZ \to YZ)$
- Transivität: $(X \to Y) \land (Y \to Z) \rightarrow (X \to Z)$

[[Datenbanken.Normaleformen]]

### Minimalabdeckung

Minimalabdeckung $G$ für eine Menge von FDs $F$ erfüllt folgende Bedingungen:
- $F^+ = G^+$
- $\forall g \in G: g \in (X \to A), A\text{: einzelnes Attribut}$

## Dekomposition

Aufteilen eines Relationschemas in mehrere Teilschemata

### Verlustfreie Dekomposition

Die Dekomposition von $R$ in $X$ und $Y$ ist verlustfrei bezüglich $F$ genau dann wenn die Hülle von
$F$, $F^+$, folgende FDs enthält:
- $X \cap Y \to X$ oder
- $X \cap Y \to Y$

### Abhängigkeitsbewahrende Dekomposition

Dekomposition von $R$ in $X$ und $Y$ ist abhängigkeitsbewahrend wenn gilt

$(F_X \cup F_Y)^+ = F^+$

mit $F_x = \{ (U \to V) \in F^+ \mid U, V \in X\}$ := Projektion einer Menge von FDs

Wenn $R$ in $X$, $Y$ und $Z$ zerlegt wird, und alle FDs eingehalten werden, die in $X$, in $Y$ und
in $Z$ gelten, dann müssen alle FDs, die in $R$ gegeben waren, auch gelten