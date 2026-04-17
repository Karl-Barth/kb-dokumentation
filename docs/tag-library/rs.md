# `<rs>` verweisende Zeichenkette

Referenzierende Zeichenkette für Akteure, die nicht als persName oder orgName ausgezeichnet werden (z.B. Pronomen, Umschreibungen). Der @type unterscheidet person, organisation, place, conference.

Siehe [Textelemente > Akteure](https://dokumentation.karl-barth.ch/textelemente/akteure/)

**Modul:** core — Kernmodule

## Attribute

**@type** (optional)
:   `conference`
:   `person`
:   `organisation`
:   `place`


## Beispiele

```xml
<rs type="person" ref="kbga-actors-27">Bruders</rs>
```

## Content Model

```xml
<content>
  <macroRef key="macro.phraseSeq"/>
</content>
```
