---
id: R2YlDjMYXwcue7I81Lffe
title: Lagemaße
desc: ''
updated: 1644407369468
created: 1644406178112
---

- Lineare Transformation erhält alle drei Lagemaße (arithm. Mittle, Median, Modus)
- Lageregeln:
    - Symmetrisch: $\overline{x} \sim x_{med} \sim x_{mod}$
    - Linksschief: $\overline{x} < x_{med} < x_{mod}$
    - Rechtsschief: $\overline{x} > x_{med} > x_{mod}$

## Arithmetisches Mittel
$\overline{x} := \frac{1}{n} \sum x_j$, mit  
$\sum_(x_j- \overline{x}) = 0$

Ergibt nur bei metrische Skalierung Sinn.

## Median
- mindestens 50% der Daten sind kleiner oder gleich $x_{med}$
- mindestens 50% der Daten sind größer oder gleich $x_{med}$

$x_{med} := \begin{cases}
    x_{(\frac{n+1}{2})} & \text{für ungerade } n\\
    \frac{1}{2} (x_{(\frac{n}{2})} + x_{(\frac{n}{2} + 1)}) & \text{für gerade } n
\end{cases}$

Ergibt nur bei Ordinalskalierung (und aufwärts) Sinn

### Quantil
$\tilde{x}_q = x_{(\lfloor nq \rfloor + 1)}, \text{falls }nq\text{ nicht ganzzahlig ist}$, sonst  
$\tilde{x}_q = \{x \vert x \in [x_{(nq)}, x_{(nq+1)}] \} \text{ oder } \frac{1}{2} (x_{(nq)} + x_{(nq + 1)})$

## Modus
Ausprägung, deren Häufigkeit am größten Ist

$x_{mod}$

## Geometrische Mittel
Anwendung, wenn Werte *Wachstumskennzahlen* sind (wie Lohnerhöhungen, Leistungssteigerungen)

$\overline{x}_G := (x_1,\ldots,x_n)^\frac{1}{n}$

## Harmonisches Mittel
Anwendung, wenn Werte *Beziehungszahlen* darstellen und verhältnisskaliert sind (z.B. falls Größe
im Zähler des Werts zur Gewichtung verwendet wird)

$\overline{x}_H := \frac{1}{\frac{1}{n} \sum \frac{1}{x_j}}$