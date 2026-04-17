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

**Modul:** core — Kernmodule

## Attribute

**att.global** stellt gemeinsame Attribute für alle Elemente im TEI-Kodierungsschema bereit.

**@xml:id** (optional)
:   liefert einen Identifikator für das Element, welches dieses Attribut trägt.
:   Datentyp: ID

**@n** (optional)
:   gibt eine Nummer (oder eine andere Bezeichnung) für ein Element an, die innerhalb des Dokuments nicht zwangsläufig eindeutig ist.
:   Datentyp: teidata.text

**@xml:lang** (optional)
:   gibt die Sprache des Elementinhalts durch ein Tag an, das nach BCP 47 festgelegt wird.
:   Datentyp: teidata.language

**@xml:base** (optional)
:   liefert eine Basis-URI-Referenz, mit der Anwendungen relative URI-Referenzen in absolute auflösen können.
:   Datentyp: teidata.pointer

**@xml:space** (optional, geschlossene Werteliste)
:   signalisiert die gewünschte Handhabung von Leerzeichen durch Anwendungen.
:   Datentyp: teidata.enumerated
:   `default`
:   `preserve`


## Enthalten in

**core:** [list](list.md) "enthält eine Reihe von Listenpunkten, die als Liste organisi"

## Content Model

```xml
<content>
    <macroRef key="macro.specialPara"/>
  </content>
```
