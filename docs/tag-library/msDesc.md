# `<msDesc>`

contains a description of a single identifiable
    manuscript or other text-bearing object such as an early printed book.

**Modul:** msdescription — Handschriftenbeschreibung

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
