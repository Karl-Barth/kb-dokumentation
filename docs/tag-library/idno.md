# `<idno>` Identifikator

Identifikator, z.B. URL oder KBA-Objektnummer.

Siehe [Textelemente > Querverweise](https://dokumentation.karl-barth.ch/textelemente/querverweise/)

**Modul:** header — Header

## Attribute

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
