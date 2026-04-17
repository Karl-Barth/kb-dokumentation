# `<sp>` Figurenrede

enthält eine einzelne Figurenrede in einem Dramentext oder eine entsprechende Passage in einem Prosatext oder lyrischen Text.

Das who-Attribut an diesem Element kann entweder zusätzlich zum
      speaker-Element eingesetzt werden oder alternativ dazu.

Siehe [Textstruktur > Woertliche Rede](https://dokumentation.karl-barth.ch/textstruktur/woertliche-rede/)

**Modul:** core — Kernmodule

## Kann enthalten

**core:** [lg](lg.md) "Strophe oder Versgruppe." [q](q.md) "Direkte Rede oder Zitat im Fliesstext." [speaker](speaker.md) "enthält eine spezielle Form von Überschrift oder Bezeichnung"

## Content Model

```xml
<content>
    <alternate minOccurs="0" maxOccurs="unbounded">
      <classRef key="model.stageLike"/>
      <classRef key="model.global"/>
      <classRef key="model.lLike"/>
      <classRef key="model.pLike"/>
      <classRef key="model.listLike"/>
      <classRef key="model.attributable"/>
      <elementRef key="speaker"/>
      <elementRef key="lg"/>
      <elementRef key="q"/>
    </alternate>
  </content>
```
