# `<idno>` Identifikator

Identifikator, z.B. URL oder KBA-Objektnummer.

Siehe [Textelemente > Querverweise](https://dokumentation.karl-barth.ch/textelemente/querverweise/)

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


**@xml:id** (optional)

**@type** (optional, erweiterbar)
:   bestimmt die Art des Identifikators (z. B. ISBN, Sozialversicherungsnummer, URI)
:   Datentyp: teidata.enumerated
:   `ISBN`
:   `ISSN`
:   `DOI`
:   `URI`
:   `VIAF`
:   `ESTC`
:   `OCLC`


## Enthalten in

**header:** [idno](idno.md) "Identifikator, z.B. URL oder KBA-Objektnummer."

**namesdates:** [event](event.md) "enthält Daten mit Bezug zu etwas Bemerkenswertem, das in der"

**msdescription:** [altIdentifier](altIdentifier.md) "Alternativer Identifikator für eine Quelle (URI, KBA-ID, KBG" [msIdentifier](msIdentifier.md) "contains the information required to identify the manuscript"

## Kann enthalten

Beliebiger Textinhalt

**header:** [idno](idno.md) "Identifikator, z.B. URL oder KBA-Objektnummer."

## Beispiele

```xml
<idno type="ISBN">978-1-906964-22-1</idno>
<idno type="ISSN">0143-3385</idno>
<idno type="DOI">10.1000/123</idno>
<idno type="URI">http://www.worldcat.org/oclc/185922478</idno>
<idno type="URI">http://authority.nzetc.org/463/</idno>
<idno type="LT">Thomason Tract E.537(17)</idno>
<idno type="Wing">C695</idno>
<idno type="oldCat">
    <g ref="#sym"/>345</idno>
```

## Content Model

```xml
<content>
  <alternate minOccurs="0" maxOccurs="unbounded">
    <textNode/>
    <classRef key="model.gLike"/>
    <elementRef key="idno"/>
  </alternate>
</content>
```
