# `<langUsage>` Sprachgebrauch

beschreibt Sprachen, Subsprachen, Register, Dialekte usw., die innerhalb eines Textes vorkommen.

**Modul:** header — Header

## Kann enthalten

**header:** [language](language.md) "beschreibt eine einzelne Sprache oder eine Subsprache, die i"

## Content Model

```xml
<content>
    <alternate>
      <classRef key="model.pLike" minOccurs="1" maxOccurs="unbounded"/>
      <elementRef key="language" minOccurs="1" maxOccurs="unbounded"/>        
    </alternate>
  </content>
```
