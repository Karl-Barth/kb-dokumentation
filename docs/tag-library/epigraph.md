# `<epigraph>` Motto

enthält ein anonymes oder jemandem zugeschriebenes Zitat, das am Beginn eines Abschnitts,
    Kapitels oder auf einer Titelseite steht.

[TEI Guidelines: epigraph](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-epigraph.html)

**Modul:** textstructure — Textstruktur

## Enthalten in

**textstructure:** [opener](opener.md) "fasst Datumszeile, Verfasserangabe, Anredeformel und ähnlich"

## Content Model

```xml
<content>
    
      <alternate minOccurs="0" maxOccurs="unbounded">
        <classRef key="model.common"/>
        <classRef key="model.global"/>
      </alternate>
    
  </content>
```
