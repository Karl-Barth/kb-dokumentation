# `<sourceDesc>` Beschreibung der Quellen

beschreibt die Quelle, von der sich der elektronische Text ableitet. 
        Üblicherweise eine bibliografische Beschreibung im Falle eines digitalisierten Textes oder eine Bezeichnung wie 
        born digital für einen nur in elektronischer Form vorliegenden Text.

**Modul:** header — Header

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


**att.declarable** provides attributes for those elements in the TEI header which
  may be independently selected by means of  the special purpose decls attribute.

**@default** (optional, geschlossene Werteliste)
:   Datentyp: teidata.truthValue
:   `true`
:   `false`


## Enthalten in

**header:** [fileDesc](fileDesc.md) "enthält die vollständige bibliografische Beschreibung einer "

## Content Model

```xml
<content>
    <alternate>
      <classRef key="model.pLike" minOccurs="1" maxOccurs="unbounded"/>
      <alternate minOccurs="1" maxOccurs="unbounded">
        <classRef key="model.biblLike"/>
        <classRef key="model.sourceDescPart"/>
        <classRef key="model.listLike"/>
      </alternate>
    </alternate>
  </content>
```
