# `<persName>`

Personenname mit Verweis auf die Meta-DB via @ref (kbga-actors-ID). Das @key kann provisorisch eine normalisierte Schreibweise enthalten.

Siehe [Textelemente > Akteure](https://dokumentation.karl-barth.ch/textelemente/akteure/)

[TEI Guidelines: persName](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-persName.html)

**Modul:** namesdates — Namen und Daten

## Attribute

**@ref** (optional)
:   Enthält eine ID aus der Meta-DB (https://kbga.karl-barth.ch)
:   Datentyp: string — Pattern: `(kbga-actors-\d+ ?)+`

**@key** (optional)
:   Enthält eine normalisierte Schreibweise. Sollte nur provisorisch genutzt werden und durch ein @ref ersetzt werden


## Beispiele

```xml
<persName ref="kbga-actors-512">Bultmann, Rudolf</persName>
```

## Content Model

```xml
<content>
  <macroRef key="macro.phraseSeq"/>
</content>
```
