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


**att.breaking** provides attributes to indicate whether or not the element
  concerned is considered to  mark the end of an orthographic token in the same way
  as whitespace.

**@break** (optional)
:   Datentyp: teidata.enumerated
:   `yes`
:   `no`
:   `maybe`


**att.cmc** provides attributes categorizing how the element content was created in a CMC environment.

**@generatedBy** (optional, erweiterbar)
:   Datentyp: teidata.enumerated
:   `human`
:   `template`
:   `system`
:   `bot`
:   `unspecified`


**att.edition** provides attributes identifying the source edition from which some encoded feature derives.

**@ed** (optional)
:   Datentyp: teidata.word

**@edRef** (optional)
:   Datentyp: teidata.pointer


**att.milestoneUnit** provides attributes to indicate the type of section which is changing at a specific milestone.

**@unit** (erforderlich, erweiterbar)
:   Datentyp: teidata.enumerated
:   `page`
:   `column`
:   `line`
:   `book`
:   `poem`
:   `canto`
:   `speaker`
:   `stanza`
:   `act`
:   `scene`
:   `section`
:   `absent`
:   `unnumbered`


**att.typed** provides attributes that can be used to classify or subclassify elements in any way.

**@type** (optional)
:   Datentyp: teidata.enumerated

**@subtype** (optional)
:   Datentyp: teidata.enumerated


## Kann enthalten

Leeres Element.

## Content Model

```xml
<content>
  <empty/>
</content>
```
