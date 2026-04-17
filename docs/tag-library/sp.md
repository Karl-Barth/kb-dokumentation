# `<sp>` Figurenrede

enthält eine einzelne Figurenrede in einem Dramentext oder eine entsprechende Passage in einem Prosatext oder lyrischen Text.

Das who-Attribut an diesem Element kann entweder zusätzlich zum
      speaker-Element eingesetzt werden oder alternativ dazu.

Siehe [Textstruktur > Woertliche Rede](https://dokumentation.karl-barth.ch/textstruktur/woertliche-rede/)

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


## Kann enthalten

**core:** [lg](lg.md) "Strophe oder Versgruppe." [q](q.md) "Direkte Rede oder Zitat im Fliesstext." [speaker](speaker.md) "enthält eine spezielle Form von Überschrift oder Bezeichnung"

## Content Model

```xml
<content>
    <alternate minOccurs="0" maxOccurs="unbounded">
      <classRef key="model.stageLike"/>
      <classRef key="model.global"/>
      <classRef key="model.lLike"/>
      <classRef key="model.pLike"/>
      <classRef key="model.listLike"/>
      <classRef key="model.attributable"/>
      <elementRef key="speaker"/>
      <elementRef key="lg"/>
      <elementRef key="q"/>
    </alternate>
  </content>
```
