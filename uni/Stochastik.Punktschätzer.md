---
id: 3NdpJ60Vc51ALj5L6Gdbw
title: Punktschätzer
desc: ''
updated: 1644576955164
created: 1644576409681
---

**Punktschätzer** $\hat\Theta$ für Parameter $\vartheta$

$T_n = g(X_1,\ldots,x_n)$  
mit $g: \mathbb{R}^n \to M$

**Schätzwert**: $\vartheta \in M$

$\hat\vartheta = g(x_1,\ldots,x_n)$

## Erwartungstreue

### Erwartungstre
$E(T_n) = \vartheta$

### Asymptotisch erwartungstre
$\lim_{n \to \infty} E(T_n) = \vartheta$

## Konsistenz

### Konsistent im quadratischen Mittel
$\lim_{n \to \infty} E((T_n - \vartheta)^2) = 0$

### Schwach konsistent
$\lim_{n \to \infty} P(\{|T_n - \vartheta| < \epsilon\}) = 1$

### Mean Squared Error
$\text{MSE}(T_n, \vartheta) := E((T_n - \vartheta)^2)$