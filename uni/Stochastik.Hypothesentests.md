---
id: jTL7qxkVgAqSyzuDMs3dG
title: Hypothesentests
desc: ''
updated: 1644580551165
created: 1644578486512
---

## Allgemein

$H_0$: Nullhypothese  
$H_1$: Alternativhypothese  
$\alpha$: Signifikanznivea (*Irrtumswahrscheinlichkeit*)  
$1 - \alpha$: Konfidenzniveau

## Einfacher Gauß-Test
$X \sim N(a, \sigma^2)$, $a$ unbekannt, $\sigma^2$ bekannt

### Prüfgröße
$T = \frac{\overline{X}_n - a_0}{\sigma} \sqrt{n} \qquad$
mit $\overline{X}_n = \frac{1}{n} \sum_{k=1}^n X_k$

### Ablehnungsbereich
$H_0: a = a_0$  
$K_1 = (-\infty, -z_{1 - \frac{\alpha}{2}}) \cup (z_{1 - \frac{\alpha}{2}}, +\infty)$  

$H_0: a \leq a_0$  
$K_1 = (z_{1 - \alpha}, +\infty)$  

$H_0: a \geq a_0$  
$K_1 = (-\infty, -z_{1 - \alpha})$  

## Einfacher t-Test
$X \sim N(a, \sigma^2)$, $a$ unbekannt, $\sigma^2$ unbekannt

### Prüfgröße
$T = \frac{\overline{X}_n - a_0}{S_n} \sqrt{n} \qquad$
mit $\overline{X}_n = \frac{1}{n} \sum_{k=1}^n X_k,\; S_n = \sqrt{\frac{1}{n-1} \sum_{k=1}^n (X_k - \overline{X}_n)^2}$

### Ablehnungsbereich
$H_0: a = a_0$  
$K_1 = (-\infty, -t_{1 - \frac{\alpha}{2};n-1}) \cup (t_{1 - \frac{\alpha}{2};n-1}, +\infty)$  

$H_0: a \leq a_0$  
$K_1 = (t_{1 - \alpha;n-1}, +\infty)$  

$H_0: a \geq a_0$  
$K_1 = (-\infty, -t_{1 - \alpha;n-1})$  

## $\chi^2$-Streuungstest (bei bekanntem Erwartungswert)
$X \sim N(a, \sigma^2)$, $a$ bekannt, $\sigma^2$ unbekannt

### Prüfgröße
$T =  \frac{n}{\sigma_0^2} \widetilde{S_n^2} \qquad$
mit $\widetilde{S_n^2} = \frac{1}{n} \sum_{k=1}^n (X_k - a)^2$

### Ablehnungsbereich
$H_0: \sigma = \sigma_0$  
$K_1 = [0, \chi^2_{\frac{\alpha}{2};n}) \cup (\chi^2_{1 - \frac{\alpha}{2};n}, +\infty)$  

$H_0: \sigma \leq \sigma_0$  
$K_1 = (\chi^2_{1 - \alpha;n}, +\infty)$  

$H_0: \sigma \geq \sigma_0$  
$K_1 = [0, \chi^2_{1 - \alpha;n})$  

## $\chi^2$-Streuungstest (bei unbekanntem Erwartungswert)
$X \sim N(a, \sigma^2)$, $a$ unbekannt, $\sigma^2$ unbekannt

### Prüfgröße
$T =  \frac{n-1}{\sigma_0^2} S_n^2 \qquad$
mit $\overline{X}_n = \frac{1}{n} \sum_{k=1^n} X_k,\;
      S_n^2 = \frac{1}{n-1} \sum_{k=1}^n (X_k - \overline{X}_n)^2$

### Ablehnungsbereich
$H_0: \sigma = \sigma_0$  
$K_1 = [0, \chi^2_{\frac{\alpha}{2};n-1}) \cup (\chi^2_{1 - \frac{\alpha}{2};n-1}, +\infty)$  

$H_0: \sigma \leq \sigma_0$  
$K_1 = (\chi^2_{1 - \alpha;n-1}, +\infty)$  

$H_0: \sigma \geq \sigma_0$  
$K_1 = [0, \chi^2_{1 - \alpha;n-1})$  

## Fehler

### Fehler 1. Art
$H_0$ wahr, aber Hypothese abgelehnt

### Fehler 2. Art
$H_1$ wahr, aber Hypothese angenommen