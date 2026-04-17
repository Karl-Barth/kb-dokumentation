# `<metamark>`

contains or describes any kind of graphic or written signal
   within a document the function of which is to determine how it
   should be read rather than forming part of the actual content of
   the document.

**Modul:** transcr — Transkription

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


**@function** (optional)
:   Datentyp: teidata.word

**@target** (optional)
:   Datentyp: teidata.pointer


## Content Model

```xml
<content>
    <macroRef key="macro.specialPara"/>
  </content>
```
