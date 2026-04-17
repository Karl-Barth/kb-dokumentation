# `<item/>` (Listenpunkt)

**Modul:** Kernmodule

## Beschreibung

enthält einen Listenpunkt.

## Erläuterung

Kann einen einfachen Fließtext enthalten oder eine Sequenz von Chunks.
    Welche Zeichenfolge auch immer für die Kennzeichnung eines Listenpunkts in der Vorlage
      benutzt wird, kann als Wert des globalen n-Attributs verwendet werden, dabei muss die
      Nummerierung nicht notwendigerweise erfasst werden. In geordneten Listen ist das
      n-Attribut des item-Elements per Definition synonym mit dem Gebrauch des
      label-Elements, um den Zähler des Listenpunkts zu erfassen. In Glossarlisten sollte
      der zu definierende Term im label-Element und nicht im n-Attribut angegeben
      werden.

Ausführliche Dokumentation:

- [Textstruktur > Listen](https://dokumentation.karl-barth.ch/textstruktur/listen/)

## Erlaubt in

**Kernmodule:** [`<list>`](list.md)

## Inhaltsmodell

- *macro.specialPara*
