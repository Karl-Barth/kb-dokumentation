# `<opener>`

fasst Datumszeile, Verfasserangabe, Anredeformel und ähnliche Phrasen zusammen, die einleitend zu
    Beginn eines Abschnitts stehen, vor allem bei einem Brief.

Siehe [Textstruktur > Dateline](https://dokumentation.karl-barth.ch/textstruktur/dateline/)

[TEI Guidelines: opener](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-opener.html)

**Modul:** textstructure — Textstruktur

## Kann enthalten

Beliebiger Textinhalt

**textstructure:** [argument](argument.md) "Zusammenfassung oder Regest eines Textes, typisch am Anfang " [dateline](dateline.md) "enthält kurze Angaben zu Entstehungsort, -datum, -zeit, usw." [epigraph](epigraph.md) "enthält ein anonymes oder jemandem zugeschriebenes Zitat, da" [salute](salute.md) "enthält eine Anrede oder Grußformel, die einem Vorwort, eine" [signed](signed.md) "enthält die abschließende Grußformel o.Ä. die ein Vorwort, e"

## Content Model

```xml
<content>
    
      <alternate minOccurs="0" maxOccurs="unbounded">
        <textNode/>
        <classRef key="model.gLike"/>
        <classRef key="model.phrase"/>
        
        <elementRef key="argument"/>
        <elementRef key="byline"/>
        <elementRef key="dateline"/>
        <elementRef key="epigraph"/>
        <elementRef key="salute"/>
        <elementRef key="signed"/>
        <classRef key="model.global"/>
      </alternate>
    
  </content>
```
