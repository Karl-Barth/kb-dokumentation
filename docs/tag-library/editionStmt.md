# `<editionStmt>` Angaben zur Ausgabe

Angaben zur digitalen Edition (Titel, Förderer).

[TEI Guidelines: editionStmt](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-editionStmt.html)

**Modul:** header — Header

## Enthalten in

**header:** [fileDesc](fileDesc.md) "enthält die vollständige bibliografische Beschreibung einer "

## Kann enthalten

**header:** [edition](edition.md) "beschreibt die Details einer Ausgabe eines Textes."

## Content Model

```xml
<content>
  <alternate minOccurs="1" maxOccurs="1">
    <classRef key="model.pLike" minOccurs="1" maxOccurs="unbounded"/>
    <sequence minOccurs="1" maxOccurs="1">
      <elementRef key="edition"/>
      <classRef key="model.respLike" minOccurs="0" maxOccurs="unbounded"/>
    </sequence>
  </alternate>
</content>
```
