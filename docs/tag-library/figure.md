# `<figure>` Abbildung

Abbildung mit optionaler Beschreibung (figDesc) und Grafik (graphic).

Siehe [Textstruktur > Bilder](https://dokumentation.karl-barth.ch/textstruktur/bilder/)

**Modul:** figures — Abbildungen und Tabellen

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


**att.typed** provides attributes that can be used to classify or subclassify elements in any way.

**@type** (optional)
:   Datentyp: teidata.enumerated

**@subtype** (optional)
:   Datentyp: teidata.enumerated


## Kann enthalten

**figures:** [figDesc](figDesc.md) "enthält einen kurzen Beschreibungstext des Inhalts oder des "

## Content Model

```xml
<content>
  <alternate minOccurs="0" maxOccurs="unbounded">
    <classRef key="model.headLike"/>
    <classRef key="model.common"/>
    <elementRef key="figDesc"/>
    <classRef key="model.graphicLike"/>
    <classRef key="model.global"/>
    <classRef key="model.divBottom"/>
  </alternate>
</content>
```
