
## Allgemein
**Konfidenzniveau**: $1 - \alpha$

$X \sim N(a, \sigma^2)$ oder $n \geq 30$ (bekannte Varianz) bzw. $n \geq 40$ (unbekannte Varianz)

$s_n^2 := \frac{1}{n-1} \sum (x_k - \overline{x}_n)^2$  
$\widetilde{s_n^2} := \frac{1}{n-1} \sum (x_k - a)^2$  


## Zweiseitiges Konfidenzintervall für Erwartungswert bei bekannter Varianz
$[\overline{x}_n - z_{1 - \frac{\alpha}{2}} \frac{\sigma}{\sqrt{n}},
  \overline{x}_n + z_{1 - \frac{\alpha}{2}} \frac{\sigma}{\sqrt{n}}]$

## Einseitige Konfidenzintervalle für Erwartungswert bei bekannter Varianz

$[\overline{x}_n - z_{1 - \alpha} \frac{\sigma}{\sqrt{n}}, +\infty)$
bzw. 
$(-\infty, \overline{x}_n + z_{1 - \alpha} \frac{\sigma}{\sqrt{n}}]$

## Zweiseitiges Konfidenzintervall für Erwartungswert bei unbekannter Varianz
$[\overline{x}_n - t_{1 - \frac{\alpha}{2};n-1} \frac{s_n}{\sqrt{n}},
  \overline{x}_n + t_{1 - \frac{\alpha}{2};n-1} \frac{s_n}{\sqrt{n}}]$

## Einseitige Konfidenzintervalle für Erwartungswert bei bekannter Varianz

$[\overline{x}_n - t_{1 - \alpha;n-1} \frac{s_n}{\sqrt{n}}, +\infty)$
bzw. 
$(-\infty, \overline{x}_n + t_{1 - \alpha;n-1} \frac{s_n}{\sqrt{n}}]$

## Zweiseitiges Konfidenzintervall für Varianz bei unbekanntem Erwartungswert
$[
    \frac{n-1}{\chi^2_{1 - \frac{\alpha}{2};n-1}} s_n^2,
    \frac{n-1}{\chi^2_{\frac{\alpha}{2};n-1}} s_n^2
]$

## Einseitige Konfidenzintervalle für Varianz bei unbekanntem Erwartungswert
$[ \frac{n-1}{\chi^2_{1 - \alpha;n-1}} s_n^2, +\infty )$
bzw.
$( 0, \frac{n-1}{\chi^2_{\alpha;n-1}} s_n^2 ]$

## Zweiseitiges Konfidenzintervall für Varianz bei bekanntem Erwartungswert
$[
    \frac{n-1}{\chi^2_{1 - \frac{\alpha}{2};n}} \widetilde{s_n^2},
    \frac{n-1}{\chi^2_{\frac{\alpha}{2};n}} \widetilde{s_n^2}
]$

## Einseitige Konfidenzintervalle für Varianz bei bekanntem Erwartungswert
$[ \frac{n-1}{\chi^2_{1 - \alpha;n}} \widetilde{s_n^2}, +\infty )$
bzw.
$( 0, \frac{n-1}{\chi^2_{\alpha;n}} \widetilde{s_n^2} ]$