---
id: qaPJpWwN07BAcU6IM5N0y
title: Empirische Varianz
desc: ''
updated: 1644408183704
created: 1644407507275
---

## Empirische Varianz
$\tilde{s}^2 = \frac{1}{n} \sum_{j=1}^n (x_j - \overline{x})^2$

bzw. **Modifizeirte** Varianz
$s^2 = \frac{1}{n-1} \sum_{j=1}^n (x_j - \overline{x})^2$

## Empirische Standardabweichung
$\tilde{s} = \sqrt{\tilde{s}^2}$

bzw. **Modifizeirte** Standardabweichung
$s = \sqrt{s^2}$

## Transformation

Für $y_j = ax_j + b$ gilt  
$\tilde{s}_Y^2 = a^2 \tilde{s}_X^2$ und $\tilde{s}_Y = |a| \tilde{s}_X$

## (Empirischer) Variationskoeffizient
- Maßstabsunabhängiges Streuungsmaß, das zum Vergleich unterschiedlicher Streuungen geeignet ist
- Es gilt: $0 \leq v \leq \sqrt{n - 1}$
- Geeignet für metrisch skalierte Merkmale

$v := \frac{\tilde{s}}{\overline{x}}$