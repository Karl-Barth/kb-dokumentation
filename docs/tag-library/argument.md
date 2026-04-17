# `<argument>`

Zusammenfassung oder Regest eines Textes, typisch am Anfang eines Briefes oder Vortrags.

[TEI Guidelines: argument](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-argument.html)

**Modul:** textstructure — Textstruktur

## Enthalten in

**textstructure:** [opener](opener.md) "fasst Datumszeile, Verfasserangabe, Anredeformel und ähnlich"

## Content Model

```xml
<content>
  <sequence minOccurs="1" maxOccurs="1">
    <alternate minOccurs="0" maxOccurs="unbounded">
      <classRef key="model.global"/>
      <classRef key="model.headLike"/>
    </alternate>
    <sequence minOccurs="1" maxOccurs="unbounded">
      <classRef key="model.common"/>
      <classRef key="model.global" minOccurs="0" maxOccurs="unbounded"/>
    </sequence>
  </sequence>
</content>
```
