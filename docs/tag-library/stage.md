# `<stage>` Regieanweisung

enthält jegliche Regieanweisung in einem Dramentext oder -fragment.

Das who-Attribut kann verwendet werden, um die Person oder Personen näher zu
      bezeichnen, die die Regieanweisung ausführen.

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


**att.cmc** provides attributes categorizing how the element content was created in a CMC environment.

**@generatedBy** (optional, erweiterbar)
:   Datentyp: teidata.enumerated
:   `human`
:   `template`
:   `system`
:   `bot`
:   `unspecified`


**att.placement** provides attributes for describing where on the source page or
  object a textual element appears.

**@place** (optional, erweiterbar)
:   Datentyp: teidata.enumerated
:   `top`
:   `bottom`
:   `margin`
:   `opposite`
:   `overleaf`
:   `above`
:   `right`
:   `below`
:   `left`
:   `end`
:   `inline`
:   `inspace`


**@type** (optional, erweiterbar)
:   beschreibt die Art der Regieanweisung.
:   Datentyp: teidata.enumerated
:   `setting` — beschreibt die Szenerie.
:   `entrance` — beschreibt einen Auftritt.
:   `exit` — beschreibt einen Abgang.
:   `business` — beschreibt eine Bühnenhandlung.
:   `novelistic` — beschreibt eine narrative Regieanweisung.
:   `delivery` — beschreibt die Art und Weise der Darbietung einer Figurenrede.
:   `modifier` — gibt nähere Details zu einer Figur an.
:   `location` — beschreibt einen Handlungsort.
:   `mixed` — mehrere der oben angeführten Funktionen.


## Content Model

```xml
<content>
    <macroRef key="macro.specialPara"/>
  </content>
```
