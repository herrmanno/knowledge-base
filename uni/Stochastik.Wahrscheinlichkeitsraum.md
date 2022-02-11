---
id: YmObnxqnvXX9KfjtzmmKY
title: Wahrscheinlichkeitsraum
desc: ''
updated: 1644511310940
created: 1644503981560
---

## Kolmogorovsche Axiomatik
-  $\Omega$ ist nichtleere Grundmenge der Elementarereignisse
- $\mathfrak{U}$ ist $\sigma$-Algebra in $\Omega$
- $P$ ist ein Maß auf $(\Omega, U)$ mit $P \,:\, U \to [0,\infty]\;, P(\Omega) = 1$

## Mengenidentitäten

- $P(\Omega \setminus A) = 1 - P(A)$
- $P(B \setminus A) = P(B) - P(A \cap B)$
- $P(A \cup B) = P(A) + P(B) - P(A \cap B)$
- $P(A|B) = \frac{P(A \cap B)}{P(B)}$
- $P(\overline{A}|B) = 1 - P(A|B)$
- $P(A|B) = \frac{P(B|A) \cdot P(A)}{P(B)}$
- $P(A \cap B) = P(A|B) \cdot P(B) = P(B|A) \cdot P(A)$

## Laplace-Wahrscheinlichkeitsraum
Zufallsexperiment, bei der jedes Elementarereignis die selbe Wahrscheinlichkeit besitzt.  
Das Wahrscheinlichkeitsmaß $P$ nennt man **diskrete Gleichverteilung** mit  
$P(A) = \frac{|A|}{|\Omega|}$

## Stochastische Unabhängigkeit
$P(A \cap B) = P(A) \cdot P(B)$ bzw.  
$P(A|B) = P(A) \land P(B|A) = P(B)$