# `<figure>` Abbildung

Abbildung mit optionaler Beschreibung (figDesc) und Grafik (graphic).

Siehe [Textstruktur > Bilder](https://dokumentation.karl-barth.ch/textstruktur/bilder/)

[TEI Guidelines: figure](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-figure.html)

**Modul:** figures — Abbildungen und Tabellen

## Attribute

**@n** (optional)

**@rend** (optional)

**@rendition** (optional)

**@xml:id** (optional)


## Kann enthalten

**figures:** [figDesc](figDesc.md) "enthält einen kurzen Beschreibungstext des Inhalts oder des "

## Content Model

```xml
<content>
  <alternate minOccurs="0" maxOccurs="unbounded">
    <classRef key="model.headLike"/>
    <classRef key="model.common"/>
    <elementRef key="figDesc"/>
    <classRef key="model.graphicLike"/>
    <classRef key="model.global"/>
    <classRef key="model.divBottom"/>
  </alternate>
</content>
```
