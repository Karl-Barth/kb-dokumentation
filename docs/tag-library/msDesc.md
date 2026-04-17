# `<msDesc>`

contains a description of a single identifiable
    manuscript or other text-bearing object such as an early printed book.

**Modul:** msdescription — Handschriftenbeschreibung

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


**att.declaring** provides attributes for elements which may be independently associated with a particular declarable element within the header, thus overriding the inherited default for that element.

**@decls** (optional)
:   Datentyp: teidata.pointer


**att.typed** provides attributes that can be used to classify or subclassify elements in any way.

**@type** (optional)
:   Datentyp: teidata.enumerated

**@subtype** (optional)
:   Datentyp: teidata.enumerated


## Kann enthalten

**msdescription:** [msContents](msContents.md) "describes the intellectual content of a manuscript, manuscri" [msIdentifier](msIdentifier.md) "contains the information required to identify the manuscript"

## Constraints

**one_ms_singleton_max**
:   Only one  is allowed as a child of .

## Content Model

```xml
<content>
    <sequence>
      <elementRef key="msIdentifier"/>
      <classRef key="model.headLike" minOccurs="0" maxOccurs="unbounded"/>
      
      <alternate>
        <classRef key="model.pLike" minOccurs="1" maxOccurs="unbounded"/>
        <alternate minOccurs="0" maxOccurs="unbounded">
          <elementRef key="msContents"/>
          <elementRef key="physDesc"/>
          <elementRef key="history"/>
          <elementRef key="additional"/>
          <elementRef key="msPart"/>
          <elementRef key="msFrag"/>
        </alternate>
      </alternate>
    </sequence>
  </content>
```
