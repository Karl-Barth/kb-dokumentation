# `<cit>` Zitat mit Referenz

Zitat mit optionaler bibliographischer Angabe.

[TEI Guidelines: cit](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-cit.html)

**Modul:** core — Kernmodule

## Kann enthalten

**core:** [q](q.md) "Direkte Rede oder Zitat im Fliesstext."

## Content Model

```xml
<content>
  <alternate minOccurs="1" maxOccurs="unbounded">
    <classRef key="model.biblLike"/>
    <classRef key="model.egLike"/>
    <classRef key="model.entryPart"/>
    <classRef key="model.global"/>
    <classRef key="model.graphicLike"/>
    <classRef key="model.ptrLike"/>
    <classRef key="model.attributable"/>
    <elementRef key="pc"/>
    <elementRef key="q"/>
  </alternate>
</content>
```
