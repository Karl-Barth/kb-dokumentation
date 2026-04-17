# `<item>` Listenpunkt

enthält einen Listenpunkt.

Kann einen einfachen Fließtext enthalten oder eine Sequenz von Chunks.
    Welche Zeichenfolge auch immer für die Kennzeichnung eines Listenpunkts in der Vorlage
      benutzt wird, kann als Wert des globalen n-Attributs verwendet werden, dabei muss die
      Nummerierung nicht notwendigerweise erfasst werden. In geordneten Listen ist das
      n-Attribut des item-Elements per Definition synonym mit dem Gebrauch des
      label-Elements, um den Zähler des Listenpunkts zu erfassen. In Glossarlisten sollte
      der zu definierende Term im label-Element und nicht im n-Attribut angegeben
      werden.

Siehe [Textstruktur > Listen](https://dokumentation.karl-barth.ch/textstruktur/listen/)

[TEI Guidelines: item](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-item.html)

**Modul:** core — Kernmodule

## Attribute

**@n** (optional)


## Enthalten in

**core:** [list](list.md) "Liste. Der @type unterscheidet geordnete und ungeordnete Lis"

## Content Model

```xml
<content>
    <macroRef key="macro.specialPara"/>
  </content>
```
