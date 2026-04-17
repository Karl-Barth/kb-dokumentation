# `<sourceDesc>` Beschreibung der Quellen

beschreibt die Quelle, von der sich der elektronische Text ableitet. 
        Üblicherweise eine bibliografische Beschreibung im Falle eines digitalisierten Textes oder eine Bezeichnung wie 
        born digital für einen nur in elektronischer Form vorliegenden Text.

[TEI Guidelines: sourceDesc](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-sourceDesc.html)

**Modul:** header — Header

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
