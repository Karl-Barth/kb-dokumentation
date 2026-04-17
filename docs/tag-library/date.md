# `<date>` Datum

Datumsangabe mit maschinenlesbarem Datum in @when, @from/@to oder @notBefore/@notAfter.

Siehe [Textelemente > Datumsangaben](https://dokumentation.karl-barth.ch/textelemente/datumsangaben/)

**Modul:** core — Kernmodule

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
