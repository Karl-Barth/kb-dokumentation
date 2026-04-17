# `<textClass>` Textklassifikation

gruppiert Informationen über Art oder Thematik eines Textes unter 
      Bezug auf ein Standard-Klassifikationsschema, einen Thesaurus o. ä.

**Modul:** header — Header

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
