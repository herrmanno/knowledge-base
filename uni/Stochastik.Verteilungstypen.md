---
id: BUfdBfKWQY2UOSLFkJCVO
title: Verteilungstypen
desc: ''
updated: 1644570177381
created: 1644523109637
---

## Stetige Gleichverteilung

$f(t) = \frac{1}{b-a}, \;\text{falls } t \in [a,b]$

$F(x) = \frac{x - a}{b - a}$

$E(X) = \frac{a + b}{2}$

$Var(X) = \frac{(b - a)^2}{12}, \; \sigma(X) = \frac{\sqrt{3}}{6} (b - a)$

## Binomialverteilung (Ziehen mit Zurücklegen ohne Reihenfolge)
$X \sim \text{Bin}(n,p)$

$P(\{X = k\}) = \binom{n}{k} p^k (1-p)^{n-k}$

$E(X) = np$

$Var(X) = np (1-p)$

$X + Y \sim Bin(n+m,p)$

## Hypergeometrische Verteilung (Ziehen ohne Zurücklegen ohne Reihenfolge)
$X \sim Hyp(N,M,n)$

$P(\{X=k\}) = \frac{\binom{M}{k} \binom{N-M}{n-k}}{\binom{N}{n}}$

## Poisson-Verteilung (Anzahl eines Ereignisses während eines Zeitfensters)
$X \sim Poi(\eta)$

$P(\{X=k\}) = \frac{\eta^k}{k!} exp(-\eta)$

$E(X) = \eta$

$X + Y \sim Poi(\eta_1 + \eta_2)$

## Geometrische Verteilung (Anzahl Misserfolge in Bernoulli-Experiment)
$X \sim Geo(p)$

$P(\{X=k\}) = (1-p)^k \cdot p$

$Y := X + 1 \to Y \sim \widetilde{Geo}(p)$

## Normalverteilung
$X \sim N(a, \sigma^2)$

$E(X) = a$

$Var(X) = \sigma^2$

$X + Y \sim N(a_1 + a_2, \sigma_1^2 + \sigma_2^2)$

$\phi(t) = f(t) = \frac{1}{\sqrt{2\pi}} exp(-\frac{t^2}{2})$  
$\phi(t) = \phi(-t)$  

$\Phi = F(x) = \frac{1}{2\pi} \int_{-\infty}{x} exp(-\frac{t^2}{2})\; dt$  
$\Phi(-x) = 1 - \Phi(x)$

$X \sim N(a,\sigma^2) \Rightarrow  P(\{X=k\}) = \Phi(\frac{x - a}{\sigma})$

## Exponentialverteilung (Lebensdauerverteilung)
$X \sim Exp(\gamma)$

$E(x) = \frac{1}{\gamma}$

$Var(X) = \frac{1}{\gamma^2}$

$x_{med} = \frac{ln 2}{\gamma}$

$F(x) = \begin{cases}1 - exp(-\gamma x), & \text{falls } x \geq 0 \\ 0, & \text{sonst}\end{cases}$

$f(t) = \begin{cases}\gamma exp(-\gamma t), & \text{falls } t \geq 0 \\ 0, & \text{sonst}\end{cases}$

## Gammaverteilung
$X \sim Ga(\gamma, \alpha)$

$E(X) = \frac{\alpha}{\gamma}$

$Var(X) = \frac{\alpha}{\gamma^2}$

## Erlangverteilung

$F(x) = 1 - \sum_{k=0}^{n -1} \frac{(\gamma x)^k}{k!} exp(-\gamma x)$, falls $x \geq 0$

## $\chi^2$-Verteilung
$X \sim \chi^2_n$, $n := \text{Anzahl d. Freiheitsgrade}$

$E(X) = n$

$Var(X) = 2n$

## t-Verteilung (Student-Verteilung)
$X \sim t_n$, $n := \text{Anzahl d. Freiheitsgrade}$

$E(X) = 0$

$Var(X) = \frac{n}{n-2}$

Für große $n$ gilt: $t_n \approx N(0,1)$