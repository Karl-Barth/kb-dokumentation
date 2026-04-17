# `<altIdentifier>`

Alternativer Identifikator für eine Quelle (URI, KBA-ID, KBGA-Sources-ID).

[TEI Guidelines: altIdentifier](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-altIdentifier.html)

**Modul:** msdescription — Handschriftenbeschreibung

## Enthalten in

**msdescription:** [msIdentifier](msIdentifier.md) "contains the information required to identify the manuscript"

## Kann enthalten

**core:** [note](note.md) "Anmerkung (Fussnote, Endnote, editorische Anmerkung). Der @t"

**header:** [idno](idno.md) "Identifikator, z.B. URL oder KBA-Objektnummer."

**msdescription:** [repository](repository.md) "contains the name of a repository within which manuscripts o"

## Content Model

```xml
<content>
  <sequence minOccurs="1" maxOccurs="1">
    <classRef key="model.placeNamePart" expand="sequenceOptional"/>
    <elementRef key="institution" minOccurs="0"/>
    <elementRef key="repository" minOccurs="0"/>
    <elementRef key="collection" minOccurs="0"/>
    <elementRef key="idno"/>
    <elementRef key="note" minOccurs="0"/>
  </sequence>
</content>
```
