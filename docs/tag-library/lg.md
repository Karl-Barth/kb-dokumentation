# `<lg>` Gruppe von Vers(zeil)en

Strophe oder Versgruppe.

Siehe [Textstruktur > Gedichte](https://dokumentation.karl-barth.ch/textstruktur/gedichte/)

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


**att.declaring** provides attributes for elements which may be independently associated with a particular declarable element within the header, thus overriding the inherited default for that element.

**@decls** (optional)
:   Datentyp: teidata.pointer


**att.typed** provides attributes that can be used to classify or subclassify elements in any way.

**@type** (optional)
:   Datentyp: teidata.enumerated

**@subtype** (optional)
:   Datentyp: teidata.enumerated


## Enthalten in

**core:** [head](head.md) "Überschrift einer Gliederungseinheit (div)." [lg](lg.md) "Strophe oder Versgruppe." [sp](sp.md) "enthält eine einzelne Figurenrede in einem Dramentext oder e"

## Kann enthalten

**core:** [lg](lg.md) "Strophe oder Versgruppe."

## Constraints

**atleast1oflggapl**
:   An lg element must contain at least one child l, lg, or gap element.

**abstractModel-structure-lg-in-l**
:   Abstract model violation: Lines may not contain line groups.

## Content Model

```xml
<content>
  <sequence minOccurs="1" maxOccurs="1">
    <alternate minOccurs="0" maxOccurs="unbounded">
      <classRef key="model.divTop"/>
      <classRef key="model.global"/>
    </alternate>
    <alternate minOccurs="1" maxOccurs="1">
      <classRef key="model.lLike"/>
      <classRef key="model.stageLike"/>
      <classRef key="model.labelLike"/>
      <classRef key="model.pPart.transcriptional"/>
      <elementRef key="lg"/>
    </alternate>
    <alternate minOccurs="0" maxOccurs="unbounded">
      <classRef key="model.lLike"/>
      <classRef key="model.stageLike"/>
      <classRef key="model.labelLike"/>
      <classRef key="model.pPart.transcriptional"/>
      <classRef key="model.global"/>
      <elementRef key="lg"/>
    </alternate>
    <sequence minOccurs="0" maxOccurs="unbounded">
      <classRef key="model.divBottom"/>
      <classRef key="model.global" minOccurs="0" maxOccurs="unbounded"/>
    </sequence>
  </sequence>
</content>
```
