# `<date>` Datum

enthält ein Datum in beliebigem Format.

Siehe [Textelemente > Datumsangaben](https://dokumentation.karl-barth.ch/textelemente/datumsangaben/)

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


**att.calendarSystem** provides attributes for indicating calendar systems to which a date belongs.

**@calendar** (optional)
:   Datentyp: teidata.pointer


**att.canonical** provides attributes that can be used to associate a representation such as a name or title
    with canonical information about the object being named or referenced.

**@key** (optional)
:   Datentyp: teidata.text

**@ref** (optional)
:   Datentyp: teidata.pointer


**att.cmc** provides attributes categorizing how the element content was created in a CMC environment.

**@generatedBy** (optional, erweiterbar)
:   Datentyp: teidata.enumerated
:   `human`
:   `template`
:   `system`
:   `bot`
:   `unspecified`


**att.datable** provides attributes for normalization of elements
    that contain dates, times, or datable events.

**@period** (optional)
:   Datentyp: teidata.pointer


**att.dimensions** provides attributes for describing the size of physical objects.

**@unit** (optional, erweiterbar)
:   Datentyp: teidata.enumerated
:   `cm`
:   `mm`
:   `in`
:   `line`
:   `char`

**@quantity** (optional)
:   Datentyp: teidata.numeric

**@extent** (optional)
:   Datentyp: teidata.text

**@precision** (optional)
:   Datentyp: teidata.certainty

**@scope** (optional)
:   Datentyp: teidata.enumerated
:   `all`
:   `most`
:   `range`


**att.typed** provides attributes that can be used to classify or subclassify elements in any way.

**@type** (optional)
:   Datentyp: teidata.enumerated

**@subtype** (optional)
:   Datentyp: teidata.enumerated


## Kann enthalten

Beliebiger Textinhalt

## Content Model

```xml
<content>    
    <alternate minOccurs="0" maxOccurs="unbounded">
      <textNode/>
      <classRef key="model.gLike"/>
      <classRef key="model.phrase"/>
      <classRef key="model.global"/>
    </alternate>
  </content>
```
