# `<correspContext>` Korrespondenzstelle

provides references to preceding or following correspondence related to this piece of correspondence.

[TEI Guidelines: correspContext](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-correspContext.html)

**Modul:** header — Header

## Enthalten in

**header:** [correspDesc](correspDesc.md) "contains a description
    of the actions related to one act"

## Kann enthalten

**core:** [note](note.md) "Anmerkung (Fussnote, Endnote, editorische Anmerkung). Der @t" [p](p.md) "Absatz. Darf nicht verschachtelt werden (ausser innerhalb vo" [ptr](ptr.md) "defines a pointer to another location." [ref](ref.md) "Verweis auf eine andere Ressource. Dient für Bibelstellen, L"

**linking:** [ab](ab.md) "Anonymer Block, verwendet für zentrierte oder anders formati"

## Content Model

```xml
<content>
    <classRef key="model.correspContextPart" minOccurs="1" maxOccurs="unbounded"/>
  </content>
```
