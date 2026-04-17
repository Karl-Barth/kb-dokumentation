# `<lg>` Gruppe von Vers(zeil)en

Strophe oder Versgruppe.

Siehe [Textstruktur > Gedichte](https://dokumentation.karl-barth.ch/textstruktur/gedichte/)

**Modul:** core — Kernmodule

## Enthalten in

**core:** [head](head.md) "Überschrift einer Gliederungseinheit (div)." [lg](lg.md) "Strophe oder Versgruppe." [sp](sp.md) "enthält eine einzelne Figurenrede in einem Dramentext oder e"

## Kann enthalten

**core:** [lg](lg.md) "Strophe oder Versgruppe."

## Constraints

**atleast1oflggapl**
:   An lg element must contain at least one child l, lg, or gap element.

**abstractModel-structure-lg-in-l**
:   Abstract model violation: Lines may not contain line groups.

## Content Model

```xml
<content>
  <sequence minOccurs="1" maxOccurs="1">
    <alternate minOccurs="0" maxOccurs="unbounded">
      <classRef key="model.divTop"/>
      <classRef key="model.global"/>
    </alternate>
    <alternate minOccurs="1" maxOccurs="1">
      <classRef key="model.lLike"/>
      <classRef key="model.stageLike"/>
      <classRef key="model.labelLike"/>
      <classRef key="model.pPart.transcriptional"/>
      <elementRef key="lg"/>
    </alternate>
    <alternate minOccurs="0" maxOccurs="unbounded">
      <classRef key="model.lLike"/>
      <classRef key="model.stageLike"/>
      <classRef key="model.labelLike"/>
      <classRef key="model.pPart.transcriptional"/>
      <classRef key="model.global"/>
      <elementRef key="lg"/>
    </alternate>
    <sequence minOccurs="0" maxOccurs="unbounded">
      <classRef key="model.divBottom"/>
      <classRef key="model.global" minOccurs="0" maxOccurs="unbounded"/>
    </sequence>
  </sequence>
</content>
```
