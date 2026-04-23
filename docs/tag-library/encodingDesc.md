# `<encodingDesc>` Beschreibung der Kodierung

dokumentiert das Verhältnis zwischen dem elektronischen Text und seiner Quelle oder den Quellen, von denen er sich ableitet.

[TEI Guidelines: encodingDesc](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-encodingDesc.html)

**Modul:** header — Header

## Enthalten in

**header:** [teiHeader](teiHeader.md) "wird aus der Meta- und Registerdatenbank erzeugt und soll im"

## Kann enthalten

**core:** [p](p.md) "Absatz. Darf nicht verschachtelt werden (ausser innerhalb vo"

**header:** [listPrefixDef](listPrefixDef.md) "contains a list of definitions of prefixing schemes used in "

**linking:** [ab](ab.md) "Anonymer Block, verwendet für zentrierte oder anders formati"

## Content Model

```xml
<content>
    <alternate minOccurs="1" maxOccurs="unbounded">
      <classRef key="model.encodingDescPart"/>
      <classRef key="model.pLike"/>
    </alternate>
  </content>
```
