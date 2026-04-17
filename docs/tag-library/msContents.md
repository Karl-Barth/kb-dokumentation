# `<msContents>`

describes the intellectual content of a manuscript, manuscript
    part, or other object either as a series of paragraphs or as a series of structured manuscript items.

[TEI Guidelines: msContents](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-msContents.html)

**Modul:** msdescription — Handschriftenbeschreibung

## Enthalten in

**msdescription:** [msDesc](msDesc.md) "contains a description of a single identifiable
    manuscri"

## Kann enthalten

**msdescription:** [msItem](msItem.md) "describes an individual work or item within the intellectual"

## Content Model

```xml
<content>
    <alternate>
      
        <classRef key="model.pLike" minOccurs="1" maxOccurs="unbounded"/>
      
      <sequence>
        
          <elementRef key="summary" minOccurs="0"/>
        
        
          <elementRef key="textLang" minOccurs="0"/>
        
        
          <elementRef key="titlePage" minOccurs="0"/>
        
        
          <alternate minOccurs="0" maxOccurs="unbounded">
            <elementRef key="msItem"/>
            <elementRef key="msItemStruct"/>
          </alternate>
        
      </sequence>
    </alternate>
  </content>
```
