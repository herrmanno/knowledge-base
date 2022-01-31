---
id: iePx7YjGJicdr96Ej4pl4
title: ER-Modell
desc: ''
updated: 1643478730492
created: 1643477765768
---

## Konzeptueller Entwurf
Beinhaltet
- Strukturen
- Operationen
- Constraints

## Konzepte
- Entities (Rechteck)
- Attribute
    - Einwertig (Oval)
    - Mehrwertig (Doppelt umrandet)
- Schlüssel (Unterstrichenes Attribut)
- Relationship (Raute)
    - Kardinalität
- Weak Entities (werden vollkommen durch Parent identifiziert)
- ISA (Dreieck)
    - Overlapping Constraint:  'Kann $E$ teil von mehreren Childentities sein?'
    - Covering Constraint: 'Ist jedes $E$ einem der Childentities zuordnungsbar?'
- Aggregation (gestricheltes Kästchen)
    - Fasst mehrere Entities zu einem zusammen (dass dann an einer Relation teilnimmt)

## Kardinalität

Sei: $R \subset E_1 \times E_2 \times \ldots E_n$

Dann bedeutet $card(R,E_i) = (max,min)$, dass jedes Element aus $E_i$ mindestens $min$ und maximal
$max$ mal in $R$ enthalten sein muss.

![](/assets/images/2022-01-29-18-43-33.png)
