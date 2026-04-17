# `<closer>`

Schlussformel eines Briefes (Gruss, Unterschrift, Datum).

Siehe [Textstruktur > Dateline](https://dokumentation.karl-barth.ch/textstruktur/dateline/)

**Modul:** textstructure — Textstruktur

## Kann enthalten

Beliebiger Textinhalt

**textstructure:** [dateline](dateline.md) "enthält kurze Angaben zu Entstehungsort, -datum, -zeit, usw." [salute](salute.md) "enthält eine Anrede oder Grußformel, die einem Vorwort, eine" [signed](signed.md) "enthält die abschließende Grußformel o.Ä. die ein Vorwort, e"

## Beispiele

```xml
<closer>
    <salute>Mit herzlichem Gruß</salute>
    <salute>Ihr</salute>
    <signed>
      <persName ref="kbga-actors-512">Rudolf Bultmann</persName>
    </signed>
  </closer>
```

## Content Model

```xml
<content>
  <alternate minOccurs="0" maxOccurs="unbounded">
    <textNode/>
    <classRef key="model.gLike"/>
    <elementRef key="byline"/>
    <elementRef key="signed"/>
    <elementRef key="dateline"/>
    <elementRef key="salute"/>
    <classRef key="model.phrase"/>
    <classRef key="model.global"/>
  </alternate>
</content>
```
