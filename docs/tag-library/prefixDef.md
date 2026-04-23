# `<prefixDef>`

defines a prefixing scheme used in teidata.pointer values,
  showing how abbreviated URIs using the scheme may be expanded into full URIs.

[TEI Guidelines: prefixDef](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-prefixDef.html)

**Modul:** header — Header

## Attribute

**@ident** (erforderlich)
:   Datentyp: teidata.prefix


## Enthalten in

**header:** [listPrefixDef](listPrefixDef.md) "contains a list of definitions of prefixing schemes used in "

## Kann enthalten

**core:** [p](p.md) "Absatz. Darf nicht verschachtelt werden (ausser innerhalb vo"

**linking:** [ab](ab.md) "Anonymer Block, verwendet für zentrierte oder anders formati"

## Content Model

```xml
<content>
      <classRef key="model.pLike" minOccurs="0" maxOccurs="unbounded"/>
  </content>
```
