# `<msItem>`

describes an individual work or item within the intellectual
  content of a manuscript, manuscript part, or other object.

**Modul:** msdescription — Handschriftenbeschreibung

## Enthalten in

**msdescription:** [msContents](msContents.md) "describes the intellectual content of a manuscript, manuscri"

## Content Model

```xml
<content>
    <sequence>
      
        <alternate minOccurs="0" maxOccurs="unbounded">
          <elementRef key="locus"/>
          <elementRef key="locusGrp"/>
        </alternate>
      
      <alternate>
        
          <classRef key="model.pLike" minOccurs="1" maxOccurs="unbounded"/>
        
        
          <alternate minOccurs="1" maxOccurs="unbounded">
            <classRef key="model.titlepagePart"/>
            <classRef key="model.msItemPart"/>
            <classRef key="model.global"/>
          </alternate>
        
      </alternate>
    </sequence>
  </content>
```
