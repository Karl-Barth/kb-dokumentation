# `<date>` Datum

Datumsangabe mit maschinenlesbarem Datum in @when, @from/@to oder @notBefore/@notAfter.

Siehe [Textelemente > Datumsangaben](https://dokumentation.karl-barth.ch/textelemente/datumsangaben/)

[TEI Guidelines: date](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-date.html)

**Modul:** core — Kernmodule

## Attribute

**@from** (optional)

**@notAfter** (optional)

**@notBefore** (optional)

**@period** (optional)

**@rend** (optional)

**@to** (optional)

**@type** (optional)

**@when** (optional)


## Kann enthalten

Beliebiger Textinhalt

## Content Model

```xml
<content>
  <alternate minOccurs="0" maxOccurs="unbounded">
    <textNode/>
    <classRef key="model.gLike"/>
    <classRef key="model.phrase"/>
    <classRef key="model.global"/>
  </alternate>
</content>
```
