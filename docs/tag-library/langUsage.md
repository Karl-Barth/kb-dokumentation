# `<langUsage>` Sprachgebrauch

beschreibt Sprachen, Subsprachen, Register, Dialekte usw., die innerhalb eines Textes vorkommen.

[TEI Guidelines: langUsage](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-langUsage.html)

**Modul:** header — Header

## Enthalten in

**header:** [profileDesc](profileDesc.md) "enthält eine detaillierte Beschreibung der nicht-bibliografi"

## Kann enthalten

**core:** [p](p.md) "Absatz. Darf nicht verschachtelt werden (ausser innerhalb vo"

**header:** [language](language.md) "beschreibt eine einzelne Sprache oder eine Subsprache, die i"

**linking:** [ab](ab.md) "Anonymer Block, verwendet für zentrierte oder anders formati"

## Content Model

```xml
<content>
    <alternate>
      <classRef key="model.pLike" minOccurs="1" maxOccurs="unbounded"/>
      <elementRef key="language" minOccurs="1" maxOccurs="unbounded"/>        
    </alternate>
  </content>
```
