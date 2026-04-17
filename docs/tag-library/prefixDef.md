# `<prefixDef>`

defines a prefixing scheme used in teidata.pointer values,
  showing how abbreviated URIs using the scheme may be expanded into full URIs.

**Modul:** header — Header

## Attribute

**@ident** (erforderlich)
:   Datentyp: teidata.prefix


## Enthalten in

**header:** [listPrefixDef](listPrefixDef.md) "contains a list of definitions of prefixing schemes used in "

## Content Model

```xml
<content>
      <classRef key="model.pLike" minOccurs="0" maxOccurs="unbounded"/>
  </content>
```
