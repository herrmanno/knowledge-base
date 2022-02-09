---
id: 5Dqt8jIelsfUckZKjH1XK
title: Empirische Unabhängikeit
desc: ''
updated: 1644409095811
created: 1644408195274
---

## Empirische Unabhängigkeit
Merkmale $X$ und $Y$ werden **(empirisch) unabhängig** angesehen, wenn (für alle Zellenäufigkeiten)
gilt  
$h_{jk} \approx \frac{1}{n} h_{j\bullet} h_{\bullet k}$

## $\chi^2$-Koeffizient (Pearsons $\chi^2$-Statistik)
- Wenn $X$ und $Y$ unabhängig sind Werte von $\chi^2$ klein (nahe 0), sonst groß
- Nachteil: Wert abhängig von Stichprobenumfang $n$ und Dimenseion der Kontingenztafel

$\chi^2 :=
  \sum_{j=1}^m \sum_{k=1}^l
    \frac{(h_{jk} - \frac{1}{n} h_{j\bullet} h_{\bullet k})^2}
         {\frac{1}{n} h_{j\bullet} h_{\bullet k}}$

## Kontingenzmaß nach Cramér

$V := \sqrt{\frac{\chi^2}{n(min\{m,l\} - 1)}}$