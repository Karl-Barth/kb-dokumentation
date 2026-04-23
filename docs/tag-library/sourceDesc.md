# `<sourceDesc>` Beschreibung der Quellen

beschreibt die Quelle, von der sich der elektronische Text ableitet. 
        Üblicherweise eine bibliografische Beschreibung im Falle eines digitalisierten Textes oder eine Bezeichnung wie 
        born digital für einen nur in elektronischer Form vorliegenden Text.

[TEI Guidelines: sourceDesc](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-sourceDesc.html)

**Modul:** header — Header

## Enthalten in

**header:** [fileDesc](fileDesc.md) "enthält die vollständige bibliografische Beschreibung einer "

## Kann enthalten

**core:** [bibl](bibl.md) "Bibliographische Angabe. Unterscheidet zwischen gedruckter G" [list](list.md) "Liste. Der @type unterscheidet geordnete und ungeordnete Lis" [listBibl](listBibl.md) "enthält eine Liste von bibliografischen Angaben jeglicher Ar" [p](p.md) "Absatz. Darf nicht verschachtelt werden (ausser innerhalb vo"

**linking:** [ab](ab.md) "Anonymer Block, verwendet für zentrierte oder anders formati"

**namesdates:** [listEvent](listEvent.md) "contains a list of descriptions, each of which provides info"

**figures:** [table](table.md) "Tabelle."

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
