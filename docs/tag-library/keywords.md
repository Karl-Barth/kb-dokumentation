# `<keywords>` Schlagwörter

enthält eine Zusammenstellung von Schlagwörtern oder Phrasen zur Art oder Thematik des Textes.

Jedes einzelne Schlagwort (zusammengesetzte Themen-Schlagwörter eingeschlossen) 
          sollte als term-Element direkt im keywords-Element notiert werden. 
          Aus Gründen der Rückwärtskompatibilität ist es zwar auch erlaubt, ein term-Element 
          in einem item-Element zu notieren, das wiederum Kindelement eines list-Elementes ist. 
          Allerdings ist dieses Vorgehen veraltet und wird daher nicht empfohlen.
      Wenn keine kontrollierte Liste für die verwendeten Schlagwörter existiert, sollte das scheme-Attribute nicht gesetzt werden.

**Modul:** header — Header

## Attribute

**@scheme** (optional)
:   gibt das kontrollierte Vokabular an, in dem die benutzten Schlagwörter 
            definiert sind. Dabei kann das scheme-Attribut auf ein taxonomy-Element oder eine andere Ressource verweisen.
:   Datentyp: teidata.pointer


## Enthalten in

**header:** [textClass](textClass.md) "gruppiert Informationen über Art oder Thematik eines Textes "

## Kann enthalten

**core:** [list](list.md) "Liste. Der @type unterscheidet geordnete und ungeordnete Lis" [term](term.md) "Sachbegriff mit Verweis auf die Begriffs-Taxonomie via @ref "

## Content Model

```xml
<content>
    <alternate>
      <elementRef key="term" minOccurs="1" maxOccurs="unbounded"/>      
      <elementRef key="list"/>
    </alternate>
  </content>
```
