# `<msIdentifier>`

contains the information required to identify the manuscript or similar object being described.

[TEI Guidelines: msIdentifier](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-msIdentifier.html)

**Modul:** msdescription — Handschriftenbeschreibung

## Enthalten in

**msdescription:** [msDesc](msDesc.md) "contains a description of a single identifiable
    manuscri"

## Kann enthalten

**header:** [idno](idno.md) "Identifikator, z.B. URL oder KBA-Objektnummer."

**msdescription:** [altIdentifier](altIdentifier.md) "Alternativer Identifikator für eine Quelle (URI, KBA-ID, KBG" [repository](repository.md) "contains the name of a repository within which manuscripts o"

## Constraints

**msId_minimal**
:   An msIdentifier must contain either a repository or location.

## Content Model

```xml
<content>
    <sequence>
      <sequence>
        <classRef key="model.placeNamePart" expand="sequenceOptional"/>        
        <elementRef key="institution" minOccurs="0"/>
        <elementRef key="repository" minOccurs="0"/>
        <elementRef key="collection" minOccurs="0" maxOccurs="unbounded"/>
        <elementRef key="idno" minOccurs="0" maxOccurs="unbounded"/>
      </sequence>
      <alternate minOccurs="0" maxOccurs="unbounded">
        <elementRef key="msName"/>
        <elementRef key="objectName"/>
        <elementRef key="altIdentifier"/>
      </alternate>
    </sequence>
  </content>
```
