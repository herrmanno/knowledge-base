---
id: yk1wjyIiXHPXnFxuks8x7
title: Erwartungswert
desc: ''
updated: 1644568106663
created: 1644567052344
---

## Diskrete Verteilung

$E(X) = \sum x_k p_k$

Existiert, falls 
$\sum |x_k| p_k = \sum |x_k p_k| < \infty$ gilt

$E(X^2) = \sum x^2 \cdot P(\{X=k\})$

## Stetige Verteilung

$E(X) = \int_{-\infty}^{+\infty} t \cdot f(t) \;\text{d}t$

Existiert, falls 
$E(X) = \int_{-\infty}^{+\infty} |t| \cdot f(t) \;\text{d}t = \int_{-\infty}^{+\infty} |t \cdot f(t)| \;\text{d}t < +\infty$ gilt

$E(X^2) = \int t^2 \cdot f(t)\,dt$

## Transformation

$E(aX + b) = a E(X) + b$

$Y := g(X) \rightarrow E(Y) = \begin{cases}
    \sum_x g(x) \cdot P(\{X=k\}) \\
    \int_{-\infty}^{+\infty} g(t) \cdot f(t) \;dt
    \end{cases}$

$E(X \cdot Y) = E(X) \cdot E(Y)$, falls $X, Y$ stochastisch unabhängig