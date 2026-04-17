# `<dateline>`

enthält kurze Angaben zu Entstehungsort, -datum, -zeit, usw. eines Briefs, Zeitungsartikels oder
    anderen Werks. Diese können als Überschrift oder Nachsatz dem Text voran- bzw. nachgestellt
    werden.

Siehe [Textstruktur > Dateline](https://dokumentation.karl-barth.ch/textstruktur/dateline/)

**Modul:** textstructure — Textstruktur

## Enthalten in

**textstructure:** [closer](closer.md) "Schlussformel eines Briefes (Gruss, Unterschrift, Datum)." [opener](opener.md) "fasst Datumszeile, Verfasserangabe, Anredeformel und ähnlich"

## Kann enthalten

Beliebiger Textinhalt

**textstructure:** [docDate](docDate.md) "enthält die Datierung des Dokuments, wie auf der Titelseite "

## Content Model

```xml
<content>
    
    
    
      <alternate minOccurs="0" maxOccurs="unbounded">
        <textNode/>
        <classRef key="model.gLike"/>
        <classRef key="model.phrase"/>
        <classRef key="model.global"/>
        <elementRef key="docDate"/>
      </alternate>
    
  </content>
```
