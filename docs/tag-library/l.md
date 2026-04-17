# `<l>` Vers(zeile)

Verszeile.

Siehe [Textstruktur > Gedichte](https://dokumentation.karl-barth.ch/textstruktur/gedichte/)

**Modul:** core — Kernmodule

## Kann enthalten

Beliebiger Textinhalt

## Constraints

**abstractModel-structure-l-in-l**
:   Abstract model violation: Lines may not contain lines or lg elements.

## Content Model

```xml
<content>
  <alternate minOccurs="0" maxOccurs="unbounded">
    <textNode/>
    <classRef key="model.gLike"/>
    <classRef key="model.phrase"/>
    <classRef key="model.inter"/>
    <classRef key="model.global"/>
  </alternate>
</content>
```
