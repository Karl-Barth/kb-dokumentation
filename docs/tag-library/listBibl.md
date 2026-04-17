# `<listBibl>` Liste bibliografischer Angaben

enthält eine Liste von bibliografischen Angaben jeglicher Art.

[TEI Guidelines: listBibl](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-listBibl.html)

**Modul:** core — Kernmodule

## Attribute

**@rend** (optional)

**@type** (optional)


## Content Model

```xml
<content>
    <sequence>
      <classRef key="model.headLike" minOccurs="0" maxOccurs="unbounded"/>
      <elementRef key="desc" minOccurs="0" maxOccurs="unbounded"/>
      <alternate minOccurs="0" maxOccurs="unbounded">
        <classRef key="model.milestoneLike" minOccurs="1" maxOccurs="1"/>
        <elementRef key="relation" minOccurs="1" maxOccurs="1"/>
        <elementRef key="listRelation" minOccurs="1" maxOccurs="1"/>
      </alternate>
      <sequence minOccurs="1" maxOccurs="unbounded">
        <classRef key="model.biblLike" minOccurs="1" maxOccurs="unbounded"/>
        <alternate minOccurs="0" maxOccurs="unbounded">
          <classRef key="model.milestoneLike" minOccurs="1" maxOccurs="1"/>
          <elementRef key="relation" minOccurs="1" maxOccurs="1"/>
          <elementRef key="listRelation" minOccurs="1" maxOccurs="1"/>
        </alternate>
      </sequence>
    </sequence>
  </content>
```
