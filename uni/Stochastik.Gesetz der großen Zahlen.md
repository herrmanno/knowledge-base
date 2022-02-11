---
id: DHUMpZlChY0RAFfjYY0qY
title: Gesetz der großen Zahlen
desc: ''
updated: 1644571485867
created: 1644570192587
---

## Schwaches Gesetz der großen Zahlen

Sei $X_n \sim \text{Bin}(n,p)$, dann gilt:

$\lim_{n\to +\infty} P(\{|\frac{1}{n} X_n - p| < \epsilon\}) = 1$

## Ungleichung von Cebysev

Für eine Zufallsgröße $X$ mit existierendem Erwartungswert $E(X)$ gilt:

$P(\{|X - E(X)|\} \geq \epsilon) \leq \frac{Var(X)}{\epsilon^2}$

## Schwaches Gesetz der großen Zahlen von Chincin

Sei $(X_k)_{k=1}^\infty$ eine Folge von Zufallsgrößen mit identischem Erwartungswert $a$, dann gilt:

$\lim_{n \to +\infty} P(\{|\frac{1}{n} \sum_{k=1}^n X_k - a| < \epsilon\}) = 1$

## Zentraler Grenzwertsatz von Moivre-Laplace

Seien $X_n \sim \text{Bin}(n,p)$, sowie $Z_n := \frac{X_n - np}{\sqrt{np(1-p)}}$ für $n \in \mathbb{N}$,
dann gilt:

$\lim_{n \to +\infty} P(\{Z_n \leq x\}) = \Phi(x)$

Faustregel für gute Approximation:  
$np(1-p) > 9$

### Stetigkeitskorrektur

Wenn $X$ diskret verteilt ist sollten Grenzen angepasst werden für besser Werte

$P(\{X=k\}) \approx \Phi(\frac{k + 0.5 - np}{\sqrt{np(1-p)}}) -  \Phi(\frac{k - 0.5 - np}{\sqrt{np(1-p)}})$