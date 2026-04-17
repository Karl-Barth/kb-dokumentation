# `<placeName>`

Ortsname mit Verweis auf die Meta-DB via @ref (kbga-places-ID). Das @key kann provisorisch eine normalisierte Schreibweise enthalten.

Siehe [Textelemente > Orte](https://dokumentation.karl-barth.ch/textelemente/orte/)

[TEI Guidelines: placeName](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-placeName.html)

**Modul:** namesdates — Namen und Daten

## Attribute

**@ref** (optional)
:   Enthält eine ID aus der Meta-DB (https://kbga.karl-barth.ch)
:   Datentyp: string — Pattern: `(kbga-places-\d+ ?)+`

**@key** (optional)
:   Enthält eine normalisierte Schreibweise. Sollte nur provisorisch genutzt werden und durch ein @ref ersetzt werden

**@rend** (optional)


## Beispiele

```xml
<placeName ref="kbga-places-41">Marburg</placeName>
```

## Content Model

```xml
<content>
  <macroRef key="macro.phraseSeq"/>
</content>
```
