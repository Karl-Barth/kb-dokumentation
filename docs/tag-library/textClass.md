# `<textClass>` Textklassifikation

gruppiert Informationen über Art oder Thematik eines Textes unter 
      Bezug auf ein Standard-Klassifikationsschema, einen Thesaurus o. ä.

[TEI Guidelines: textClass](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-textClass.html)

**Modul:** header — Header

## Enthalten in

**header:** [profileDesc](profileDesc.md) "enthält eine detaillierte Beschreibung der nicht-bibliografi"

## Kann enthalten

**header:** [keywords](keywords.md) "enthält eine Zusammenstellung von Schlagwörtern oder Phrasen"

## Content Model

```xml
<content>
    <alternate minOccurs="0" maxOccurs="unbounded">
      <elementRef key="classCode"/>
      <elementRef key="catRef"/>
      <elementRef key="keywords"/>
    </alternate>
  </content>
```
