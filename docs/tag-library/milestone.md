# `<milestone>` Grenzpunkt

markiert einen Grenzpunkt, der Abschnitte eines Textes trennen kann, 
    typischerweise (aber nicht notwendigerweise) den Wechsel eines Bezugssystems, 
    der nicht durch ein strukturelles Markup beschrieben werden kann.

Das globale n-Attribut gibt für dieses Element die neue Zahl 
      (oder einen anderen Wert) der Einheit an, die an diesem Grenzpunkt wechselt. 
      Der besondere Wert unnumbered (ungezählt) sollte für Abschnitte gewählt werden, 
      die außerhalb des normalen Zählsystems fallen, wie beispielsweise Kapitel- 
      oder andere Überschriften, Gedichtnummern oder -titel etc.
    Die Reihenfolge des Auftretens von mehreren milestone-Elementen 
      an einem gegebenen Punkt ist normalerweise nicht signifikant.

**Modul:** core — Kernmodule

## Kann enthalten

Leeres Element.

## Content Model

```xml
<content>
  <empty/>
</content>
```
