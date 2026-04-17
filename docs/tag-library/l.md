# `<l>` Vers(zeile)

Verszeile.

Siehe [Textstruktur > Gedichte](https://dokumentation.karl-barth.ch/textstruktur/gedichte/)

[TEI Guidelines: l](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-l.html)

**Modul:** core — Kernmodule

## Attribute

**@rend** (optional)

**@xml:space** (optional)


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
