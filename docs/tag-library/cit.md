# `<cit>` Zitat mit Referenz

Zitat mit optionaler bibliographischer Angabe.

**Modul:** core — Kernmodule

## Attribute

**att.cmc** provides attributes categorizing how the element content was created in a CMC environment.

**@generatedBy** (optional, erweiterbar)
:   Datentyp: teidata.enumerated
:   `human`
:   `template`
:   `system`
:   `bot`
:   `unspecified`


## Kann enthalten

**core:** [q](q.md) "enthält Material, das vom umgebenden Text durch 
    Anführu"

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
