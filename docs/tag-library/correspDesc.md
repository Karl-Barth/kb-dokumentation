# `<correspDesc>`

contains a description
    of the actions related to one act of correspondence.

[TEI Guidelines: correspDesc](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-correspDesc.html)

**Modul:** header — Header

## Enthalten in

**header:** [profileDesc](profileDesc.md) "enthält eine detaillierte Beschreibung der nicht-bibliografi"

## Kann enthalten

**core:** [note](note.md) "Anmerkung (Fussnote, Endnote, editorische Anmerkung). Der @t" [p](p.md) "Absatz. Darf nicht verschachtelt werden (ausser innerhalb vo"

**header:** [correspAction](correspAction.md) "contains a structured
  description of the place, the name o" [correspContext](correspContext.md) "provides references to preceding or following correspondence"

**linking:** [ab](ab.md) "Anonymer Block, verwendet für zentrierte oder anders formati"

## Content Model

```xml
<content>
    
    <alternate>
      <classRef key="model.correspDescPart" minOccurs="1" maxOccurs="unbounded"/>
      <classRef key="model.pLike" minOccurs="1" maxOccurs="unbounded"/>      
    </alternate>
  </content>
```
