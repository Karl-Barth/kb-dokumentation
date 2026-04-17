# `<keywords/>` (Schlagwörter)

**Modul:** Header

## Beschreibung

enthält eine Zusammenstellung von Schlagwörtern oder Phrasen zur Art oder Thematik des Textes.

## Erläuterung

Jedes einzelne Schlagwort (zusammengesetzte Themen-Schlagwörter eingeschlossen) 
          sollte als term-Element direkt im keywords-Element notiert werden. 
          Aus Gründen der Rückwärtskompatibilität ist es zwar auch erlaubt, ein term-Element 
          in einem item-Element zu notieren, das wiederum Kindelement eines list-Elementes ist. 
          Allerdings ist dieses Vorgehen veraltet und wird daher nicht empfohlen.
      Wenn keine kontrollierte Liste für die verwendeten Schlagwörter existiert, sollte das scheme-Attribute nicht gesetzt werden.

## Erlaubt in

**Header:** [`<textClass>`](textClass.md)

## Inhaltsmodell

- [`<term>`](term.md)
- [`<list>`](list.md)

## Attribute

### `@scheme` (optional)

gibt das kontrollierte Vokabular an, in dem die benutzten Schlagwörter 
            definiert sind. Dabei kann das scheme-Attribut auf ein taxonomy-Element oder eine andere Ressource verweisen.

**Datentyp:** teidata.pointer
